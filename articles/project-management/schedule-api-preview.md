---
title: Utilizzare API di pianificazione per eseguire operazioni con le entità di pianificazione
description: Questo argomento fornisce informazioni ed esempi sull'utilizzo delle API di pianificazione.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868134"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utilizzare API di pianificazione per eseguire operazioni con le entità di pianificazione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

> [!IMPORTANT] 
> L'intera funzionalità, o una sua parte, descritta in questo articolo è disponibile nella versione di anteprima. Il contenuto e la funzionalità sono soggetti a modifiche. 

## <a name="scheduling-entities"></a>Entità di pianificazione

Le API di pianificazione consentono di eseguire operazioni di creazione, aggiornamento ed eliminazione con **Entità di pianificazione**. Queste entità vengono gestite tramite il motore di pianificazione in Project per il Web. Le operazioni di creazione, aggiornamento ed eliminazione con **Entità di pianificazione** erano limitate nelle versioni precedenti di Dynamics 365 Project Operations.

La tabella seguente fornisce un elenco completo delle **Entità di pianificazione**.

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

## <a name="schedule-apis"></a>API di pianificazione

Di seguito è riportato un elenco delle API di pianificazione correnti.

- **msdyn_CreateProjectV1**: questa API può essere utilizzata per creare un progetto. Il progetto e il bucket di progetto predefinito vengono creati immediatamente.
- **msdyn_CreateTeamMemberV1**: questa API può essere utilizzata per creare un membro del team di progetto. Il record Membro del team viene creato immediatamente.
- **msdyn_CreateOperationSetV1**: questa API può essere utilizzata per pianificare diverse richieste che devono essere eseguite in una transazione.
- **msdyn_PSSCreateV1**: questa API può essere utilizzata per creare un'entità. L'entità può essere una qualsiasi delle entità di pianificazione che supportano l'operazione di creazione.
- **msdyn_PSSUpdateV1**: questa API può essere utilizzata per aggiornare un'entità. L'entità può essere una qualsiasi delle entità di pianificazione che supportano l'operazione di aggiornamento.
- **msdyn_PSSDeleteV1**: questa API può essere utilizzata per eliminare un'entità. L'entità può essere una qualsiasi delle entità di pianificazione che supportano l'operazione di eliminazione.
- **msdyn_ExecuteOperationSetV1**: questa API viene utilizzata per eseguire tutte le operazioni in un determinato set di operazioni.

## <a name="using-schedule-apis-with-operationset"></a>Utilizzo delle API di pianificazione con OperationSet

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

## <a name="limitations-and-known-issues"></a>Limitazioni e problemi noti
Di seguito è riportato un elenco di limitazioni e problemi noti:

- Le API di pianificazione possono essere utilizzate solo da **utenti con licenza Microsoft Project**. Non possono essere utilizzate da:
    - Utenti dell'applicazione
    - Utenti di sistema
    - Utenti integrazione
    - Altri utenti che non dispongono della licenza richiesta
- Ogni **OperationSet** può avere un massimo di 100 operazioni.
- Ogni utente può avere un massimo di 10 **OperationSets** aperti.
- Project Operations attualmente supporta un massimo di 500 attività totali in un progetto.
- Lo stato di errore e i registri degli errori di **OperationSet** non sono attualmente disponibili.
- Le API di pianificazione sono in anteprima pubblica. L'utilizzo di queste API in un ambiente di produzione non è supportato da Microsoft.

## <a name="sample-scenario"></a>Scenario di esempio

In questo scenario, creerai un progetto, un membro del team, quattro attività e due assegnazioni di risorse. Successivamente, aggiornerai un'attività e il progetto, eliminerai un'attività e un'assegnazione di risorse e creerai una dipendenza attività.

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Esempi aggiuntivi

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
