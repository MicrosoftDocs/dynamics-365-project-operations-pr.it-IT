---
title: Panoramica delle approvazioni
description: Questo argomento fornisce informazioni su come utilizzare le approvazioni in Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961171"
---
# <a name="approvals-overview"></a>Panoramica delle approvazioni

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Gli invii di tempo e spese passano attraverso un flusso di lavoro di approvazione. Dopo l'approvazione degli inserimenti, le transazioni vengono registrate in valori effettivi o viene prenotata un'ora nella pianificazione.

## <a name="approvals-workflow"></a>Flusso di lavoro per le approvazioni
Quando crei e invii una voce di tempo o di spesa, viene creata una voce di approvazione. L'approvatore del progetto o il tuo responsabile esamina e approva il tuo inserimento. Se la voce è correlata a un progetto, quando viene approvata, verranno creati i valori effettivi. Ciò consente di monitorare il costo e la fatturazione. 

## <a name="approve-an-entry"></a>Approvare una voce
Il modulo **Approvazioni** consente di passare da una visualizzazione all'altra in modo da poter visualizzare i diversi tipi di approvazioni.
  
1. Vai al modulo **Approvazioni** e seleziona **Spese**, **Tempo** o **Ricorda**.
2. Rivedi ogni approvazione e seleziona quelle che desideri approvare.
3. Seleziona **Approva** per approvare le voci selezionate.
Il sistema elaborerà queste voci e creerà valori effettivi o una prenotazione.

## <a name="reject-an-entry"></a>Rifiutare una voce
In qualità di approvatore del progetto, potrebbe essere necessario inviare una voce a un utente per la correzione.
  
1. Vai al modulo **Approvazioni** e seleziona la voce da rifiutare. 
2. Seleziona **Rifiuta**.
3. Facoltativo: aggiungi un commento nella finestra di dialogo **Commenti rifiuto** per informare l'utente del motivo per cui la voce è stata rifiutata.
4. Seleziona **OK**. La voce verrà restituita all'utente.
  
## <a name="recall-entries"></a>Richiamare le voci
Ad un certo punto, potrebbe essere necessario richiamare una voce inviata. Se la voce non è stata approvata, verrà restituita immediatamente. Tuttavia, una voce approvata può avere un impatto sostanziale. L'approvatore del progetto è tenuto ad approvare il richiamo per stornare la transazione in Valori effettivi.

## <a name="specify-project-approvers"></a>Specificare gli approvatori di progetto
Ogni progetto ha un numero di membri del team di progetto. È possibile specificare quali membri del team sono anche approvatori del progetto.

1. Vai al modulo **Progetti** e apri il progetto dall'elenco.
2. Nella scheda **Team**, seleziona il membro del team che sarà un approvatore del progetto, quindi seleziona **Modifica**.
3. Imposta il campo **Responsabile approvazione di progetto** su **Sì**.
4. Seleziona **Salva**.
5. Ripeti i passaggi da 2 a 4 per aggiungere altri responsabili dell'approvazione del progetto.

## <a name="configure-the-users-manager"></a>Configura il responsabile dell'utente

1. Andare a **Impostazioni** > **Sicurezza** > **Utenti**.
2. Seleziona l'utente a cui stai assegnando un responsabile e nell'area **Informazioni sull'organizzazione**, seleziona il responsabile dall'elenco. 
3. Seleziona **Salva**.


