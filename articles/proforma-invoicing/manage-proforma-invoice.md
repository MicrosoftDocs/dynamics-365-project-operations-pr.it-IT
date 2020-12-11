---
title: Gestire una fattura proforma
description: Questo argomento fornisce informazioni su come gestire e utilizzare le fatture proforma.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f3aab57f159dbb522ebe5d24dc3693034f6f81f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181457"
---
# <a name="manage-a-proforma-invoice"></a>Gestire una fattura proforma

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

In Dynamics 365 Project Operations, le fatture proforma vengono create come estensione delle fatture in Dynamics 365 Sales. Tuttavia, ci sono molte differenze nel processo di fatturazione tra Sales e Project Operations quando si tratta di fatturazione. Ad esempio, non è possibile creare una nuova fattura dalla pagina **Elenco fatture** in Project Operations, ma è possibile farlo in Sales. Queste differenze ed estensioni sono in atto per supportare i processi di fatturazione per progetti diversi da una tipica fattura per un ordine di vendita.

> [!IMPORTANT]
> A causa delle differenze, non utilizzare le fatture in Sales e Project Operations in modo intercambiabile.

## <a name="invoice-header"></a>Intestazione della fattura

Le seguenti informazioni sono disponibili nell'intestazione di una fattura proforma in Project Operations.

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| **ID fattura** | Scheda **Riepilogo** | L'ID che viene generato automaticamente quando una fattura proforma viene creata. Un campo di sola lettura che non è possibile modificare. | Questo campo viene utilizzato come riferimento per ogni fattura proforma. |
| **Nome** | Scheda **Riepilogo** | Imposta il nome del contratto di progetto predefinito. Questo campo può essere modificato dall'utente. | &nbsp;  |
| **valuta** | Scheda **Riepilogo** | Imposta la valuta del contratto di progetto predefinito. Un campo di sola lettura che non è possibile modificare. |&nbsp; |
| **Listino prezzi** | Scheda **Riepilogo** | Imposta il listino prezzi del contratto di progetto predefinito. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Opportunità** | Scheda **Riepilogo** | Il riferimento all'opportunità collegata. Un campo di sola lettura che non è possibile modificare. | &nbsp;  |
| **Contratto** | Scheda **Riepilogo** | Il riferimento al contratto di progetto collegato. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Cliente** | Scheda **Riepilogo** | Il riferimento al contratto di progetto collegato. Un campo di sola lettura che non è possibile modificare. |&nbsp;  |
| **Descrizione** | Scheda **Riepilogo** | Il campo di testo che descrive la fattura. Questo campo può essere modificato dall'utente. | &nbsp; |
| **Fatturazione** e campi correlati | **Scheda Riepilogo** | I valori predefiniti vengono impostati dal cliente del contratto di progetto. Questo campo può essere modificato dall'utente.  | &nbsp; |
| **Stato** | Scheda **Riepilogo** | Imposta le seguenti opzioni: **Attivo**, **Chiuso**, **Pagato** e **Annullato** che possono essere modificate dall'utente. | Gli stati non supportati per Project Operations sono **Chiuso** e **Annullato**. </br> Lo stato è impostato su **Attivo** quando viene creata la fattura. </br>Lo stato deve essere impostato su **Pagato** solo dopo la conferma della fattura. |
| **Stato fattura di progetto** | Scheda **Riepilogo** | Imposta le seguenti opzioni: **Bozza**, **In revisione** e **Confermato** che possono essere modificate dall'utente. | In entrambi gli stati **Bozza** e **In revisione**, la fattura può essere modificata. La fattura non può essere modificata dopo la conferma. |
| **Totale dettagli** | Scheda **Riepilogo** | La somma degli importi su tutte le righe della fattura dopo anticipi e detrazioni. Un campo di sola lettura che non è possibile modificare. | Questo campo viene utilizzato per calcolare l'importo finale. |
| **Sconto (%)** | Scheda **Riepilogo** | Questo campo può essere modificato per inserire una percentuale di sconto. Questo campo non è supportato dalla funzionalità Project Operations. | Questo campo non è supportato. |
| **Importo sconto** | Scheda **Riepilogo** | Questo campo può essere modificato per inserire un importo di sconto. Questo campo non è supportato dalla funzionalità Project Operations. | Questo campo non è supportato. |
| **Totale senza spedizione** | **Scheda Riepilogo** | L'importo totale della fattura dopo l'applicazione degli sconti. Un campo di sola lettura che non è possibile modificare. | Questo campo viene utilizzato per calcolare l'importo finale. |
| **Spese di spedizione** | Scheda **Riepilogo** | Questo campo può essere modificato per inserire le spese di spedizione. Questo campo non è supportato dalla funzionalità Project Operations. | Questo campo non è supportato. |
| **Totale imposte** | Scheda **Riepilogo** | L'imposta totale da tutte le righe di fattura nella fattura. Un campo di sola lettura che non è possibile modificare. | Nessuna. |
| **Totale offerta/ordine/fattura** | Scheda **Riepilogo** | La somma dell'importo dopo sconti e imposte. | La somma è l'importo che il cliente deve pagare. |

