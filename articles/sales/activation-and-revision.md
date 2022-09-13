---
title: Revisione e attivazione di un'offerta di progetto
description: In questo articolo vengono fornite informazioni sulla revisione e sull'attivazione di offerte in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410329"
---
# <a name="activate-and-revise-a-project-quote"></a>Revisione e attivazione di un'offerta di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione lite: dalla transazione alla fatturazione proforma_

Le funzionalità di attivazione e revisione ti aiutano a tenere traccia del controllo delle versioni per i preventivi basati su progetto durante le fasi di stima e negoziazione. Quando viene attivata una bozza di preventivo, diventa di sola lettura.

Le funzionalità di attivazione e revisione consentono di eseguire le seguenti attività:

- Vinci o perdi offerte solo dopo l'attivazione.
- Rivedere un'offerta per apportare modifiche all'offerta esistente o creare una nuova versione.

> [!NOTE]
> Dopo che la funzione per l'attivazione e la revisione dei preventivi è stata abilitata, non può essere disabilitata.

Per abilitare la possibilità di attivare e rivedere i preventivi basati su progetto, attenersi alla seguente procedura.

1. Vai a **Impostazioni** \> **Parametri**.
1. Apri il record **Parametti**.
1. Nel riquadro azioni, nella scheda **Controllo funzionalità**, seleziona **Abilita attivazione e revisioni delle offerte**.
1. Nella finestra di dialogo di conferma seleziona **OK**.
1. Dopo qualche istante, aggiorna il browser. Le funzionalità di attivazione e revisione dovrebbero ora essere disponibili. Saprai che queste funzionalità sono state abilitate se il pulsante **Abilita attivazione e revisioni delle offerte** non viene più visualizzato nel riquadro azioni.

## <a name="activating-a-quote"></a>Attivazione di un'offerta

Dopo aver abilitato la funzionalità per l'attivazione e la revisione dei preventivi, i pulsanti **Chiudere offerta come acquisita** e **Chiudi offerta come persa** nel riquadro azioni non sono disponibili per i preventivi di progetto in bozza. Sono disponibili solo dopo l'attivazione di un'offerta.

L'attivazione rappresenta la fase del processo di offerta in cui si desidera evitare ulteriori modifiche all'offerta. In questa fase, l'offerta viene inviata per la revisione interna o al cliente.

I pulsanti **Chiudi offerta come vinta** e **Chiudi offerta come persa** nel riquadro azioni sono disponibili per le offerte attivate. A seconda dell'esito della revisione interna o del cliente, puoi utilizzare uno di questi pulsanti per chiudere un'offerta attivata. Puoi effettuare trattative e modifiche sui preventivi attivati selezionando **Rivedi offerta**.

## <a name="revising-a-quote"></a>Revisione di un'offerta

Se è necessario apportare modifiche a un'offerta attivata, seleziona **Aggiorna offerta**. L'offerta è chiusa e il codice motivo **rivisto** viene utilizzato. Viene quindi creata una nuova offerta con lo stesso ID e un numero di revisione incrementato. Tutti i dettagli dell'offerta originale vengono copiati nella nuova offerta. La nuova offerta è in stato di bozza e può essere modificata secondo necessità.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
