---
title: Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione
description: Questo argomento fornisce informazioni ed esempi per l'utilizzo delle API di pianificazione del progetto.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293232"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

> [!IMPORTANT] 
> L'intera funzionalità, o una sua parte, descritta in questo articolo è disponibile nella versione di anteprima. Il contenuto e la funzionalità sono soggetti a modifiche. 

## <a name="scheduling-entities"></a>Entità di pianificazione

Le API di pianificazione del progetto offrono la possibilità di eseguire operazioni di creazione, aggiornamento ed eliminazione con **entità di pianificazione**. Queste entità vengono gestite tramite il motore di pianificazione in Project per il Web. Le operazioni di creazione, aggiornamento ed eliminazione con **Entità di pianificazione** erano limitate nelle versioni precedenti di Dynamics 365 Project Operations.

La tabella seguente fornisce un elenco completo delle entità di pianificazione del progetto.

| Nome dell'entità  | Nome logico entità |
| --- | --- |
| Project | msdyn_project |
| Attività di progetto  | msdyn_projecttask  |
| Dipendenza attività di progetto  | msdyn_projecttaskdependency  |
| Assegnazione risorse | msdyn_resourceassignment |
| Bucket di progetto  | msdyn_projectbucket |
| Membro del team di progetto | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet è un modello di unità di lavoro che può essere utilizzato quando in una transazione devono essere elaborate diverse richieste che influiscono sulla pianificazione.

## <a name="project-schedule-apis"></a>API di pianificazione di progetto

Di seguito è riportato un elenco delle API di pianificazione del progetto correnti.

- **msdyn_CreateProjectV1**: questa API può essere utilizzata per creare un progetto. Il progetto e il bucket di progetto predefinito vengono creati immediatamente.
- **msdyn_CreateTeamMemberV1**: questa API può essere utilizzata per creare un membro del team di progetto. Il record Membro del team viene creato immediatamente.
- **msdyn_CreateOperationSetV1**: questa API può essere utilizzata per pianificare diverse richieste che devono essere eseguite in una transazione.
- **msdyn_PSSCreateV1**: questa API può essere utilizzata per creare un'entità. L'entità può essere una qualsiasi delle entità di pianificazione del progetto che supportano l'operazione di creazione.
- **msdyn_PSSUpdateV1**: questa API può essere utilizzata per aggiornare un'entità. L'entità può essere una qualsiasi delle entità di pianificazione del progetto che supportano l'operazione di aggiornamento.
- **msdyn_PSSDeleteV1**: questa API può essere utilizzata per eliminare un'entità. L'entità può essere una qualsiasi delle entità di pianificazione del progetto che supportano l'operazione di eliminazione.
- **msdyn_ExecuteOperationSetV1**: questa API viene utilizzata per eseguire tutte le operazioni in un determinato set di operazioni.

## <a name="using-project-schedule-apis-with-operationset"></a>Utilizzo delle API di pianificazione del progetto con OperationSet

Poiché i record con **CreateProjectV1** e **CreateTeamMemberV1** vengono creati immediatamente, queste API non possono essere utilizzate direttamente in **OperationSet**. Tuttavia, puoi utilizzare l'API per creare i record necessari, creare un **OperationSet**, quindi utilizzare questi record predefiniti in **OperationSet**.

## <a name="supported-operations"></a>Operazioni supportate

| Entità di pianificazione | Creazione di | Aggiornamento | CANC | Considerazioni importanti |
| --- | --- | --- | --- | --- |
Attività di progetto | Sì | Sì | Sì | Nessuna |
| Dipendenza attività di progetto | Sì | Sì | | I record Dipendenza attività di progetto non vengono aggiornati. È invece possibile eliminare un vecchio record e crearne uno nuovo. |
| Assegnazione risorse | Sì | Sì | | Le operazioni con i seguenti campi non sono supportate: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**. I record Assegnazione risorse non vengono aggiornati. È invece possibile eliminare il vecchio record e crearne uno nuovo. |
| Bucket di progetto | N/D | N/D | N/D | Il bucket predefinito viene creato utilizzando l'API **CreateProjectV1**. |
| Membro del team di progetto | Sì | Sì | Sì | Per l'operazione di creazione, utilizza l'API **CreateTeamMemberV1**. |
| Project | Sì | Sì | N/D | Le operazioni con i seguenti campi non sono supportate: : **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**. |

Queste API possono essere chiamate con oggetti entità che includono campi personalizzati.

La proprietà ID è facoltativa. Se fornita, il sistema tenta di utilizzarla e genera un'eccezione se non può essere utilizzata. Se non è fornita, il sistema la genererà.

## <a name="restricted-fields"></a>Campi con limitazioni

Le seguenti tabelle definiscono i campi con limitazioni **Crea** e **Modifica.**

### <a name="project-task"></a>Attività di progetto