## <a name="project-based-invoice-lines"></a>Righe di fattura basate su progetto

In Project Operations, è sempre presente una riga di fattura per ogni voce di contratto di progetto. La riga di fattura viene creata anche se non sono presenti valori effettivi. Le seguenti informazioni sono disponibili in una riga di fattura proforma.

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| **ID fattura** | Scheda **Generale** | Il riferimento all'ID fattura. Un campo di sola lettura che non è possibile modificare. | Il collegamento dell'ID fattura può essere utilizzato per tornare all'intestazione della fattura. |
| **Nome** | Scheda **Generale** | Il nome della riga di fattura impostato per impostazione predefinita dal nome della voce di contratto. Questo campo può essere modificato dall'utente. | &nbsp; |
| **Project** | Scheda **Generale** | Il progetto nella relativa voce di contratto di progetto. Un campo di sola lettura che non è possibile modificare. | Il collegamento al progetto può essere utilizzato per passare al progetto. |
| **Metodo di fatturazione** | Scheda **Generale** | Il metodo di fatturazione nella relativa voce di contratto di progetto. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Importo voce di contratto** | Scheda **Generale** | L'importo di contratto nella relativa voce di contratto di progetto. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Fatturato fino alla data** | Scheda **Generale** | La somma degli importi su tutti i dettagli della riga fattura di questa fattura. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Importo** | Scheda **Generale** | La somma degli importi su tutti i dettagli della riga fattura addebitabili di questa fattura. Un campo di sola lettura che non è possibile modificare. | Questo campo viene utilizzato per calcolare l'importo finale nell'intestazione fattura. |
| **Imposte** | Scheda **Generale** | La somma degli importi delle imposte su tutti i dettagli della riga fattura di questa riga di fattura. Un campo di sola lettura che non è possibile modificare. | Questo campo viene utilizzato per calcolare l'importo finale delle imposte nell'intestazione fattura. |
| **Importo totale** | Scheda **Generale** | La somma degli importi totali (**imposte + importi**) su tutti i dettagli della riga fattura addebitabili di questa riga di fattura. Un campo di sola lettura che non è possibile modificare. | Questo campo viene utilizzato per calcolare l'importo finale nell'intestazione fattura. |

## <a name="invoice-line-details"></a>Dettagli di riga fattura

Ogni riga di fattura in una fattura di progetto include i dettagli della riga di fattura. Questi dettagli di riga sono correlati ai valori effettivi di vendita non fatturati e ai passaggi fondamentali relativi alla voce di contratto a cui fa riferimento la riga fattura. Tutte queste transazioni sono contrassegnate come **Pronto per la fatturazione**.

Per la riga **Fattura tempo e materiale**, i dettagli della riga di fattura sono raggruppati in **Addebitabile**, **Non addebitabile** e **Gratuito** della pagina **Riga di fattura**. I dettagli **Riga fattura addebitabile** si sommano al totale della riga di fattura. **Gratuito** e **Valori effettivi non addebitabili** non si sommano al totale della riga di fattura.

