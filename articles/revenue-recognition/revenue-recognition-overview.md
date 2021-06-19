---
title: Panoramica del riconoscimento ricavi
description: In questo argomento vengono fornite informazioni sul riconoscimento dei ricavi in Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013761"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="cbe9e-103">Panoramica del riconoscimento ricavi</span><span class="sxs-lookup"><span data-stu-id="cbe9e-103">Revenue recognition overview</span></span>

<span data-ttu-id="cbe9e-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="cbe9e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cbe9e-105">In Dynamics 365 Project Operations, i principi di riconoscimento dei ricavi variano in base al metodo di fatturazione selezionato per un progetto o una parte del progetto.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="cbe9e-106">In questo argomento vengono fornite informazioni sul riconoscimento dei ricavi in Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="cbe9e-107">Transazioni contabilizzate utilizzando il metodo di fatturazione per tempo e materiali</span><span class="sxs-lookup"><span data-stu-id="cbe9e-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="cbe9e-108">Il riconoscimento dei costi è collegato al riconoscimento dei ricavi.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="cbe9e-109">Il costo della transazione e le vendite non fatturate vengono registrati utilizzando l'estensione [Giornale di integrazione di Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="cbe9e-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="cbe9e-110">Il profilo dei costi e dei ricavi del progetto determina se le transazioni di vendita non fatturate vengono registrate nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="cbe9e-111">Se l'opzione **Accumula ricavi** è selezionata, il sistema utilizza **Valore di vendita WIP** e i conti **Ricavi sospesi - Valore netto di vendita** durante la registrazione.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="cbe9e-112">Di seguito viene riportato un esempio di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="cbe9e-113">Tipo di transazione</span><span class="sxs-lookup"><span data-stu-id="cbe9e-113">Transaction type</span></span> | <span data-ttu-id="cbe9e-114">Debito/Credito</span><span class="sxs-lookup"><span data-stu-id="cbe9e-114">Debit/Credit</span></span> | <span data-ttu-id="cbe9e-115">Importa</span><span class="sxs-lookup"><span data-stu-id="cbe9e-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="cbe9e-116">WIP - Valore netto di vendita</span><span class="sxs-lookup"><span data-stu-id="cbe9e-116">WIP Sales value</span></span> | <span data-ttu-id="cbe9e-117">Dare</span><span class="sxs-lookup"><span data-stu-id="cbe9e-117">Debit</span></span> | <span data-ttu-id="cbe9e-118">100</span><span class="sxs-lookup"><span data-stu-id="cbe9e-118">100</span></span> |
  | <span data-ttu-id="cbe9e-119">Ricavi sospesi - Valore netto di vendita</span><span class="sxs-lookup"><span data-stu-id="cbe9e-119">Accrued revenue sales value</span></span> | <span data-ttu-id="cbe9e-120">Avere</span><span class="sxs-lookup"><span data-stu-id="cbe9e-120">Credit</span></span> | <span data-ttu-id="cbe9e-121">100</span><span class="sxs-lookup"><span data-stu-id="cbe9e-121">100</span></span> |

- <span data-ttu-id="cbe9e-122">I ricavi vengono riconosciuti durante la fatturazione.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="cbe9e-123">Il sistema utilizza il conto **Ricavi fatturati** durante la registrazione.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="cbe9e-124">Di seguito viene riportato un esempio di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="cbe9e-125">Tipo di transazione</span><span class="sxs-lookup"><span data-stu-id="cbe9e-125">Transaction type</span></span> | <span data-ttu-id="cbe9e-126">Dare/Avere</span><span class="sxs-lookup"><span data-stu-id="cbe9e-126">Debit/Credit</span></span> | <span data-ttu-id="cbe9e-127">Importa</span><span class="sxs-lookup"><span data-stu-id="cbe9e-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="cbe9e-128">Saldo cliente</span><span class="sxs-lookup"><span data-stu-id="cbe9e-128">Customer balance</span></span> | <span data-ttu-id="cbe9e-129">Dare</span><span class="sxs-lookup"><span data-stu-id="cbe9e-129">Debit</span></span> | <span data-ttu-id="cbe9e-130">120</span><span class="sxs-lookup"><span data-stu-id="cbe9e-130">120</span></span> |
  | <span data-ttu-id="cbe9e-131">IVA a debito</span><span class="sxs-lookup"><span data-stu-id="cbe9e-131">Sales tax payable</span></span> | <span data-ttu-id="cbe9e-132">Avere</span><span class="sxs-lookup"><span data-stu-id="cbe9e-132">Credit</span></span> | <span data-ttu-id="cbe9e-133">20</span><span class="sxs-lookup"><span data-stu-id="cbe9e-133">20</span></span> |
  | <span data-ttu-id="cbe9e-134">Ricavi fatturati</span><span class="sxs-lookup"><span data-stu-id="cbe9e-134">Invoiced Revenue</span></span> | <span data-ttu-id="cbe9e-135">Avere</span><span class="sxs-lookup"><span data-stu-id="cbe9e-135">Credit</span></span> | <span data-ttu-id="cbe9e-136">100</span><span class="sxs-lookup"><span data-stu-id="cbe9e-136">100</span></span> |

