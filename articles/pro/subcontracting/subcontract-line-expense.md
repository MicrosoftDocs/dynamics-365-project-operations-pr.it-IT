---
title: Righe conto lavoro per categorie di spesa
description: In questo articolo viene spiegato come registrare le righe di conto lavoro per le spese e utilizzare i campi per registrare l'acquisto di tempo dei fornitori.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ba1241ce40b7c5b488e278e8f1b8e9f352f45dc8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522612"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Righe conto lavoro per categorie di spesa

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione lite: dalla transazione alla fatturazione proforma_

Un conto lavoro in Dynamics 365 Project Operations può avere una riga per le categorie di spesa. Le voci di conto lavoro per le categorie di spesa consentono a un responsabile di progetto di acquistare categorie di servizi o prodotti da fornitori che possono eseguire un addebito su un progetto.

Per creare una voce di conto lavoro per le categorie di spesa in Project Operations, completa la seguente procedura.

1. Nel riquadro di spostamento, seleziona **Conti lavoro** e apri il conto lavoro con cui desideri lavorare.
2. Nella scheda **Voci di conto lavoro**, seleziona **Nuovo** per creare una nuova riga.
3. Nella pagina **Creazione rapida**, nel campo **Classe di transazione**, seleziona **Spesa** e inserisci o seleziona qualsiasi altra informazione richiesta per il campo.

La seguente tabella fornisce informazioni sui campi nella pagina dei dettagli **Voce conto lavoro** e nella pagina **Creazione rapida**.

| **Campo** | **Descrizione** | **Impatto funzionale** |
| --- | --- | --- |
| Nome | Nome della riga di conto lavoro per facilitare l'identificazione. | Questa verrà mostrata come prima colonna in tutte le ricerche basate sulle righe di conto lavoro. |
| Descrizione | Una breve descrizione delle categorie di spesa acquistate nella riga del contratto di conto lavoro. | Nessuna |
|Tipo di linea | Il valore predefinito di questo campo è **Basato su quantità**. |Nessuna |
| Metodo di fatturazione | Questo è un set di opzioni che rappresenta i due principali modelli di contrattazione supportati da Project Operations: **Prezzo fisso** e **Tempistica e materiali**. | Se è stato selezionato il metodo di fatturazione a prezzo fisso, per le righe del conto di lavoro viene resa disponibile una pianificazione fattura basata su passaggi fondamentali. |
| Classe di transazione | Il valore predefinito di questo campo è **Data/Ora**. Per creare voci di conto lavoro per l'acquisto di prodotti, impostare il campo **Classe di transazione** su **Spesa**.  | Ciò indica che la riga del conto lavoro viene utilizzata per registrare l'acquisto di una categoria di spesa da utilizzare sui progetti. |
| Categoria di transazione | Mostra un elenco di categorie di transazioni attive nel sistema. |Nessuna |
| Inizio richiesto | Inserisci la data in cui le categorie di acquisto devono essere disponibili presso il fornitore. | L'inizio richiesto viene utilizzato per selezionare un listino prezzi dai listini prezzi del progetto allegati al conto lavoro. Il costo della categoria nella riga del conto lavoro deriva da quel listino prezzi. |
| Fine richiesta | Inserisci la data in cui le categorie di acquisto non sarebbero più necessarie. | Verrà utilizzata per visualizzare avvisi quando un responsabile di progetto associa questa riga di conto lavoro a specifiche stime di spesa del progetto richieste dopo questa data. |
| Quantità ordinata | Quantità della categoria acquistata dal fornitore. | Questa verrà utilizzata per visualizzare avvisi quando un responsabile di progetto sta andando oltre questa quantità.|
| Unità di vendita | Il valore predefinito si basa sul gruppo di unità predefinito impostato per la categoria selezionata. |Nessuna |
| Unità | Il valore si basa sull'unità predefinita impostata per la categoria selezionata.  | La combinazione di **Categoria** e **Unità** verrà utilizzata come valore predefinito o calcolato per il prezzo unitario per la riga di conto lavoro.  |
| Prezzo unitario | Il valore predefinito utilizza la combinazione di **Categoria** e **Unità** dai prezzi di categoria relativi al listino prezzi del progetto, applicabile per l'inizio richiesto della riga di conto lavoro. |Nessuna |
| Subtotale | Questo è un campo di sola lettura che viene calcolato come Quantità X Prezzo unitario, se vengono immessi sia i valori di quantità che di prezzo unitario. Se uno o entrambi i campi sono vuoti, puoi inserire un valore in questo campo. |Nessuna |
| IVA | Immetti l'importo IVA. |Nessuna |
| Totale importo | L'importo totale della voce di conto lavoro incluse le imposte. Questo campo viene calcolato come Subtotale + IVA. |Nessuna |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