| **Nome logico**                       | **Creazione possibile** | **Modifica possibile**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | no             | no               |
| msdyn_actualcost_base                  | no             | no               |
| msdyn_actualend                        | no             | no               |
| msdyn_actualsales                      | no             | no               |
| msdyn_actualsales_base                 | no             | no               |
| msdyn_actualstart                      | no             | no               |
| msdyn_costatcompleteestimate           | no             | no               |
| msdyn_costatcompleteestimate_base      | no             | no               |
| msdyn_costconsumptionpercentage        | no             | no               |
| msdyn_effortcompleted                  | no             | no               |
| msdyn_effortestimateatcomplete         | no             | no               |
| msdyn_iscritical                       | no             | no               |
| msdyn_iscriticalname                   | no             | no               |
| msdyn_ismanual                         | no             | no               |
| msdyn_ismanualname                     | no             | no               |
| msdyn_ismilestone                      | no             | no               |
| msdyn_ismilestonename                  | no             | no               |
| msdyn_LinkStatus                       | no             | no               |
| msdyn_linkstatusname                   | no             | no               |
| msdyn_msprojectclientid                | no             | no               |
| msdyn_plannedcost                      | no             | no               |
| msdyn_plannedcost_base                 | no             | no               |
| msdyn_plannedsales                     | no             | no               |
| msdyn_plannedsales_base                | no             | no               |
| msdyn_pluginprocessingdata             | no             | no               |
| msdyn_progress                         | no             | no (sì per P4W) |
| msdyn_remainingcost                    | no             | no               |
| msdyn_remainingcost_base               | no             | no               |
| msdyn_remainingsales                   | no             | no               |
| msdyn_remainingsales_base              | no             | no               |
| msdyn_requestedhours                   | no             | no               |
| msdyn_resourcecategory                 | no             | no               |
| msdyn_resourcecategoryname             | no             | no               |
| msdyn_resourceorganizationalunitid     | no             | no               |
| msdyn_resourceorganizationalunitidname | no             | no               |
| msdyn_salesconsumptionpercentage       | no             | no               |
| msdyn_salesestimateatcomplete          | no             | no               |
| msdyn_salesestimateatcomplete_base     | no             | no               |
| msdyn_salesvariance                    | no             | no               |
| msdyn_salesvariance_base               | no             | no               |
| msdyn_scheduleddurationminutes         | no             | no               |
| msdyn_scheduledend                     | no             | no               |
| msdyn_scheduledstart                   | no             | no               |
| msdyn_schedulevariance                 | no             | no               |
| msdyn_skipupdateestimateline           | no             | no               |
| msdyn_skipupdateestimatelinename       | no             | no               |
| msdyn_summary                          | no             | no               |
| msdyn_varianceofcost                   | no             | no               |
| msdyn_varianceofcost_base              | no             | no               |

### <a name="project-task-dependency"></a>Dipendenza attività di progetto

| **Nome logico**              | **Creazione possibile** | **Modifica possibile** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | no             | no           |
| msdyn_linktypename            | no             | no           |
| msdyn_predecessortask         | sì            | no           |
| msdyn_predecessortaskname     | sì            | no           |
| msdyn_project                 | sì            | no           |
| msdyn_projectname             | sì            | no           |
| msdyn_projecttaskdependencyid | sì            | no           |
| msdyn_successortask           | sì            | no           |
| msdyn_successortaskname       | sì            | no           |

### <a name="resource-assignment"></a>Assegnazione risorse

| **Nome logico**             | **Creazione possibile** | **Modifica possibile** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | sì            | no           |
| msdyn_bookableresourceidname | sì            | no           |
| msdyn_bookingstatusid        | no             | no           |
| msdyn_bookingstatusidname    | no             | no           |
| msdyn_committype             | no             | no           |
| msdyn_committypename         | no             | no           |
| msdyn_effort                 | no             | no           |
| msdyn_effortcompleted        | no             | no           |
| msdyn_effortremaining        | no             | no           |
| msdyn_finish                 | no             | no           |
| msdyn_plannedcost            | no             | no           |
| msdyn_plannedcost_base       | no             | no           |
| msdyn_plannedcostcontour     | no             | no           |
| msdyn_plannedsales           | no             | no           |
| msdyn_plannedsales_base      | no             | no           |
| msdyn_plannedsalescontour    | no             | no           |
| msdyn_plannedwork            | no             | no           |
| msdyn_projectid              | sì            | no           |
| msdyn_projectidname          | no             | no           |
| msdyn_projectteamid          | no             | no           |
| msdyn_projectteamidname      | no             | no           |
| msdyn_start                  | no             | no           |
| msdyn_taskid                 | no             | no           |
| msdyn_taskidname             | no             | no           |
| msdyn_userresourceid         | no             | no           |

### <a name="project-team-member"></a>Membro del team di progetto

| **Nome logico**                                 | **Creazione possibile** | **Modifica possibile** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | no             | no           |
| msdyn_creategenericteammemberwithrequirementname | no             | no           |
| msdyn_deletestatus                               | no             | no           |
| msdyn_deletestatusname                           | no             | no           |
| msdyn_effort                                     | no             | no           |
| msdyn_effortcompleted                            | no             | no           |
| msdyn_effortremaining                            | no             | no           |
| msdyn_finish                                     | no             | no           |
| msdyn_hardbookedhours                            | no             | no           |
| msdyn_hours                                      | no             | no           |
| msdyn_markedfordeletiontimer                     | no             | no           |
| msdyn_markedfordeletiontimestamp                 | no             | no           |
| msdyn_msprojectclientid                          | no             | no           |
| msdyn_percentage                                 | no             | no           |
| msdyn_requiredhours                              | no             | no           |
| msdyn_softbookedhours                            | no             | no           |
| msdyn_start                                      | no             | no           |

