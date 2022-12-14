---
title: Stimare una riga di offerta basata su progetto
description: In questo articolo vengono fornite informazioni su come creare una stima su una riga di offerta di progetto.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bac3a3fa2d14c857edfb469a005406c346c8dbf6
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825992"
---
# <a name="estimate-a-project-quote-line"></a>Stimare una riga di offerta basata su progetto

_**Si applica a:** Distribuzione lite: dalla transazione alla fatturazione proforma, Project Operations per scenari basati su risorse/materiali non stoccati_

Una riga di offerta basata su progetto contiene dettagli che aiutano a stimare il costo e i potenziali ricavi del lavoro richiesto per consegnare la riga di offerta.

Per stimare una riga di offerta basata su progetto, nella riga dell'offerta basata su progetto seleziona la scheda **Dettagli riga di offerta**. Esistono due modi per creare una stima su una riga di offerta basata su progetto:

- Creare manualmente la stima direttamente sulla riga dell'offerta utilizzando i dettagli della riga di offerta. 
- Creare un progetto e un piano di progetto, quindi associare il progetto e le attività nel progetto alla riga dell'offerta. Verrà abilitato il processo per importare le stime sul piano di progetto nella riga dell'offerta in base alle informazioni fornite.

## <a name="create-estimates-directly-on-a-project-quote-line"></a>Creare stime direttamente su una riga di offerta di progetto

Per creare una stima su una riga di offerta basata su progetto, seleziona la scheda **Dettagli riga di offerta**. L'elemento della riga creato in questa scheda riepilogherà il valore offerto per questa riga di offerta. 

Per creare i dettagli della riga di offerta, seleziona **Nuovo dettaglio riga di offerta** nella griglia secondaria **Dettagli riga di offerta**. Si aprirà un cursore di creazione rapida. La tabella seguente fornisce dettagli sui campi nella pagina **Dettagli riga di offerta** e su come i valori influiscono sulla funzionalità.

| **Campo** | **Posizione** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- | --- |
| Descrizione | Creazione rapida | Una descrizione della stima specifica. | Il valore predefinito è il dettaglio della riga di offerta correlata per il costo creato automaticamente. |
| Classe di transazione | Creazione rapida | Questo elenco a discesa fornisce le classi di transazioni incluse nella scheda **Generale** della riga di offerta basata su progetto.  | Il valore predefinito è il dettaglio della riga di offerta correlata per il costo creato automaticamente. |
| Selezione prodotto | Creazione rapida | Si applica quando la classe di transazione è **Materiale**. Puoi specificare se questa riga di stima è per un prodotto **Esistente** (catalogo) o un prodotto **Fuori catalogo**. | Il valore predefinito è il dettaglio della riga di offerta correlata per il costo creato automaticamente. |
| Prodotto | Creazione rapida | L'ID del prodotto nel catalogo prodotti. Questo campo è abilitato se selezioni **Esistente** nel campo **Selezione prodotto**. L'ID viene utilizzato per recuperare il prezzo di vendita dal listino prezzi di progetto nell'offerta. | Il valore predefinito è il dettaglio della riga di offerta correlata per il costo creato automaticamente. |
| Prodotto fuori catalogo | Creazione rapida | Una casella di testo in cui immettere il nome del prodotto. Questo campo è abilitato solo se selezioni **Fuori catalogo** nel campo **Selezione prodotto**.| Il valore predefinito è il dettaglio della riga di offerta correlata per il costo creato automaticamente. |
| Ruolo | Creazione rapida | Il ruolo della persona che eseguirà questo lavoro o dovrà sostenere questa spesa. | Il valore predefinito è il dettaglio della riga di offerta correlata per il costo creato automaticamente. |
| Categoria. | Creazione rapida | La categoria del lavoro o della spesa. | Il valore predefinito è il dettaglio della riga di offerta correlata per il costo creato automaticamente. |
| Data di inizio | Creazione rapida | Data di inizio del lavoro. | Il valore predefinito è il dettaglio della riga di offerta per il costo creato automaticamente. |
| Data di fine | Creazione rapida | Data di fine del lavoro. | Il valore predefinito è il dettaglio della riga di offerta per il costo creato automaticamente. |
| Unità gestione risorse | Creazione rapida | L'unità di gestione risorse che sosterrà questo costo e fornirà la risorsa su cui lavorare. | Il valore predefinito è il dettaglio della riga di offerta correlata per il costo creato automaticamente e utilizzato nel recupero del prezzo di costo. |
| Pianificazione unità | Creazione rapida | L'unità di vendita di lavoro, prodotto o spesa. Le unità appartengono a una pianificazione di unità o a un gruppo di unità. Ad esempio, miglia e chilometri sono unità che appartengono a un gruppo di unità che descrive la distanza. | Il valore predefinito è il dettaglio della riga di offerta correlata per il costo creato automaticamente. |
| Unità | Creazione rapida | L'unità di lavoro, prodotto o spesa. | Il valore predefinito è il dettaglio della riga di offerta correlata per il costo creato automaticamente. |
| Quantità | Creazione rapida | La quantità di lavoro, prodotto o spesa. | Il valore predefinito è il dettaglio della riga di offerta correlata per il costo creato automaticamente. |
| Prezzo unitario | Creazione rapida |Il tasso di fatturazione del ruolo che esegue il lavoro, il prezzo unitario del prodotto o il prezzo di vendita del prodotto o della categoria di spesa. Il valore predefinito per questo campo è **Tempo** basato sulla combinazione dei valori delle dimensioni di determinazione dei prezzi nella riga del prezzo del ruolo del listino di progetto in vigore alla data di inizio. Per **Spese**, il valore predefinito è basato sull'impostazione del prezzo per la categoria di transazione nel listino prezzi di progetto in vigore alla data di inizio. Se il metodo di determinazione dei prezzi per la categoria di transazione non è il prezzo unitario, non si ha un valore predefinito e questo campo viene lasciato vuoto. Per i prodotti, il valore predefinito è basato sulla riga **Voce di listino** nel listino prezzi di progetto in vigore alla data di inizio.| Il tasso di costo del ruolo che esegue il lavoro, il costo unitario della categoria di spesa o il costo unitario del prodotto. Il valore predefinito per questo campo è **Tempo** basato sulla combinazione dei valori delle dimensioni di determinazione dei prezzi nella riga del prezzo del ruolo del listino di progetto in vigore alla data di inizio. Per **Spese**, il valore predefinito è basato sull'impostazione del prezzo per la categoria di transazione nel listino prezzi di progetto in vigore alla data di inizio. Se il metodo di determinazione dei prezzi per la categoria di transazione non è il prezzo unitario, non si ha un valore predefinito e questo campo viene lasciato vuoto. Per i prodotti, il valore predefinito è basato sulla riga **Voce di listino** nel listino prezzi di progetto in vigore alla data di inizio.|
| Imposta stimata | Creazione rapida | Puoi inserire manualmente l'imposta stimata per questo lavoro o spesa. | Non vi è alcun impatto downstream per questo campo. |
| Importa | Creazione rapida | Puoi possibile inserire manualmente le informazioni in questo campo se i campi **Quantità** e **Prezzo** vengono lasciati vuoti. Se questi campi non sono vuoti, questo campo diventa di sola lettura e viene calcolato come (Quantità \* Prezzo unitario) + IVA. | Non vi è alcun impatto downstream per questo campo. |


