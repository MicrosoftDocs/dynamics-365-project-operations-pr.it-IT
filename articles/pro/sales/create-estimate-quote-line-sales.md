---
title: Stima di una riga dell'offerta basata su progetto
description: Questo argomento fornisce informazioni su come creare una stima su una riga di offerta basata su progetto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dbd3876e555ee6bc70308ef11a3528a5dd8b6a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273518"
---
# <a name="estimating-a-project-based-quote-line"></a>Stima di una riga dell'offerta basata su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Una riga di offerta basata su progetto contiene dettagli che aiutano a stimare il costo e i potenziali ricavi del lavoro richiesto per consegnare la riga di offerta.

Per stimare una riga di offerta basata su progetto, nella riga dell'offerta basata su progetto seleziona la scheda **Dettagli riga di offerta**. Esistono due modi per creare una stima su una riga di offerta basata su progetto:

- Creare manualmente la stima direttamente sulla riga dell'offerta utilizzando i dettagli della riga di offerta 
- Creare un progetto e un piano di progetto, quindi associare il progetto e le attività nel progetto alla riga dell'offerta. Verrà abilitato il processo per importare le stime sul piano di progetto nella riga dell'offerta in base alle informazioni fornite.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Creare stime direttamente su una riga di offerta basata su progetto

Per creare una stima su una riga di offerta basata su progetto, seleziona la scheda **Dettagli riga di offerta**. L'elemento della riga creato in questa scheda riepilogherà il valore offerto per questa riga di offerta. 

Per creare i dettagli della riga di offerta, seleziona **+ Nuovo dettaglio della riga di offerta** nella griglia secondaria **Dettagli riga di offerta**. Si aprirà un cursore di creazione rapida. I seguenti campi nel modulo **Riga di offerta**:

| **Campo** | **Luogo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- | --- |
| Descrizione | Creazione rapida | Una descrizione della stima specifica. | L'impostazione predefinita di questo campo è il dettaglio della riga di offerta correlato per il costo che viene creato automaticamente. |
| Classe di transazione | Creazione rapida | Questo elenco a discesa fornisce le classi di transazione incluse nella scheda **Generale** della riga di offerta basata su progetto.  | L'impostazione predefinita di questo campo è il dettaglio della riga di offerta correlato per il costo che viene creato automaticamente. |
| Ruolo | Creazione rapida | La persona che eseguirà questo lavoro o sosterrà questa spesa. | L'impostazione predefinita di questo campo è il dettaglio della riga di offerta correlato per il costo che viene creato automaticamente. |
| Categoria. | Creazione rapida | Categoria del lavoro o di spesa. | L'impostazione predefinita di questo campo è il dettaglio della riga di offerta correlato per il costo che viene creato automaticamente. |
| Data di inizio | Creazione rapida | Data di inizio del lavoro. | L'impostazione predefinita di questo campo è il dettaglio della riga di offerta correlato per il costo che viene creato automaticamente. |
| Data di fine | Creazione rapida | Data di fine del lavoro. | L'impostazione predefinita di questo campo è il dettaglio della riga di offerta correlato per il costo che viene creato automaticamente. |
| Unità gestione risorse | Creazione rapida | Unità di risorse che sosterrà questo costo e fornirà la risorsa per lavorarci. | L'impostazione predefinita di questo campo è il dettaglio della riga di offerta correlato per il costo che viene creato automaticamente. Questo campo viene utilizzato anche nel recupero del prezzo di costo. |
| Pianificazione unità | Creazione rapida | Unità di vendita del lavoro o della spesa. Le unità appartengono a una pianificazione di unità o a un gruppo di unità. Ad esempio, miglia e KM sono unità che appartengono a un gruppo di unità che descrive la distanza. | L'impostazione predefinita di questo campo è il dettaglio della riga di offerta correlato per il costo che viene creato automaticamente. |
| Unità | Creazione rapida | Unità del lavoro o della spesa. | L'impostazione predefinita di questo campo è il dettaglio della riga di offerta correlato per il costo che viene creato automaticamente. |
| Quantità | Creazione rapida | Quantità del lavoro o della spesa | L'impostazione predefinita di questo campo è il dettaglio della riga di offerta correlato per il costo che viene creato automaticamente. |
| Prezzo unitario | Creazione rapida | Tasso di fatturazione del ruolo che esegue il lavoro o prezzo di vendita della categoria di spesa. L'impostazione predefinita di questo campo è Ora in base alla combinazione di ruolo e unità di risorse nel listino prezzi del progetto valido per la data di inizio. Per le spese, questo campo ha come valore predefinito l'impostazione del prezzo per la categoria di transazione nel listino prezzi del progetto che è valido per la data di inizio. Se il metodo di determinazione del prezzo per la categoria di transazione non è il prezzo per unità, non esiste un valore predefinito e questo campo viene lasciato vuoto. | Tasso di costo del ruolo che esegue il lavoro o costo per unità della categoria di spesa. L'impostazione predefinita di questo campo è Ora in base alla combinazione di ruolo e unità di risorse nel prezzo dell'unità contratto del listino prezzi dell'offerta valido per la data di inizio. Per le spese, questo campo ha come valore predefinito l'impostazione del prezzo per la categoria di transazione nel listino dei prezzi di costo dell'unità contratto che è valido per la data di inizio. Se il metodo di determinazione del prezzo per la categoria di transazione non è il prezzo per unità, non esiste un valore predefinito e questo campo viene lasciato vuoto. |
| Imposta stimata | Creazione rapida | Puoi inserire manualmente l'imposta stimata per questo lavoro o spesa. | Non vi è alcun impatto downstream di questo campo. |
| Importa | Creazione rapida | Puoi possibile inserire manualmente le informazioni in questo campo se i campi **Quantità** e **Prezzo** vengono lasciati vuoti. Se questi campi non sono vuoti, questo campo diventa di sola lettura e viene calcolato come (Quantità \* Prezzo unitario) + IVA. | Non vi è alcun impatto downstream di questo campo. |

