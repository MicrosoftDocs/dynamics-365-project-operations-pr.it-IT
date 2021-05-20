---
title: Novità o modifiche nella versione di aggiornamento 21 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 21 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: ad44f6747486222cc1f48c7b645f2525d382dca3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949054"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="20da5-103">Versione di aggiornamento di Project Service Automation 21, V3</span><span class="sxs-lookup"><span data-stu-id="20da5-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="20da5-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="20da5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="20da5-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="20da5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="20da5-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="20da5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="20da5-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="20da5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="20da5-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="20da5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="20da5-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 21 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="20da5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="20da5-110">Questa versione ha il numero di build V 3.10.32.50 ed è generalmente disponibile tramite un aggiornamento automatico a giugno 2020.</span><span class="sxs-lookup"><span data-stu-id="20da5-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="20da5-111">Rilascio 21 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="20da5-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="20da5-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="20da5-112">Bug fixes</span></span>

<span data-ttu-id="20da5-113">**Tempo e spesa**</span><span class="sxs-lookup"><span data-stu-id="20da5-113">**Time and Expense**</span></span>

<span data-ttu-id="20da5-114">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="20da5-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="20da5-115">Quando si ospita il **controllo Griglia inserimento ore** nei dashboard, la griglia non utilizza l'intera larghezza del contenitore della griglia del dashboard.</span><span class="sxs-lookup"><span data-stu-id="20da5-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="20da5-116">Per fusi orari specifici, il controllo della griglia **inserimento ore** non visualizza i record.</span><span class="sxs-lookup"><span data-stu-id="20da5-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="20da5-117">Gli inserimenti ore successivi alle 21:00 vengono visualizzati nel giorno sbagliato.</span><span class="sxs-lookup"><span data-stu-id="20da5-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="20da5-118">Gli utenti non possono inviare le spese se la categoria di spesa, **Ricevuta spesa obbligatoria** non ha valore.</span><span class="sxs-lookup"><span data-stu-id="20da5-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="20da5-119">**Gestione risorse**</span><span class="sxs-lookup"><span data-stu-id="20da5-119">**Resource Management**</span></span>

<span data-ttu-id="20da5-120">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="20da5-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="20da5-121">Le prenotazioni inattive vengono visualizzate nella visualizzazione **Riconciliazione**.</span><span class="sxs-lookup"><span data-stu-id="20da5-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="20da5-122">Nell'evasione di risorse generiche manca la convalida per garantire la presenza di uno stato di prenotazione valido.</span><span class="sxs-lookup"><span data-stu-id="20da5-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="20da5-123">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="20da5-123">**Project Management**</span></span>

<span data-ttu-id="20da5-124">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="20da5-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="20da5-125">Le griglie del modulo **Progetto** (**Assegnazione risorse**, **Attività**, visualizzazione **Riconciliazione**, **Stime di spesa**) rimangono modificabili anche quando un progetto non è attivo.</span><span class="sxs-lookup"><span data-stu-id="20da5-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="20da5-126">I clienti duplicati non possono essere uniti a clienti collegati a contratti di progetto confermati.</span><span class="sxs-lookup"><span data-stu-id="20da5-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="20da5-127">Quando viene aggiunta una risorsa che non dispone di un calendario valido, il sistema non restituisce un messaggio di errore descrittivo.</span><span class="sxs-lookup"><span data-stu-id="20da5-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="20da5-128">Il pulsante **Aggiungi attività** sulla griglia delle attività è abilitato quando il progetto è collegato al **componente aggiuntivo Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="20da5-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="20da5-129">L'impegno cresce in modo incontrollabile quando un'attività con una categoria viene assegnata a una risorsa con un ruolo per il quale è stato definito un prezzo di costo.</span><span class="sxs-lookup"><span data-stu-id="20da5-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="20da5-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="20da5-130">**Sales**</span></span>

<span data-ttu-id="20da5-131">Sono stati apportati i seguenti miglioramenti:</span><span class="sxs-lookup"><span data-stu-id="20da5-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="20da5-132">**Frequenza di fatturazione** e **Inizio fatturazione** sono stati spostati nella scheda **Pianificazione fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="20da5-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="20da5-133">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="20da5-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="20da5-134">**Prezzo di vendita totale** è zero (0) per **Categoria** nonostante **Ruolo** abbia un prezzo di vendita totale diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="20da5-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="20da5-135">I clienti non possono modificare il valore del campo **Stato fattura** in **Pronto per la fatturazione** quando un altro processo personalizzato aggiorna un campo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="20da5-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="20da5-136">Il pulsante **Aggiorna righe fattura** può creare più righe duplicate se viene selezionato ripetutamente.</span><span class="sxs-lookup"><span data-stu-id="20da5-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="20da5-137">Il pulsante **Aggiorna prezzi** non funziona nella griglia secondaria **Prezzi ruolo** del modulo di **visualizzazione rapida**.</span><span class="sxs-lookup"><span data-stu-id="20da5-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="20da5-138">La logica **Risoluzione listino prezzi di vendita** gestisce in modo inaccurato i fusi orari, determinando una selezione errata dei listini prezzi.</span><span class="sxs-lookup"><span data-stu-id="20da5-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="20da5-139">Il **costo effettivo totale** di un progetto può essere disattivato di un importo in frazione dopo l'approvazione di una singola voce.</span><span class="sxs-lookup"><span data-stu-id="20da5-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="20da5-140">La logica **Risoluzione prezzi** non fornisce un messaggio di errore descrittivo se **RolePrice recuperato** non ha valori nei campi **"Unità primaria"** e **"Prezzo in unità primaria"**.</span><span class="sxs-lookup"><span data-stu-id="20da5-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]