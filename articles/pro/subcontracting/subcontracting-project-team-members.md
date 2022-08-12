---
title: Membri del team di progetto in conto lavoro
description: Questo articolo spiega come subappaltare i membri del team di progetto in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 649687cb9ac66e684069434a353b63155103aefb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916891"
---
# <a name="subcontracting-project-team-members"></a>Membri del team di progetto in conto lavoro

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

In Microsoft Dynamics 365 Project Operations, puoi scegliere di subappaltare i membri del team di progetto senza personale o con personale.

- Ai membri del team di progetto senza personale è assegnata una risorsa generica.
- Ai membri del team con personale è assegnata una risorsa denominata.

Quando si collega un membro del team di progetto a una riga di conto lavoro, tutte le assegnazioni alle attività di cui dispone il membro del team verranno rideterminati in base al listino prezzi di acquisto allegato al contratto di lavoro.  Nella scheda **Stime** della pagina **Dettagli progetto** seleziona il pulsante **Aggiorna prezzi** per visualizzare i prezzi aggiornati e/o i costi risultanti dalla decisione di subappaltare. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Opzioni di conto lavoro per un membro del team di progetto senza personale
La pagina **Dettagli membro del team** dispone dei campi della riga di conto lavoro e del conto lavoro che consentono a un responsabile di progetto di esprimere come desidera ricavare la capacità richiesta da un conto lavoro. Per subappaltare un membro del team di progetto come risorsa generica, attieniti alla seguente procedura:

1.  Scegli un conto lavoro nella pagina **Dettagli membro del team**.

2.  È possibile selezionare solo conto lavori con stato **Bozza** o **Confermato**. I conto lavoro con stato **Chiuso** o **Annullato** non possono essere selezionati. 

3.  Il campo **Riga conto lavoro** diventa visibile dopo aver selezionato un conto lavoro.

4.  Nel campo **Riga di conto lavoro** puoi selezionare solo le righe di conto lavoro relative al tempo. Non è possibile selezionare righe di conto lavoro per spese o materiali.

5.  Il ruolo per il record del membro del team di progetto deve corrispondere al ruolo nella riga di conto lavoro. Ciò garantisce che il tempo per il ruolo che viene stimato nel progetto sia lo stesso ruolo acquistato nella riga di conto lavoro. 

Quando un membro del team generico è associato a una riga di conto lavoro e un conto lavoro, il campo **Tipo di lavoratore** sulla riga del membro del team generico verrà aggiornato su **Lavoratore a contratto** e **Validità conto lavoro** sarà impostato su **Valido**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Opzioni di conto lavoro per un membro del team di progetto con personale
Come i membri del team generici o senza personale, anche la capacità dei membri del team con personale richiesta in un progetto può essere collegata a un conto lavoro. Per subappaltare un membro del team di progetto denominato, attieniti alla seguente procedura:

1.  Assicurati che la risorsa denominata sia configurata come un tipo di lavoratore a contratto di risorsa prenotabile. Inoltre, assicurati che il campo **Fornitore** sulla risorsa prenotabile corrisponda al fornitore del contratto di lavoro che stai selezionando. 

2.  È possibile selezionare solo conto lavori con stato **Bozza** o **Confermato**. I conto lavoro con stato **Chiuso** o **Annullato** non possono essere selezionati. 

3.  Il campo **Riga conto lavoro** diventa visibile dopo aver selezionato un conto lavoro.

4.  Nel campo **Riga di conto lavoro** puoi selezionare solo le righe di conto lavoro relative al tempo. Non è possibile selezionare righe di conto lavoro per spese o materiali.

5.  Il ruolo per il record del membro del team di progetto deve corrispondere al ruolo nella riga di conto lavoro. Ciò garantisce che il tempo per il ruolo che viene stimato nel progetto sia lo stesso ruolo acquistato nella riga di conto lavoro. 

Membri del team di progetto nominati che sono impostati come un tipo di lavoratore a contratto di **Risorsa prenotabile** verrà mostrato con lo stato di validità del conto lavoro **Non valido** se non sono collegati con un conto lavoro. Quando un membro del team di progetto denominato è associato a una riga di conto lavoro e un conto lavoro, il campo **Tipo di lavoratore** sulla riga del membro del team verrà aggiornato su **Lavoratore a contratto** e **Validità conto lavoro** sarà impostato su **Valido**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]