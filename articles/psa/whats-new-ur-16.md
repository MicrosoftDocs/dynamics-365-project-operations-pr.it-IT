---
title: Novità o modifiche nella versione di aggiornamento 16 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 16 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 5d4851ed27028117d25efb0610c25a5aac9c8b70
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006786"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="626cc-103">Versione di aggiornamento di Project Service Automation 16, V3</span><span class="sxs-lookup"><span data-stu-id="626cc-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="626cc-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="626cc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="626cc-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="626cc-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="626cc-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="626cc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="626cc-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="626cc-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="626cc-108">Per ulteriori informazioni, vedi [Installare o aggiornare una soluzione preferita](/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="626cc-108">For more information, see [Install, Update a Preferred Solution](/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="626cc-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 16 di PSA V3.</span><span class="sxs-lookup"><span data-stu-id="626cc-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="626cc-110">Questa versione ha il numero di build V3.10.6.34 ed è generalmente disponibile tramite un aggiornamento automatico in gennaio 2020.</span><span class="sxs-lookup"><span data-stu-id="626cc-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="626cc-111">Rilascio 16 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="626cc-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="626cc-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="626cc-112">Bug fixes</span></span>

-   <span data-ttu-id="626cc-113">Tempo e spesa</span><span class="sxs-lookup"><span data-stu-id="626cc-113">Time and Expense</span></span>

    -   <span data-ttu-id="626cc-114">Risolto: gli utenti che tentano di inviare voci di spesa e inserimenti ore eliminati per le approvazioni riceveranno ora messaggi di errore rilevanti.</span><span class="sxs-lookup"><span data-stu-id="626cc-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="626cc-115">Gestione progetti</span><span class="sxs-lookup"><span data-stu-id="626cc-115">Project Management</span></span>

    -   <span data-ttu-id="626cc-116">Risolto: le unità gestione risorse definite per i membri del team nei modelli sono rispettate con i modelli applicati a un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="626cc-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="626cc-117">Risolto: gestione migliorata della riassegnazione della proprietà dei record.</span><span class="sxs-lookup"><span data-stu-id="626cc-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="626cc-118">Risolto: i progetti in fase di copia non potranno essere copiati fino al completamento di tutte le operazioni di copia.</span><span class="sxs-lookup"><span data-stu-id="626cc-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="626cc-119">Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="626cc-119">Resource Management</span></span>

    -   <span data-ttu-id="626cc-120">Risolto: l'estensione delle prenotazioni gestiscono ora correttamente le durate brevi e non creano più valori pari a 0 (zero) ore per le prenotazioni estese.</span><span class="sxs-lookup"><span data-stu-id="626cc-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="626cc-121">Risolto: la visualizzazione della riconciliazione è ora soggetta a rendering quando il fuso orario del progetto è +5:30 GMT e l'ora dell'utente è diversa.</span><span class="sxs-lookup"><span data-stu-id="626cc-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="626cc-122">Sales</span><span class="sxs-lookup"><span data-stu-id="626cc-122">Sales</span></span>

    -   <span data-ttu-id="626cc-123">Risolto: quando un progetto mappato a una voce di contratto veniva rimosso e veniva mappato un nuovo progetto, i record effettivi sul nuovo progetto non venivano rivalutati in base alle regole di fatturazione e determinazione dei prezzi definite nella voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="626cc-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="626cc-124">Questo problema è stato risolto in questa versione.</span><span class="sxs-lookup"><span data-stu-id="626cc-124">This has been fixed in this release.</span></span> <span data-ttu-id="626cc-125">Prezzi e record effettivi sul nuovo progetto mappato verranno annullati e ricreati correttamente in base alle regole di fatturazione e determinazione dei prezzi della voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="626cc-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="626cc-126">Anche i record effettivi del progetto non mappato verranno rivalutati e ricreati di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="626cc-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="626cc-127">Risolto: è stata aggiunta un'ulteriore convalida al campo **Quantità** di un riga di stima per garantire che i valori null non siano persistenti.</span><span class="sxs-lookup"><span data-stu-id="626cc-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="626cc-128">Risolto: quando sono stati aggiornati i valori effettivi su un progetto, è stato aggiunto un pulsante di aggiornamento al modulo principale del progetto per consentire agli utenti di risincronizzare i valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="626cc-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="626cc-129">Risolto: quando gli utenti eseguono l'aggiornamento da 2.X a 3.X, saranno consentiti progetti con un valore NULL per il nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="626cc-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]