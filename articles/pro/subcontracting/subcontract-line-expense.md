---
title: Righe conto lavoro per categorie di spesa
description: Questo argomento spiega come registrare le righe di conto lavoro per le spese e utilizzare i campi per registrare l'acquisto di prodotti dai fornitori.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323826"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Righe conto lavoro per categorie di spesa

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Un conto lavoro in Dynamics 365 Project Operations può avere una riga per le categorie di spesa. Le voci di conto lavoro per le categorie di spesa consentono a un responsabile di progetto di acquistare categorie di servizi o prodotti da fornitori che possono eseguire un addebito su un progetto.

Per creare una voce di conto lavoro per le categorie di spesa in Project Operations, completa la seguente procedura.

1. Nel riquadro di spostamento, seleziona **Conti lavoro** e apri il conto lavoro con cui desideri lavorare.
2. Nella scheda **Voci di conto lavoro**, seleziona **Nuovo** per creare una nuova riga.
3. Nella pagina **Creazione rapida**, nel campo **Classe di transazione**, seleziona **Spesa** e inserisci o seleziona qualsiasi altra informazione richiesta per il campo.

La seguente tabella fornisce informazioni sui campi nella pagina dei dettagli **Voce conto lavoro** e nella pagina **Creazione rapida**.

| **Campo** |  **Descrizione** |
| ----------| ---------------- |
| Nome | Il nome della voce di conto lavoro. |
| Descrizione | Una breve descrizione delle categorie di prodotti o servizi acquistati nella voce di conto lavoro. |
| Tipo di linea | Il valore predefinito di questo campo è **Basato su quantità**.  |
| Metodo di fatturazione | Il metodo di fatturazione della voce di conto lavoro. In base al metodo di fatturazione della riga, viene resa disponibile una pianficazione di fatturazione basata su passaggi fondamentali per il metodo di fatturazione a prezzo fisso.  |
| Classe di transazione | Il valore predefinito di questo campo è **Ore**. Per creare voci di conto lavoro per l'acquisto di prodotti, impostare il campo **Classe di transazione** su **Spesa**. Questo valore del campo indica che la voce del conto lavoro viene utilizzata per registrare un acquisto di una categoria di prodotti o servizi da utilizzare nei progetti. |
| Categoria di transazione | Seleziona la categoria di transazione. |
| Inizio richiesto | La data in cui le categorie di acquisto devono essere disponibili dal fornitore. La data richiesta viene utilizzata anche per selezionare un listino prezzi per il progetto dai listini allegati al conto lavoro. Il costo della categoria nella voce del conto lavoro viene quindi predefinito da quel listino prezzi. |
| Fine richiesta | La data in cui le categorie di acquisto non sono più necessarie. Questa data richiama un avviso quando un responsabile di progetto associa questa voce di conto lavoro a specifiche stime di spesa sui progetti con data successiva a tale data. |
| Quantità ordinata | La quantità della categoria acquistata dal venditore. Quando un responsabile di progetto eccede questa quantità acquistata, verrà visualizzato un avviso.  |
| Unità di vendita | Il valore predefinito per questo campo si basa sulle unità di vendita impostate per la categoria selezionata. |
| Unità | Il valore predefinito per questo campo si basa sulle unità impostate per la categoria selezionata. La combinazione di categoria e unità viene utilizzata per calcolare il prezzo unitario predefinito nella voce del conto lavoro. |
| Prezzo unitario | Il valore del campo Prezzo unitario viene predefinito utilizzando la combinazione di categoria e unità dai prezzi di categoria relativi al listino prezzi del progetto applicabile per la data di consegna richiesta della riga di conto lavoro.  |
| Subtotale | Questo è un campo di sola lettura che viene calcolato automaticamente come prezzo unitario della quantità se vengono inseriti sia il valore della quantità che del prezzo unitario. Se uno o tutti e due i campi sono vuoti puoi inserire un valore manualmente in questo campo.  |
| IVA | Immetti l'importo IVA.  |
| Totale importo | L'importo totale della voce di conto lavoro incluse le imposte. Questo campo viene calcolato come subtotale + importo IVA.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
