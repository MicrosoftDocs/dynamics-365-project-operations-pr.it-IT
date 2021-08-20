---
title: Gestire una fattura basata su progetto proforma
description: Questo argomento fornisce informazioni su come gestire e utilizzare fatture basate su progetto proforma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cba74c14f6d039dce0650f25ee04cbe35ec8f668b774cdaaa3bbf1aab99cb44d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989331"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Gestire una fattura basata su progetto proforma

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

In Dynamics 365 Project Operations, le fatture proforma vengono create come estensione delle fatture in Dynamics 365 Sales. Tuttavia, ci sono molte differenze nel processo di fatturazione tra Sales e Project Operations quando si tratta di fatturazione. Ad esempio, non è possibile creare una nuova fattura dalla pagina **Elenco fatture** in Project Operations, ma è possibile farlo in Sales. Queste differenze ed estensioni sono in atto per supportare i processi di fatturazione per progetti diversi da una tipica fattura per un ordine di vendita.

> [!IMPORTANT]
> A causa delle differenze, non utilizzare le fatture in Sales e Project Operations in modo intercambiabile.

## <a name="invoice-header"></a>Intestazione della fattura

Le seguenti informazioni sono disponibili nell'intestazione di una fattura proforma in Project Operations.

| Campo | Posizione | Descrizione |
| --- | --- | --- | 
| **ID fattura** | Scheda **Riepilogo** | L'ID che viene generato automaticamente quando una fattura proforma viene creata. Un campo di sola lettura che non è possibile modificare. Questo campo viene utilizzato come riferimento per ogni fattura proforma. |
| **Nome** | Scheda **Riepilogo** | Imposta il nome del contratto di progetto predefinito. Questo campo può essere modificato. | 
| **Valuta** | Scheda **Riepilogo** | Imposta la valuta del contratto di progetto predefinito. Un campo di sola lettura che non è possibile modificare. |
| **Listino prezzi** | Scheda **Riepilogo** | Imposta il listino prezzi del contratto di progetto predefinito. Un campo di sola lettura che non è possibile modificare. | 
| **Opportunità** | Scheda **Riepilogo** | Il riferimento all'opportunità collegata. Un campo di sola lettura che non è possibile modificare. | 
| **Contratto** | Scheda **Riepilogo** | Il riferimento al contratto di progetto collegato. Un campo di sola lettura che non è possibile modificare. | 
| **Cliente** | Scheda **Riepilogo** | Il riferimento al contratto di progetto collegato. Un campo di sola lettura che non è possibile modificare. |
| **Descrizione** | Scheda **Riepilogo** | Il campo di testo che descrive la fattura. Questo campo può essere modificato. | 
| **Fatturazione** e campi correlati | **Scheda Riepilogo** | I valori predefiniti vengono impostati dal cliente del contratto di progetto. Questo campo può essere modificato.  | 
| **Stato** | Scheda **Riepilogo** | Consente di impostare le opzioni **Attiva**, **Chiusa**, **Pagata** e **Annullata** che possono essere modificate. Gli stati non supportati per Project Operations sono **Chiuso** e **Annullato**. </br> Lo stato è impostato su **Attivo** quando viene creata la fattura. </br>Lo stato deve essere impostato su **Pagato** solo dopo la conferma della fattura.  | 
| **Stato fattura di progetto** | Scheda **Riepilogo** | Consente di impostare le opzioni **Bozza**, **In revisione** e **Confermata**, che possono essere modificate. In entrambi gli stati **Bozza** e **In revisione**, la fattura può essere modificata. La fattura non può essere modificata dopo la conferma. | 
| **Totale dettagli** | Scheda **Riepilogo** | La somma degli importi su tutte le righe della fattura dopo anticipi e detrazioni. Un campo di sola lettura che non è possibile modificare.  Questo campo viene utilizzato per calcolare l'importo finale. | 
| **Sconto (%)** | Scheda **Riepilogo** | Questo campo può essere modificato per inserire una percentuale di sconto. Questo campo non è supportato dalla funzionalità Project Operations. Questo campo non è supportato.|  
| **Importo sconto** | Scheda **Riepilogo** | Questo campo può essere modificato per inserire un importo di sconto. Questo campo non è supportato dalla funzionalità Project Operations. Questo campo non è supportato. |  
| **Totale senza spedizione** | **Scheda Riepilogo** | L'importo totale della fattura dopo l'applicazione degli sconti. Un campo di sola lettura che non è possibile modificare. Questo campo viene utilizzato per calcolare l'importo finale.  | 
| **Spese di spedizione** | Scheda **Riepilogo** | Questo campo può essere modificato per inserire le spese di spedizione. Questo campo non è supportato dalla funzionalità Project Operations. Questo campo non è supportato. |
| **Totale imposte** | Scheda **Riepilogo** | L'imposta totale da tutte le righe di fattura nella fattura. Un campo di sola lettura che non è possibile modificare. | 
| **Totale importo** | Scheda **Riepilogo** | La somma dell'importo dopo sconti e imposte. La somma è l'importo che il cliente deve pagare. | 

