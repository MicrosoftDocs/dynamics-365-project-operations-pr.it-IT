---
title: Panoramica delle approvazioni
description: Questo argomento fornisce informazioni su come utilizzare le approvazioni in Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368661"
---
# <a name="approvals-overview"></a>Panoramica delle approvazioni

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Gli invii di tempo, spese e utilizzo di materiale passano attraverso un flusso di lavoro per le approvazioni. Dopo l'approvazione degli inserimenti, le transazioni vengono registrate in valori effettivi o viene prenotata un'ora nella pianificazione.

## <a name="approvals-workflow"></a>Flusso di lavoro per le approvazioni
Quando si crea e si invia una voce di tempo, spesa o utilizzo di materiale, viene creato un record approvazione. Il revisore o il responsabile del progetto esamina e approva la voce. Se la voce è correlata a un progetto, i valori effettivi verranno creati al momento dell'approvazione. Ciò consente di monitorare il costo e la fatturazione.

## <a name="approve-an-entry"></a>Approvare una voce
La pagina **Approvazioni** consente di passare da una visualizzazione all'altra in modo da poter visualizzare i diversi tipi di approvazioni.
  
1. Vai alla pagina **Approvazioni** e seleziona **Spese**, **Tempo**, **Utilizzo di materiale** o **Richiami**.
2. Rivedi ogni approvazione e seleziona quelle che desideri approvare.
3. Seleziona **Approva** per approvare le voci selezionate.
Il sistema elabora queste voci e crea valori effettivi.

## <a name="reject-an-entry"></a>Rifiutare una voce
In qualità di approvatore del progetto, potrebbe essere necessario inviare una voce a un utente per la correzione.
  
1. Vai alla pagina **Approvazioni** e seleziona la voce da rifiutare. 
2. Seleziona **Rifiuta**.
3. Facoltativo: aggiungi un commento nella finestra di dialogo **Commenti rifiuto** per informare l'utente del motivo per cui la voce è stata rifiutata.
4. Seleziona **OK**. La voce verrà restituita all'utente.
  
## <a name="cancel-approval"></a>Annulla approvazione
In alcuni casi, potrebbe essere necessario annullare una voce precedentemente approvata. L'annullamento di una voce precedentemente approvata avrà un impatto finanziario. 

## <a name="approving-recall-requests"></a>Approvare richieste di richiamo
In alcuni casi, un consulente potrebbe dover richiamare una voce precedentemente approvata. L'annullamento di una voce precedentemente approvata avrà un impatto finanziario. L'approvatore del progetto deve approvare il richiamo per stornare la transazione in Valori effettivi.

## <a name="specify-project-approvers"></a>Specificare gli approvatori di progetto
Ogni progetto ha un numero di membri del team di progetto. È possibile specificare quali membri del team sono anche approvatori del progetto.

1. Vai alla pagina **Progetti** e apri il progetto dall'elenco.
2. Nella scheda **Team**, seleziona il membro del team che sarà un approvatore del progetto, quindi seleziona **Modifica**.
3. Imposta il campo **Responsabile approvazione di progetto** su **Sì**.
4. Seleziona **Salva**.
5. Ripeti i passaggi da 2 a 4 per aggiungere altri responsabili dell'approvazione del progetto.

## <a name="configure-the-users-manager"></a>Configura il responsabile dell'utente

1. Andare a **Impostazioni** > **Sicurezza** > **Utenti**.
2. Seleziona l'utente a cui stai assegnando un responsabile e nell'area **Informazioni sull'organizzazione**, seleziona il responsabile dall'elenco. 
3. Seleziona **Salva**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
