---
title: Stimare una voce di contratto basata su progetto - semplice
description: Questo argomento fornisce informazioni sulla stima di una voce di contratto basata su progetto.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 186b982ee440576e10cf5b78922848b8877afd51
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273542"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Stimare una voce di contratto basata su progetto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

In Dynamics 365 Project Operations, una voce di contratto basata su progetto contiene dettagli che aiutano a stimare il costo e il ricavo potenziale del lavoro richiesto per consegnare la voce di contratto.

Per stimare una voce di contratto basata su progetto, vai alla scheda **Dettagli di voce di contratto** della **voce di contratto** basata su progetto.  Esistono due modi per creare una stima su una voce di contratto basata su progetto:

   - Crea un stima direttamente nella voce di contratto aggiungendo manualmente i dettagli della voce di contratto.
   - Crea un progetto e un piano di progetto, quindi associa il progetto e le attività alla voce di contratto di progetto. Ciò abilita il processo mediante il quale è possibile importare la stima del piano di progetto nella voce di contratto in base ai componenti inclusi nella voce di contratto.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Creare una stima direttamente in una voce di contratto basata su progetto

1. Vai alla voce di contratto e seleziona la scheda **Dettagli di voce di contratto**. Le righe create in questa scheda vengono riepilogate e visualizzate come **Valore di contratto** per questa **voce di contratto**. 
2. Nella griglia secondaria **Dettagli di voce di contratto**, seleziona **+ Nuovi dettagli di voce di contratto**. Si apre un indicatore di creazione rapida. I seguenti campi sono disponibili nel modulo **Dettagli di voce di contratto**:

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| **Descrizione** | **Creazione rapida** | Una descrizione della stima specifica. | L'impostazione predefinita di questo campo è il dettaglio della voce di contratto correlato per i costi che vengono creati automaticamente. |
| **Classe di transazione** | **Creazione rapida** | Questo menu a discesa è un elenco di classi di transazione incluse nella scheda **Generale** della voce di contratto basata su progetto. | L'impostazione predefinita di questo campo è il dettaglio della voce di contratto correlato per i costi che vengono creati automaticamente. |
| **Ruolo** | **Creazione rapida** | Il ruolo della persona che esegue questo lavoro o sostiene questa spesa. | L'impostazione predefinita di questo campo è il dettaglio della voce di contratto correlato per i costi che vengono creati automaticamente. |
| **Categoria** | **Creazione rapida** | La categoria del lavoro o della spesa. | L'impostazione predefinita di questo campo è il dettaglio della voce di contratto correlato per i costi che vengono creati automaticamente. |
| **Data di inizio** | **Creazione rapida** | Data di inizio del lavoro. | L'impostazione predefinita di questo campo è il dettaglio della voce di contratto correlato per i costi che vengono creati automaticamente. |
| **Data di fine** | **Creazione rapida** | Data di fine del lavoro. | L'impostazione predefinita di questo campo è il dettaglio della voce di contratto correlato per il costo che viene creato automaticamente. |
| **Unità gestione risorse** | **Creazione rapida** | L'unità gestione risorse che sostiene questo costo e fornisce la risorsa in cui lavorare. | L'impostazione predefinita di questo campo è il dettaglio della voce di contratto correlato per i costi che vengono creati automaticamente. Questo campo viene utilizzato anche nel recupero del prezzo di costo. |
| **Pianificazione unità** | **Creazione rapida** | Il gruppo di unità del lavoro o della spesa. Le unità appartengono a una pianificazione di unità o a un gruppo di unità. Per esempio, *miglia* e *chilometri (Km)* sono unità che appartengono a un gruppo di unità che descrivono la distanza. | L'impostazione predefinita di questo campo è il dettaglio della voce di contratto correlato per i costi che vengono creati automaticamente. |
| **Unità** | **Creazione rapida** | L'unità del lavoro o della spesa. | L'impostazione predefinita di questo campo è il dettaglio della voce di contratto correlato per i costi che vengono creati automaticamente. |
| **Quantità** | **Creazione rapida** | La quantità del lavoro o della spesa. | L'impostazione predefinita di questo campo è il dettaglio della voce di contratto correlato per i costi che vengono creati automaticamente. |
| **Prezzo unitario** | **Creazione rapida** | Il tasso di fatturazione del ruolo che esegue il lavoro o il prezzo di vendita della categoria di spesa. L'impostazione predefinita di questo campo è **Ora** in base alla combinazione di ruolo e unità gestione risorse nel listino prezzi di progetto valido per la data di inizio. Per le spese, l'impostazione predefinita di questo campo proviene dall'impostazione del prezzo per la categoria di transazione nel listino prezzi di progetto che è valido per la data di inizio. Se il metodo di determinazione del prezzo per la categoria di transazione non è il **prezzo per unità**, non esiste un valore predefinito e questo campo viene lasciato vuoto. | Il tasso di costo del ruolo che esegue il lavoro o il costo per unità della categoria di spesa. Il valore predefinito di questo campo è **Ora basata su ruolo** e la combinazione di unità gestione risorse sulla riga di prezzo del ruolo del listino prezzi di costo allegato all'unità contratto valida per la data di inizio. Per le spese, l'impostazione predefinita di questo campo si basa sulla riga di prezzo di categoria del listino prezzi di costo allegato all'unità contratto che è valida per la data di inizio. Se il metodo di determinazione del prezzo per la categoria di transazione non è il prezzo per unità, non esiste un valore predefinito e questo campo viene lasciato vuoto. |
| **Imposta stimata** | **Creazione rapida** | L'imposta stimata per questo lavoro o spesa come input dell'utente. | L'imposta stimata per questo lavoro o spesa come input dell'utente. |
| **Importo** | **Creazione rapida** | Questo valore in questo campo può essere aggiunto dall'utente se i campi **Quantità** e **Prezzo** vengono lasciati vuoti. Se **Quantità** e **Prezzo** sono compilati, il campo **Importo** è di sola lettura e viene calcolato come **(Quantità \* Prezzo unitario) + Imposta**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Aggiornare i prezzi sui dettagli della voce di contratto

