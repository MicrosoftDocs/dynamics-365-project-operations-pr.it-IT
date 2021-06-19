---
title: Impostazioni dell'offerta di progetto
description: Questo argomento fornisce informazioni sulle informazioni e le impostazioni che si applicano e influiscono sulle offerte di progetto.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9181fc1f6a4820662cb145abab55072e9743bbaa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011331"
---
# <a name="header-details-for-project-based-quotes"></a>Dettagli dell'intestazione per offerte basate su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_


Questo articolo spiega le informazioni che si applicano a un'offerta di progetto. Queste includono le impostazioni che influiscono su tutte le righe dell'offerta e le informazioni sull'offerta che vengono riepilogate in tutte le voci per guidare i KPI dell'offerta di progetto.

La tabella seguente elenca i campi con le informazioni di riepilogo di una offerta di progetto che sono univoci per Dynamics 365 Project Operations o hanno alcune importanti modifiche nel comportamento rispetto alle offerte in Dynamics 365 Sales.

| **Campo** | **Luogo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- | --- |
| Digita | Scheda Riepilogo (nascosta) | Questo campo di set di opzioni include le seguenti opzioni:</br>- Basato su lavoro (disponibile solo quando è installato Project Operations)</br>- Basato su articolo (disponibile solo quando sono installati Project Operations e Sales)</br>- Basato su manutenzione di servizio (disponibile quando è installato Dynamics 365 Field Service) | Quando si utilizza l'applicazione Project Operations, il valore di questo campo viene impostato automaticamente su **Basato su lavoro**. Questo classifica l'offerta come offerta basata su progetto. Un'offerta dovrebbe essere basata su progetto per abilitare tutte le estensioni e funzionalità specifiche del progetto. |
| Società proprietaria | Riepilogo | La persona giuridica che dovrà rendere conto dei costi e dei ricavi derivanti da questo progetto o progetti associati a questa offerta. Quando un'offerta viene creata da un'opportunità, questo campo viene copiato dal campo corrispondente dell'opportunità. | La società proprietaria corrisponde al concetto di persona giuridica nel modulo **Gestione progetti e contabilità** di Project Operations. Tutti i costi e i ricavi derivati da questo progetto verranno contabilizzati nella contabilità generale della società proprietaria. |
| Potenziale cliente | Scheda Riepilog | Riferimento alla società o al record di account del cliente. Un cliente valido a cui fare riferimento nell'offerta di progetto deve essere impostato come cliente nella società proprietaria dell'offerta. La società proprietaria mostra l'elenco di persone giuridiche che sono configurate nel modulo **Gestione progetti e contabilità** di Project Operations. Quando un'offerta viene creata da un'opportunità, questo campo viene copiato dal campo corrispondente dell'opportunità. | La valuta dell'offerta di progetto viene impostata in modo predefinito in base alla valuta del cliente. Tuttavia, questa impostazione può essere modificata prima di salvare l'offerta. |
| Gestione account | Scheda Riepilog | Il nome del responsabile della gestione account per questa transazione. Quando un'offerta viene creata da un'opportunità, questo campo viene copiato dal campo corrispondente dell'opportunità. | Il responsabile della gestione account è responsabile della gestione del rapporto con il cliente fino al completamento di questo progetto. In base al record della risorsa prenotabile collegato al responsabile della gestione account, l'unità contratto è predefinita nell'offerta di progetto.|
| Unità contratto | Scheda Riepilog | L'unità organizzativa responsabile della consegna del progetto o dei progetti associati a questa offerta. Quando un'offerta viene creata da un'opportunità, questo campo viene copiato dal campo corrispondente dell'opportunità. | L'unità contratto è la divisione dell'azienda che eseguirà i progetti dopo la chiusura della trattativa. Ogni unità contratto ha una valuta e questa valuta viene utilizzata per riportare i costi stimati ed effettivi sostenuti durante l'esecuzione del progetto. |
| Listino prezzi prodotto | Scheda Riepilog | Questo è il listino prezzi utilizzato per i prezzi predefiniti nelle righe dell'offerta basata su prodotto. L'elenco delle opzioni per questo campo mostra un elenco di listini prezzi in cui la valuta del listino prezzi corrisponde alla valuta dell'offerta. Quando un'offerta viene creata da un'opportunità, questo campo viene copiato dal campo corrispondente dell'opportunità. Questo campo dell'opportunità è predefinito in base al record di account ma può essere modificato. | Quando l'offerta viene acquisita, il valore del campo viene copiato nel contratto di progetto che viene creato. |
| Valuta | Scheda Riepilog | Indica la valuta che verrà utilizzata per riportare il valore di questa transazione. Questa è anche la valuta in cui verrà emessa la fattura al cliente se la trattativa viene acquisita. Quando un'offerta viene creata da un'opportunità, questo campo viene copiato dal campo corrispondente dell'opportunità. Questo campo dell'opportunità è predefinito in base al record di account ma può essere modificato dall'utente.  | Dopo aver salvato un'offerta, questo campo non è più modificabile. Viene utilizzato per impostare in modo predefinito i listini prezzi dei prodotti e dei progetti nell'offerta. La valuta dell'offerta viene utilizzata per corrispondere alla valuta del listino prezzi. |
| Limite da non superare | Scheda Riepilog | Questo indica il limite massimo negoziato per il valore finale che il cliente accetta per questa transazione. | Questo limite massimo viene valutato durante l'esecuzione ed è applicabile a tutte le voci e i progetti associati a questa transazione. |
| Data consegna richiesta | Scheda Riepilog | Quando un'offerta viene creata da un'opportunità, questo campo viene copiato dal campo corrispondente dell'opportunità. | Questa data viene utilizzata come data di fine per la generazione di pianificazioni di fatturazione. |

Di seguito sono riportate le schede e gli indicatori KPI disponibili in un'offerta di progetto che sono univoci per Project Operations o presentano alcune importanti modifiche nel comportamento rispetto alle offerte di Sales:

| **Campo** | **Luogo** | **Descrizione** |
| --- | --- | --- |
| Analisi della redditività | Scheda sull'offerta | La scheda mostra le metriche seguenti:</br>- Costo addebitabile totale</br></br>- Costo non addebitabile totale</br>- Ricavi totali</br>- Ricavi totali (base)</br>- Margine lordo</br>- Margine lordo rettificato|
| Confronto con aspettative cliente | Scheda sull'offerta | Questa scheda mostra le metriche seguenti:</br>- Completamento stimato</br>- Completamento richiesto</br>- Budget cliente</br>- Valore offerto |
| Analisi offerta | Scheda sull'offerta | Questa scheda riepiloga i seguenti KPI principali per un'offerta di progetto</br>- Confronto con le aspettative dei clienti per budget e pianificazione</br>- Margine lordo</br>- Margine lordo rettificato |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
