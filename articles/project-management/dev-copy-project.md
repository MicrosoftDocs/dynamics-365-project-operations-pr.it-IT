---
title: Sviluppare i modelli di progetto con Copia progetto
description: Questo argomento fornisce informazioni su come creare modelli di progetto utilizzando l'azione personalizzata Copia progetto.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 27847575e2d6ec9af77d24f756b13d3aeb0efea7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286928"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="264c9-103">Sviluppare i modelli di progetto con Copia progetto</span><span class="sxs-lookup"><span data-stu-id="264c9-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="264c9-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="264c9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="264c9-105">Dynamics 365 Project Operations supporta la capacità di copiare un progetto e ripristinare eventuali assegnazioni alle risorse generiche che ne rappresentano il ruolo.</span><span class="sxs-lookup"><span data-stu-id="264c9-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="264c9-106">I clienti possono utilizzare questa funzionalità per creare modelli di progetto di base.</span><span class="sxs-lookup"><span data-stu-id="264c9-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="264c9-107">Quando selezioni **Copia progetto**, lo stato del progetto di destinazione viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="264c9-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="264c9-108">Usa il **motivo stato** per determinare quando l'azione di copia è stata completata.</span><span class="sxs-lookup"><span data-stu-id="264c9-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="264c9-109">La selezione di **Copia progetto** aggiorna anche la data di inizio del progetto sulla data di inizio corrente se non viene rilevata alcuna data di destinazione nell'entità del progetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="264c9-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="264c9-110">Azione personalizzata Copia progetto</span><span class="sxs-lookup"><span data-stu-id="264c9-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="264c9-111">Nome</span><span class="sxs-lookup"><span data-stu-id="264c9-111">Name</span></span> 

<span data-ttu-id="264c9-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="264c9-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="264c9-113">Parametri di input</span><span class="sxs-lookup"><span data-stu-id="264c9-113">Input parameters</span></span>
<span data-ttu-id="264c9-114">Sono presenti tre parametri di input:</span><span class="sxs-lookup"><span data-stu-id="264c9-114">There are three input parameters:</span></span>

| <span data-ttu-id="264c9-115">Parametro</span><span class="sxs-lookup"><span data-stu-id="264c9-115">Parameter</span></span>          | <span data-ttu-id="264c9-116">Digita</span><span class="sxs-lookup"><span data-stu-id="264c9-116">Type</span></span>   | <span data-ttu-id="264c9-117">Valori</span><span class="sxs-lookup"><span data-stu-id="264c9-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="264c9-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="264c9-118">ProjectCopyOption</span></span>  | <span data-ttu-id="264c9-119">Stringa</span><span class="sxs-lookup"><span data-stu-id="264c9-119">String</span></span> | <span data-ttu-id="264c9-120">**{"removeNamedResources":true}** o **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="264c9-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="264c9-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="264c9-121">SourceProject</span></span>      | <span data-ttu-id="264c9-122">Riferimento entità</span><span class="sxs-lookup"><span data-stu-id="264c9-122">Entity Reference</span></span> | <span data-ttu-id="264c9-123">Progetto di origine</span><span class="sxs-lookup"><span data-stu-id="264c9-123">Source Project</span></span> |
| <span data-ttu-id="264c9-124">Destinazione</span><span class="sxs-lookup"><span data-stu-id="264c9-124">Target</span></span>             | <span data-ttu-id="264c9-125">Riferimento entità</span><span class="sxs-lookup"><span data-stu-id="264c9-125">Entity Reference</span></span> | <span data-ttu-id="264c9-126">Progetto di destinazione</span><span class="sxs-lookup"><span data-stu-id="264c9-126">Target Project</span></span> |


- <span data-ttu-id="264c9-127">**{"clearTeamsAndAssignments":true}**: il comportamento predefinito di Project per il Web e rimuove tutte le assegnazioni e i membri del team.</span><span class="sxs-lookup"><span data-stu-id="264c9-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="264c9-128">**{"removeNamedResources":true}**: il comportamento predefinito di Project Operations e ripristina le assegnazioni a risorse generiche.</span><span class="sxs-lookup"><span data-stu-id="264c9-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="264c9-129">Per ulteriori valori predefiniti delle azioni, vedi [Usare le azioni API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="264c9-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="264c9-130">Specificare i campi da copiare</span><span class="sxs-lookup"><span data-stu-id="264c9-130">Specify fields to copy</span></span> 
<span data-ttu-id="264c9-131">Quando l'azione viene chiamata, **Copia progetto** guarda la vista del progetto **Copia colonne di progetto** per determinare quali campi copiare quando il progetto viene copiato.</span><span class="sxs-lookup"><span data-stu-id="264c9-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="264c9-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="264c9-132">Example</span></span>
<span data-ttu-id="264c9-133">L'esempio seguente mostra come chiamare l'azione personalizzata **CopyProject** con il set di parametri **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="264c9-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]