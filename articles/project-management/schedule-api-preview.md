---
title: Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione
description: Questo articolo fornisce informazioni ed esempi per l'utilizzo delle API di pianificazione del progetto.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541129"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


**Entità di pianificazione**

Le API di pianificazione del progetto offrono la possibilità di eseguire operazioni di creazione, aggiornamento ed eliminazione con **entità di pianificazione**. Queste entità vengono gestite tramite il motore di pianificazione in Project for the Web. Le operazioni di creazione, aggiornamento ed eliminazione con **Entità di pianificazione** erano limitate nelle versioni precedenti di Dynamics 365 Project Operations.

La tabella seguente fornisce un elenco completo delle entità di pianificazione del progetto.

| **Nome entità**         | **Nome logico entità**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Attività di progetto            | msdyn_projecttask           |
| Dipendenza attività di progetto | msdyn_projecttaskdependency |
| Assegnazione risorse     | msdyn_resourceassignment    |
| Bucket di progetto          | msdyn_projectbucket         |
| Membro del team di progetto     | msdyn_projectteam           |
| Elenchi di controllo del progetto      | msdyn_projectchecklist      |
| Etichetta del progetto           | msdyn_projectlabel          |
| Relazione tra attività di progetto ed etichetta   | msdyn_projecttasktolabel    |
| Sprint di progetto          | msdyn_projectsprint         |

**OperationSet**

OperationSet è un modello di unità di lavoro che può essere utilizzato quando in una transazione devono essere elaborate diverse richieste che influiscono sulla pianificazione.

**API di pianificazione di progetto**

Di seguito è riportato un elenco delle API di pianificazione del progetto correnti.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Questa API viene utilizzata per creare un progetto. Il progetto e il bucket del progetto predefinito vengono creati immediatamente.                         |
| **msdyn_CreateTeamMemberV1**            | Questa API viene utilizzata per creare un membro del team di progetto. Il record Membro del team viene creato immediatamente.                                  |
| **msdyn_CreateOperationSetV1**          | Questa API viene utilizzata per pianificare diverse richieste che devono essere eseguite in una transazione.                                        |
| **msdyn_PssCreateV1**                   | Questa API viene utilizzata per creare un'entità. L'entità può essere una qualsiasi delle entità di pianificazione del progetto che supportano l'operazione di creazione. |
| **msdyn_PssUpdateV1**                   | Questa API viene utilizzata per aggiornare un'entità. L'entità può essere una qualsiasi delle entità di pianificazione del progetto che supportano l'operazione di aggiornamento.  |
| **msdyn_PssDeleteV1**                   | Questa API viene utilizzata per eliminare un'entità. L'entità può essere una qualsiasi delle entità di pianificazione del progetto che supportano l'operazione di eliminazione. |
| **msdyn_ExecuteOperationSetV1**         | Questa API viene utilizzata per eseguire tutte le operazioni in un determinato set di operazioni.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Questa API viene utilizzata per aggiornare la distribuzione del lavoro pianificato per l'assegnazione delle risorse.                                                        |



**Utilizzo delle API di pianificazione del progetto con OperationSet**

Poiché i record con **CreateProjectV1** e **CreateTeamMemberV1** vengono creati immediatamente, queste API non possono essere utilizzate direttamente in **OperationSet**. Tuttavia, puoi utilizzare l'API per creare i record necessari, creare un **OperationSet**, quindi utilizzare questi record predefiniti in **OperationSet**.

**Operazioni supportate**

