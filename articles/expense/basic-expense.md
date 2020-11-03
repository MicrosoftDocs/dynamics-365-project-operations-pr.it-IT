---
title: Voce di spesa (semplice)
description: Questo argomento fornisce informazioni su come lavorare con le voci di spesa in una distribuzione semplice.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078760"
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

## <a name="recall-a-basic-expense"></a>Richiamare una spesa di base

Quando invii una spesa per errore, puoi richiamarla. Il tempo necessario per richiamare una voce di spesa dipende dalla sua fase di approvazione.  Se il responsabile approvazione non ha ancora approvato la voce, il richiamo può avvenire immediatamente. Tuttavia, se la voce è già stata approvata, al responsabile approvazione viene chiesto di approvare il richiamo e di stornare le transazioni.

1. Vai a **Spese** , quindi, nell'elenco delle spese, seleziona la spesa da richiamare.
2. Seleziona **Richiama**. Se la voce di spesa non è stata ancora approvata, il sistema la richiama immediatamente. Se la voce di spesa è già stata approvata, viene creata una richiesta di richiamo per notificare al responsabile approvazione che si desidera stornare la spesa. Il responsabile approvazione confermerà quindi che lo storno può essere eseguito e la voce verrà restituita.

## <a name="delete-a-basic-expense"></a>Eliminare una spesa di base

Le spese che non sono state ancora inviate possono essere eliminate. Per eliminare una spesa già inviata, è necessario prima richiamarla.

## <a name="see-also"></a>Vedi anche

- [Panoramica delle approvazioni](../approvals/approvals-overview.md)
