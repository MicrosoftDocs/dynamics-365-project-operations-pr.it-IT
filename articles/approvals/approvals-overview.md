---
title: Panoramica delle approvazioni
description: Questo argomento fornisce informazioni su come utilizzare le approvazioni in Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a7573b95998387453b72dbcb73c3de977ed7d913
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290364"
---
# <a name="approvals-overview"></a><span data-ttu-id="69eb5-103">Panoramica delle approvazioni</span><span class="sxs-lookup"><span data-stu-id="69eb5-103">Approvals overview</span></span>

<span data-ttu-id="69eb5-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="69eb5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="69eb5-105">Gli invii di tempo e spese passano attraverso un flusso di lavoro di approvazione.</span><span class="sxs-lookup"><span data-stu-id="69eb5-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="69eb5-106">Dopo l'approvazione degli inserimenti, le transazioni vengono registrate in valori effettivi o viene prenotata un'ora nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="69eb5-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="69eb5-107">Flusso di lavoro per le approvazioni</span><span class="sxs-lookup"><span data-stu-id="69eb5-107">Approvals workflow</span></span>
<span data-ttu-id="69eb5-108">Quando crei e invii una voce di tempo o di spesa, viene creata una voce di approvazione.</span><span class="sxs-lookup"><span data-stu-id="69eb5-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="69eb5-109">L'approvatore del progetto o il tuo responsabile esamina e approva il tuo inserimento.</span><span class="sxs-lookup"><span data-stu-id="69eb5-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="69eb5-110">Se la voce è correlata a un progetto, quando viene approvata, verranno creati i valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="69eb5-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="69eb5-111">Ciò consente di monitorare il costo e la fatturazione.</span><span class="sxs-lookup"><span data-stu-id="69eb5-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="69eb5-112">Approvare una voce</span><span class="sxs-lookup"><span data-stu-id="69eb5-112">Approve an entry</span></span>
<span data-ttu-id="69eb5-113">Il modulo **Approvazioni** consente di passare da una visualizzazione all'altra in modo da poter visualizzare i diversi tipi di approvazioni.</span><span class="sxs-lookup"><span data-stu-id="69eb5-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="69eb5-114">Vai al modulo **Approvazioni** e seleziona **Spese**, **Tempo** o **Ricorda**.</span><span class="sxs-lookup"><span data-stu-id="69eb5-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="69eb5-115">Rivedi ogni approvazione e seleziona quelle che desideri approvare.</span><span class="sxs-lookup"><span data-stu-id="69eb5-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="69eb5-116">Seleziona **Approva** per approvare le voci selezionate.</span><span class="sxs-lookup"><span data-stu-id="69eb5-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="69eb5-117">Il sistema elaborerà queste voci e creerà valori effettivi o una prenotazione.</span><span class="sxs-lookup"><span data-stu-id="69eb5-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="69eb5-118">Rifiutare una voce</span><span class="sxs-lookup"><span data-stu-id="69eb5-118">Reject an entry</span></span>
<span data-ttu-id="69eb5-119">In qualità di approvatore del progetto, potrebbe essere necessario inviare una voce a un utente per la correzione.</span><span class="sxs-lookup"><span data-stu-id="69eb5-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="69eb5-120">Vai al modulo **Approvazioni** e seleziona la voce da rifiutare.</span><span class="sxs-lookup"><span data-stu-id="69eb5-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="69eb5-121">Seleziona **Rifiuta**.</span><span class="sxs-lookup"><span data-stu-id="69eb5-121">Select **Reject**.</span></span>
3. <span data-ttu-id="69eb5-122">Facoltativo: aggiungi un commento nella finestra di dialogo **Commenti rifiuto** per informare l'utente del motivo per cui la voce è stata rifiutata.</span><span class="sxs-lookup"><span data-stu-id="69eb5-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="69eb5-123">Seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="69eb5-123">Select **OK**.</span></span> <span data-ttu-id="69eb5-124">La voce verrà restituita all'utente.</span><span class="sxs-lookup"><span data-stu-id="69eb5-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="69eb5-125">Richiamare le voci</span><span class="sxs-lookup"><span data-stu-id="69eb5-125">Recall entries</span></span>
<span data-ttu-id="69eb5-126">Ad un certo punto, potrebbe essere necessario richiamare una voce inviata.</span><span class="sxs-lookup"><span data-stu-id="69eb5-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="69eb5-127">Se la voce non è stata approvata, verrà restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="69eb5-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="69eb5-128">Tuttavia, una voce approvata può avere un impatto sostanziale.</span><span class="sxs-lookup"><span data-stu-id="69eb5-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="69eb5-129">L'approvatore del progetto è tenuto ad approvare il richiamo per stornare la transazione in Valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="69eb5-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="69eb5-130">Specificare gli approvatori di progetto</span><span class="sxs-lookup"><span data-stu-id="69eb5-130">Specify Project approvers</span></span>
<span data-ttu-id="69eb5-131">Ogni progetto ha un numero di membri del team di progetto.</span><span class="sxs-lookup"><span data-stu-id="69eb5-131">Each project has a number of project team members.</span></span> <span data-ttu-id="69eb5-132">È possibile specificare quali membri del team sono anche approvatori del progetto.</span><span class="sxs-lookup"><span data-stu-id="69eb5-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="69eb5-133">Vai al modulo **Progetti** e apri il progetto dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="69eb5-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="69eb5-134">Nella scheda **Team**, seleziona il membro del team che sarà un approvatore del progetto, quindi seleziona **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="69eb5-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="69eb5-135">Imposta il campo **Responsabile approvazione di progetto** su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="69eb5-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="69eb5-136">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="69eb5-136">Select **Save**.</span></span>
5. <span data-ttu-id="69eb5-137">Ripeti i passaggi da 2 a 4 per aggiungere altri responsabili dell'approvazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="69eb5-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="69eb5-138">Configura il responsabile dell'utente</span><span class="sxs-lookup"><span data-stu-id="69eb5-138">Configure the user's manager</span></span>

1. <span data-ttu-id="69eb5-139">Andare a **Impostazioni** > **Sicurezza** > **Utenti**.</span><span class="sxs-lookup"><span data-stu-id="69eb5-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="69eb5-140">Seleziona l'utente a cui stai assegnando un responsabile e nell'area **Informazioni sull'organizzazione**, seleziona il responsabile dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="69eb5-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="69eb5-141">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="69eb5-141">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]