## <a name="project-based-invoice-lines"></a>Righe di fattura basate su progetto

In Project Operations, è sempre presente una riga di fattura per ogni voce di contratto di progetto. La riga di fattura viene creata anche se non sono presenti valori effettivi. Le seguenti informazioni sono disponibili in una riga di fattura proforma.

| Campo | Posizione | Descrizione | 
| --- | --- | --- |
| **ID fattura** | Scheda **Generale** | Il riferimento all'ID fattura. Un campo di sola lettura che non è possibile modificare. Il collegamento dell'ID fattura può essere utilizzato per tornare all'intestazione della fattura. | 
| **Nome** | Scheda **Generale** | Il nome della riga di fattura impostato per impostazione predefinita dal nome della voce di contratto. Questo campo può essere modificato. |
| **Project** | Scheda **Generale** | Il progetto nella relativa voce di contratto di progetto. Un campo di sola lettura che non è possibile modificare. Il collegamento al progetto può essere utilizzato per passare al progetto. | 
| **Metodo di fatturazione** | Scheda **Generale** | Il metodo di fatturazione nella relativa voce di contratto di progetto. Un campo di sola lettura che non è possibile modificare. |
| **Importo voce di contratto** | Scheda **Generale** | L'importo di contratto nella relativa voce di contratto di progetto. Un campo di sola lettura che non è possibile modificare. | 
| **Fatturato fino alla data** | Scheda **Generale** | La somma degli importi su tutti i dettagli della riga fattura di questa fattura. Un campo di sola lettura che non è possibile modificare. | 
| **Importo** | Scheda **Generale** | La somma degli importi su tutti i dettagli della riga fattura addebitabili di questa fattura. Un campo di sola lettura che non è possibile modificare. Questo campo viene utilizzato per calcolare l'importo finale nell'intestazione fattura. | 
| **Imposte** | Scheda **Generale** | La somma degli importi delle imposte su tutti i dettagli della riga fattura di questa riga di fattura. Un campo di sola lettura che non è possibile modificare. Questo campo viene utilizzato per calcolare l'importo finale delle imposte nell'intestazione fattura. | 
| **Importo totale** | Scheda **Generale** | La somma degli importi totali (**imposte + importi**) su tutti i dettagli della riga fattura addebitabili di questa riga di fattura. Un campo di sola lettura che non è possibile modificare. Questo campo viene utilizzato per calcolare l'importo finale nell'intestazione fattura. |

## <a name="invoice-line-details"></a>Dettagli di riga fattura

Ogni riga di fattura in una fattura di progetto include i dettagli della riga di fattura. Questi dettagli di riga sono correlati ai valori effettivi di vendita non fatturati e ai passaggi fondamentali relativi alla voce di contratto a cui fa riferimento la riga fattura. Tutte queste transazioni sono contrassegnate come **Pronto per la fatturazione**.

Per un riga **Fattura tempo e materiali**, i dettagli della riga di fattura sono raggruppati in **Addebitabile**, **Non addebitabile** e **Gratuito** nella pagina **Riga fattura**. I dettagli **Riga fattura addebitabile** si sommano al totale della riga di fattura. **Gratuito** e **Valori effettivi non addebitabili** non si sommano al totale della riga di fattura.

Per un riga **Fattura a prezzo fisso**, i dettagli della riga di fattura vengono creati da passaggi fondamentali contrassegnati come **Pronto per la fatturazione** nella voce di contratto correlata. Dopo che il dettaglio della riga di fattura è stato creato da un passaggio fondamentale, lo stato di fatturazione del passaggio fondamentale viene aggiornato su **Fattura cliente creata**.

### <a name="edit-invoice-line-details"></a>Modificare i dettagli di riga fattura

I seguenti campi sono disponibili nel dettaglio della riga di fattura supportato da vendite effettive non fatturate.

