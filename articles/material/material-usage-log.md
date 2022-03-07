---
title: Registrare l'utilizzo di materiale in progetti e attività di progetto
description: Questo argomento fornisce informazioni su come registrare l'utilizzo di materiale in progetti e attività di progetto.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d8757049953fab0ad8bf6ee1a1d695fcb6df75b1be52641ad4af3b3137d7a0a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999276"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Registrare l'utilizzo di materiale in progetti e attività di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Quando un team di progetto svolge le attività di un progetto, consuma o utilizza materiali. Un registro di utilizzo di materiale fornisce un modo per registrare questo utilizzo in modo che possa essere approvato dal responsabile di progetto ed eventualmente fatturato al cliente. 

Per registrare l'utilizzo dei materiali in catalogo o fuori catalogo e inviarli all'approvatore, procedi come segue: 

1. Nel riquadro di spostamento, seleziona **Utilizzo di materiale** e quindi seleziona **Nuovo**.
2. Nella pagina **Nuovo utilizzo di materiale**, immetti le informazioni sull'utilizzo di materiale necessarie, quindi seleziona **Salva**.

La tabella seguente fornisce informazioni sui campi nella pagina **Registro dell'utilizzo di materiale**. 

| **Campo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- |
| Descrizione | Una descrizione dell'utilizzo di materiale specifico. | Non vi è alcun impatto downstream per questo campo. |
| Data | La data prevista per l'utilizzo di materiale. | Non vi è alcun impatto downstream per questo campo. |
| Project | Un elenco di progetti attivi. | La selezione di un progetto per un registro di utilizzo di materiale modifica il campo **Attività** per mostrare solo le attività presenti nel progetto. |
| Attività | Un elenco di attività per il progetto comprese le attività di riepilogo e del nodo foglia. | La selezione di un'attività per un registro di utilizzo di materiale influisce sul costo effettivo del materiale e sulle vendite effettive di materiale per un'attività. Se questo campo è vuoto, le vendite e il costo dell'utilizzo di materiale corrispondente vengono registrate e riepilogate solo a livello di progetto. |
| Selezione prodotto | Specifica se questo utilizzo di materiale è per un prodotto **Esistente** (catalogo) o un prodotto **Fuori catalogo**. | Questo campo determina il tipo di prodotto. |
| Prodotto | L'ID del prodotto del catalogo prodotti. Quando selezioni un ID prodotto, il campo **Selezione prodotto** diventa automaticamente **Prodotto esistente**. L'ID viene utilizzato per recuperare il prezzo di costo e di vendita dal listino prezzi. | Non vi è alcun impatto downstream per questo campo. |
| Descrizione prodotto fuori catalogo | Un campo di testo in cui immettere il nome del prodotto. Questo campo è disponibile quando selezioni il prodotto **Fuori catalogo** nel campo **Seleziona prodotto**.| Non vi è alcun impatto downstream per questo campo. |
| Risorsa prenotabile| Risorsa che ha utilizzato questo materiale nel progetto. L'impostazione predefinita di questo campo è la risorsa prenotabile dell'utente connesso, ma può essere modificata per registrare l'utilizzo per conto di altri membri del team di progetto. | Non vi è alcun impatto downstream per questo campo. |
| Unità di vendita | Il valore predefinito in questo campo proviene dall'unità di vendita impostata come valore predefinito nel prodotto del catalogo. Puoi aggiornare questo campo per selezionare un'altra unità di vendita. | Non vi è alcun impatto downstream per questo campo. |
| Unità | Il valore predefinito in questo campo è l'unità predefinita del prodotto selezionato. Puoi aggiornare questo campo per selezionare un'altra unità. | La modifica dell'unità comporta un costo e un prezzo unitario predefiniti differenti. |
| Quantità | La quantità del prodotto che è stata utilizzata nel progetto o nell'attività del progetto. | Non vi è alcun impatto downstream per questo campo. |
| Costo unitario | Il costo unitario della combinazione di prodotto e unità selezionati come impostato nel listino prezzi di costo applicabile. | Il costo unitario viene sempre mostrato nella valuta del costo del progetto. Se un costo unitario per la combinazione di prodotto e unità nel listino prezzi non è specificato, il costo unitario verrà impostato automaticamente su 0,00. |
| Costo totale | L'importo del costo calcolato come quantità \* costo unitario.| L'importo dei costi viene sempre visualizzato nella valuta di costo del progetto. |


## <a name="submit-material-usage-for-review-and-approval"></a>Inviare l'utilizzo di materiale per la revisione e l'approvazione 
Dopo aver acquisito tutto l'utilizzo di materiale e sei pronto per l'approvazione, devi inviare le informazioni sull'utilizzo affinché siano esaminate.

1. Vai a **Registro utilizzo di materiale** e seleziona una o più voci. Oppure seleziona tutti i record di utilizzo di materiale utilizzando la casella di controllo nell'intestazione.
2. Seleziona **Invia**. Il sistema elabora le voci selezionate e quindi crea le richieste di approvazione dell'utilizzo di materiale.

## <a name="recall-a-material-usage-log"></a>Richiamare un registro di utilizzo di materiale

Se necessario, puoi richiamare un utilizzo di materiale inviato. Il tempo necessario per richiamare una voce di utilizzo di materiale dipende dalla fase di approvazione.  Se il responsabile approvazione non ha ancora approvato la voce, il richiamo può avvenire immediatamente. Tuttavia, se la voce è già stata approvata, al responsabile approvazione viene chiesto di approvare il richiamo e di stornare le transazioni.

1. Vai a **Utilizzo di materiale** e nell'elenco dei registri di utilizzo di materiale, seleziona l'utilizzo di materiale da richiamare.
2. Seleziona **Richiama**. Se la voce di utilizzo di materiale non è stata ancora approvata, il sistema la richiama immediatamente. Se la voce di materiale è già stata approvata, viene creata una richiesta di richiamo per notificare al responsabile approvazione che si desidera richiamare l'utilizzo di materiale. Il responsabile approvazione confermerà quindi che lo storno può essere eseguito e la voce verrà restituita.

## <a name="delete-a-material-usage-log"></a>Eliminare un registro di utilizzo di materiale

Puoi eliminare i registri di utilizzo di materiale che non sono stati inviati. Per eliminare un registro di utilizzo di materiale che è già stato inviato, devi prima richiamarlo.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
