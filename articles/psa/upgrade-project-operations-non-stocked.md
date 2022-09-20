---
title: Aggiornamento da Project Service Automation a Project Operations
description: Questo articolo fornisce una panoramica del processo di aggiornamento da Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 43ea29aeafb62f3ecd69b316f2c0a5b791707da5
ms.sourcegitcommit: bc21fbe8547534d2644269f873eb05d509840f23
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446040"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Aggiornamento da Project Service Automation a Project Operations

Siamo lieti di annunciare la prima delle tre fasi per l'aggiornamento da Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations. Questo articolo fornisce una panoramica per i clienti che stanno intraprendendo questo entusiasmante percorso. Gli articoli successivi includeranno considerazioni per gli sviluppatori e dettagli sui miglioramenti delle funzionalità. Non solo forniranno indicazioni per aiutarti a preparare l'aggiornamento a Project Operations, ma illustreranno anche cosa puoi aspettarti dopo l'aggiornamento.

Il programma di consegna dell'aggiornamento sarà suddiviso in tre fasi.

| Consegna dell'aggiornamento | Fase 1 (gennaio 2022) | Fase 2 (novembre 2022) | Fase 3 (ciclo di aprile 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nessuna dipendenza dalla struttura di suddivisione del lavoro (WBS) per i progetti | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| La struttura di suddivisione del lavoro entro i limiti attualmente supportati di Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| La struttura di suddivisione del lavoro al di fuori dei limiti attualmente supportati di Project Operations, incluso il supporto per Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funzionalità del processo di aggiornamento 

Come parte del processo di aggiornamento, abbiamo aggiunto i registri di aggiornamento alla mappa del sito, in modo che gli amministratori possano diagnosticare più facilmente gli errori. Oltre alla nuova interfaccia, verranno aggiunte nuove regole di convalida per garantire l'integrità dei dati dopo un aggiornamento. Le seguenti convalide verranno aggiunte al processo di aggiornamento.