- <span data-ttu-id="cbe9e-137">Se i ricavi sono stati maturati quando vengono registrate le vendite non fatturate, il sistema stornerà i ricavi maturati al momento della fatturazione.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="cbe9e-138">Tipo di transazione</span><span class="sxs-lookup"><span data-stu-id="cbe9e-138">Transaction type</span></span> | <span data-ttu-id="cbe9e-139">Dare/Avere</span><span class="sxs-lookup"><span data-stu-id="cbe9e-139">Debit/Credit</span></span> | <span data-ttu-id="cbe9e-140">Importa</span><span class="sxs-lookup"><span data-stu-id="cbe9e-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="cbe9e-141">WIP - Valore netto di vendita</span><span class="sxs-lookup"><span data-stu-id="cbe9e-141">WIP Sales value</span></span> | <span data-ttu-id="cbe9e-142">Avere</span><span class="sxs-lookup"><span data-stu-id="cbe9e-142">Credit</span></span> | <span data-ttu-id="cbe9e-143">100</span><span class="sxs-lookup"><span data-stu-id="cbe9e-143">100</span></span> |
  | <span data-ttu-id="cbe9e-144">Ricavi sospesi - Valore netto di vendita</span><span class="sxs-lookup"><span data-stu-id="cbe9e-144">Accrued revenue sales value</span></span> | <span data-ttu-id="cbe9e-145">Dare</span><span class="sxs-lookup"><span data-stu-id="cbe9e-145">Debit</span></span> | <span data-ttu-id="cbe9e-146">100</span><span class="sxs-lookup"><span data-stu-id="cbe9e-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="cbe9e-147">Transazioni contabilizzate utilizzando il metodo di fatturazione a prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="cbe9e-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="cbe9e-148">Il riconoscimento dei costi e dei ricavi sono separati.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="cbe9e-149">Il costo della transazione viene registrato utilizzando l'estensione [Giornale di integrazione di Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="cbe9e-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="cbe9e-150">Le transazioni di vendita non fatturate non vengono create.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="cbe9e-151">I ricavi possono essere riconosciuti durante la fatturazione se il costo del progetto e il profilo dei ricavi hanno **Principio utilizzato per i calcoli di completamento del progetto** impostato su **Nessuna WIP**.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="cbe9e-152">Utilizzare questo metodo solo per progetti semplici e a breve termine.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="cbe9e-153">I ricavi possono essere riconosciuti utilizzando le stime dei ricavi a prezzo fisso, sia con il metodo **Contratto completato** che **Percentuale di completamento del riconoscimento ricavi**.</span><span class="sxs-lookup"><span data-stu-id="cbe9e-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cbe9e-154">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="cbe9e-154">Additional resources</span></span>
[<span data-ttu-id="cbe9e-155">Configurare la contabilità per l'articolo progetti fatturabili</span><span class="sxs-lookup"><span data-stu-id="cbe9e-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="cbe9e-156">Progetti di stima dei ricavi a prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="cbe9e-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="cbe9e-157">Gestire le stime dei ricavi</span><span class="sxs-lookup"><span data-stu-id="cbe9e-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="cbe9e-158">Metodi Costi di completamento</span><span class="sxs-lookup"><span data-stu-id="cbe9e-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]