## <a name="update-prices-on-quote-line-details"></a>Aggiornare i prezzi sui dettagli della riga di offerta

Se hai modificato i prezzi sul listino prezzi di progetto allegato all'offerta o sul listino prezzi di costo dell'unità contratto, puoi selezionare **Ricalcola** nella pagina **Offerta**, per aggiornare i prezzi nei dettagli delle singole righe di offerta per riflettere questa modifica. Quando selezioni **Ricalcola**, viene visualizzato un avviso che informa che i prezzi sui dettagli delle righe di offerta per tutte le righe di offerta in questa offerta verranno reimpostati. Seleziona **Sì** per aggiornare i prezzi sia per i dettagli delle righe di offerta che di vendita.

## <a name="access-quote-line-details-for-cost"></a>Accedere ai dettagli della riga di offerta per il costo

Nella scheda **Dettagli riga di offerta** seleziona una riga nella griglia per abilitare alcune azioni sulla barra degli strumenti della griglia secondaria. La prima azione sulla barra degli strumenti della griglia secondaria quando viene selezionato un dettaglio della linea di offerta è **Apri dettagli di costo**. Seleziona **Apri dettagli di costo** per visualizzare il tasso di costo e l'importo correlati per questa riga di offerta.

> [!NOTE]
> Modificando l'unità di risorse, la quantità, le date, il ruolo o i valori di categoria nei dettagli della riga dell'offerta per il costo, cambierà i valori corrispondenti nei dettagli della riga dell'offerta per le vendite.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta sui dettagli della riga di offerta per costo e vendite

Valuta nel dettaglio della riga di offerta per i valori predefiniti di vendita dal listino prezzi del progetto che è valido per la data di inizio del dettaglio della riga di offerta.

Valuta nel dettaglio della riga di offerta per i valori predefiniti di costo dal listino prezzi dell'unità contratto dell'offerta che è valido per la data di inizio del dettaglio della riga di offerta per il costo.

I calcoli della redditività convertono l'importo sui dettagli della riga dell'offerta per costi e vendite nella valuta di base dell'ambiente per riportare il margine stimato complessivo sull'offerta.

Ciò potrebbe causare errori di arrotondamento della valuta e modificare i margini a causa della mancanza di tassi di cambio effettivi. Utilizza questi calcoli sulle offerte di progetto solo come approssimazioni e non come rapporti legali o di altro tipo effettivi che richiedono una maggiore precisione di arrotondamento e consapevolezza dell'efficacia della data per i tassi di cambio.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]