Se si modificano i prezzi nel listino prezzi di progetto allegato al contratto o nel listino prezzi di costo dell'unità contratto, è possibile aggiornare i prezzi nei dettagli della singola voce di contratto per riflettere la modifica. Nella pagina **Contratto** seleziona **Ricalcola**. Si apre un avviso per informarti che i prezzi per tutte le voci di contratto su questo contratto vengono reimpostati. Seleziona **Sì** per aggiornare i prezzi per i dettagli della voce di contratto di vendita e di costo.

## <a name="access-contract-line-details-for-cost"></a>Accedere ai dettagli della voce di contratto per il costo

Nella scheda **Dettagli voce di contratto** seleziona una riga nella griglia per visualizzare le azioni sulla barra degli strumenti della griglia secondaria. La prima azione sulla barra degli strumenti della griglia secondaria è **Apri dettagli di costo**. Per visualizzare il tasso di costo e l'importo correlati per questo dettaglio della voce di contratto, seleziona **Apri dettagli di costo**. 

> [!NOTE]
> La modifica dei valori della società di gestione risorse, unità gestione risorse, quantità, date, ruolo o categoria nei dettagli della voce di contratto per **Costi** modifica anche i valori corrispondenti nei dettagli della voce di contratto per **Vendite**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta sui dettagli della voce di contratto per costi e vendite

Il dettaglio della voce di contratto per **Vendite** imposta la valuta predefinita dal listino prezzi di progetto che è valida per la data di inizio dei dettagli della voce di contratto.

Il dettaglio della voce di contratto per **Costi** imposta la valuta predefinita dal listino prezzi dell'unità contraente del contratto che è valido per la data di inizio dei dettagli della voce di contratto per **Costi**.

I calcoli della redditività convertono gli importi per i dettagli della voce di contratto per **Costi** e **Vendite** nella valuta di base dell'ambiente per riportare i margini complessivi effettivi e stimati sul contratto.

> [!NOTE]
> Potrebbero verificarsi errori di arrotondamento della valuta e margini modificati a causa della mancanza di tassi di cambio validi. Utilizza questi calcoli sui contratti di progetto solo come approssimazione e non per documenti legali effettivi o di altro tipo che richiedono una maggiore precisione di arrotondamento e consapevolezza della validità della data per i tassi di cambio.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]