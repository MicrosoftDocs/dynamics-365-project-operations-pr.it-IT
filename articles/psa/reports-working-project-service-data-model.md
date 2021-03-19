---
title: Utilizzo del modello di dati di Project Service Automation
description: In questo argomento vengono fornite informazioni su come utilizzare il modello di dati.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25f1af15c03001a92f96689ff36a3159a5352a46
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283238"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Utilizzo del modello di dati di Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation estende le entità di altre app e introduce le proprie entità nel modello di dati di Common Data Service. In questo argomento vengono descritte alcune delle entità utilizzate in scenari di creazione di report PSA tipici.

## <a name="reporting-on-opportunities"></a>Creazione di report sulle opportunità

Project Service Automation estende l'entità **Opportunità** di Dynamics 365 Sales tramite l'aggiunta di campi che abilitano scenari basati su progetto. Questi campi sono identificati da un nome di schema con il prefisso **msdyn\_**. Un nuovo campo che è importante per la creazione di report sulle opportunità di PSA è **Tipo di ordine**. Se il valore di questo campo è **Basato su lavoro** indica che l'opportunità rappresenta un'opportunità PSA. Altri campi che sono stati aggiunti all'entità includono **Organizzazione di contratto**, che acquisisce l'organizzazione che ha l'opportunità e **Gestione account**, che acquisisce il nome del responsabile della gestione account responsabile dell'opportunità.

Anche l'entità **Riga opportunità** include campi correlati a Project Service. **Metodo di fatturazione** indica se la riga opportunità deve essere fatturata su una base tempistica e materiali o su una base a prezzo fisso e **Progetto** acquisisce il nome del progetto che supporta l'opportunità. Altri campi che è possibile utilizzare per i report acquisiscono i costi e gli importi di budget del cliente per la voce.

## <a name="reporting-on-quotes"></a>Creazione di report sulle offerte

PSA estende l'entità **Offerta** di Sales aggiungendo di campi correlati al progetto. **Tipo di ordine** distingue le offerte PSA dalle offerte non PSA. Se il valore di questo campo è **Basato su lavoro** indica che l'offerta rappresenta un'offerta PSA. Altri campi che possono essere significativi per la creazione di report sulle offerte PSA includono i campi di importo, ad esempio **Costo addebitabile**, **Costo non addebitabile**, **Margine lordo**, **Stime** e **Costi preventivati**. Altri campi utili indicano se l'offerta è proficua, se verrà completata come pianificato e se soddisfa le aspettative di budget del cliente.

PSA estende inoltre l'entità **Riga di offerta** di Sales. Un campo aggiunto da PSA è **Metodo di fatturazione**, che indica come la riga di offerta sarà fatturata (tempistica e materiali o prezzo fisso). Altri campi che sono stati aggiunti a un'entità acquisiscono il progetto correlato che supporta riga di offerta, fatturazione, costo e budget.

PSA aggiunge inoltre nuove entità correlate all'offerta al modello di dati di Dynamics 365. Di seguito sono riportati alcuni esempi.

- **Dettagli riga di offerta** - Questa entità contiene dettagli di stima del progetto della riga di offerta. Include due record per ogni riga di offerta. Un record memorizza il costo e i relativi dettagli della riga di offerta e l'altro record memorizza i dettagli sulle vendite e l'importo delle vendite della riga di offerta.
- **Pianificazione fatturazione riga di offerta** - Questa entità contiene la pianificazione della fatturazione per la riga di offerta. Questa pianificazione viene generata in base alla frequenza di fatturazione assegnata alla riga di offerta.
- **Passaggio fondamentale riga di offerta** - Questa entità contiene i passaggi fondamentali della fatturazione per le righe di offerta a prezzo fisso.
- **Suddivisione analisi riga di offerta** - Questa entità contiene i dettagli finanziari della riga di offerta. Questi dettagli possono essere utili per la creazione di report sugli importi delle vendite offerta e dei costi stimati in base a varie dimensioni.

Altre entità aggiunte da PSA per le offerte sono **Listino prezzi di progetto riga di offerta**, **Categoria di risorsa riga di offerta** e **Categoria di transazione riga di offerta**.

