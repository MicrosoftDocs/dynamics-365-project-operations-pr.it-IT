---
title: Note spese e più approvatori
description: Questo argomento fornisce informazioni sulle note spese che richiedono l'approvazione di più persone.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078879"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="3ec95-103">Note spese e più approvatori</span><span class="sxs-lookup"><span data-stu-id="3ec95-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="3ec95-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="3ec95-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3ec95-105">A seconda dei criteri di approvazione delle spese dell'organizzazione, più di una persona potrebbe dover approvare una nota spese inviata.</span><span class="sxs-lookup"><span data-stu-id="3ec95-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="3ec95-106">Quando imposti il processo del flusso di lavoro per l'approvazione della nota spese, puoi aggiungere elementi del flusso di lavoro che includono attività o passaggi per uno o più responsabili dell'approvazione della nota spese.</span><span class="sxs-lookup"><span data-stu-id="3ec95-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="3ec95-107">Ad esempio, puoi richiedere che tutte le note spese siano approvate da due persone separate, il responsabile del dipendente che ha inviato il report e il coordinatore della contabilità fornitori.</span><span class="sxs-lookup"><span data-stu-id="3ec95-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="3ec95-108">Se decidi di richiedere più approvatori della nota spese, puoi aggiungere gli elementi del flusso di lavoro in uno dei seguenti modi:</span><span class="sxs-lookup"><span data-stu-id="3ec95-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="3ec95-109">Aggiungi un elemento di approvazione con un passaggio.</span><span class="sxs-lookup"><span data-stu-id="3ec95-109">Add one approval element that has one step.</span></span> <span data-ttu-id="3ec95-110">Ad esempio, il passaggio potrebbe richiedere che una nota spese venga assegnata a un gruppo di utenti e che venga approvata dal 50% dei membri del gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="3ec95-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="3ec95-111">Aggiungi un elemento di approvazione con più passaggi.</span><span class="sxs-lookup"><span data-stu-id="3ec95-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="3ec95-112">Ad esempio, l'elemento di approvazione potrebbe avere i seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="3ec95-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="3ec95-113">Il responsabile del dipendente che ha presentato la nota spese la approva.</span><span class="sxs-lookup"><span data-stu-id="3ec95-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="3ec95-114">L'addetto alla contabilità fornitori verifica le ricevute e le voci della nota spese.</span><span class="sxs-lookup"><span data-stu-id="3ec95-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="3ec95-115">Il proprietario del budget approva la nota spese.</span><span class="sxs-lookup"><span data-stu-id="3ec95-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="3ec95-116">Aggiungi più elementi di approvazione, ognuno dei quali ha un passaggio.</span><span class="sxs-lookup"><span data-stu-id="3ec95-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="3ec95-117">Ad esempio, puoi aggiungere un elemento di approvazione separato per ciascuno dei seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="3ec95-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="3ec95-118">Il responsabile del dipendente approva la nota spese.</span><span class="sxs-lookup"><span data-stu-id="3ec95-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="3ec95-119">Il proprietario del budget approva la nota spese.</span><span class="sxs-lookup"><span data-stu-id="3ec95-119">The budget owner approves the expense report.</span></span>
