---
title: Novità o modifiche nella versione di aggiornamento 24 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 24 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c789a65f1996d082410b3d8dd9e76e5065e708a2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280493"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="82195-103">Versione di aggiornamento di Project Service Automation 24, V3</span><span class="sxs-lookup"><span data-stu-id="82195-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="82195-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="82195-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="82195-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="82195-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="82195-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="82195-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="82195-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="82195-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="82195-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="82195-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="82195-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 24 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="82195-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="82195-110">Questa versione ha il numero di build V 3.10.42.43 ed è generalmente disponibile tramite un aggiornamento automatico in ottobre 2020</span><span class="sxs-lookup"><span data-stu-id="82195-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="82195-111">Rilascio 24 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="82195-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="82195-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="82195-112">Bug fixes</span></span>

<span data-ttu-id="82195-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="82195-113">**Sales**</span></span>

<span data-ttu-id="82195-114">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="82195-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="82195-115">Problema durante l'impostazione del listino prezzi predefinito dei prodotti.</span><span class="sxs-lookup"><span data-stu-id="82195-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="82195-116">Le prestazioni della conclusione dell'offerta sono lente a causa del listino prezzi incorporato e della copia dei record dei prezzi del ruolo.</span><span class="sxs-lookup"><span data-stu-id="82195-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="82195-117">**Contratto di progetto/Hub di vendita** > **Voce prodotto/Quantità riga ordine** viene automaticamente arrotondato al numero intero più vicino.</span><span class="sxs-lookup"><span data-stu-id="82195-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="82195-118">Eleva i privilegi di sistema durante la lettura dei listini prezzi.</span><span class="sxs-lookup"><span data-stu-id="82195-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="82195-119">Copia i campi dell'indirizzo del cliente **address1_freighttermscode** e **address1_shippingmethodcode** per Offerta/Ordine.</span><span class="sxs-lookup"><span data-stu-id="82195-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="82195-120">**Tempo e spesa**</span><span class="sxs-lookup"><span data-stu-id="82195-120">**Time and Expense**</span></span>

<span data-ttu-id="82195-121">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="82195-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="82195-122">La **Griglia di inserimento ore** non supporta il comportamento dell'ora **Solo data**.</span><span class="sxs-lookup"><span data-stu-id="82195-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="82195-123">**Inserimento ore** non si aggiorna automaticamente.</span><span class="sxs-lookup"><span data-stu-id="82195-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="82195-124">È richiesto un aggiornamento manuale.</span><span class="sxs-lookup"><span data-stu-id="82195-124">A manual refresh is required.</span></span>
- <span data-ttu-id="82195-125">Impossibile importare gli inserimenti ore da un'assegnazione quando c'è un'interruzione (0 ore) nelle assegnazioni di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="82195-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="82195-126">Quando si crea un inserimento ore, imposta l'inizio come **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="82195-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="82195-127">Riabilita la modifica di massa per l'inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="82195-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="82195-128">**Gestione risorse**</span><span class="sxs-lookup"><span data-stu-id="82195-128">**Resource Management**</span></span>

<span data-ttu-id="82195-129">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="82195-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="82195-130">Il tentativo di aggiornare lo stato di una prenotazione giornaliera senza un requisito genera un'eccezione null-ref.</span><span class="sxs-lookup"><span data-stu-id="82195-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="82195-131">Errore durante il caricamento della **Visualizzazione riconciliazione**.</span><span class="sxs-lookup"><span data-stu-id="82195-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="82195-132">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="82195-132">**Project Management**</span></span>

<span data-ttu-id="82195-133">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="82195-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="82195-134">In **Pianificazione di progetti**, quando si passa da **Manuale** ad **Automatico**, il salvataggio automatico non viene completato.</span><span class="sxs-lookup"><span data-stu-id="82195-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="82195-135">I costi di spesa non devono essere calcolati per la varianza nella **Griglia di registrazione di progetto**.</span><span class="sxs-lookup"><span data-stu-id="82195-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="82195-136">Comportamento incoerente per le colonne **Tag delle stime** durante il caricamento rispetto alla modifica del tipo **Scala cronologica**.</span><span class="sxs-lookup"><span data-stu-id="82195-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="82195-137">Il costo effettivo di un progetto potrebbe non riflettere i totali di **Valori effettivi**.</span><span class="sxs-lookup"><span data-stu-id="82195-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="82195-138">**Data di fine prevista** nella scheda **Riepilogo** non corrisponde a **Pianificazione WBS**.</span><span class="sxs-lookup"><span data-stu-id="82195-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="82195-139">**Aggiorna ore effettive** su rientro negativo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="82195-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="82195-140">Un project manager esterno alla **BU** radice non può creare un progetto.</span><span class="sxs-lookup"><span data-stu-id="82195-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="82195-141">Le modifiche all'attività o alla categoria in **Stime di spesa** non sono persistenti.</span><span class="sxs-lookup"><span data-stu-id="82195-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="82195-142">**Copia del contratto** copia le pianificazioni fatture e lo stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="82195-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="82195-143">Il pulsante **Aggiorna valori effettivi** calcola in modo errato le attività di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="82195-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="82195-144">Componente aggiuntivo Microsoft Project: corregge l'errore di riferimento nullo se un membro del team dispone di un'unità di di gestione risorse vuota.</span><span class="sxs-lookup"><span data-stu-id="82195-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]