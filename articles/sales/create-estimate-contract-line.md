---
title: Stimare una voce di contratto di progetto
description: Questo argomento fornisce informazioni relative alle stime su una voce di contratto di progetto.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7cb7d7eccf62837ee5abf4cbe29a21dc728eb7ef
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858523"
---
# <a name="estimate-a-project-contract-line"></a>Stimare una voce di contratto di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_ 

In Dynamics 365 Project Operations, una voce di contratto basata su progetto contiene dettagli che aiutano a stimare il costo e il ricavo potenziale del lavoro richiesto per consegnare la voce di contratto.

Per stimare una voce di contratto basata su progetto, vai alla scheda **Dettaglio voce di contratto** della **voce di contratto** basata su progetto.  Esistono due modi per creare una stima su una voce di contratto basata su progetto:

   - Crea un stima direttamente nella voce di contratto aggiungendo manualmente i dettagli della voce di contratto.
   - Crea un progetto e un piano di progetto, quindi associa il progetto e le attività alla voce di contratto di progetto. Ciò abilita il processo mediante il quale è possibile importare la stima del piano di progetto nella voce di contratto in base ai componenti inclusi nella voce di contratto.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Creare una stima direttamente su una voce di contratto di progetto

Per creare una stima direttamente su una voce di contratto di progetto, procedi come segue:

1. Vai alla voce di contratto e seleziona la scheda **Dettaglio voce di contratto**. Le righe create in questa scheda vengono riepilogate e visualizzate come **Valore di contratto** per questa **voce di contratto**. 
2. Nella griglia secondaria **Dettagli di voce di contratto**, seleziona **Nuovo dettaglio voce di contratto**. Si apre un indicatore di creazione rapida. I seguenti campi sono disponibili nella pagina **Dettagli voce di contratto**.

| Campo | Posizione | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| **Descrizione** | **Creazione rapida** | Una descrizione della stima specifica. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente. |
| **Classe di transazione** | **Creazione rapida** | Questo elenco di classi di transazioni è incluso nella scheda **Generale** della voce di contratto basata su progetto. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente. |
| **Selezione prodotto** | **Creazione rapida** | Si applica quando la classe di transazione è **Materiale**. Puoi specificare se questa riga di stima è per un prodotto **Esistente** (catalogo) o un prodotto **Fuori catalogo**. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente. |
| **Prodotto** | **Creazione rapida** | L'ID del prodotto del catalogo prodotti. Questo campo è abilitato solo quando selezioni **Prodotto esistente** nel campo **Selezione prodotto**. L'ID viene utilizzato per recuperare il prezzo di vendita dal listino prezzi di progetto nel contratto. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente. |
| **Prodotto fuori catalogo** | **Creazione rapida** | Un campo di testo in cui inserire il nome del prodotto. Questo campo è abilitato solo quando selezioni **Fuori catalogo** nel campo **Selezione prodotto**.| Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente. |
| **Ruolo** | **Creazione rapida** | Il ruolo della persona che esegue questo lavoro o sostiene questa spesa. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente.|
| **Categoria.** | **Creazione rapida** | La categoria del lavoro o della spesa. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente.|
| **Data di inizio** | **Creazione rapida** | Data di inizio del lavoro. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente. |
| **Data di fine** | **Creazione rapida** | Data di fine del lavoro. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente. |
| **Società resourcing** | **Creazione rapida** | La società di gestione risorse o la persona giuridica che sostiene questo costo e fornisce la risorsa su cui lavorare. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente e utilizzato nel recupero del prezzo di costo. |
| **Unità gestione risorse** | **Creazione rapida** | L'unità di gestione risorse che sostiene questo costo e fornisce la risorsa su cui lavorare. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente e utilizzato nel recupero del prezzo di costo. |
| **Pianificazione unità** | **Creazione rapida** | L'unità di vendita di lavoro, prodotto o spesa. Le unità appartengono a una pianificazione di unità o a un gruppo di unità. Ad esempio, *miglia* e *chilometri (km)* sono unità che appartengono a un gruppo di unità che descrive la distanza. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente. |
| **Unità** | **Creazione rapida** | L'unità di lavoro, prodotto o spesa. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente. |
| **Quantità** | **Creazione rapida** | La quantità di lavoro, prodotto o spesa. | Il valore predefinito è il dettaglio della voce di contratto correlata per il costo creato automaticamente. |
| **Prezzo unitario** | **Creazione rapida** | Il tasso di fatturazione del ruolo che esegue il lavoro, il prezzo unitario del prodotto o il prezzo di vendita del prodotto o della categoria di spesa. Il valore predefinito di **Tempo** è basato sulla combinazione dei valori delle dimensioni di determinazione dei prezzi nella riga del prezzo del ruolo del listino prezzi del progetto in vigore alla data di inizio. Per **Spese**, il valore predefinito di questo campo è basato sull'impostazione del prezzo per la categoria di transazione nel listino prezzi del progetto in vigore alla data di inizio. Se il metodo di determinazione del prezzo per la categoria di transazione non è il **prezzo per unità**, non esiste un valore predefinito e questo campo viene lasciato vuoto. Per i prodotti, il valore predefinito di questo campo è basato sulla riga **Voce di listino** nel listino prezzi del progetto in vigore alla data di inizio.| Il tasso di costo del ruolo che esegue il lavoro o il costo unitario della categoria di spesa o il costo unitario del prodotto. Il valore predefinito di **Tempo** è basato sulla combinazione dei valori delle dimensioni di determinazione dei prezzi sulla riga del listino prezzi di costo associato all'unità contratto in vigore alla data di inizio. Per **Spese**, il valore predefinito di questo campo è basato sulla riga dei prezzi di categoria del listino prezzi di costo associato all'unità contratto in vigore alla data di inizio. Se il metodo di determinazione del prezzo per la categoria di transazione non è il prezzo per unità, non esiste un valore predefinito e questo campo viene lasciato vuoto. Per i prodotti, il valore predefinito di questo campo è basato sulla riga **Voce di listino** del listino prezzi di costo associato all'unità contratto in vigore alla data di inizio.|
| **Imposta stimata** | **Creazione rapida** | L'imposta stimata per questo lavoro o spesa come input dell'utente. | &nbsp; |
| **Importa** | **Creazione rapida** | Il valore in questo campo può essere aggiunto se i campi **Quantità** e **Prezzo** sono lasciati vuoti. Se i campi **Quantità** e **Prezzo** sono riempiti, il campo **Quantità** è di sola lettura ed è calcolato come **(Quantità \* Prezzo unitario) + IVA**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Aggiornare i prezzi sui dettagli della voce di contratto

