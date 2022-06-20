---
title: Voce di spesa (semplice)
description: Questo articolo fornisce informazioni su come lavorare con la voce di spesa in una distribuzione semplice.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b69cc4ec0a4b51cd1d27f8b8a4a94248ae884797
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917949"
---
# <a name="expense-entry-lite"></a>Voce di spesa (semplice)

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

La gestione delle spese di base, o semplice, è la capacità di registrare semplici spese. È possibile registrare le spese a fronte di un progetto, quindi il responsabile dell'approvazione del progetto le esaminerà e le approverà.

Per ulteriori informazioni sulle funzionalità di spesa in Dynamics 365 Project Operations, vedi [Panoramica delle spese](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Acquisire una spesa di base

Puoi acquisire le tue spese in modo da poterle inviare al responsabile approvazione.

1. Vai a **Spese** e seleziona **Nuovo**.
2. Nella pagina **Nuova spesa** immetti le informazioni richieste sulla spesa, quindi seleziona **Salva**.

## <a name="submit-a-basic-expense"></a>Inviare una spesa di base

Dopo che hai acquisito tutte le spese e sei pronto per l'approvazione, devi inviarle.

1. Vai a **Spese** e seleziona una spesa. Oppure seleziona tutte le spese utilizzando la casella di controllo nell'intestazione.
2. Seleziona **Invia**. Il sistema elabora le voci selezionate e quindi crea le richieste di approvazione delle spese.

## <a name="add-an-attachment"></a>Aggiungi un allegato

Potrebbe essere necessario fornire al revisore documentazione aggiuntiva sulle spese. È possibile allegare una ricevuta nella cronologia della voce di spesa. Seleziona **Modifica** e nella sezione **Sequenza temporale**, quindi seleziona l'icona della graffetta per allegare la ricevuta.

## <a name="recall-a-basic-expense"></a>Richiamare una spesa di base

Quando invii una spesa per errore, puoi richiamarla. Il tempo necessario per richiamare una voce di spesa dipende dalla sua fase di approvazione.  Se il responsabile approvazione non ha ancora approvato la voce, il richiamo può avvenire immediatamente. Tuttavia, se la voce è già stata approvata, al responsabile approvazione viene chiesto di approvare il richiamo e di stornare le transazioni.

1. Vai a **Spese**, quindi, nell'elenco delle spese, seleziona la spesa da richiamare.
2. Seleziona **Richiama**. Se la voce di spesa non è stata ancora approvata, il sistema la richiama immediatamente. Se la voce di spesa è già stata approvata, viene creata una richiesta di richiamo per notificare al responsabile approvazione che si desidera stornare la spesa. Il responsabile approvazione confermerà quindi che lo storno può essere eseguito e la voce verrà restituita.

## <a name="delete-a-basic-expense"></a>Eliminare una spesa di base

Le spese che non sono state ancora inviate possono essere eliminate. Per eliminare una spesa già inviata, è necessario prima richiamarla.

## <a name="see-also"></a>Vedi anche

- [Panoramica delle approvazioni](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]