| **Entità di pianificazione**   | **Creazione di** | **Update** | **Elimina** | **Considerazioni importanti**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Attività di progetto            | Sì        | Sì        | Sì        | I campi **Progress**, **EffortCompleted**, e **EffortRemaining** possono essere modificati in Project for the Web, ma non possono essere modificati in Project Operations.                                                                                                                                                                                             |
| Dipendenza attività di progetto | Sì        | No         | Sì        | I record Dipendenza attività di progetto non vengono aggiornati. È invece possibile eliminare un vecchio record e crearne uno nuovo.                                                                                                                                                                                                                                 |
| Assegnazione risorse     | Sì        | Sì\*      | Sì        | Le operazioni con i seguenti campi non sono supportate: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**. I record Assegnazione risorse non vengono aggiornati. È invece possibile eliminare il vecchio record e crearne uno nuovo. È stata fornita un'API distinta per aggiornare le distribuzioni dell'assegnazione delle risorse. |
| Bucket di progetto          | Sì        | Sì        | Sì        | Il bucket predefinito viene creato utilizzando l'API **CreateProjectV1**. Il supporto per la creazione e l'eliminazione di bucket di progetto è stato aggiunto nell'aggiornamento versione 16.                                                                                                                                                                                                   |
| Membro del team di progetto     | Sì        | Sì        | Sì        | Per l'operazione di creazione, utilizza l'API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Sì        | Sì        |            | Le operazioni con i seguenti campi non sono supportate: : **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.                                                                                       |
| Elenchi di controllo del progetto      | Sì        | Sì        | Sì        |                                                                                                                                                                                                                                                                                                                                                         |
| Etichetta del progetto           | No         | Sì        | No         | I nomi delle etichette possono essere modificati. Questa funzionalità è disponibile solo per Project for the Web                                                                                                                                                                                                                                                                      |
| Relazione tra attività di progetto ed etichetta   | Sì        | No         | Sì        | Questa funzionalità è disponibile solo per Project for the Web                                                                                                                                                                                                                                                                                                  |
| Sprint di progetto          | Sì        | Sì        | Sì        | Il campo **Inizio** deve avere una data antecedente al campo **Fine**. Gli sprint per lo stesso progetto non possono sovrapporsi. Questa funzionalità è disponibile solo per Project for the Web                                                                                                                                                                    |




La proprietà ID è facoltativa. Se fornita, il sistema tenta di utilizzarla e genera un'eccezione se non può essere utilizzata. Se non è fornita, il sistema la genererà.

**Limitazioni e problemi noti**

Di seguito è riportato un elenco di limitazioni e problemi noti:

-   Le API di pianificazione del progetto possono essere utilizzate solo da **Utenti con licenza Microsoft Project**. Non possono essere utilizzate da:
    -   Utenti dell'applicazione
    -   Utenti di sistema
    -   Utenti integrazione
    -   Altri utenti che non dispongono della licenza richiesta
-   Ogni **OperationSet** può avere un massimo di 100 operazioni.
-   Ogni utente può avere un massimo di 10 **OperationSets** aperti.
-   Project Operations attualmente supporta un massimo di 500 attività totali in un progetto.
-   Ogni operazione di aggiornamento delle distribuzioni dell'assegnazione delle risorse conta come singola operazione.
-   Ogni elenco di distribuzioni aggiornate può contenere un massimo di 100 periodi di tempo.
-   Lo stato di errore e i registri degli errori di **OperationSet** non sono attualmente disponibili.
-   Possono esistere al massimo 400 sprint per progetto.
-   [Limiti e restrizioni per progetti e attività](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Le etichette sono attualmente disponibili solo per Project for the Web.

**Gestione errori**

-   Per rivedere gli errori generati dai set di operazioni, vai a **Impostazioni** \> **Pianifica integrazione** \> **Set di operazioni**.
-   Per rivedere gli errori generati dal servizio di pianificazione del progetto, vai a **Impostazioni** \> **Integrazione di pianificazione** \> **Registri errori PSS**.

**Modifica delle distribuzioni dell'assegnazione delle risorse**

A differenza di tutte le altre API di pianificazione di progetti che aggiornano un'entità, l'API di distribuzione dell'assegnazione delle risorse è l'unica responsabile degli aggiornamenti a un singolo campo, msdyn_plannedwork, in una singola entità, msydn_resourceassignment.

La modalità di pianificazione è:

-   **unità fisse**
-   calendario del progetto dalle 9 alle 17 PST, dal lunedì al venerdì (SALVO IL MERCOLEDÌ)
-   calendario delle risorse dalle 9 alle 13 PST, dal lunedì al venerdì

Questa assegnazione è per una settimana, quattro ore al giorno. Questo perché il calendario delle risorse è dalle 9 alle 13 PST o quattro ore al giorno.

| &nbsp;     | Attività | Data di inizio | Data finali  | Quantità | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Lavoratore 9-13 |  T1  | 13/6/2022  | 17/6/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Ad esempio, se vuoi che il lavoratore lavori solo tre ore al giorno questa settimana e dedichi un'ora ad altre attività.

#### <a name="updatedcontours-sample-payload"></a>Payload di esempio UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Questa è l'assegnazione dopo l'esecuzione dell'API di aggiornamento della pianificazione delle distribuzioni.

| &nbsp;     | Attività | Data di inizio | Data finali  | Quantità | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Lavoratore 9-13 | T1   | 13/6/2022  | 17/6/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Scenario di esempio**

In questo scenario, creerai un progetto, un membro del team, quattro attività e due assegnazioni delle risorse. Successivamente, aggiornerai un'attività e il progetto, eliminerai un'attività e un'assegnazione delle risorse e creerai una dipendenza attività.

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

** Ulteriori esempi

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
