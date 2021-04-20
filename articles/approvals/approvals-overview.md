---
title: Panoramica delle approvazioni
description: Questo argomento fornisce informazioni su come utilizzare le approvazioni in Project Operations.
author: stsporen
manager: Annbe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b2da22e10cf6c40a2c84bcd32437b2830f830d07
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852504"
---
# <a name="approvals-overview"></a><span data-ttu-id="94058-103">Panoramica delle approvazioni</span><span class="sxs-lookup"><span data-stu-id="94058-103">Approvals overview</span></span>

<span data-ttu-id="94058-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="94058-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94058-105">Gli invii di tempo, spese e utilizzo di materiale passano attraverso un flusso di lavoro per le approvazioni.</span><span class="sxs-lookup"><span data-stu-id="94058-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="94058-106">Dopo l'approvazione degli inserimenti, le transazioni vengono registrate in valori effettivi o viene prenotata un'ora nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="94058-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="94058-107">Flusso di lavoro per le approvazioni</span><span class="sxs-lookup"><span data-stu-id="94058-107">Approvals workflow</span></span>
<span data-ttu-id="94058-108">Quando si crea e si invia una voce di tempo, spesa o utilizzo di materiale, viene creato un record approvazione.</span><span class="sxs-lookup"><span data-stu-id="94058-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="94058-109">Il revisore o il responsabile del progetto esamina e approva la voce.</span><span class="sxs-lookup"><span data-stu-id="94058-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="94058-110">Se la voce è correlata a un progetto, i valori effettivi verranno creati al momento dell'approvazione.</span><span class="sxs-lookup"><span data-stu-id="94058-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="94058-111">Ciò consente di monitorare il costo e la fatturazione.</span><span class="sxs-lookup"><span data-stu-id="94058-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="94058-112">Approvare una voce</span><span class="sxs-lookup"><span data-stu-id="94058-112">Approve an entry</span></span>
<span data-ttu-id="94058-113">La pagina **Approvazioni** consente di passare da una visualizzazione all'altra in modo da poter visualizzare i diversi tipi di approvazioni.</span><span class="sxs-lookup"><span data-stu-id="94058-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="94058-114">Vai alla pagina **Approvazioni** e seleziona **Spese**, **Tempo**, **Utilizzo di materiale** o **Richiami**.</span><span class="sxs-lookup"><span data-stu-id="94058-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="94058-115">Rivedi ogni approvazione e seleziona quelle che desideri approvare.</span><span class="sxs-lookup"><span data-stu-id="94058-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="94058-116">Seleziona **Approva** per approvare le voci selezionate.</span><span class="sxs-lookup"><span data-stu-id="94058-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="94058-117">Il sistema elabora queste voci e crea valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="94058-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="94058-118">Rifiutare una voce</span><span class="sxs-lookup"><span data-stu-id="94058-118">Reject an entry</span></span>
<span data-ttu-id="94058-119">In qualità di approvatore del progetto, potrebbe essere necessario inviare una voce a un utente per la correzione.</span><span class="sxs-lookup"><span data-stu-id="94058-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="94058-120">Vai alla pagina **Approvazioni** e seleziona la voce da rifiutare.</span><span class="sxs-lookup"><span data-stu-id="94058-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="94058-121">Seleziona **Rifiuta**.</span><span class="sxs-lookup"><span data-stu-id="94058-121">Select **Reject**.</span></span>
3. <span data-ttu-id="94058-122">Facoltativo: aggiungi un commento nella finestra di dialogo **Commenti rifiuto** per informare l'utente del motivo per cui la voce è stata rifiutata.</span><span class="sxs-lookup"><span data-stu-id="94058-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="94058-123">Seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="94058-123">Select **OK**.</span></span> <span data-ttu-id="94058-124">La voce verrà restituita all'utente.</span><span class="sxs-lookup"><span data-stu-id="94058-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="94058-125">Annulla approvazione</span><span class="sxs-lookup"><span data-stu-id="94058-125">Cancel approval</span></span>
<span data-ttu-id="94058-126">In alcuni casi, potrebbe essere necessario annullare una voce precedentemente approvata.</span><span class="sxs-lookup"><span data-stu-id="94058-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="94058-127">L'annullamento di una voce precedentemente approvata avrà un impatto finanziario.</span><span class="sxs-lookup"><span data-stu-id="94058-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="94058-128">Approvare richieste di richiamo</span><span class="sxs-lookup"><span data-stu-id="94058-128">Approving recall requests</span></span>
<span data-ttu-id="94058-129">In alcuni casi, un consulente potrebbe dover richiamare una voce precedentemente approvata.</span><span class="sxs-lookup"><span data-stu-id="94058-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="94058-130">L'annullamento di una voce precedentemente approvata avrà un impatto finanziario.</span><span class="sxs-lookup"><span data-stu-id="94058-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="94058-131">L'approvatore del progetto deve approvare il richiamo per stornare la transazione in Valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="94058-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="94058-132">Specificare gli approvatori di progetto</span><span class="sxs-lookup"><span data-stu-id="94058-132">Specify Project approvers</span></span>
<span data-ttu-id="94058-133">Ogni progetto ha un numero di membri del team di progetto.</span><span class="sxs-lookup"><span data-stu-id="94058-133">Each project has a number of project team members.</span></span> <span data-ttu-id="94058-134">È possibile specificare quali membri del team sono anche approvatori del progetto.</span><span class="sxs-lookup"><span data-stu-id="94058-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="94058-135">Vai alla pagina **Progetti** e apri il progetto dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="94058-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="94058-136">Nella scheda **Team**, seleziona il membro del team che sarà un approvatore del progetto, quindi seleziona **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="94058-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="94058-137">Imposta il campo **Responsabile approvazione di progetto** su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="94058-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="94058-138">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="94058-138">Select **Save**.</span></span>
5. <span data-ttu-id="94058-139">Ripeti i passaggi da 2 a 4 per aggiungere altri responsabili dell'approvazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="94058-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="94058-140">Configura il responsabile dell'utente</span><span class="sxs-lookup"><span data-stu-id="94058-140">Configure the user's manager</span></span>

1. <span data-ttu-id="94058-141">Andare a **Impostazioni** > **Sicurezza** > **Utenti**.</span><span class="sxs-lookup"><span data-stu-id="94058-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="94058-142">Seleziona l'utente a cui stai assegnando un responsabile e nell'area **Informazioni sull'organizzazione**, seleziona il responsabile dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="94058-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="94058-143">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="94058-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