### <a name="project"></a>Project

| **Nome logico**                       | **Creazione possibile** | **Modifica possibile** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | no             | no           |
| msdyn_actualexpensecost_base           | no             | no           |
| msdyn_actuallaborcost                  | no             | no           |
| msdyn_actuallaborcost_base             | no             | no           |
| msdyn_actualsales                      | no             | no           |
| msdyn_actualsales_base                 | no             | no           |
| msdyn_contractlineproject              | sì            | no           |
| msdyn_contractorganizationalunitid     | sì            | no           |
| msdyn_contractorganizationalunitidname | sì            | no           |
| msdyn_costconsumption                  | no             | no           |
| msdyn_costestimateatcomplete           | no             | no           |
| msdyn_costestimateatcomplete_base      | no             | no           |
| msdyn_costvariance                     | no             | no           |
| msdyn_costvariance_base                | no             | no           |
| msdyn_duration                         | no             | no           |
| msdyn_effort                           | no             | no           |
| msdyn_effortcompleted                  | no             | no           |
| msdyn_effortestimateatcompleteeac      | no             | no           |
| msdyn_effortremaining                  | no             | no           |
| msdyn_finish                           | sì            | sì          |
| msdyn_globalrevisiontoken              | no             | no           |
| msdyn_islinkedtomsprojectclient        | no             | no           |
| msdyn_islinkedtomsprojectclientname    | no             | no           |
| msdyn_linkeddocumenturl                | no             | no           |
| msdyn_msprojectdocument                | no             | no           |
| msdyn_msprojectdocumentname            | no             | no           |
| msdyn_plannedexpensecost               | no             | no           |
| msdyn_plannedexpensecost_base          | no             | no           |
| msdyn_plannedlaborcost                 | no             | no           |
| msdyn_plannedlaborcost_base            | no             | no           |
| msdyn_plannedsales                     | no             | no           |
| msdyn_plannedsales_base                | no             | no           |
| msdyn_progress                         | no             | no           |
| msdyn_remainingcost                    | no             | no           |
| msdyn_remainingcost_base               | no             | no           |
| msdyn_remainingsales                   | no             | no           |
| msdyn_remainingsales_base              | no             | no           |
| msdyn_replaylogheader                  | no             | no           |
| msdyn_salesconsumption                 | no             | no           |
| msdyn_salesestimateatcompleteeac       | no             | no           |
| msdyn_salesestimateatcompleteeac_base  | no             | no           |
| msdyn_salesvariance                    | no             | no           |
| msdyn_salesvariance_base               | no             | no           |
| msdyn_scheduleperformance              | no             | no           |
| msdyn_scheduleperformancename          | no             | no           |
| msdyn_schedulevariance                 | no             | no           |
| msdyn_taskearlieststart                | no             | no           |
| msdyn_teamsize                         | no             | no           |
| msdyn_teamsize_date                    | no             | no           |
| msdyn_teamsize_state                   | no             | no           |
| msdyn_totalactualcost                  | no             | no           |
| msdyn_totalactualcost_base             | no             | no           |
| msdyn_totalplannedcost                 | no             | no           |
| msdyn_totalplannedcost_base            | no             | no           |


## <a name="limitations-and-known-issues"></a>Limitazioni e problemi noti
Di seguito è riportato un elenco di limitazioni e problemi noti:

- Le API di pianificazione del progetto possono essere utilizzate solo da **Utenti con licenza Microsoft Project.** Non possono essere utilizzate da:
    - Utenti dell'applicazione
    - Utenti di sistema
    - Utenti integrazione
    - Altri utenti che non dispongono della licenza richiesta
- Ogni **OperationSet** può avere un massimo di 100 operazioni.
- Ogni utente può avere un massimo di 10 **OperationSets** aperti.
- Project Operations attualmente supporta un massimo di 500 attività totali in un progetto.
- Lo stato di errore e i registri degli errori di **OperationSet** non sono attualmente disponibili.
- [Limiti e confini per progetti e attività](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Gestione errori

   - Per rivedere gli errori generati dai set di operazioni, vai a **Impostazioni** \> **Pianifica integrazione** \> **Set di operazioni**.
   - Per rivedere gli errori generati dal servizio di pianificazione del progetto, vai a **Impostazioni** \> **Integrazione di pianificazione** \> **Registri errori PSS**.

## <a name="sample-scenario"></a>Scenario di esempio

In questo scenario, creerai un progetto, un membro del team, quattro attività e due assegnazioni di risorse. Successivamente, aggiornerai un'attività e il progetto, eliminerai un'attività e un'assegnazione di risorse e creerai una dipendenza attività.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Esempi aggiuntivi

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