Per la riga **Fattura a prezzo fisso**, i dettagli della riga fattura vengono creati dai passaggi fondamentali contrassegnati come **Pronto per la fatturazione** nella relativa voce di contratto. Dopo che il dettaglio della riga di fattura è stato creato da un passaggio fondamentale, lo stato di fatturazione del passaggio fondamentale viene aggiornato su **Fattura cliente creata**.

### <a name="edit-invoice-line-details"></a>Modificare i dettagli di riga fattura

I seguenti campi sono disponibili nel dettaglio della riga di fattura supportato da vendite effettive non fatturate.

| Campo | Descrizione | Impatto downstream |
| --- | --- | --- |
| **Riga fattura** | Il riferimento all'**ID riga fattura**. Campo di sola lettura che non è possibile modificare. | Questo collegamento può essere utilizzato per tornare all'intestazione della fattura. |
| **Descrizione** | Una descrizione del dettaglio di riga fattura. Impostato per impostazione predefinita dal campo **Commenti interni** in **Inserimento ore** e dal campo **Descrizione** in **Inserimento spese**. Il campo può essere modificato dall'utente.| &nbsp; |
| **Descrizione esterna** | Una descrizione del dettaglio di riga fattura. Impostato per impostazione predefinita dal campo **Commenti esterni** in **Inserimento ore** e dal campo **Descrizione** in **Inserimento spese**. Il campo può essere modificato dall'utente. | Questa descrizione può essere utilizzata per determinare gli elementi che devono essere sulla fattura stampata che verrà inviata al cliente. In Project Operations, una fattura proforma non dispone di tutte le funzionalità necessarie per configurare le impostazioni di stampa per una fattura. |
| **Data di inizio** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Questo campo può essere modificato in un nuovo dettaglio della riga di fattura che non è supportato da un valore effettivo di origine. |
| **Project** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Impostato per impostazione predefinita sul progetto nella relativa voce di contratto. |
| **Attività** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Il campo può essere modificato in un nuovo dettaglio della riga di fattura che non è supportato da un valore effettivo di origine. Un elenco a discesa mostra tutte le attività associate alla voce di contratto di progetto correlata.  |
| **Categoria di transazione** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Il campo può essere modificato in un nuovo dettaglio della riga di fattura che non è supportato da un valore effettivo di origine. |
| **Ruolo** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Il campo può essere modificato in un nuovo dettaglio della riga di fattura che non è supportato da un valore effettivo di origine. |
| **Risorsa prenotabile** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Il campo può essere modificato in un nuovo dettaglio della riga di fattura che non è supportato da un valore effettivo di origine. |
| **Società resourcing** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Il campo può essere modificato in un nuovo dettaglio della riga di fattura che non è supportato da un valore effettivo di origine. |
| **Unità gestione risorse** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Il campo può essere modificato in un nuovo dettaglio della riga di fattura che non è supportato da un valore effettivo di origine. |
| **Quantità** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Il campo può essere modificato in un nuovo dettaglio della riga di fattura che non è supportato da un valore effettivo di origine. |
| **Pianificazione unità** | Per i dettagli della riga di fattura per l'ora, questa è sempre impostata sull'ora e non può essere modificata. Per le spese, questo è impostato per impostazione predefinita dalla spesa di origine effettiva. Un campo di sola lettura che non è possibile modificare. | Impostato per impostazione predefinita su **Ore** in un nuovo dettaglio della riga di fattura che non è supportato da un valore effettivo. |
| **Unità** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Il campo può essere modificato in un nuovo dettaglio della riga di fattura che non è supportato da un valore effettivo di origine |
| **Prezzo** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Il campo può essere modificato in un nuovo dettaglio della riga di fattura che non è supportato da un valore effettivo di origine. Se non viene inserito alcun valore, viene impostato per impostazione predefinita dopo **Salva**. |
| **valuta** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Impostato per impostazione predefinita dall'intestazione della fattura quando si crea un nuovo dettaglio della fattura senza supporto di valore effettivo.  Un campo di sola lettura che non è possibile modificare. |
| **Importo** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Calcolato come **Quantità \* Prezzo** quando si crea un nuovo dettaglio della fattura senza un valore effettivo di supporto. Viene calcolato dopo **Salva**. Un campo di sola lettura che non è possibile modificare. |
| **Imposte** | Impostata per impostazione predefinita dal valore effettivo di origine. Il campo può essere modificato dall'utente | Il campo può essere modificato dall'utente durante la creazione di un nuovo dettaglio della riga di fattura senza un valore effettivo di supporto. |
| **Importo totale** | Un campo calcolato, calcolato come **importo + imposte**. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Tipo di fatturazione** | Impostata per impostazione predefinita dal valore effettivo di origine. Il campo può essere modificato dall'utente. | La selezione di **Addebitabile** aggiunge la riga al totale della riga di fattura. **Gratuito** e **Non addebitabile** sono esclusi dal totale della riga di fattura. |
| **Tipo di transazione** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Impostato per impostazione predefinita su **Vendite fatturate** e bloccato durante la creazione di un nuovo **dettaglio riga fattura** senza valore effettivo di supporto.  |
| **Classe di transazione** | Impostata per impostazione predefinita dal valore effettivo di origine. Un campo di sola lettura che non è possibile modificare. | Impostato per impostazione predefinita in base alla scelta dell'utente di creare un dettaglio di riga fattura **Ore**, **Spese** o **Commissione** mentre viene creato anche un nuovo **Dettaglio riga fattura** senza un valore effettivo di supporto. Bloccato per la modifica. |

