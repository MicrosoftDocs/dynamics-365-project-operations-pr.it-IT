---
title: Concetti chiave dei conti lavoro
description: In questo articolo vengono illustrati alcuni concetti chiave che si applicano al conto lavoro in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9577169f12198222e647ed07ae8a1b6c55da4323
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522753"
---
# <a name="key-concepts-in-subcontracting"></a>Concetti chiave dei conti lavoro


_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione lite: dalla transazione alla fatturazione proforma_

L'articolo spiega alcuni concetti chiave di cui dovresti essere a conoscenza prima di iniziare a utilizzare la funzionalità di conto lavoro in Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Unità di contratto sul conto lavoro

L'unità di contratto rappresenta la divisione o la pratica proprietaria della consegna dell'eventuale progetto. L'unità di contratto è anche la divisione che intrattiene il rapporto contrattuale con il fornitore.

## <a name="purchase-currency"></a>Valuta di acquisto

In Project Operations, la valuta di acquisto è la valuta in cui viene creato il conto lavoro. È anche la valuta in cui sono registrati i costi del terzista su un progetto. La valuta di acquisto può differire dalla valuta del progetto e la valuta del progetto può, a sua volta, differire dalla valuta di vendita.

## <a name="billing-methods-on-subcontract-lines"></a>Modalità di fatturazione su righe di conto lavoro

Per i progetti, ci sono in genere modelli di contratto a tariffa fissa e basati sul consumo. Project Operations supporta questi metodi di fatturazione nei contesti di vendita e acquisto. Per un acquisto, le modalità di fatturazione funzionano nel modo seguente:

- **Tempo e materiale** – Quando una riga di conto lavoro utilizza il metodo di fatturazione **Tempo e materiale**, il costo del tempo viene registrato sul progetto poiché i terzisti lavorano su quel progetto e registrano il tempo. Queste transazioni di costo dai terzisti vengono quindi abbinate alle voci nelle fatture fornitore. In questo modello, i project manager che utilizzano Project Operations possono abbinare e verificare le righe della fattura fornitore con il tempo del terzista registrato e approvato. Al termine della verifica, i costi effettivi precedenti registrati dopo l'approvazione vengono stornati e nel progetto vengono creati nuovi effettivi costi basati sulla fattura fornitore.
- **Prezzo fisso** – In questo modello di contratto a tariffa fissa, le fatture fornitore si basano su passaggi fondamentali fissi. Tuttavia, le risorse del terzista possono anche indicare il tempo. Il tempo viene quindi rivisto e approvato dal project manager. Quando viene approvato, Project Operations crea effettivi di costo temporanei per il progetto. Dopo che il fornitore ha inviato una fattura per un passaggio fondamentale, il project manager può confrontare i costi effettivi registrati in precedenza con il passaggio fondamentale. Una volta completata la verifica, i costi effettivi vengono stornati e viene registrato il costo basato sul passaggio fondamentale.

## <a name="project-price-lists-on-subcontracts"></a>Listini prezzi di progetto nei conti lavoro

I listini prezzi di progetto sono listini prezzi utilizzati per impostare i prezzi di acquisto per tempi, spese e altri componenti relativi al progetto. Possono essere presenti più listini prezzi, ognuno dei quali può avere il proprio contratto di conto lavoro con data di validità in Project Operations. Project Operations non supporta la sovrapposizione di date di validità nei listini prezzi di progetto per un conto lavoro.

## <a name="transaction-classes-on-subcontracts"></a>Classi di transazione sui conti lavoro

Project Operations supporta quattro tipi di classi di transazione:

- Inserimento ore
- Spesa
- Materiale
- Quota

I costi di acquisto possono essere stimati e sostenuti solo sulle classi di transazione **Tempo**, **Spesa** e **Materiale**. **Tariffa** è una classe di transazione solo per le entrate e non è disponibile nel contenuto dell'acquisto.

## <a name="purchase-pricing-dimensions"></a>Dimensioni di determinazione dei prezzi di acquisto

Le dimensioni dei prezzi consentono di decidere quali attributi vengono utilizzati per l'impostazione del prezzo di acquisto e per l'impostazione predefinita delle transazioni orarie. In relazione agli acquisti, Project Operations supporta solo set di dimensioni fisse per l'impostazione del prezzo di acquisto e l'impostazione predefinita. Per l'impostazione del prezzo di acquisto e l'impostazione predefinita su righe di contratto di lavoro e transazioni di tempo di conto lavoro, gli attributi sono **Ruolo** e **Risorsa prenotabile**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
