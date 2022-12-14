---
title: Impostare la conversione di valuta per calcolare i prezzi di vendita dalle tariffe del costo
description: Questo articolo spiega come configurare il comportamento di conversione della valuta che verrà utilizzato in Microsoft Dynamics 365 Project Operations quando le transazioni di vendita vengono generate dalle transazioni di costo.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816669"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Impostare la conversione di valuta per calcolare i prezzi di vendita dalle tariffe del costo

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

In Microsoft Dynamics 365 Project Operations, i prezzi di vendita per le categorie di spesa possono essere impostati come valori numerici oppure possono essere impostati in modo che vengano calcolati in base al costo sostenuto.

Quando sono impostati per essere calcolati in base al costo sostenuto, sono disponibili le seguenti opzioni:

- Al costo
- Percentuale di ricarico sul costo

Negli scenari in cui il costo di spesa è sostenuto in una valuta diversa dalla valuta di vendita per il contratto di progetto, è necessaria la conversione di valuta per calcolare il prezzo di vendita in base al costo.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Comportamento di conversione della valuta che utilizza i tassi di cambio Dataverse nativi

Per impostazione predefinita, Project Operations utilizza i tassi di cambio della valuta archiviati nella tabella Valuta in Dataverse. Per configurare Project Operations per utilizzare i tassi di cambio nativi per calcolare i prezzi di vendita dal costo, attieniti alla seguente procedura.

1. Vai a **Project Operations \> Impostazioni \> Parametri**.
1. Apri la pagina dei dettagli **Parametro di progetto**.
1. Imposta il campo **Logica di conversione valuta** su un valore vuoto.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Comportamento di conversione della valuta che utilizza i tassi di cambio delle app per la finanza e le operazioni

I tassi di cambio nella tabella Valuta disponibile in modo nativo in Dataverse non hanno data di validità. Pertanto, potrebbero non essere sempre adattati ai requisiti per il calcolo dei prezzi di vendita dai tassi di costo.

È possibile utilizzare i tassi di cambio dell'ambiente per la finanza e le operazioni per calcolare il prezzo di vendita nella valuta di vendita da un tasso di costo nella valuta di costo. Per configurare questo comportamento di conversione di valuta, attieniti alla seguente procedura.

1. Nella pagina **Parametri di progetto** , aggiungi il campo **Logica conversione valuta** . Quindi salva e pubblica la personalizzazione.
1. Vai a **Project Operations \> Impostazioni \> Parametri**.
1. Apri la pagina dei dettagli **Parametro di progetto**. 
1. Imposta il campo **Comportamento conversione valuta** su **Esteso con fallback su predefinito**.
1. Concedi al ruolo di sicurezza **utente app a doppia scrittura** l'autorizzazione **lettura globale** per le seguenti tabelle:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. Nel tuo ambiente per la finanza e le operazioni, esegui le seguenti mappe a doppia scrittura con la sincronizzazione iniziale:

    - Tipo di tasso di cambio (msdyn\_exchangeratetypes)
    - Coppia di valute tasso di cambio (msdyn\_currencyexchangeratepairs)
    - Tassi di cambio CDS (msdyn\_currencyexchangerates)

Una volta completate queste modifiche, la doppia scrittura renderà disponibili i tassi di cambio dall'ambiente per la finanza e le operazioni in Dataverse. Project Operations utilizza quindi tali tassi di cambio per convertire i tassi di costo nella valuta di vendita del contratto.

> [!NOTE]
> Questo comportamento di conversione valuta si applica solo al calcolo dei prezzi di vendita dai tassi di costo. Non verrà utilizzato per calcolare genericamente i valori della valuta di base. I valori della valuta di base utilizzeranno sempre i tassi di cambio nativi di Dataverse , indipendentemente da questa procedura.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