| Campo | Descrizione |
| --- | --- | 
| **Riga fattura** | Il riferimento all'**ID riga fattura**. Questo campo è di sola lettura e bloccato per la modifica. Questo collegamento può essere utilizzato per tornare all'intestazione della fattura. | 
| **Descrizione** | Una descrizione del dettaglio di riga fattura. Impostato per impostazione predefinita dal campo **Commenti interni** in **Inserimento ore** e dal campo **Descrizione** in **Inserimento spese**. Il campo può essere modificato.| 
| **Descrizione esterna** | Una descrizione del dettaglio di riga fattura. Impostato per impostazione predefinita dal campo **Commenti esterni** in **Inserimento ore** e dal campo **Descrizione** in **Inserimento spese**. Il campo può essere modificato. Questa descrizione può essere utilizzata per determinare gli elementi che devono essere sulla fattura stampata che verrà inviata al cliente. In Project Operations, una fattura proforma non dispone di tutte le funzionalità necessarie per configurare le impostazioni di stampa per una fattura. | 
| **Data di inizio** | Campo di sola lettura impostato per impostazione predefinita dal valore effettivo di origine. |
| **Project** | Campo di sola lettura impostato per impostazione predefinita dal valore effettivo di origine sul progetto nella voce di contratto correlata. |  
| **Attività** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. |
| **Categoria di transazione** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | 
| **Ruolo** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. |  
| **Risorsa prenotabile** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | 
| **Società resourcing** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | 
| **Unità gestione risorse** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | 
| **Quantità** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. |  
| **Pianificazione unità** | Per il dettaglio della riga di fattura per il tempo, questa è sempre impostata sull'ora e non può essere modificata. Per le spese, questo è impostato per impostazione predefinita dalla spesa di origine effettiva. Un campo di sola lettura che non è possibile modificare. | 
| **Unità** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. |  
| **Prezzo** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. |
| **Valuta** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | 
| **Importa** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | 
| **Imposta** | Impostata per impostazione predefinita dal valore effettivo di origine. Il campo può essere modificato.| 
| **Importo totale** | Un campo calcolato, calcolato come **importo + imposte**. Un campo di sola lettura che non è possibile modificare. | 
| **Tipo di fatturazione** | Impostata per impostazione predefinita dal valore effettivo di origine. Il campo può essere modificato. La selezione di **Addebitabile** aggiunge la riga al totale della riga di fattura. **Gratuito** e **Non addebitabile** sono esclusi dal totale della riga di fattura.| 
| **Selezione prodotto** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. |
| **Prodotto** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | 
| **Nome prodotto** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. |  
| **Descrizione prodotto fuori catalogo** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. |
| **Tipo di transazione** | Campo di sola lettura impostato per impostazione predefinita dal valore effettivo di origine su **Vendite fatturate**. |  
| **Classe di transazione** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | 

I seguenti campi sono disponibili in un dettaglio della riga di fattura supportato da un passaggio fondamentale.

| Campo | Descrizione |
| --- | --- | 
| **Riga fattura** | Riferimento all'**ID riga fattura**. Un campo di sola lettura che non è possibile modificare. Il collegamento può essere utilizzato per tornare all'intestazione della fattura.  | 
| **Descrizione** | Descrizione del dettaglio di riga fattura. Impostato per impostazione predefinita dalla descrizione del passaggio fondamentale di origine. | 
|**Descrizione esterna** | Descrizione del dettaglio della riga di fattura impostato per impostazione predefinita dalla descrizione del passaggio fondamentale di origine. Questo campo può essere utilizzato per determinare gli elementi che devono essere sulla fattura stampata che verrà inviata al cliente. In Project Operations una fattura proforma non dispone di tutte le funzionalità necessarie per configurare le impostazioni di stampa per una fattura. | 
| **Data di inizio** | Impostato per impostazione predefinita dalla data del **passaggio fondamentale** del passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | 
| **Project** | Impostata per impostazione predefinita dal passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. |
| **Attività** | Impostata per impostazione predefinita dal passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | 
| **Categoria di transazione** | Un campo di sola lettura che non è possibile modificare. |
| **Ruolo** | Un campo di sola lettura che non è possibile modificare. | 
| **Risorsa prenotabile** | Un campo di sola lettura che non è possibile modificare. | 
| **Unità gestione risorse** | Un campo di sola lettura che non è possibile modificare. | 
| **Pianificazione unità** | Un campo di sola lettura che non è possibile modificare. | 
| **Unità** | Un campo di sola lettura che non è possibile modificare. | 
| **Prezzo** | Impostato per impostazione predefinita dall'importo del passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. |
| **valuta** | Impostata per impostazione predefinita dal passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. |
| **Importo** | Impostato per impostazione predefinita dall'importo del passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | 
| **Imposte** | Impostato per impostazione predefinita dall'importo delle imposte del passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. |
| **Importo totale** | Impostato per impostazione predefinita dall'importo totale del passaggio fondamentale di origine. Il campo può essere modificato. | 
| **Tipo di fatturazione** | Impostato sempre per impostazione predefinita su **Addebitabile**. Un campo di sola lettura che non è possibile modificare. |
| **Tipo di transazione** | Impostata per impostazione predefinita dal passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | 
| **Classe di transazione** | Impostata per impostazione predefinita dal passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | 

## <a name="refresh-invoice-transactions"></a>Aggiornare le transazioni fattura

Se sono presenti valori effettivi ricevuti dopo la creazione della fattura, è possibile includere questi valori effettivi nella fattura.

1. Nella **Visualizzazione backlog di fatturazione**, contrassegna i dati come **Pronto per la fatturazione**.   
2. Apri la bozza della fattura proforma e nella barra multifunzione **Azioni**, seleziona **Aggiorna transazioni di riga fattura**.

  I dettagli della riga di fattura vengono creati per qualsiasi valore effettivo datato nel passato e contrassegnato come **Pronto per la fatturazione**, ma non è incluso nella fattura.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
