---
title: Opzioni di conto lavoro per i membri del team di progetto
description: Questo argomento spiega le opzioni di conto lavoro per i membri del team di progetto in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903456"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opzioni di conto lavoro per i membri del team di progetto

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

In Microsoft Dynamics 365 Project Operations, puoi valutare le opzioni di conto lavoro disponibili per uno o più membri del team di progetto. Le opzioni di conto lavoro disponibili ti consentono di:

- Creare un nuovo conto lavoro e/o creare nuove righe su un conto lavoro esistente per i membri del team di progetto selezionati. 
- Riservare un conto lavoro già esistente e una riga di conto lavoro. 

È possibile scegliere tra le opzioni di conto lavoro disponibili per i membri del team di progetto generico o scegliere tra i membri del team di progetto che hanno lavorato con una risorsa denominata che è un lavoratore a contratto. 

Non sono disponibili opzioni di conto lavoro per quanto segue:

- Membri del team di progetto che hanno lavorato con un dipendente. 
- Membri del team di progetto già associati a una riga di conto lavoro e un conto lavoro. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Opzioni di conto lavoro per un membro del team di progetto senza personale

Per rivedere e scegliere tra le opzioni di conto lavoro disponibili per un membro del team di progetto generico o senza personale, attieniti alla seguente procedura:

1. Seleziona uno o più record dei membri del team di progetto in cui la risorsa è una risorsa generica.
2. Assicurati che nessuno dei record dei membri del team di progetto selezionati sia già in conto lavoro. 
3. Seleziona **Opzioni di conto lavoro** nella griglia secondaria dei membri del team di progetto. Viene aperta la finestra di dialogo **Opzioni di conto lavoro**. 
4. Se hai selezionato solo un record di membro del team di progetto nel passaggio 1, saranno disponibili le seguenti opzioni:
    - Crea nuove righe di conto lavoro. 
    - Prenota un conto lavoro esistente. Se sono stati selezionati più record di membri del team di progetto nel passaggio 1, l'unica opzione disponibile è creare nuove righe di conto lavoro.
5. L'opzione di prenotazione di una riga di conto lavoro esistente consente di selezionare un conto lavoro e una riga di conto lavoro che vuoi prenotare. Quando si seleziona una riga di conto lavoro per riservare capacità, è necessario assicurarsi che la riga di conto lavoro selezionata sia per il tempo e che il ruolo richiesto nel membro del team di progetto corrisponda al ruolo che è stato acquistato nella riga di conto lavoro.
6. Quando scegli di creare nuove righe di conto lavoro per i membri del team di progetto, il sistema consentirà di selezionare il contratto di conto lavoro che vuoi per creare queste righe. Il conto lavoro selezionato per creare nuove righe dovrebbe essere nello stato **Bozza**. Con questa opzione per creare nuove righe di conto lavoro per i membri del team di progetto selezionati, il sistema creerà una riga di conto lavoro per tempo per ciascun membro del team di progetto. Il ruolo, le ore e le date verranno copiati dal membro del team di progetto in ciascuna riga di conto lavoro creata. 
7. Quando un membro del team generico è associato a una riga di conto lavoro e un conto lavoro, il campo **Tipo di lavoratore** sulla riga del membro del team generico verrà aggiornato su **Lavoratore a contratto** e il valore **Validità conto lavoro** sarà impostato su **Valido**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Opzioni di conto lavoro per un membro del team di progetto con personale

Come i membri del team generici o senza personale, è anche possibile visualizzare le opzioni di conto lavoro per un membro del team di progetto con personale purché il membro del team con personale sia un lavoratore a contratto. Per rivedere e scegliere tra le opzioni di conto lavoro disponibili per un membro del team di progetto denominato o con personale, attieniti alla seguente procedura:

1. Seleziona uno o più record dei membri del team di progetto in cui la risorsa è un lavoratore a contratto denominato.
2. Assicurati che nessuno dei record dei membri del team di progetto selezionati sia già in conto lavoro. 
3. Seleziona **Opzioni di conto lavoro** nella griglia secondaria dei membri del team di progetto. Viene aperta la finestra di dialogo **Opzioni di conto lavoro**. 
4. Se hai selezionato solo un record di membro del team di progetto nel passaggio 1, saranno disponibili le seguenti opzioni:
      - Crea nuove righe di conto lavoro.
      - Prenota rispetto a un conto lavoro.
  Se sono stati selezionati più record di membri del team di progetto nel passaggio 1, l'unica opzione disponibile è creare nuove righe di conto lavoro.
5. L'opzione di prenotazione di una riga di conto lavoro esistente consente di selezionare un conto lavoro e una riga di conto lavoro che vuoi prenotare. Quando si seleziona una riga di conto lavoro per riservare capacità, è necessario garantire quanto segue:
      - La riga di conto lavoro selezionata è per il tempo. 
      - Il ruolo richiesto per il membro del team di progetto corrisponde al ruolo acquistato nella riga di conto lavoro. 
      - Il fornitore a cui è associato il lavoratore a contratto è lo stesso del fornitore del conto lavoro.
6. Quando scegli di creare nuove righe di conto lavoro per i membri del team di progetto, il sistema consentirà di selezionare il contratto di conto lavoro che vuoi per creare queste righe. Con questa opzione è necessario assicurare che il fornitore a cui appartiene il lavoratore a contratto è lo stesso del fornitore del conto lavoro. 
7. Il conto lavoro selezionato per creare nuove righe dovrebbe essere nello stato **Bozza**. Con questa opzione per creare nuove righe di conto lavoro per i membri del team di progetto selezionati, il sistema creerà una riga di conto lavoro per tempo per ciascun membro del team di progetto. Il ruolo, le ore e le date verranno copiati dal membro del team di progetto in ciascuna riga di conto lavoro creata.  
8. Quando un membro del team denominato è associato a una riga di conto lavoro e un conto lavoro, il campo **Tipo di lavoratore** sulla riga del membro del team denominato verrà aggiornato su **Lavoratore a contratto** e il valore **Validità conto lavoro** sarà impostato su **Valido**.

## <a name="re-costing-subcontractor-assignments"></a>Rideterminazione dei costi delle assegnazioni dei conti lavoro

Quando un membro del team di progetto (generico o denominato) è collegato a righe di conto lavoro tramite le finestra di dialogo **Opzioni di conto lavoro**, tutte le assegnazioni alle attività di cui dispone il membro del team verranno rideterminati in base al listino prezzi di acquisto allegato al contratto di lavoro. Nella scheda **Stime** della pagina **Dettagli progetto** seleziona il pulsante **Aggiorna prezzi** per visualizzare i prezzi aggiornati e/o i costi risultanti dalla decisione di subappaltare.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
