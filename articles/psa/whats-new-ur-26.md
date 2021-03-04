---
title: Novità o modifiche nella versione di aggiornamento 26 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 26 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143563"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="9c1cc-103">Versione di aggiornamento di Project Service Automation 26, V3</span><span class="sxs-lookup"><span data-stu-id="9c1cc-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9c1cc-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9c1cc-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9c1cc-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9c1cc-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9c1cc-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9c1cc-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9c1cc-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 26 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="9c1cc-110">Questa versione ha un numero di build di V3.10.44.59 ed è generalmente disponibile tramite un aggiornamento automatico a dicembre 2020.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="9c1cc-111">Rilascio 26 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9c1cc-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9c1cc-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="9c1cc-112">Bug fixes</span></span>

<span data-ttu-id="9c1cc-113">**Ore e spesa**</span><span class="sxs-lookup"><span data-stu-id="9c1cc-113">**Time and Expense**</span></span>

<span data-ttu-id="9c1cc-114">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="9c1cc-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c1cc-115">Gli utenti possono modificare l'attività su una voce di tempo che è stata approvata/inviata.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="9c1cc-116">Errore "Riferimento oggetto non impostato" durante il salvataggio dell'immissione dell'ora.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="9c1cc-117">L'importazione dell'inserimento ore dalle assegnazioni di risorse crea voci di ora con i valori DateTime non corretti.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="9c1cc-118">Quando sono installate le app Project Service Automation e Field Service, il pulsante **Nuovo** viene visualizzato due volte sulla barra dei comandi per le voci di tempo nell'app Field Service.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="9c1cc-119">Gli aggiornamenti alle celle **Consenti unità** e **Gruppo unità** ora funzionano nella griglia **Stime di spesa**.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="9c1cc-120">Il modulo **Aggiorna modifica inserimento orario** include la **Sequenza temporale**.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="9c1cc-121">L'approvazione del tempo per voci di orario non di progetto blocca il sistema durante la ricerca di un ruolo di approvazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="9c1cc-122">**Gestione risorse**</span><span class="sxs-lookup"><span data-stu-id="9c1cc-122">**Resource Management**</span></span>

<span data-ttu-id="9c1cc-123">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="9c1cc-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c1cc-124">Aggiunta convalida nel plugin **PostProjectCreate** per verificare un requisito principale prima di crearne uno.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="9c1cc-125">Il modulo di creazione rapida **Membro del team di progetto** genera un'eccezione di riferimento null se i campi vengono rimossi dal modulo.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="9c1cc-126">La generazione di requisiti per 12 ore su 1 anno non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="9c1cc-127">Migliorata l'eccezione di riferimento null del messaggio di errore durante la creazione del requisito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="9c1cc-128">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="9c1cc-128">**Project Management**</span></span>

<span data-ttu-id="9c1cc-129">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="9c1cc-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c1cc-130">Convalida migliorata per affrontare l'eccezione di riferimento null generata nelplugin **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="9c1cc-131">I progetti pubblicati dal componente aggiuntivo desktop di Microsoft Project eliminano le assegnazioni non assegnate.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="9c1cc-132">Aggiunta una nuova convalida quando il riferimento al progetto di un'attività non è valido a causa di un'eccezione di riferimento null nel plugin **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="9c1cc-133">La griglia dei membri del team non mostra assegnazioni distinte nel record del membro del team.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="9c1cc-134">Aggiunta nuova convalida e messaggi di errore a causa di un'eccezione di riferimento null nel plugin **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="9c1cc-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9c1cc-135">**Sales**</span></span>

<span data-ttu-id="9c1cc-136">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="9c1cc-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c1cc-137">Quando si seleziona una riga basata su progetto nel preventivo o contratto, il pulsante **Suggerimento** dovrebbe essere visibile solo quando si seleziona una linea basata sul prodotto associata a un prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="9c1cc-138">Suddividi il privilegio **Create_Product** dal privilegio **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="9c1cc-139">L'eliminazione di una riga della fattura causa l'errore di riferimento null su **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="9c1cc-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>