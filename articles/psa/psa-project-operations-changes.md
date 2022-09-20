---
title: Modifiche della funzionalità da Project Service Automation a Project Operations
description: Questo articolo fornisce una panoramica delle modifiche alla funzionalità da Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459931"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Modifiche della funzionalità da Project Service Automation a Project Operations

L'aggiornamento da Dynamics 365 Project Service Automation a Dynamics 365 Project Operations Lite sarà consegnato in tre fasi. Questo articolo fornisce le informazioni sulle principali modifiche che puoi aspettarti di vedere al termine dell'aggiornamento.

| Consegna dell'aggiornamento | Fase 1 <br>(Gennaio 2022) | Fase 2 <br>(Novembre 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Nessuna dipendenza dalla struttura di suddivisione del lavoro (WBS) per i progetti. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| La struttura di suddivisione del lavoro è inclusa nei limiti attualmente supportati di Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| La struttura di suddivisione del lavoro al di fuori dei limiti attualmente supportati di Project Operations, incluso il supporto per Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Gestione dei progetti

I cambiamenti più significativi nell'esperienza utente riguarderanno l'area della pianificazione del progetto. Project Operations adotta una nuova esperienza moderna per la gestione di una struttura di suddivisione del lavoro sfruttando le capacità di pianificazione fornite da [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Differenze nell'esperienza di pianificazione

La tabella seguente riassume le differenze di pianificazione tra Project Service Automation e Project Operations.

|  Pianificazione     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Modelli di progetto: capacità di definire e applicare modelli di progetto quando viene creato un progetto  |  &nbsp;    | :heavy_check_mark: |
| Integrazione della struttura di suddivisione del lavoro del progetto con il client desktop   |    &nbsp;  | :heavy_check_mark: |
| Vincoli - Inizia non prima del giorno, Termina non più tardi del giorno  | :heavy_check_mark: |   &nbsp;  |
| Passaggi fondamentali - Attività con durata zero   | :heavy_check_mark:  |  &nbsp;  |
| Le attività basate sulle risorse rispetteranno la disponibilità delle risorse assegnate   | :heavy_check_mark: |  &nbsp;    |
| Modifica su scala cronologica: modifica i piani e lavora giorno per giorno   |   &nbsp;  | :heavy_check_mark: |
| Pianificazione automatica/manuale: utilizza il motore di pianificazione del progetto per pianificare automaticamente o manualmente le attività |  &nbsp; | :heavy_check_mark:  |
| Modifica progetti di grandi dimensioni direttamente nell'interfaccia utente: non c'è limite alle dimensioni dei piani modificabili  | Limite di 500 attività  | :heavy_check_mark:       |
| Percentuale di completamento: contrassegna l'avanzamento dell'attività   | :heavy_check_mark:  |  &nbsp;  |
| [Modalità di pianificazione del progetto](../project-management/scheduling-modes.md) - Definisci il progetto come unità fisse, impegno fisso o durata fissa | :heavy_check_mark: | &nbsp; |
| Sequenza temporale: crea e personalizza la visualizzazione della sequenza temporale per visualizzare i dettagli della pianificazione e comunicare con le parti interessate. | :heavy_check_mark:  | &nbsp; |
| Attività basate sull'impegno - Pianificazione del supporto del motore per la pianificazione di un'attività in base all'impegno  | :heavy_check_mark:  | &nbsp; |
| Finestra di dialogo **Informazioni sull'attività** - Salva i dettagli dell'attività utilizzando una finestra di dialogo | :heavy_check_mark:  |  &nbsp;  |
| Trascina e rilascia: seleziona più attività e modifica la loro posizione sulla struttura di suddivisione del lavoro | :heavy_check_mark: | &nbsp;  |
| Viste persistenti flessibili - Definisci viste più granulari degli attributi delle attività   | :heavy_check_mark:  | &nbsp; |
| Ordina e filtra la struttura di suddivisione del lavoro  | :heavy_check_mark:  | &nbsp; |
| Visualizzazione delle schede per la consegna di progetti non a cascata  | :heavy_check_mark:   | &nbsp; |
| Visualizzazione sequenza temporale: diagramma di Gantt interattivo utilizzato per visualizzare e modificare la struttura di suddivisione del lavoro   | :heavy_check_mark:  | &nbsp; |
| Tasti di scelta rapida: utilizza i tasti di scelta rapida per operazioni comuni, come il rientro o l'inserimento  | :heavy_check_mark:  |  &nbsp; |
| Annulla a più livelli: esegui analisi what-if per comprendere appieno l'impatto delle modifiche invertendo e riapplicando un intero set di operazioni | :heavy_check_mark: | &nbsp; |
| Taglia/Copia/Incolla: collabora allo sviluppo della pianificazione copiando e incollando i dettagli della pianificazione tra le applicazioni  | :heavy_check_mark: | &nbsp; |
| Elenchi di controllo delle attività: aggiungi fino a 20 elementi di elenco di controllo a un'attività   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Pianificazione di un progetto

La pagina **Progetto** in Project Operations presenta un numero significativo di differenze rispetto alla pagina **Progetto** in Project Service Automation.

Le seguenti azioni sono state rimosse dalla pagina **Progetti** come parte dell'aggiornamento Fase 1:

  - **Apri in MS Project**
  - **Crea modello**
  - **Scollega da MS Project**

La pagina **Progetto** in Project Operations include le seguenti nuove schede.

- **Stime materiale**
- **Configurazione fatturazione attività**

La scheda **Stato** è stata rimossa e il campo **Stato** è ora nella scheda **Riepilogo** con la modalità di pianificazione del progetto.

   ![Aggiornamenti alla pagina Progetto.](media/projectform.png)

La scheda **Pianifica** è stata rinominata in **Attività** e presenta la nuova esperienza di pianificazione del progetto con Project for the Web.

   ![Nuova scheda Attività del progetto.](media/tasktab.png)

## <a name="scheduling-modes"></a>Modalità di pianificazione

Project Operations ha introdotto una nuova funzionalità, [Modalità di pianificazione](../project-management/scheduling-modes.md). Tutti i progetti di Project Service Automation esistenti verranno impostati automaticamente su **Durata fissa** in Project Operations. Tuttavia, l'impostazione predefinita per i nuovi progetti può essere gestita andando in **Impostazioni** > **Parametri** > **Parametro** > **Modalità di pianificazione**.

   ![Impostazioni dei parametri di progetto per la modalità Pianificazione.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Limiti di pianificazione di un progetto

Project Operations si basa su Project for the Web per tutte le operazioni di pianificazione del progetto. Project for the Web gestisce la struttura di suddivisione del lavoro utilizzando i limiti nella tabella seguente.

| **Campo**                                          | **Limit**             |
|----------------------------------------------------|-----------------------|
| Numero massimo di attività totali per un progetto                  | 500                   |
| Durata massima totale per un progetto               | 3650 giorni (10 anni)  |
| Numero massimo di risorse totali per un progetto              | 300                   |
| Numero massimo di collegamenti totali (solo attività successiva) per un progetto | 600                   |
| Numero massimo di campi personalizzati totali per un progetto          | 10                    |
| Numero massimo di livelli di gerarchia                            | 10 livelli             |
| Numero massimo di collegamenti (attività successiva + attività precedente)            | 20                    |
| Durata massima dell'attività del nodo foglia                      | 1250 giorni             |
| Durata massima di un'attività di riepilogo                 | 3650 giorni (10 anni)  |
| Numero massimo di risorse assegnate a un'attività               | 20 risorse          |
| Intervallo di date supportato per un'attività                    | 1/1/2000 - 31/12/2149 |
| Voci dell'elenco di controllo                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Estendibilità e sviluppo della pianificazione del progetto

Dopo aver eseguito l'aggiornamento a Project Operations, è necessario utilizzare le API di pianificazione del processo per eseguire operazioni di creazione, aggiornamento ed eliminazione sulle seguenti entità:

|   Nome dell'entità           |   Nome logico entità       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Attività di progetto            | msdyn_projecttask           |
| Dipendenza attività di progetto | msdyn_projecttaskdependency |
| Assegnazione risorse     | msdyn_resourceassignment    |
| Bucket di progetto          | msdyn_projectbucket         |
| Membro del team di progetto     | msdyn_projectteam           |

Se al momento disponi di personalizzazioni che coinvolgono queste entità, vedi [Utilizzare le API di pianificazione del progetto per eseguire operazioni con le entità di pianificazione](../project-management/schedule-api-preview.md) per la guida all'implementazione.

## <a name="data-model-changes"></a>Modifiche del modello di dati

Nell'ambito della fase di aggiornamento 1, sono state apportate modifiche al modello di dati. Queste modifiche sono principalmente modifiche di campo alle entità esistenti. Nella Fase 1, le entità, **msydn_project** e **msdyn_projectteam** sono un refactoring delle personalizzazioni. 

> [!IMPORTANT]
> Questa sezione verrà aggiornata con entità aggiuntive man mano che le fasi di aggiornamento future saranno completate.

I seguenti campi sono stati sostituiti con nuovi campi.

|   Entity          |   Nome logico precedente   |   Nuovo nome logico    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Sono stati aggiunti i seguenti campi.

|   Entity          |   Nome logico                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Mostra l'aggregazione della vendita commissione effettiva sul progetto. Solo per utilizzo con Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Mostra l'aggregazione del costo materiale effettivo sul progetto. Solo per utilizzo con Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Mostra l'aggregazione della vendita materiale effettiva sul progetto. Solo per utilizzo con Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Voce di contratto associata al progetto. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Questo è un campo interno di sistema usato per **copiare il progetto** correlato all'identificatore di correlazione. Solo per utilizzo con Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Questo è un campo interno di sistema usato per **copiare il progetto** correlato all'identificatore di sessione. Solo per utilizzo con Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Token di revisione globale xRM ultima sincronizzazione dal servizio di pianificazione del progetto. |
| msdyn_project     | msdyn_msprojectdocument                      | Il documento di Microsoft Project che appartiene al progetto. |
| msdyn_project     | msdyn_plannedmaterialcost                    | L'aggregazione del costo materiale pianificato sul progetto. Solo per utilizzo con Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | L'aggregazione delle vendite materiale pianificate sul progetto. Solo per utilizzo con Project Service Automation. |
| msdyn_project     | msdyn_program                                | Programma a cui questo progetto è correlato. |
| msdyn_project     | msdyn_quotelineproject                       | Riga dell'offerta associata al progetto. |
| msdyn_project     | msdyn_replaylogheader                        | Intestazione dei registri di riproduzione. |
| msdyn_project     | msdyn_schedulemode                           | Modalità di pianificazione predefinita utilizzata per tutte le attività del progetto.  |
| msdyn_project     | msdyn_taskearlieststart                      | Prima data di inizio di qualsiasi attività nel progetto.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Il membro del team di progetto da cui questo membro del team di progetto è stato copiato. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Indica se creare il requisito di risorsa per un membro del team generico appena creato.  |
| msdyn_projectteam | msdyn_deletestatus                           | Stato di eliminazione del membro del team per registrare se è presente una richiesta di eliminazione inviata al servizio di pianificazione del progetto e se il servizio di pianificazione del progetto invia una risposta con esito positivo e nell'intervallo di tempo previsto. |
| msdyn_projectteam | msdyn_effortcompleted                        | Tiene traccia delle attività svolte dal membro del team sulla sua assegnazione. |
| msdyn_projectteam | msdyn_effortremaining                        | Tiene traccia delle attività da completare dal membro del team sulla sua assegnazione. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Il periodo di attesa da quando il membro del team invia una richiesta di eliminazione al servizio di pianificazione del progetto fino a quando il membro del team viene effettivamente eliminato in Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Timestamp da registrare quando la richiesta di eliminazione del membro del team viene inviata al servizio di pianificazione del progetto. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Mostra il membro del team di progetto da cui questo membro del team di progetto è stato copiato.  |

## <a name="project-templates"></a>Modelli di progetto

Project Operations non fornisce supporto per i modelli di progetto. Tuttavia, puoi replicare gran parte delle funzionalità di base con l'uso dell'[API di copia del progetto](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Supporto per componenti aggiuntivi desktop

Il supporto per il componente aggiuntivo Microsoft Project Desktop non sarà disponibile nelle prime 2 fasi dell'aggiornamento. Nella fase 3, i clienti che hanno progetti più grandi dei limiti attualmente supportati di Project for the Web potranno utilizzare il componente aggiuntivo desktop.

## <a name="editing-resource-assignment-contours"></a>Modifica dei profili di assegnazione delle risorse

La possibilità di modificare i profili di assegnazione delle risorse sarà disponibile con la Fase 2 dell'aggiornamento.

## <a name="billing-and-pricing"></a>Determinazione dei prezzi e fatturazione

Le seguenti nuove funzionalità sono state aggiunte in Project Operations. Queste funzionalità sono di natura additiva e non influiscono sul modello di dati di Project Service Automation.

- [Registrazione dell'uso dei materiali su progetti e attività di progetto](../material/material-usage-log.md)
- [Gestione dei conto lavoro](../pro/subcontracting/managing-subcontracts-overview.md)
- [Anticipi e contratti basati su acconto](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Convalide e stato da non superare del contratto](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Fatturazione basata su attività](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Componenti deprecati

Le tabelle seguenti documentano tutti i campi deprecati che vengono spostati nella soluzione dei componenti deprecati dopo l'aggiornamento. Per ulteriori informazioni e un collegamento alla soluzione, vedi [Componenti deprecati da Dynamics 365 Project Service Automation 3x a Project Operations 4x](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Campi                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