## <a name="update-prices-on-quote-line-details"></a>Aggiornare i prezzi sui dettagli della riga di offerta

Se sono stati modificati i prezzi nel listino prezzi di progetto allegato all'offerta o nel listino prezzi di costo dell'unità contratto, puoi selezionare **Ricalcola** nella pagina **Offerta** per aggiornare i prezzi nei dettagli delle singole righe di offerta per riflettere questa modifica. Quando selezioni **Ricalcola**, viene visualizzato un avviso che informa che i prezzi nei dettagli delle righe di offerta per tutte le righe di offerta in questa offerta verranno reimpostati. Seleziona **Sì** per aggiornare i prezzi sia per i dettagli delle righe di offerta per costo e vendite.

## <a name="access-quote-line-details-for-cost"></a>Accedere ai dettagli delle righe di offerta per il costo

Nella scheda **Dettagli riga di offerta** seleziona una riga nella griglia per abilitare alcune azioni sulla barra degli strumenti della griglia secondaria. La prima azione sulla barra degli strumenti della griglia secondaria quando viene selezionato un dettaglio della riga di offerta è **Apri dettagli di costo**. Seleziona **Apri dettagli di costo** per visualizzare il tasso di costo e l'importo correlati per questa riga di offerta.

> [!NOTE]
> Modificando l'unità di risorse, la quantità, le date, il ruolo o i valori di categoria nel dettaglio della riga di offerta per il costo, cambierà i valori corrispondenti nei dettagli della riga di offerta per le vendite.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta sui dettagli della riga di offerta per costo e vendite

Valuta nel dettaglio della riga di offerta per i valori predefiniti di vendita dal listino prezzi del progetto in vigore alla data di inizio del dettaglio della riga di offerta.

Valuta nel dettaglio della riga di offerta per i valori predefiniti di costo dal listino prezzi dell'unità contratto dell'offerta in vigore alla data di inizio del dettaglio della riga di offerta per il costo.

I calcoli della redditività convertono l'importo sui dettagli della riga di offerta per costi e vendite nella valuta di base dell'ambiente per riportare il margine stimato complessivo sull'offerta.

> [!NOTA: potrebbero verificarsi errori di arrotondamento della valuta e margini modificati a causa della mancanza di tassi di cambio validi. Utilizza questi calcoli solo nei contratti di progetto poiché si tratta di approssimazioni e non sono per report legali o di altro tipo effettivi che richiedono una maggiore precisione di arrotondamento e consapevolezza dell'effettività della data per i tassi di cambio.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
