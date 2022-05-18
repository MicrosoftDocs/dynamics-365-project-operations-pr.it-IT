---
title: Impostazione della ritenuta ai fornitori
description: In questo argomento viene spiegato come impostare la ritenuta ai fornitori.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583709"
---
# <a name="set-up-vendor-retention"></a>Impostazione della ritenuta ai fornitori

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento fornisce informazioni su come configurare la ritenuta ai fornitori.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Imposta un conto di ritenuta ai fornitori in Contabilità generale

1. In Dynamics 365 Finance, vai a **Contabilità generale** > **Impostazione di registrazione** > **Conti per transazioni automatiche**.
2. Aggiungi una nuova riga.
3. Nel campo **Tipo di registrazione** seleziona **Ritenuta fornitore**.
4. Seleziona il conto principale per la registrazione della ritenuta fornitore.

## <a name="create-vendor-retention-terms"></a>Creare termini di ritenuta per i fornitori

Utilizzare la pagina **Termini di ritenuta fornitore** per impostare e mantenere i termini di ritenuta per i pagamenti dei fornitori. Immetti la percentuale di ritenuta per il pagamento fornitore da trattenere e la percentuale degli importi di ritenute precedenti da rilasciare. Gli importi vengono automaticamente trattenuti sulle fatture fornitore fino a quando il contratto non raggiunge lo stato di completamento specificato. Dopo aver impostato i termini di ritenuta fornitore, puoi applicarli a qualsiasi progetto su cui lavora il fornitore.

1. In Finance, vai a **Gestione progetti e contabilità** > **Installazione** > **Ritenuta** > **Termini ritenuta pagamento fornitore**.
2. Seleziona **Nuovo** per aggiungere una nuova condizione di trattenimento del fornitore. Viene automaticamente immesso il valore nel campo **ID regola** per il nuovo termine. 
3. Nel campo **Descrizione** immetti un nome descrittivo per il nuovo termine.
4. Nella scheda **Termini**, seleziona **Aggiungi riga** per immettere un termine di ritenuta fornitore.
5. Nel campo **Percentuale di unità consegnate** immetti una percentuale di completamento per la regola. Gli importi vengono automaticamente trattenuti nelle fatture fornitore fino a quando la fase di completamento del progetto non è uguale alla percentuale immessa. Ad esempio, se si immette 50,00, gli importi vengono trattenuti fino al completamento del 50% del progetto.
6. Nel campo **Percentuale da trattenere** immetti la percentuale di un importo della fattura fornitore da trattenere. Ad esempio, se immetti 10.00 in questo campo, viene trattenuto il 10% dell'importo nelle fatture fornitore finché il progetto non raggiunge la percentuale di completamento impostata nel campo **Percentuale di unità consegnate**.
7. Nel campo **Percentuale da rilasciare** immetti la percentuale di qualsiasi importo di ritenuta precedente da rilasciare al raggiungimento del livello di completamento selezionato del progetto.

> [!NOTE]
> Se vi sono più passaggio fondamentali per diversi livelli di completamento del progetto, immetti una riga di termini di ritenuta fornitore separata per ciascuna regola di ritenuta. In ogni riga è possibile specificare una percentuale di ritenuta differente e una percentuale di rilascio differente per ogni livello specificato di completamento del progetto.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Impostare un contratto fornitore per il progetto

Imposta i termini di ritenuta fornitore che si applicano al progetto. Le condizioni di trattenimento per il fornitore vengono visualizzate anche negli ordini di acquisto creati per il fornitore.

1. In Finance, vai a **Gestione progetti e contabilità** > **Progetti** > **Tutti i progetti**. 
2. Seleziona un progetto e nel riquadro azioni, seleziona **Gruppo di progetti** > **Contratti fornitore**.
3. Nella pagina **Contratti fornitore**, aggiungi una nuova riga.
4. Nel campo **Codice conto**, seleziona una delle seguenti opzioni:
   - **Tabella**: le condizioni di trattenimento per il fornitore si applicano a un singolo fornitore.
   - **Gruppo**: le condizioni di trattenimento per il fornitore si applicano a tutti i fornitori in un gruppo di fornitori.
   - **Tutto**: le condizioni di trattenimento per il fornitore si applicano a tutti i fornitori.
5. Nel campo **Fornitore/gruppo fornitori**, seleziona il fornitore o il gruppo di fornitori a cui si applicano le condizioni di ritenuta per il fornitore. Se hai selezionato **Tutto** nel passaggio precedente, questo campo non è disponibile.
6. Nel campo **Termini di ritenuta fornitore**, seleziona l'ID della regola per i termini di ritenuta da applicare a questo fornitore.

