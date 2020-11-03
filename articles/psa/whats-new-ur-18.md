---
title: Novità o modifiche nella versione di aggiornamento 18 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 18 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078830"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="559c4-103">Versione di aggiornamento di Project Service Automation 18, V3</span><span class="sxs-lookup"><span data-stu-id="559c4-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="559c4-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="559c4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="559c4-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="559c4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="559c4-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="559c4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="559c4-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="559c4-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="559c4-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="559c4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="559c4-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 18 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="559c4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="559c4-110">Questa versione ha il numero di build V3.10.8.12 ed è generalmente disponibile tramite un aggiornamento automatico nell'aprile 2020.</span><span class="sxs-lookup"><span data-stu-id="559c4-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="559c4-111">Rilascio 18 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="559c4-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="559c4-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="559c4-112">Bug fixes</span></span>

<span data-ttu-id="559c4-113">**Tempo e spesa**</span><span class="sxs-lookup"><span data-stu-id="559c4-113">**Time and Expense**</span></span>

- <span data-ttu-id="559c4-114">Corretto: i flussi **Richiama** , **Richiesta** e **Annulla approvazione** generano eccezioni con messaggi di errore poco chiari.</span><span class="sxs-lookup"><span data-stu-id="559c4-114">Fixed: **Recall** , **Request** , and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="559c4-115">Corretto: quando **Annulla approvazione** non riesce per una spesa, non viene generato un errore di eccezione rilevante.</span><span class="sxs-lookup"><span data-stu-id="559c4-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="559c4-116">Corretto: la griglia di inserimento dell'ora gestisce erroneamente i giorni non lavorativi in Australia dopo il cambio dell'ora legale (DST) in ottobre.</span><span class="sxs-lookup"><span data-stu-id="559c4-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="559c4-117">Corretto: una logica predefinita errata impedisce l'invio delle spese.</span><span class="sxs-lookup"><span data-stu-id="559c4-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="559c4-118">Corretto: quando l'approvazione dell'immissione del tempo non riesce, l'approvazione rimane nello stato **In sospeso**.</span><span class="sxs-lookup"><span data-stu-id="559c4-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="559c4-119">Corretto: errori SQL nelle approvazioni in blocco (deadlock/timeout).</span><span class="sxs-lookup"><span data-stu-id="559c4-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="559c4-120">Corretto: problemi significativi relativi alle prestazioni nell'esperienza utente causati dall'aggiornamento dei membri del team durante l'approvazione delle immissioni del tempo.</span><span class="sxs-lookup"><span data-stu-id="559c4-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="559c4-121">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="559c4-121">**Project Management**</span></span>

- <span data-ttu-id="559c4-122">Corretto: notifica del fuso orario spostata dalla visualizzazione **Riconciliazione** al modulo principale **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="559c4-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="559c4-123">Corretto: il modello di calendario non è correttamente predefinito quando si apre un nuovo modulo di progetto.</span><span class="sxs-lookup"><span data-stu-id="559c4-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="559c4-124">Corretto: per i browser basati su Cromo, gli utenti non sono in grado di selezionare facilmente le attività precedenti da eliminare.</span><span class="sxs-lookup"><span data-stu-id="559c4-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="559c4-125">Corretto: la creazione o la copia di un **progetto da modello vuoto** recupera assegnazioni non correlate.</span><span class="sxs-lookup"><span data-stu-id="559c4-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="559c4-126">Corretto: in casi limite specifici, la creazione di una nuova assegnazione dalla griglia delle attività comporta la creazione di record duplicati.</span><span class="sxs-lookup"><span data-stu-id="559c4-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="559c4-127">Corretto: in modalità manuale, gli utenti non sono in grado di aggiornare le date di inizio dell'attività in modo che siano successive alla data corrente salvata.</span><span class="sxs-lookup"><span data-stu-id="559c4-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="559c4-128">**Gestione risorse**</span><span class="sxs-lookup"><span data-stu-id="559c4-128">**Resource Management**</span></span>

- <span data-ttu-id="559c4-129">Corretto: la riga del totale parziale della visualizzazione **Riconciliazione** calcola erroneamente la varianza delle prenotazioni dopo l'estensione delle prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="559c4-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="559c4-130">Corretto: la visualizzazione **Riconciliazione** visualizza erroneamente le assegnazioni delle risorse quando la risorsa prenotabile ha un calendario che non corrisponde al calendario del progetto.</span><span class="sxs-lookup"><span data-stu-id="559c4-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="559c4-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="559c4-131">**Sales**</span></span>

- <span data-ttu-id="559c4-132">Corretto: quando le immissioni del tempo sono state nuovamente approvate ( **Approva > Annulla >** approva di nuovo), viene creato un duplicato non addebitabile effettivo.</span><span class="sxs-lookup"><span data-stu-id="559c4-132">Fixed: When time entries are re-approved ( **Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
