---
title: Creare e applicare le condizioni di trattenimento dei pagamenti del fornitore
description: Questo argomento fornisce informazioni su come impostare e mantenere le condizioni di trattenimento per i pagamenti dei fornitori.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079013"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Creare e applicare le condizioni di trattenimento dei pagamenti del fornitore

[!include [banner](../includes/banner.md)] 

L'impostazione delle condizioni di trattenimento dei pagamenti del fornitore per un progetto è utile quando l'organizzazione desidera trattenere parte dei pagamenti effettuati a un fornitore. Ad esempio, quando desideri trattenere il pagamento a un fornitore finché i prodotti consegnati non soddisfano le tue aspettative. Le condizioni di trattenimento del pagamento del fornitore possono essere specificate quando si negozia un contratto con il fornitore.

## <a name="create-vendor-payment-retention-terms"></a>Creare le condizioni di trattenimento dei pagamenti del fornitore

Puoi inserire la percentuale del pagamento del fornitore da trattenere e la percentuale degli importi precedentemente trattenuti da rilasciare. Gli importi vengono automaticamente trattenuti sulle fatture fornitore fino a quando il contratto non raggiunge lo stato di completamento specificato. Dopo aver impostato le condizioni di trattenimento, è possibile applicarle a qualsiasi progetto per quel fornitore.

Utilizza i passaggi seguenti per impostare e mantenere condizioni di trattenimento per i pagamenti del fornitore. 

1. Vai a **Gestione progetti e contabilità** > **Trattenimento** > **Condizioni di trattenimento del pagamento del fornitore**.
2. Seleziona **Nuovo** per aggiungere una nuova condizione di trattenimento del fornitore. Il valore **ID regola** per il nuovo termine viene inserito automaticamente. 
3. Immetti una breve descrizione nel campo **Descrizione** e nella scheda dettaglio **Condizioni** seleziona **Aggiungi riga** per inserire i valori delle condizioni per quanto segue:

   - **Percentuale di unità consegnate**: immetti una percentuale di completamento per la condizione. Gli importi vengono automaticamente trattenuti sulle fatture fornitore fino a quando la fase di completamento del progetto è uguale alla percentuale specificata. Ad esempio, se si immette 50,00, gli importi vengono trattenuti fino al completamento del 50% del progetto.
   - **Percentuale da trattenere**: immetti una percentuale dell'importo della fattura fornitore da trattenere. Ad esempio, se immetti 10,00, viene trattenuto il 10 percento dell'importo su una fattura fornitore fino a quando il progetto non raggiunge la percentuale di completamento come impostato nel **campo Percentuale di unità consegnate**.
   - **Percentuale da rilasciare**: seleziona **Aggiungi riga** per immettere una percentuale di eventuali importi precedentemente trattenuti da rilasciare per il livello di completamento del progetto selezionato.

> [!NOTE]
> Se hai più passaggi fondamentali per diversi livelli di completamento del progetto, immetti una riga della condizione di trattenimento del fornitore separata per ciascuna regola di trattenimento. Ogni riga può specificare una percentuale di trattenimento diversa e una percentuale di rilascio diversa per ogni livello designato di completamento del progetto.

Dopo aver creato le condizioni di trattenimento per un fornitore, è possibile applicarle a un progetto.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Applicare le condizioni di trattenimento del fornitore a un progetto

1. Vai a **Gestione progetti e contabilità** > **Progetti** > **Tutti i progetti** e apri un progetto dalla pagina elenco dei progetti.
2. Nella scheda dettaglio **Contratti fornitori** seleziona **Aggiungi riga**.
3. Nel **campo Codice conto**, seleziona una delle seguenti opzioni: 

   - **Tabella**: le condizioni di trattenimento per il fornitore si applicano a un singolo fornitore.
   - **Gruppo**: le condizioni di trattenimento per il fornitore si applicano a tutti i fornitori in un gruppo di fornitori.
   - **Tutto**: le condizioni di trattenimento per il fornitore si applicano a tutti i fornitori.

4. Nel **campo fornitore/gruppo di fornitori**, seleziona il fornitore o il gruppo di fornitori a cui si applicano le condizioni di trattenimento per il fornitore. Se hai selezionato **Tutto** nel passaggio precedente, questo campo non è disponibile.
5. Nel campo **Condizioni di trattenimento per il fornitore** seleziona le condizioni di trattenimento che hai creato nella procedura precedente.
6. Se il progetto ha anche le condizioni di pagamento su pagamento impostati per il fornitore, immetti la percentuale di soglia per il progetto nel campo **Percentuale soglia pagamento su pagamento**.

Le condizioni di trattenimento per il fornitore vengono visualizzate anche negli ordini di acquisto creati per il fornitore.
