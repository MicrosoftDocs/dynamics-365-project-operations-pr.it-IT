---
title: Definire i criteri di spesa
description: Puoi definire i criteri di spesa che i dipendenti devono seguire quando inseriscono e inviano note spese e richieste di viaggio.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 863d1e44dad9fa0d2174cf77582a1d820988e92d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276083"
---
# <a name="define-expense-policies"></a><span data-ttu-id="c13b2-103">Definire i criteri di spesa</span><span class="sxs-lookup"><span data-stu-id="c13b2-103">Define expense policies</span></span>

<span data-ttu-id="c13b2-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="c13b2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c13b2-105">Puoi definire i criteri che i dipendenti devono seguire quando inseriscono e inviano note spese e richieste di viaggio.</span><span class="sxs-lookup"><span data-stu-id="c13b2-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="c13b2-106">L'implementazione dei criteri di spesa può aiutarti a gestire le spese in modo efficace.</span><span class="sxs-lookup"><span data-stu-id="c13b2-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="c13b2-107">Ad esempio, puoi impostare un criterio per le spese dell'hotel a New York City, in cui si stabilisce che la spesa per notte non può superare USD 250.</span><span class="sxs-lookup"><span data-stu-id="c13b2-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="c13b2-108">Se un lavoratore invia una nota spese o una richiesta di viaggio in cui la tariffa della camera supera questo importo, il sistema avviserà il</span><span class="sxs-lookup"><span data-stu-id="c13b2-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="c13b2-109">lavoratore che l'importo dei criteri per la spesa è stato superato.</span><span class="sxs-lookup"><span data-stu-id="c13b2-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="c13b2-110">Puoi configurare il messaggio che il lavoratore riceverà quando</span><span class="sxs-lookup"><span data-stu-id="c13b2-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="c13b2-111">definisci i criteri.</span><span class="sxs-lookup"><span data-stu-id="c13b2-111">define the policy.</span></span>      
        
<span data-ttu-id="c13b2-112">Puoi definire tre tipi di criteri:</span><span class="sxs-lookup"><span data-stu-id="c13b2-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="c13b2-113">**Avviso**: consente al lavoratore di inviare una nota spese o una richiesta di viaggio, ma la spesa verrà contrassegnata per tutti gli approvatori e</span><span class="sxs-lookup"><span data-stu-id="c13b2-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="c13b2-114">per i report successivi.</span><span class="sxs-lookup"><span data-stu-id="c13b2-114">for later reporting.</span></span>        

- <span data-ttu-id="c13b2-115">**Errore**: richiede al lavoratore di rivedere la spesa per conformarsi ai criteri prima di inviare la nota spese o la richiesta di viaggio.</span><span class="sxs-lookup"><span data-stu-id="c13b2-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="c13b2-116">**Giustificazione**: richiede al lavoratore o a un responsabile di inserire una giustificazione per il superamento dell'importo dei criteri prima di inviare la nota spese o la richiesta di viaggio.</span><span class="sxs-lookup"><span data-stu-id="c13b2-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="c13b2-117">Suggerimenti per i criteri</span><span class="sxs-lookup"><span data-stu-id="c13b2-117">Policy tips</span></span>
<span data-ttu-id="c13b2-118">Di seguito sono riportati alcuni suggerimenti che possono essere utili durante la creazione di nuovi criteri per la gestione delle spese:</span><span class="sxs-lookup"><span data-stu-id="c13b2-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="c13b2-119">I criteri hanno una data di validità, il che significa che un criterio non avrà effetto se viene creato con una data successiva alla data in cui si è verificata la spesa.</span><span class="sxs-lookup"><span data-stu-id="c13b2-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="c13b2-120">Ad esempio, oggi crei un nuovo criterio per applicare una spesa massima per i pasti di 50 USD.</span><span class="sxs-lookup"><span data-stu-id="c13b2-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="c13b2-121">Qualsiasi spesa esistente inserita a partire da ieri non verrà verificata rispetto a questo criterio.</span><span class="sxs-lookup"><span data-stu-id="c13b2-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="c13b2-122">Quando si crea un criterio per una categoria di spesa che può essere dettagliata, considera l'aggiunta di una condizione per il tipo di riga di spesa.</span><span class="sxs-lookup"><span data-stu-id="c13b2-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="c13b2-123">Alcuni criteri, come la richiesta di una ricevuta, potrebbero non avere senso per le righe dettagliate.</span><span class="sxs-lookup"><span data-stu-id="c13b2-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="c13b2-124">In questa situazione, il criterio viene applicato solo alla riga di intestazione o a una riga non dettagliata.</span><span class="sxs-lookup"><span data-stu-id="c13b2-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="c13b2-125">Per impostazione predefinita, i criteri di gestione delle spese vengono valutati rispetto all'entità di origine.</span><span class="sxs-lookup"><span data-stu-id="c13b2-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="c13b2-126">Per gli scenari interaziendali, puoi impostare invece la valutazione del criterio rispetto all'entità di destinazione (entità mutuataria).</span><span class="sxs-lookup"><span data-stu-id="c13b2-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="c13b2-127">Per eseguire i criteri sull'entità di destinazione, attiva la funzionalità **Valuta criteri di spesa rispetto alla persona giuridica mutuataria** nell'area di lavoro **Gestione delle funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="c13b2-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="c13b2-128">Quando valutare i criteri</span><span class="sxs-lookup"><span data-stu-id="c13b2-128">When to evaluate policies</span></span>

<span data-ttu-id="c13b2-129">Nei parametri di gestione delle spese, puoi scegliere di valutare i criteri di gestione delle spese quando viene salvata una riga o quando viene inviata una nota spese.</span><span class="sxs-lookup"><span data-stu-id="c13b2-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="c13b2-130">Se scegli di valutare quando una riga viene salvata, gli utenti avranno visibilità in anticipo su ciò che devono fare per completare la loro nota spese tutto insieme.</span><span class="sxs-lookup"><span data-stu-id="c13b2-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="c13b2-131">In caso contrario, puoi ritardare la valutazione del criterio e risparmiare tempo convalidando alla fine, durante l'invio al flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c13b2-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]