I seguenti campi sono disponibili in un dettaglio della riga di fattura supportato da un passaggio fondamentale:

| Campo | Descrizione | Impatto downstream |
| --- | --- | --- |
| **Riga fattura** | Riferimento all'**ID riga fattura**. Un campo di sola lettura che non è possibile modificare. | Il collegamento può essere utilizzato per tornare all'intestazione della fattura. |
| **Descrizione** | Descrizione del dettaglio di riga fattura. Impostato per impostazione predefinita dalla descrizione del passaggio fondamentale di origine. | &nbsp; |
|**Descrizione esterna** | Descrizione del dettaglio della riga di fattura impostato per impostazione predefinita dalla descrizione del passaggio fondamentale di origine. | Questo campo può essere utilizzato per determinare gli elementi che devono essere sulla fattura stampata che verrà inviata al cliente. In Project Operations una fattura proforma non dispone di tutte le funzionalità necessarie per configurare le impostazioni di stampa per una fattura. |
| **Data di inizio** | Impostato per impostazione predefinita dalla data del **passaggio fondamentale** del passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Project** | Impostata per impostazione predefinita dal passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Attività** | Impostata per impostazione predefinita dal passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Categoria di transazione** | Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Ruolo** | Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Risorsa prenotabile** | Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Unità gestione risorse** | Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Pianificazione unità** | Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Unità** | Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Prezzo** | Impostato per impostazione predefinita dall'importo del passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **valuta** | Impostata per impostazione predefinita dal passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. |&nbsp; |
| **Importo** | Impostato per impostazione predefinita dall'importo del passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Imposte** | Impostato per impostazione predefinita dall'importo delle imposte del passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Importo totale** | Impostato per impostazione predefinita dall'importo totale del passaggio fondamentale di origine. Il campo può essere modificato dall'utente | &nbsp; |
| **Tipo di fatturazione** | Impostato sempre per impostazione predefinita su **Addebitabile**. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Tipo di transazione** | Impostata per impostazione predefinita dal passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | &nbsp; |
| **Classe di transazione** | Impostata per impostazione predefinita dal passaggio fondamentale di origine. Un campo di sola lettura che non è possibile modificare. | &nbsp; |

## <a name="refresh-invoice-transactions"></a>Aggiornare le transazioni fattura

Se sono presenti valori effettivi ricevuti dopo la creazione della fattura, è possibile includere questi valori effettivi nella fattura.

1. Nella **Visualizzazione backlog di fatturazione**, contrassegna i dati come **Pronto per la fatturazione**.   
2. Apri la bozza di fattura proforma e, sulla barra multifunzione **Azioni**, fai clic su **Aggiorna transazioni riga fattura**.

  In questo modo vengono creati i dettagli della riga di fattura per qualsiasi valore effettivo che è datato e contrassegnato come **Pronto per la fatturazione** ma non è incluso nella fattura.