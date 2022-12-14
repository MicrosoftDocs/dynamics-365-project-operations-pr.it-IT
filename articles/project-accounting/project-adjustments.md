---
title: Rettifiche di progetto
description: In questo articolo vengono fornite informazioni sulle rettifiche di progetto.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788301"
---
# <a name="project-adjustments"></a>Rettifiche di progetto

_**Si applica a:** Project Operations per scenari basati su materiali stoccati/produzione_

## <a name="adjustments-overview"></a>Panoramica delle rettifiche

Puoi configurare Microsoft Dynamics 365 Project Operations in modo che gli utenti possano apportare modifiche alle transazioni registrate. Puoi modificare le transazioni di progetto una alla volta o selezionare più transazioni da un elenco di tutte le transazioni di progetto. Le rettifiche di progetto vengono utilizzate ad esempio, per aggiornare in blocco lo stato fatturabile, ricalcolare il costo dopo una modifica della configurazione o aggiornare le fonti di finanziamento.

Gli utenti possono accedere alla funzionalità di rettifica di progetto in diversi modi:

- Utilizzando la pagina **Rettifica transazioni** a cui si accede da **Gestione progetti e contabilità** \> **Impostazione**.
- Utilizzando il pulsante **Rettifica** nella pagina **Transazioni progetto registrate** a cui si può accedere da **Gestione progetti e contabilità** \> **Transazioni**.
- Utilizzando il pulsante **Adeguamento** nella pagina **Transazioni progetto registrate** nel contesto di un progetto. Questa pagina è accessibile da **Gestione progetti e contabilità** \> **Tutti i progetti**.

Per consentire le rettifiche è necessario abilitare uno o più stati transazione da **Gestione progetto e contabilità** \> **Parametri gestione progetto e contabilità** sulla scheda **Generale** sotto la sezione **Consenti rettifica dello stato della transazione**. Esempi di stati di transazione includono le transazioni registrate, le transazioni fatturate o le transazioni eliminate. Qualsiasi stato di transazione impostato su **No** comporta che le transazioni in quello stato non appariranno nel processo di rettifica come selezionabili per la rettifica.

Un'opzione di configurazione denominata **Crea sempre transazione di rettifica** è attualmente disponibile in Parametri gestione progetti e contabilità. È possibile disabilitare questa opzione per aggiornare la transazione originale invece di creare nuove transazioni durante la rettifica in un sottoinsieme di scenari. È stato annunciato che questo parametro sarà deprecato entro il 1° marzo 2023. Dopo il 1 marzo 2023, il sistema si comporterà sempre come se l'opzione fosse abilitata.

## <a name="adjustments-process-flow"></a>Flusso del processo di rettifica

I passaggi seguenti mostrano il flusso tipico per l'elaborazione delle rettifiche.

1. Apri la pagina **Rettifiche di progetto** .
2. Scegli **Seleziona** per cercare le transazioni che soddisfano i criteri previsti per la rettifica.
3. Nell'elenco delle transazioni seleziona tutte le transazioni o un sottoinsieme delle transazioni per la rettifica.
4. Seleziona **Rettifica** e modifica gli attributi sulla riga. In alternativa, se i valori sono stati specificati manualmente durante l'immissione della transazione, è possibile scegliere di immettere i valori di sistema predefiniti.
5. Viene restituito l'elenco delle transazioni e nella colonna **Rettifica in attesa** viene visualizzato un segno di spunta per indicare dove sono state apportate le modifiche. Eventuali rettifiche con modifiche in sospeso vengono visualizzate nella metà inferiore della pagina. Qui puoi apportare ulteriori modifiche dettagliate oltre a quanto mostrato nella pagina precedente.
6. Seleziona **Registra** per registrare le transazioni di rettifica.

A seconda della configurazione, in genere vengono create nuove transazioni per la rettifica.

- Il campo **Stato fattura** della transazione originale è impostato su **Rettificato**.
- Viene creata una transazione di storno per stornare la transazione originale e il campo **Stato** è impostato su **Rettificato**.
- Viene creata una nuova transazione con le modifiche apportate durante il processo di rettifica.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Selezione di più transazioni di progetto registrate alla volta per rettifiche e note di credito

