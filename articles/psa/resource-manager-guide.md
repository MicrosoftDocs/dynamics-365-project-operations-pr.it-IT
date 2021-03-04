---
title: Guida di Resource Manager
description: Guida alla gestione delle risorse in Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 543be23d95b1b821fcdca628612d03c343fd5b06
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147343"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="bdd17-103">Guida di resource manager (Project Service)</span><span class="sxs-lookup"><span data-stu-id="bdd17-103">Resource manager guide (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="bdd17-104">Le funzionalità di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] consentono di trovare le risorse esatte nel momento giusto per il progetto giusto e verificano che tutte le risorse vengano utilizzate in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="bdd17-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="bdd17-105">Distribuire i consulenti della società in modo efficiente con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="bdd17-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="bdd17-106">Queste forniscono gli strumenti necessari per pianificare le risorse in base ai requisiti e alle pianificazioni dei progetti di consulenza e alle competenze e la disponibilità dei consulenti.</span><span class="sxs-lookup"><span data-stu-id="bdd17-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="bdd17-107">Puoi trovare rapidamente i consulenti più qualificati disponibili a lavorare sui progetti e puoi facilmente vedere come migliorarne la pianificazione durante ogni progetto.</span><span class="sxs-lookup"><span data-stu-id="bdd17-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="bdd17-108">La pianificazione delle risorse consente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="bdd17-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="bdd17-109">La corrispondenza delle risorse ai progetti, in base a come i livelli di competenze e di preparazione soddisfano i requisiti della risorsa di progetto.</span><span class="sxs-lookup"><span data-stu-id="bdd17-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="bdd17-110">La corrispondenza di una pianificazione della risorsa a un calendario di progetto, in base alla disponibilità e all'indisponibilità pianificata.</span><span class="sxs-lookup"><span data-stu-id="bdd17-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="bdd17-111">Il calendario contrassegnato dal colore offre segnali visivi di disponibilità della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bdd17-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="bdd17-112">Rivedi la capacità di ogni consulente e determina come viene al momento utilizzata tale capacità.</span><span class="sxs-lookup"><span data-stu-id="bdd17-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="bdd17-113">Ciò può consentire di identificare in quale posizione un consulente è poco o troppo utilizzato, o se sta lavorando in base alla sua capacità.</span><span class="sxs-lookup"><span data-stu-id="bdd17-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="bdd17-114">Assegna una percentuale o un numero specifico di ore a un progetto in base alla capacità del lavoratore .</span><span class="sxs-lookup"><span data-stu-id="bdd17-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="bdd17-115">Effettua prenotazioni risorse di gruppo.</span><span class="sxs-lookup"><span data-stu-id="bdd17-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="bdd17-116">Prenota provvisoriamente o definitivamente le risorse, e converti le ore programmate provvisoriamente in ore programmate definitivamente in un solo passaggio.</span><span class="sxs-lookup"><span data-stu-id="bdd17-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="bdd17-117">Forma automaticamente un team di progetto in base alle risorse definite in una struttura di suddivisione del lavoro per un progetto.</span><span class="sxs-lookup"><span data-stu-id="bdd17-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="bdd17-118">Evadi le richieste di risorse (prenota, proponi, cerca risorse sostitutive).</span><span class="sxs-lookup"><span data-stu-id="bdd17-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="bdd17-119">Assegna le risorse in base a un modello centrale (assegnazioni gestore risorse) o ibrido (possono assegnare il gestore risorse e gli altri gestori).</span><span class="sxs-lookup"><span data-stu-id="bdd17-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="bdd17-120">Per ulteriori informazioni sull'impostazione di un modello di gestione delle risorse centrale rispetto a un modello ibrido, vedere [Configurare le impostazioni dei parametri aggiuntivi (Project Service)](../psa/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="bdd17-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="bdd17-121">Puoi gestire le risorse in modo efficiente nei progetti e garantire che i progetti siano destinati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="bdd17-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="bdd17-122">Dovrai eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="bdd17-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="bdd17-123">[Gestire richieste risorse](../psa/manage-resource-requests.md)</span><span class="sxs-lookup"><span data-stu-id="bdd17-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="bdd17-124">Fai corrispondere le competenze e le capacità dei consulenti ai progetti corretti.</span><span class="sxs-lookup"><span data-stu-id="bdd17-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="bdd17-125">[Visualizzare la disponibilità delle risorse](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="bdd17-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="bdd17-126">Controlla la disponibilità dei consulenti in una visualizzazione del Calendario.</span><span class="sxs-lookup"><span data-stu-id="bdd17-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="bdd17-127">[Visualizzare l'utilizzo delle risorse](../psa/view-resource-utilization.md)</span><span class="sxs-lookup"><span data-stu-id="bdd17-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="bdd17-128">Vedi la percentuale di tempo per cui sono prenotati i tuoi consulenti.</span><span class="sxs-lookup"><span data-stu-id="bdd17-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="bdd17-129">[Pianificare le risorse per un progetto](../psa/schedule-resources-project.md)</span><span class="sxs-lookup"><span data-stu-id="bdd17-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="bdd17-130">Pianifica i consulenti per un progetto.</span><span class="sxs-lookup"><span data-stu-id="bdd17-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="bdd17-131">Per ulteriori informazioni sull'invio delle richieste di risorsa per singoli progetti, vedi [Inviare richieste di risorse](../psa/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="bdd17-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="bdd17-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdd17-132">See Also</span></span>  
 <span data-ttu-id="bdd17-133">[Panoramica di Project Service](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="bdd17-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="bdd17-134">[Guida dell'amministratore](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="bdd17-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="bdd17-135">[Guida per la gestione dell'account](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="bdd17-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="bdd17-136">[Guida del responsabile di progetto](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="bdd17-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="bdd17-137">Guida per tempo, spese e collaborazione</span><span class="sxs-lookup"><span data-stu-id="bdd17-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