Se si modificano i prezzi nel listino prezzi di progetto allegato al contratto o nel listino prezzi di costo dell'unità contratto, è possibile aggiornare i prezzi nel dettaglio della singola voce di contratto per riflettere la modifica. Nella pagina **Contratto** seleziona **Ricalcola**. Viene visualizzato un avviso per informarti che i prezzi di tutte le voci di contratto in questo contratto vengono reimpostati. Seleziona **Sì** per aggiornare i prezzi per i dettagli della voce di contratto di vendita e di costo.

## <a name="access-contract-line-details-for-cost"></a>Accedere ai dettagli della voce di contratto per il costo

Nella scheda **Dettagli voce di contratto** seleziona una riga nella griglia per visualizzare le azioni sulla barra degli strumenti della griglia secondaria. La prima azione sulla barra degli strumenti della griglia secondaria è **Apri dettagli di costo**. Per visualizzare il tasso di costo e l'importo correlati per questo dettaglio della voce di contratto, seleziona **Apri dettagli di costo**. 

> [!NOTE]
> La modifica dei valori della società di gestione risorse, unità gestione risorse, quantità, date, ruolo o categoria nel dettaglio della voce di contratto per **Costi** modifica anche i valori corrispondenti nel dettaglio della voce di contratto per **Vendite**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta sui dettagli della voce di contratto per costi e vendite

Il dettaglio della voce di contratto per **Vendite** imposta la valuta predefinita dal listino prezzi di progetto in vigore alla data di inizio del dettaglio della voce di contratto.

Il dettaglio della voce di contratto per **Costi** imposta la valuta predefinita dal listino prezzi dell'unità contraente del contratto in vigore alla data di inizio del dettaglio della voce di contratto per **Costi**.

I calcoli della redditività convertono gli importi per i dettagli della voce di contratto per **Costi** e **Vendite** nella valuta di base dell'ambiente per riportare i margini complessivi effettivi e stimati sul contratto.

> [!NOTE]
> Potrebbero verificarsi errori di arrotondamento della valuta e margini modificati a causa della mancanza di tassi di cambio validi. Utilizza questi calcoli solo nei contratti di progetto poiché si tratta di approssimazioni e non sono per report legali o di altro tipo effettivi che richiedono una maggiore precisione di arrotondamento e consapevolezza dell'effettività della data per i tassi di cambio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
