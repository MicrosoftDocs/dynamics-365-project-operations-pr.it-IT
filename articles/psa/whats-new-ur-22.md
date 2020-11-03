---
title: Novità o modifiche nella versione di aggiornamento 22 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 22 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078824"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="7b786-103">Versione di aggiornamento di Project Service Automation 22, V3</span><span class="sxs-lookup"><span data-stu-id="7b786-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="7b786-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7b786-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="7b786-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="7b786-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7b786-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="7b786-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7b786-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7b786-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="7b786-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7b786-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7b786-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 22 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="7b786-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="7b786-110">Questa versione ha il numero di build V 3.10.33.48 ed è generalmente disponibile tramite un aggiornamento automatico a giugno 2020.</span><span class="sxs-lookup"><span data-stu-id="7b786-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="7b786-111">Rilascio 22 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7b786-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7b786-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="7b786-112">Bug fixes</span></span>



<span data-ttu-id="7b786-113">**Tempo e spesa**</span><span class="sxs-lookup"><span data-stu-id="7b786-113">**Time and Expense**</span></span>

<span data-ttu-id="7b786-114">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="7b786-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="7b786-115">Gli **inserimenti ore** non vengono aggiunti automaticamente nella pianificazione inserimenti ore dopo l'importazione.</span><span class="sxs-lookup"><span data-stu-id="7b786-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="7b786-116">Il selettore della data della griglia **Inserimento ore** non riconosce le impostazioni internazionali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7b786-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="7b786-117">**Gestione risorse**</span><span class="sxs-lookup"><span data-stu-id="7b786-117">**Resource Management**</span></span>

<span data-ttu-id="7b786-118">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="7b786-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="7b786-119">In modalità manuale, le modifiche ai contorni di **Assegnazione risorse** non vengono riconosciute durante la generazione di **Requisiti di risorse**.</span><span class="sxs-lookup"><span data-stu-id="7b786-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="7b786-120">Le **richieste di risorse** non supportano gli stati delle richieste personalizzati.</span><span class="sxs-lookup"><span data-stu-id="7b786-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="7b786-121">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="7b786-121">**Project Management**</span></span>

<span data-ttu-id="7b786-122">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="7b786-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="7b786-123">L'utilizzo del doppio clic su ForecastGridControl non analizza correttamente i numeri del formato olandese.</span><span class="sxs-lookup"><span data-stu-id="7b786-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="7b786-124">Le ore assegnate non vengono aggiornate correttamente quando le assegnazioni vengono modificate utilizzando il componente aggiuntivo del client desktop Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="7b786-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="7b786-125">Le griglie Registrazione di progetto e Stime visualizzano un codice valuta di vendita errato quando la valuta del contratto è diversa dalla valuta del cliente e l'organizzazione è configurata per visualizzare i codici di valuta invece dei simboli di valuta.</span><span class="sxs-lookup"><span data-stu-id="7b786-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="7b786-126">La data di fine di un membro del team aggiunge un giorno se la pianificazione dell'orario di lavoro è di 24 ore al giorno.</span><span class="sxs-lookup"><span data-stu-id="7b786-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="7b786-127">Nella pianificazione del progetto, l'aggiunta di una categoria di transazione a un'attività non attiva il salvataggio automatico.</span><span class="sxs-lookup"><span data-stu-id="7b786-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="7b786-128">Quando si aggiunge un membro del team al modello di progetto, viene visualizzato il seguente errore: "I requisiti di risorsa non possono essere associati a modelli di progetto".</span><span class="sxs-lookup"><span data-stu-id="7b786-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="7b786-129">Lo script della regola della barra multifunzione "msdyn.Approval.CanApproveOrReject" visualizza un errore di timeout.</span><span class="sxs-lookup"><span data-stu-id="7b786-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="7b786-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="7b786-130">**Sales**</span></span>

<span data-ttu-id="7b786-131">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="7b786-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="7b786-132">Messaggio di errore di convalida non visualizzato quando si seleziona un listino prezzi di costo nella ricerca Listino prezzi nel modulo/entità "Nuovo listino prezzi progetto offerta".</span><span class="sxs-lookup"><span data-stu-id="7b786-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="7b786-133">La chiusura dell'offerta come vinta non consente di accedere al contratto creato se un processo aziendale collegato all'offerta è nella fase finale.</span><span class="sxs-lookup"><span data-stu-id="7b786-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="7b786-134">Lo storno delle **vendite non fatturate** è collegato al costo originale quando viene richiamato un inserimento di ore.</span><span class="sxs-lookup"><span data-stu-id="7b786-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="7b786-135">Dopo aver selezionato il pulsante **Conferma** lo stato della fattura non cambia in **Confermato** a meno che la fattura non venga aggiornata.</span><span class="sxs-lookup"><span data-stu-id="7b786-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