![Diagramma che mostra l'offerta, la riga di offerta e le relazioni del progetto](media/PS-Reporting-image2.png "Diagramma che mostra l'offerta, la riga di offerta e le relazioni del progetto")

## <a name="reporting-on-project-contracts"></a>Creazione di report su contratti di progetto

PSA estende l'entità **Ordine** di Sales utilizzata quando i contratti di progetto vengono registrati. Aggiunge un nuovo campo importante, **Tipo di ordine**, che identifica il contratto come contratto di progetto PSA anziché come ordine di vendita. Se il valore di questo campo è **Basato su lavoro** indica che l'ordine rappresenta un contratto di progetto PSA. Altri nuovi campi aggiunti all'entità **Ordine** acquisiscono dettagli su costi, stato del contratto PSA e organizzazione proprietaria del contratto.

PSA estende inoltre l'entità **Righe ordine di vendita**. Tra i campi che aggiunge vi sono i campi che acquisiscono il metodo di fatturazione (tempistica e materiali o prezzo fisso), gli importi di budget del cliente e il progetto sottostante.

PSA aggiunge inoltre nuove entità progettate per i contratti di progetto. Di seguito sono riportati alcuni esempi.

- **Dettagli di voce di contratto di progetto** - Questa entità contiene i dettagli a livello di riga di cui viene eseguito il rollup all'importo della voce di contratto. Questi dati possono essere dettagliati quanto le voci generate da una pianificazione di progetto a livello di attività.
- **Pianificazione fatturazione voce di contratto di progetto** - Questa entità contiene la pianificazione della fatturazione che viene generata in base alla frequenza di fatturazione assegnata alla voce di contratto.
- **Passaggi fondamentali contratto di progetto** - Questa entità contiene i passaggi fondamentali di fatturazione per le voci di contratto che hanno un periodo di fatturazione a prezzo fisso.

Altre entità aggiunte da PSA per i contratti sono **Listino prezzi di progetto voce di contratto di progetto**, **Categoria di risorsa voce di contratto di progetto** e **Categoria di transazione voce di contratto di progetto**.

![Diagramma che mostra l'ordine, la riga dell'ordine e le relazioni del progetto](media/PS-Reporting-image3.png "Diagramma che mostra l'ordine, la riga dell'ordine e le relazioni del progetto")

## <a name="reporting-on-projects"></a>Creazione di report su progetti

L'entità **Progetti** e le relative entità correlate sono esclusive di PSA. **Progetto** è l'entità di primo livello utilizzata per acquisire il lato lavoro e costo delle operazioni. Di seguito è riportato un elenco delle entità correlate:

- **Membro del team di progetto** - Questa entità contiene dettagli sulle risorse prenotabili che assegnate al progetto. Tali risorse possono essere risorse prenotabili generiche, oppure risorse prenotabili generiche immesse dal responsabile del progetto o generate dalla pianificazione del progetto.
- **Attività di progetto** - Questa entità contiene le attività che costituiscono il piano o la pianificazione del progetto.
- **Assegnazione risorse** - Questa entità contiene l'assegnazione di attività per la risorsa prenotabile.
- **Requisito di risorsa** - Questa entità contiene i requisiti di tutti i membri del team di risorse generiche.
- **Stima** e **Riga di stima** - Queste entità hanno una relazione intestazione/riga e contengono stime di spesa per il progetto. Le stime di attività si trovano nell'entità **Stima basata su risorsa**.

![Diagramma che mostra il requisito risorsa e le relazioni del progetto](media/PS-Reporting-image4.png "Diagramma che mostra il requisito risorsa e le relazioni del progetto")

## <a name="reporting-on-resources"></a>Creazione di report su risorse

Le risorse di progetto utilizzano le entità **Risorsa prenotabile** di Universal Resource Scheduling (URS ) condivise con altre app come Microsoft Dynamics 365 Field Service. Di seguito viene fornito un elenco delle entità che potresti utilizzare quando si creano report sulle risorse di progetto:

- **Risorsa prenotabile** - Questa entità rappresenta l'utente, il contatto, la risorsa generica, l'account, il gruppo o le attrezzature utilizzati dal team di progetto.
- **Caratteristiche di risorse prenotabili** - Questa entità include competenze, certificazioni o livello di istruzione della risorsa. Le caratteristiche possono avere valori di classificazione definiti dal modello di classificazione.
- **Categoria di risorsa prenotabile** - Questa entità rappresenta il ruolo della risorsa prenotabile.
- **Prenotazioni risorse prenotabili** - Questa entità rappresenta il tempo prenotato nei progetti per la risorsa. Ogni prenotazione include un'entità intestazione e entità riga e ogni riga ha uno stato che rappresenta lo stato della prenotazione.

![Diagramma che mostra le relazioni delle caratteristiche delle risorse prenotabili](media/PS-Reporting-image5.png "Diagramma che mostra le relazioni delle caratteristiche delle risorse prenotabili")

## <a name="reporting-on-actual-transactions"></a>Creazione di report su transazioni effettive

Quando approvi una scheda orario o una spesa oppure fatturi un contratto in PSA, la transazione commerciale viene acquisita nell'entità **Valore effettivo**. Questa entità può essere utilizzata come base per quasi tutti i report di tipo finanziario in PSA. L'entità **Valore effettivo** acquisisce le transazioni di costo e vendita per l'evento commerciale. Acquisisce inoltre molti attributi pertinenti.

Quando utilizzi l'entità **Valore effettivo**, è importante comprendere quali transazioni vengono memorizzate nell'entità e quando le transazioni vengono registrate. Di seguito è riportato il flusso tipico quando si utilizzano inserimenti ore (il flusso delle voci di spesa è simile):

1. Quando l'inserimento ore viene salvato, nessun record viene creato nell'entità **Valore effettivo**.
2. Quando l'inserimento ore viene inviato, nessun record viene creato nell'entità **Valore effettivo**.
3. Quando l'inserimento ore viene approvato, viene creato un record nell'entità **Valore effettivo** ed è possibile che venga creato anche un secondo record. Il primo record memorizza il costo dell'inserimento ore. Il secondo record memorizza l'importo delle vendite non fatturate dell'inserimento ore. Il secondo record dipende dal progetto a cui è assegnato un cliente, un'offerta o una voce di contratto.

    | Data documento | Tipo di transazione | Classe di transazione | Cliente         | Contratto   | Risorsa     | Ruolo risorsa | Tipo di fatturazione | Quantità | Prezzo unitario | Importo |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 3/2/18        | Costo             | Time              | Chalet alpino | CRM alpino | Lucia Cattaneo | Resp. di progetto   | Addebitabile   | 8.0      | 50.00      | 400.00 |
    | 3/2/18        | Vendite non fatturate   | Time              | Chalet alpino | CRM alpino | Lucia Cattaneo | Resp. di progetto   | Addebitabile   | 8.0      | 100.00     | 800.00 |

    Questi due record sono distinti ma correlati. Non sono né debiti né crediti.

4. Se un contratto è associato al progetto, quando si fattura l'inserimento ore, vengono creati due nuovi record nell'entità **Valore effettivo**. Innanzitutto, viene creato un importo negativo per il record delle vendite non fatturate. Questo record in pratica storna la vendita non fatturata. Quindi viene creata una transazione per la vendita fatturata. Anche in questo caso i record sono distinti ma correlati e non sono né debiti né crediti.

    | Data documento | Tipo di transazione | Classe di transazione | Cliente         | Contratto   | Risorsa     | Ruolo risorsa | Tipo di fatturazione | Quantità | Prezzo unitario | Importo   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 4/2/18        | Vendite non fatturate   | Time              | Chalet alpino | CRM alpino | Lucia Cattaneo | Resp. di progetto   | Addebitabile   | - 8,0    | 100.00     | - 800,00 |
    | 4/2/18        | Vendite fatturate     | Time              | Chalet alpino | CRM alpino | Lucia Cattaneo | Resp. di progetto   | Addebitabile   | 8.0      | 100.00     | 800.00   |

L'entità **Origine transazione** registra l'origine del record **Valore effettivo** e l'entità entità **Connessione della transazione** registra i record correlati per il record **Valore effettivo**. Inoltre, il record **Valore effettivo** contiene riferimenti al progetto, il contratto di progetto (ordine), la risorsa prenotabile e il cliente.

![Diagramma che mostra la connessione della transazione, l'origine e le relazioni effettive](media/PS-Reporting-image6.png "Diagramma che mostra la connessione della transazione, l'origine e le relazioni effettive")


[!INCLUDE[footer-include](../includes/footer-banner.md)]