Una nuova funzionalità introdotta nella versione 10.0.30 consente la selezione di più transazioni per la rettifica alla volta dalla pagina **Transazioni progetto registrate** .

Prima di utilizzare questa funzionalità, è necessario abilitarla nel sistema. Gli amministratori possono utilizzare l'area di lavoro **Gestione funzionalità** per controllare lo stato della funzionalità e, se necessario, abilitarla. Nell'area di lavoro **Gestione funzionalità** , cerca e seleziona **Selezione di più transazioni di progetto registrate alla volta per rettifiche e note di credito**, e poi seleziona **Abilita ora**.

Questa opzione abilita la seguente funzionalità chiave:

- È possibile accedervi dalla pagina della transazione registrata all'interno di un progetto utilizzando il pulsante **Rettifica** esistente.
- Abilita un controllo di selezione di più righe nella pagina **Transazioni progetto registrate** . Puoi applicare filtri alla pagina dell'elenco e selezionare i tuoi record prima di iniziare le rettifiche.
- Disabilita il pulsante **Rettifica** se una singola transazione non può essere rettificata o se selezioni una combinazione di note di credito e giornali di registrazione insieme anziché singolarmente.
- A causa dell'aggiunta del controllo di selezione di più righe, il collegamento **Costo impegnato** nella barra multifunzione non è più disabilitato se vengono selezionate più righe.
- Aggiunge il seguente messaggio di avviso: "Hai selezionato più di (numero selezionato) record per la rettifica. L'esecuzione di questa azione potrebbe richiedere del tempo. Procedere con questa azione?"

Questa funzionalità rimuove anche il passaggio 2 dal flusso di processo descritto in precedenza in questo articolo. Pertanto, tutte le transazioni selezionate prima dell'apertura della pagina **Rettifica transazioni** verranno incluse nell'elenco delle transazioni per la rettifica. Non è necessario utilizzare il pulsante **Seleziona** per cercarli.

> [!NOTE] 
> Anche se questa funzione è disabilitata, puoi comunque selezionare più record per la rettifica. Tuttavia, solo un record *rimarrà selezionato* e la finestra di dialogo **Seleziona transazioni** apparirà immediatamente dopo aver selezionato di aprire le rettifiche.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Stati della transazione di rettifica che possono essere abilitati o disabilitati per le rettifiche

I seguenti stati possono essere abilitati o disabilitati nella scheda **Generale** della pagina **Parametri gestione progetti e contabilità** :

- Registrato
- Proposta di fattura
- Fatturato
- Stimato
- Eliminato
- Saldo iniziale (ora)

## <a name="adjustment-parameters"></a>Parametri di rettifica

Questi parametri sono elencati nella pagina **Parametri gestione progetti e contabilità** nella scheda **Generale** del gruppo **Rettifica** e modificano il comportamento relativo all'elaborazione delle rettifiche. 

| Nome parametro | Description |
|----------------|-------------
| Crea sempre una transazione di rettifica | Se questo parametro è abilitato, il processo di rettifica creerà sempre una nuova transazione di storno e una nuova transazione rettificata in caso di impatto finanziario o di report. Se il parametro è disabilitato, il processo di rettifica aggiornerà la transazione originale invece di creare uno storno e una nuova transazione per uno scenario come un aggiornamento del testo della transazione. |
| Aggiorna automaticamente campo | Se questo parametro è abilitato, il sistema ricalcolerà il prezzo di costo e il prezzo di vendita. |
| Usa la data di rettifica come nuovo progetto | Questo parametro viene utilizzato per spostare le transazioni in un futuro periodo fiscale prima che il sistema supportasse questa funzione. Si sconsiglia di utilizzarla, perché modifica la data aziendale della transazione e sarà deprecata in una versione futura. |
| Consenti impegni chiusi | Di solito, le transazioni non possono essere create per le attività chiuse. Se questo parametro è abilitato, tale comportamento viene ignorato. Pertanto, è possibile creare rettifiche per gli impegni chiusi. |
