---
title: Confermare un contratto di progetto
description: Questo argomento fornisce informazioni su come confermare un contratto in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d807d3631f40a93ec7dbd918b64c287fd4875c79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273833"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="104b4-103">Confermare un contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="104b4-103">Confirm a project contract</span></span>

<span data-ttu-id="104b4-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="104b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="104b4-105">Un contratto di progetto in Dynamics 365 Project Operations può essere attivo con il motivo **Confermato** o chiuso con il motivo **Perso**.</span><span class="sxs-lookup"><span data-stu-id="104b4-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="104b4-106">Quando confermi un contratto di progetto, lo stato viene aggiornato da **Bozza** ad **Attivo** e il motivo dello stato è **Confermato**.</span><span class="sxs-lookup"><span data-stu-id="104b4-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="104b4-107">Un contratto attivo o chiuso non può essere modificato o riaperto.</span><span class="sxs-lookup"><span data-stu-id="104b4-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="104b4-108">Impatto finanziario della conferma di un contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="104b4-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="104b4-109">Dopo che un contratto di progetto viene confermato, l'applicazione ricalcola i costi stornando i valori effettivi di costo precedenti e creando nuovi valori effettivi di costo.</span><span class="sxs-lookup"><span data-stu-id="104b4-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="104b4-110">I nuovi valori effettivi vengono elaborati in base al metodo di fatturazione della voce di contratto di progetto associata.</span><span class="sxs-lookup"><span data-stu-id="104b4-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="104b4-111">Se i valori effettivi di costo fanno riferimento a una voce di contratto per tempistica e materiali, l'applicazione ricrea automaticamente i valori effettivi di vendita non fatturati corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="104b4-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="104b4-112">Se i costi effettivi fanno riferimento a una voce di contratto a prezzo fisso, l'applicazione interrompe la rielaborazione dei valori effettivi di costo.</span><span class="sxs-lookup"><span data-stu-id="104b4-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="104b4-113">I limiti da non superare, l'impostazione dell'esigibilità e la determinazione del prezzo e dei costi sui valori effettivi vengono valutati e quindi aggiornati come parte del processo di conferma.</span><span class="sxs-lookup"><span data-stu-id="104b4-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="104b4-114">Chiudere un contratto di progetto come perso</span><span class="sxs-lookup"><span data-stu-id="104b4-114">Close a project contract as lost</span></span>

<span data-ttu-id="104b4-115">Quando chiudi un contratto di progetto come perso, lo stato del contratto viene aggiornato a **Chiuso** e il motivo dello stato è **Perso**.</span><span class="sxs-lookup"><span data-stu-id="104b4-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="104b4-116">Il contratto di progetto diventa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="104b4-116">The project contract becomes read-only.</span></span> <span data-ttu-id="104b4-117">Viene visualizzata una finestra di dialogo di conferma prima del completamento delle modifiche poiché non è possibile riaprire un contratto di progetto chiuso.</span><span class="sxs-lookup"><span data-stu-id="104b4-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="104b4-118">Se il contratto di progetto chiuso come perso fa riferimento a un progetto nelle righe, anche quel progetto viene contrassegnato come chiuso.</span><span class="sxs-lookup"><span data-stu-id="104b4-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="104b4-119">Qualsiasi prenotazione di risorse da quel giorno in poi viene annullata.</span><span class="sxs-lookup"><span data-stu-id="104b4-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="104b4-120">Eventuali valori effettivi di vendita non fatturati nel contratto di progetto che non sono già presenti in una fattura verranno stornati.</span><span class="sxs-lookup"><span data-stu-id="104b4-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="104b4-121">In Dynamics 365 Project Operations, la chiusura di un contratto di progetto come perso non influisce sullo stato dell'opportunità associata.</span><span class="sxs-lookup"><span data-stu-id="104b4-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="104b4-122">L'opportunità rimarrà aperta e dovrà essere chiusa manualmente.</span><span class="sxs-lookup"><span data-stu-id="104b4-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]