| Convalide | Fase 1 (gennaio 2022) | Fase 2 (novembre 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| La struttura di suddivisione del lavoro verrà convalidata rispetto alle comuni violazioni dell'integrità dei dati (ad esempio, assegnazioni di risorse associate alla stessa attività padre ma con progetti padre diversi). | | :heavy_check_mark: | :heavy_check_mark: |
| La struttura di suddivisione del lavoro sarà convalidata rispetto ai [limiti noti di Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| La struttura di suddivisione del lavoro sarà convalidata rispetto ai limiti noti di Project Desktop Client. | |  | :heavy_check_mark: |
| Le risorse prenotabili e i calendari di progetto verranno valutati rispetto alle eccezioni comuni alle regole di calendario incompatibili. | | :heavy_check_mark: | :heavy_check_mark: |

Nella fase 2, i clienti che eseguono l'aggiornamento a Project Operations avranno i loro progetti esistenti aggiornati a un'esperienza di sola lettura per la pianificazione del progetto. In questa esperienza di sola lettura, la struttura di suddivisione del lavoro completa sarà visibile nella griglia di monitoraggio. Per modificare la struttura di suddivisione del lavoro, i responsabili di progetto possono selezionare **Converti** nella pagina principale **Progetti**. Un processo in background aggiornerà quindi il progetto in modo che supporti la nuova esperienza di pianificazione del progetto da Project for the Web. Questa fase è appropriata per i clienti che hanno progetti che rientrano nei [limiti noti di Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Nella fase 3 verrà aggiunto il supporto per Project Desktop Client, a vantaggio dei clienti che desiderano continuare a modificare i propri progetti da tale applicazione. Tuttavia, se i progetti esistenti vengono convertiti nella nuova esperienza Project for the Web, l'accesso al componente aggiuntivo verrà disabilitato per ogni progetto convertito.

## <a name="prerequisites"></a>Prerequisiti

Per essere idoneo per l'aggiornamento della fase 1, un cliente deve soddisfare i seguenti criteri:

- L'ambiente di destinazione non deve contenere alcun record nell'entità **msdyn_projecttask**.
- Le licenze valide per Project Operations devono essere assegnate a tutti gli utenti attivi del cliente. 
- Il cliente deve convalidare il processo di aggiornamento in almeno un ambiente non di produzione con un set di dati rappresentativo allineato con i dati di produzione.
- L'ambiente di destinazione deve essere aggiornato al rilascio 41 (3.10.62.162) di Project Service Automation o successivo.

I prerequisiti per la fase 2 e la fase 3 verranno aggiornati con l'avvicinarsi delle date di disponibilità generale.

## <a name="licensing"></a>Licenze

Se disponi di licenze attive per Project Service Automation, puoi installare e utilizzare Project Operations, che include tutte le funzionalità di Project Service Automation e altro ancora. In questo modo, puoi testare le funzionalità di Project Operations mentre continui a utilizzare Project Service Automation in produzione. Dopo la scadenza delle licenze di Project Service Automation, dovrai passare a Project Operations. Quando pianifichi questa transizione, devi tenere conto del fatto che la licenza di Project Operations non include una licenza di Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Test e refactoring delle personalizzazioni

Come punto di partenza, importa tutte le personalizzazioni in un ambiente pulito di Project Operations (semplice) per confermare che l'importazione ha esito positivo e che le operazioni aziendali si comportano come previsto.

Ecco alcune cose a cui prestare attenzione:

- L'importazione potrebbe non riuscire a causa delle dipendenze mancanti. In altre parole, le personalizzazioni fanno riferimento ai campi o ad altri componenti che sono stati rimossi in Project Operations. In questo caso, rimuovi queste dipendenze dall'ambiente di sviluppo.
- Se le soluzioni gestite e non gestite includono componenti non personalizzati, rimuovi tali componenti dalla soluzione. Ad esempio, quando personalizzi l'entità **Progetto**, aggiungi solo l'intestazione dell'entità alla tua soluzione. Non aggiungi tutti i campi. Se in precedenza hai aggiunto tutti i sottocomponenti, potresti dover creare manualmente una nuova soluzione e aggiungervi i componenti pertinenti.
- I moduli e le visualizzazioni potrebbero non apparire come previsto. In alcune circostanze, se hai personalizzato uno dei moduli o delle visualizzazioni predefiniti, le personalizzazioni potrebbero impedire l'applicazione dei nuovi aggiornamenti in Project Operations. Per identificare questi problemi, ti consigliamo di eseguire una revisione affiancata di un'installazione pulita di Project Operations e un'installazione di Project Operations che includa le tue personalizzazioni. Confronta i moduli più comunemente usati nella tua azienda per confermare che la tua versione del modulo ha ancora senso e non manca niente dalla versione pulita del modulo. Esegui lo stesso tipo di revisione affiancata per tutte le visualizzazioni che hai personalizzato.
- La logica aziendale potrebbe non riuscire in fase di esecuzione. Poiché i riferimenti ai campi nei plug-in non vengono convalidati al momento dell'importazione, la logica aziendale potrebbe non riuscire a causa di riferimenti a campi che non esistono più e potresti ricevere un messaggio di errore simile al seguente esempio: "L'entità "Progetto" non contiene attributi con Name = "msdyn_plannedhours" e NameMapping = "Logical"." In questo caso, modifica le tue personalizzazioni in modo che utilizzino i nuovi campi. Se utilizzi classi proxy generate automaticamente e riferimenti di tipo sicuro nella logica del plug-in, considera la possibilità di rigenerare tali proxy da un'installazione pulita. In questo modo, puoi identificare facilmente tutti i punti in cui i tuoi plug-in dipendono dai campi deprecati.

Dopo aver aggiornato le personalizzazioni per importare in modo pulito Project Operations, vai ai passaggi successivi.

## <a name="end-to-end-testing-in-development-environments"></a>Test end-to-end in ambienti di sviluppo

### <a name="initiate-upgrade"></a>Avviare l'aggiornamento 

1. Nell'interfaccia di amministrazione di Power Platform trova e seleziona il tuo ambiente. Quindi, nelle applicazioni, trova e seleziona **Dynamics 365 Project Operations**.
2. Seleziona **Installa** per iniziare l'aggiornamento. L'interfaccia di amministrazione di Power Platform presenterà questa installazione come una nuova installazione. Tuttavia, verrà rilevata la presenza di una versione precedente di Project Service Automation e l'installazione esistente verrà aggiornata.

    Al termine dell'aggiornamento, l'ambiente mostra che Project Operations è installato e che Project Service Automation non è installato.

    > [!NOTE]
    > A seconda della quantità di dati nell'ambiente, l'aggiornamento potrebbe richiedere diverse ore. Il team principale che gestisce l'aggiornamento deve pianificare di conseguenza ed eseguire l'aggiornamento durante le ore non lavorative. In alcuni casi, se il volume di dati è grande, l'aggiornamento deve essere eseguito durante il fine settimana. La decisione sulla pianificazione deve essere basata sui risultati dei test in ambienti inferiori.

3. Aggiorna le soluzioni personalizzate in base alle esigenze. A questo punto, distribuisci tutte le modifiche che hai apportato alle tue personalizzazioni nella sezione [Test e refactoring delle personalizzazioni](#testing-and-refactoring-customizations) di questo articolo.
4. Vai a **Impostazioni** \> **Soluzioni** e seleziona di disinstallare la soluzione **Componenti deprecati di Project Operations**.

    Questa soluzione è una soluzione temporanea che contiene il modello di dati esistente e i componenti presenti durante l'aggiornamento. Rimuovendo questa soluzione, rimuovi tutti i campi e i componenti che non vengono più utilizzati. In questo modo, contribuisci a semplificare l'interfaccia e a rendere più facili l'integrazione e l'estensione.
    
### <a name="validate-common-scenarios"></a>Scenari di convalida comuni

Quando convalidi le tue personalizzazioni specifiche, ti consigliamo di rivedere anche i processi aziendali supportati nelle applicazioni. Questi processi aziendali includono, tra gli altri, la creazione di entità di vendita come offerte e contratti e la creazione di progetti che includono la struttura di suddivisione del lavoro e l'approvazione dei valori effettivi.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Principali cambiamenti tra Project Service Automation e Project Operations

Questa sezione fornisce un riepilogo delle principali modifiche previste tra Project Service Automation e Project Operations.

### <a name="project-planning"></a>Pianificazione di un progetto

Le funzionalità di pianificazione del progetto in Project Operations non si basano più su una combinazione di logica lato client e logica lato server. Project Operations usa Project for the Web come suo motore di pianificazione. Questo cambiamento nelle capacità di pianificazione abilita diverse nuove funzionalità, come le visualizzazioni Scheda e Gantt, la pianificazione basata sulle risorse, [voci dell'elenco di controllo delle attività](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) e modalità di pianificazione del progetto. Le nuove capacità di pianificazione sono supportate anche da un ricco set di nuove [API](../project-management/schedule-api-preview.md). Queste API hanno lo scopo di garantire che nessuna operazione programmatica per la creazione, l'aggiornamento o l'eliminazione di un'entità nella struttura di suddivisione del lavoro danneggi i campi calcolati nella pianificazione.

## <a name="billing-and-pricing"></a>Determinazione dei prezzi e fatturazione

Nell'ambito dei continui investimenti in Project Operations, sono disponibili diverse nuove funzionalità in Fatturazione e prezzi. Di seguito sono riportati alcuni esempi.

- [Registrazione dell'uso dei materiali su progetti e attività di progetto](../material/material-usage-log.md)
- [Gestione dei conto lavoro](../pro/subcontracting/managing-subcontracts-overview.md)
- [Anticipi e contratti basati su acconto](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Convalide e stato da non superare del contratto](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Fatturazione basata su attività

## <a name="frequently-asked-questions"></a>Domande frequenti

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Quali tipi di distribuzione sono attualmente supportati per l'aggiornamento?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automazione servizi di progetto                             | Distribuzione di Project Operations semplice                        | Supportato               |
| Gestione progetti e contabilità in Dynamics 365 Finance | Distribuzione di Project Operations semplice                        | Non è al momento supportato |
| Contabilità e gestione dei progetti in Finance              | Project Operations per scenari di risorse/materiali non stoccati     | Non è al momento supportato |
| Project Service Automation 3.x                         | Project Operations per scenari di risorse/materiali non stoccati     | Non è al momento supportato |
| Project for the Web (ambiente dedicato)            | Distribuzione di Project Operations semplice                        | Non è al momento supportato |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Come posso installare Project Operations prima che gli strumenti di aggiornamento siano disponibili?

Sono disponibili due opzioni per l'installazione di Project Operations prima che gli strumenti di aggiornamento siano disponibili:

- Effettua il provisioning di un nuovo ambiente.
- Distribuisci Project Operations separatamente in qualsiasi organizzazione di vendita in cui Project Service Automation non è presente.

> [!NOTE]
> Se Project Service Automation è installato in un'organizzazione, ma non è stato utilizzato, può essere disinstallato. Dopo aver rimosso completamente Project Service Automation, Project Operations può essere installato nella stessa organizzazione.
