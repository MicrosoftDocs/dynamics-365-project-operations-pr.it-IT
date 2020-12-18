---
title: Novità o modifiche nella versione di aggiornamento 26 di Project Service Automation V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643268"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="35522-102">Versione di aggiornamento di Project Service Automation 26, V3</span><span class="sxs-lookup"><span data-stu-id="35522-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="35522-103">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="35522-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="35522-104">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="35522-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="35522-105">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="35522-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="35522-106">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="35522-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="35522-107">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="35522-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="35522-108">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 26 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="35522-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="35522-109">Questa versione ha un numero di build di V3.10.44.59 ed è generalmente disponibile tramite un aggiornamento automatico a dicembre 2020.</span><span class="sxs-lookup"><span data-stu-id="35522-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="35522-110">Rilascio 26 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="35522-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="35522-111">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="35522-111">Bug fixes</span></span>

<span data-ttu-id="35522-112">**Ore e spesa**</span><span class="sxs-lookup"><span data-stu-id="35522-112">**Time and Expense**</span></span>

<span data-ttu-id="35522-113">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="35522-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="35522-114">Gli utenti possono modificare l'attività su una voce di tempo che è stata approvata/inviata.</span><span class="sxs-lookup"><span data-stu-id="35522-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="35522-115">Errore "Riferimento oggetto non impostato" durante il salvataggio dell'immissione dell'ora.</span><span class="sxs-lookup"><span data-stu-id="35522-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="35522-116">L'importazione dell'inserimento ore dalle assegnazioni di risorse crea voci di ora con i valori DateTime non corretti.</span><span class="sxs-lookup"><span data-stu-id="35522-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="35522-117">Quando sono installate le app Project Service Automation e Field Service, il pulsante **Nuovo** viene visualizzato due volte sulla barra dei comandi per le voci di tempo nell'app Field Service.</span><span class="sxs-lookup"><span data-stu-id="35522-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="35522-118">Gli aggiornamenti alle celle **Consenti unità** e **Gruppo unità** ora funzionano nella griglia **Stime di spesa**.</span><span class="sxs-lookup"><span data-stu-id="35522-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="35522-119">Il modulo **Aggiorna modifica inserimento orario** include la **Sequenza temporale**.</span><span class="sxs-lookup"><span data-stu-id="35522-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="35522-120">L'approvazione del tempo per voci di orario non di progetto blocca il sistema durante la ricerca di un ruolo di approvazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="35522-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="35522-121">**Gestione risorse**</span><span class="sxs-lookup"><span data-stu-id="35522-121">**Resource Management**</span></span>

<span data-ttu-id="35522-122">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="35522-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="35522-123">Aggiunta convalida nel plugin **PostProjectCreate** per verificare un requisito principale prima di crearne uno.</span><span class="sxs-lookup"><span data-stu-id="35522-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="35522-124">Il modulo di creazione rapida **Membro del team di progetto** genera un'eccezione di riferimento null se i campi vengono rimossi dal modulo.</span><span class="sxs-lookup"><span data-stu-id="35522-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="35522-125">La generazione di requisiti per 12 ore su 1 anno non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="35522-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="35522-126">Migliorata l'eccezione di riferimento null del messaggio di errore durante la creazione del requisito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35522-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="35522-127">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="35522-127">**Project Management**</span></span>

<span data-ttu-id="35522-128">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="35522-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="35522-129">Convalida migliorata per affrontare l'eccezione di riferimento null generata nelplugin **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="35522-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="35522-130">I progetti pubblicati dal componente aggiuntivo desktop di Microsoft Project eliminano le assegnazioni non assegnate.</span><span class="sxs-lookup"><span data-stu-id="35522-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="35522-131">Aggiunta una nuova convalida quando il riferimento al progetto di un'attività non è valido a causa di un'eccezione di riferimento null nel plugin **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="35522-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="35522-132">La griglia dei membri del team non mostra assegnazioni distinte nel record del membro del team.</span><span class="sxs-lookup"><span data-stu-id="35522-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="35522-133">Aggiunta nuova convalida e messaggi di errore a causa di un'eccezione di riferimento null nel plugin **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="35522-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="35522-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="35522-134">**Sales**</span></span>

<span data-ttu-id="35522-135">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="35522-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="35522-136">Quando si seleziona una riga basata su progetto nel preventivo o contratto, il pulsante **Suggerimento** dovrebbe essere visibile solo quando si seleziona una linea basata sul prodotto associata a un prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="35522-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="35522-137">Suddividi il privilegio **Create_Product** dal privilegio **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="35522-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="35522-138">L'eliminazione di una riga della fattura causa l'errore di riferimento null su **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="35522-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
