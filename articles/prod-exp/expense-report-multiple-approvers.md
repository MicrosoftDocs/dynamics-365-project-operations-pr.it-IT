---
title: Più responsabili approvatore per una nota spese
description: Questo argomento fornisce informazioni sulle note spese che richiedono l'approvazione di più responsabili.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271718"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="18fde-103">Più responsabili approvatore per una nota spese</span><span class="sxs-lookup"><span data-stu-id="18fde-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="18fde-104">A seconda dei criteri di approvazione delle spese dell'organizzazione, più di una persona potrebbe dover approvare una nota spese inviata da un dipendente.</span><span class="sxs-lookup"><span data-stu-id="18fde-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="18fde-105">Quando imposti il processo del flusso di lavoro per l'approvazione della nota spese, puoi aggiungere elementi del flusso di lavoro che includono attività o passaggi per uno o più responsabili dell'approvazione della nota spese.</span><span class="sxs-lookup"><span data-stu-id="18fde-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="18fde-106">Ad esempio, puoi richiedere che tutte le note spese siano approvate dal responsabile del dipendente che ha inviato il report e dal coordinatore della contabilità fornitori.</span><span class="sxs-lookup"><span data-stu-id="18fde-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="18fde-107">Se decidi di richiedere più approvatori della nota spese, puoi aggiungere gli elementi del flusso di lavoro in uno dei seguenti modi:</span><span class="sxs-lookup"><span data-stu-id="18fde-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="18fde-108">Aggiungi un elemento di approvazione con un passaggio.</span><span class="sxs-lookup"><span data-stu-id="18fde-108">Add one approval element that has one step.</span></span> <span data-ttu-id="18fde-109">Ad esempio, il passaggio potrebbe richiedere che una nota spese venga assegnata a un gruppo di utenti e che venga approvata dal 50% dei membri del gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="18fde-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="18fde-110">Aggiungi un elemento di approvazione con più passaggi.</span><span class="sxs-lookup"><span data-stu-id="18fde-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="18fde-111">Ad esempio, l'elemento di approvazione potrebbe avere i seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="18fde-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="18fde-112">Il responsabile del dipendente che ha presentato la nota spese la approva.</span><span class="sxs-lookup"><span data-stu-id="18fde-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="18fde-113">L'addetto alla contabilità fornitori verifica le ricevute e le voci della nota spese.</span><span class="sxs-lookup"><span data-stu-id="18fde-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="18fde-114">Il proprietario del budget approva la nota spese.</span><span class="sxs-lookup"><span data-stu-id="18fde-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="18fde-115">Aggiungi più elementi di approvazione, ognuno dei quali ha un passaggio.</span><span class="sxs-lookup"><span data-stu-id="18fde-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="18fde-116">Ad esempio, puoi aggiungere un elemento di approvazione separato per ciascuno dei seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="18fde-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="18fde-117">Il responsabile del dipendente approva la nota spese.</span><span class="sxs-lookup"><span data-stu-id="18fde-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="18fde-118">Il proprietario del budget approva la nota spese.</span><span class="sxs-lookup"><span data-stu-id="18fde-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]