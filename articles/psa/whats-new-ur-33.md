---
title: Novità o modifiche nella versione di aggiornamento 33 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 33 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334557"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="e1a77-103">Novità o modifiche nella versione di aggiornamento 33 di Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="e1a77-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e1a77-104">Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e1a77-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="e1a77-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="e1a77-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e1a77-106">È compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e1a77-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e1a77-107">Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e1a77-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="e1a77-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e1a77-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e1a77-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 33 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="e1a77-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="e1a77-110">Questa versione ha il numero di build V3.10.54.98 ed è generalmente disponibile tramite un aggiornamento automatico di luglio 2021.</span><span class="sxs-lookup"><span data-stu-id="e1a77-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="e1a77-111">Rilascio 33 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e1a77-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e1a77-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="e1a77-112">Bug fixes</span></span>

<span data-ttu-id="e1a77-113">**Ore e spesa**</span><span class="sxs-lookup"><span data-stu-id="e1a77-113">**Time and Expense**</span></span>

<span data-ttu-id="e1a77-114">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="e1a77-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e1a77-115">Due campi bloccati, **msdyn_description** e **msdyn_externaldescription** sono modificabili dopo l'invio.</span><span class="sxs-lookup"><span data-stu-id="e1a77-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="e1a77-116">Viene visualizzato un messaggio di errore se viene creata una spesa non correlata a un progetto.</span><span class="sxs-lookup"><span data-stu-id="e1a77-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="e1a77-117">Quando viene creato un inserimento ore, per impostazione predefinita il ruolo della risorsa viene impostato su un ruolo inattivo.</span><span class="sxs-lookup"><span data-stu-id="e1a77-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="e1a77-118">Le righe del giornale di registrazione associate a una spesa richiamata ed eliminata non vengono eliminate.</span><span class="sxs-lookup"><span data-stu-id="e1a77-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="e1a77-119">Nel **Modulo di creazione rapida inserimento ore**, aggiorna la vista **Elenco attività di progetto** per modificare la data visualizzata per impostazione predefinita con la data di inizio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e1a77-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="e1a77-120">Quando crei un inserimento ore dalla scheda **Correlato** della risorsa prenotabile, l'inserimento ore viene creato in modo errato per l'utente che ha eseguito l'accesso anziché per la risorsa prenotabile padre.</span><span class="sxs-lookup"><span data-stu-id="e1a77-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="e1a77-121">Nuovi campi sono stati aggiunti alla finestra di dialogo **Approvazione in blocco MDD**.</span><span class="sxs-lookup"><span data-stu-id="e1a77-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="e1a77-122">**Pianificazione di un progetto**</span><span class="sxs-lookup"><span data-stu-id="e1a77-122">**Project planning**</span></span>

<span data-ttu-id="e1a77-123">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="e1a77-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="e1a77-124">Prestazioni lente nella creazione del progetto quando i modelli di ore di lavoro del progetto vengono applicati con calendari complessi.</span><span class="sxs-lookup"><span data-stu-id="e1a77-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="e1a77-125">Quando la data di inizio è successiva alla data di fine, viene visualizzato un errore sul modello del progetto di copia a causa delle differenze nel componente temporale di ciascun campo.</span><span class="sxs-lookup"><span data-stu-id="e1a77-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="e1a77-126">**Gestione delle risorse**</span><span class="sxs-lookup"><span data-stu-id="e1a77-126">**Resource management**</span></span>

<span data-ttu-id="e1a77-127">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="e1a77-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="e1a77-128">Viene utilizzato un parametro errato nella query sull'utilizzo delle risorse e l'XML porta a risultati di filtro errati nella griglia **Utilizzo delle risorse**.</span><span class="sxs-lookup"><span data-stu-id="e1a77-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="e1a77-129">La **Conferma estensione prenotazioni** mostra una data di fine errata per le prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="e1a77-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="e1a77-130">**Vendite**</span><span class="sxs-lookup"><span data-stu-id="e1a77-130">**Sales**</span></span>

<span data-ttu-id="e1a77-131">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="e1a77-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="e1a77-132">Viene visualizzato un messaggio di errore se viene creato un prezzo di categoria con valori mancanti.</span><span class="sxs-lookup"><span data-stu-id="e1a77-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="e1a77-133">Viene visualizzato un messaggio di errore se viene creato un passaggio fondamentale della voce di contratto senza una riga d'ordine.</span><span class="sxs-lookup"><span data-stu-id="e1a77-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
