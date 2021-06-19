---
title: Configurare la gestione delle spese
description: In questo articolo vengono descritte le considerazioni e le decisioni da prendere durante il processo di pianificazione prima di configurare la gestione delle spese in Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52538946c7260fad4076a64e8dc34fecf08b90cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005391"
---
# <a name="configure-expense-management"></a><span data-ttu-id="5670a-103">Configurare la gestione delle spese</span><span class="sxs-lookup"><span data-stu-id="5670a-103">Configure expense management</span></span>

<span data-ttu-id="5670a-104">In questo argomento vengono descritte le considerazioni e le decisioni da prendere durante il processo di pianificazione prima di configurare la gestione delle spese.</span><span class="sxs-lookup"><span data-stu-id="5670a-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="5670a-105">In Gestione spese è possibile archiviare informazioni su metodi di pagamento, richieste di viaggio, note spese, criteri e così via.</span><span class="sxs-lookup"><span data-stu-id="5670a-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="5670a-106">Poiché molte delle decisioni prese durante la pianificazione della configurazione per la gestione delle spese si basano sulla gerarchia e sulla struttura finanziaria dell'organizzazione, è necessario fare riferimento ai documenti di pianificazione per quelle aree.</span><span class="sxs-lookup"><span data-stu-id="5670a-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="5670a-107">Spese interaziendali</span><span class="sxs-lookup"><span data-stu-id="5670a-107">Intercompany expenses</span></span>

<span data-ttu-id="5670a-108">Quando abiliti le spese interaziendali, consenti alle persone giuridiche e ai dipendenti di sostenere spese per conto di un'altra persona giuridica e riscuotere il pagamento dalla persona giuridica che impiega il dipendente all'interno dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5670a-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="5670a-109">Ad esempio, un dipendente della persona giuridica A completa un progetto per la persona giuridica B e il progetto include le spese relative al viaggio.</span><span class="sxs-lookup"><span data-stu-id="5670a-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="5670a-110">Se le spese interaziendali sono abilitate, il dipendente può quindi presentare una nota spese che registra la spesa nella persona giuridica B e la spesa deve quindi essere pagata dalla persona giuridica A. Se la tua organizzazione non ha più persone giuridiche, non devi abilitare le spese interaziendali.</span><span class="sxs-lookup"><span data-stu-id="5670a-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="5670a-111">**Decisione:** vuoi abilitare le spese interaziendali?</span><span class="sxs-lookup"><span data-stu-id="5670a-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="5670a-112">Gestione finanziaria</span><span class="sxs-lookup"><span data-stu-id="5670a-112">Financial management</span></span>

<span data-ttu-id="5670a-113">La gestione delle spese è strettamente integrata con la gestione finanziaria della tua organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5670a-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="5670a-114">Gran parte della tua configurazione per la gestione delle spese sarà basata sulle decisioni che hai preso per i dati finanziari della tua organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5670a-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="5670a-115">Le sezioni seguenti descrivono le varie aree che richiedono pianificazione e decisioni, in base alle decisioni dei dati finanziari dell'organizzazione e alle linee guida del team di leadership.</span><span class="sxs-lookup"><span data-stu-id="5670a-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="5670a-116">Diaria</span><span class="sxs-lookup"><span data-stu-id="5670a-116">Per diems</span></span>

<span data-ttu-id="5670a-117">È necessario definire la diaria dei dipendenti fornita dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5670a-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="5670a-118">Poiché la diaria giornaliera viene generalmente utilizzata per coprire spese quali vitto, alloggio e altre spese accessorie, puoi creare regole per le diarie giornaliere offerte dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5670a-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="5670a-119">Le tariffe giornaliere possono essere basate sul periodo dell'anno, sulla destinazione del viaggio o su entrambi.</span><span class="sxs-lookup"><span data-stu-id="5670a-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="5670a-120">Quando definisci una regola per la diaria, puoi specificare che una percentuale della tariffa giornaliera sarà trattenuta se un lavoratore riceve vitto o servizi gratuiti.</span><span class="sxs-lookup"><span data-stu-id="5670a-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="5670a-121">Puoi inoltre definire livelli di tariffe giornaliere per impostare un numero minimo e massimo di ore che la tariffa giornaliera può applicare al viaggio di un lavoratore.</span><span class="sxs-lookup"><span data-stu-id="5670a-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="5670a-122">**Decisioni:**</span><span class="sxs-lookup"><span data-stu-id="5670a-122">**Decisions:**</span></span>

- <span data-ttu-id="5670a-123">Regole per la diaria predefinite per il primo e l'ultimo giorno:</span><span class="sxs-lookup"><span data-stu-id="5670a-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="5670a-124">Qual è il numero minimo di ore che un dipendente può richiedere per un giorno e ricevere la diaria?</span><span class="sxs-lookup"><span data-stu-id="5670a-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="5670a-125">È prevista una riduzione dell'importo offerto per i pasti del primo e dell'ultimo giorno?</span><span class="sxs-lookup"><span data-stu-id="5670a-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="5670a-126">Se c'è una riduzione, qual è la percentuale della riduzione?</span><span class="sxs-lookup"><span data-stu-id="5670a-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="5670a-127">È prevista una riduzione dell'importo offerto per l'hotel del primo e dell'ultimo giorno?</span><span class="sxs-lookup"><span data-stu-id="5670a-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="5670a-128">Se c'è una riduzione, qual è la percentuale della riduzione?</span><span class="sxs-lookup"><span data-stu-id="5670a-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="5670a-129">È prevista una riduzione dell'importo offerto per le altre spese sostenute nel primo e nell'ultimo giorno?</span><span class="sxs-lookup"><span data-stu-id="5670a-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="5670a-130">Se c'è una riduzione, qual è la percentuale della riduzione?</span><span class="sxs-lookup"><span data-stu-id="5670a-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="5670a-131">Regole per la diaria predefinite:</span><span class="sxs-lookup"><span data-stu-id="5670a-131">Default per diem rules:</span></span>

    - <span data-ttu-id="5670a-132">C'è una riduzione in percentuale della diaria giornaliera per ogni pasto se, ad esempio, il pasto è gratuito?</span><span class="sxs-lookup"><span data-stu-id="5670a-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="5670a-133">Se c'è una riduzione, qual è la percentuale della riduzione per ogni pasto?</span><span class="sxs-lookup"><span data-stu-id="5670a-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="5670a-134">La riduzione del pasto è calcolata al giorno, per viaggio o in base al numero di pasti giornalieri?</span><span class="sxs-lookup"><span data-stu-id="5670a-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="5670a-135">Gli importi giornalieri devono essere arrotondati in modo regolare o per eccesso?</span><span class="sxs-lookup"><span data-stu-id="5670a-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="5670a-136">Le diarie sono calcolate su un periodo di 24 ore o su un giorno di calendario?</span><span class="sxs-lookup"><span data-stu-id="5670a-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="5670a-137">Regole per la diaria basate sulla posizione:</span><span class="sxs-lookup"><span data-stu-id="5670a-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="5670a-138">Le tariffe per la diaria variano a seconda della località?</span><span class="sxs-lookup"><span data-stu-id="5670a-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="5670a-139">Quali località sono incluse?</span><span class="sxs-lookup"><span data-stu-id="5670a-139">What locations are included?</span></span>
    - <span data-ttu-id="5670a-140">Se le tariffe per la diaria variano a seconda della località, per ciascuna località, quale percentuale è prevista per le seguenti tipologie di spese:</span><span class="sxs-lookup"><span data-stu-id="5670a-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="5670a-141">Vitto</span><span class="sxs-lookup"><span data-stu-id="5670a-141">Meals</span></span>
        - <span data-ttu-id="5670a-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="5670a-142">Hotel</span></span>
        - <span data-ttu-id="5670a-143">Altre spese</span><span class="sxs-lookup"><span data-stu-id="5670a-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="5670a-144">Giornali di registrazione e conti di gestione delle spese</span><span class="sxs-lookup"><span data-stu-id="5670a-144">Expense management journals and accounts</span></span>

<span data-ttu-id="5670a-145">La gestione delle spese richiede l'utilizzo di più giornali di registrazione e conti.</span><span class="sxs-lookup"><span data-stu-id="5670a-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="5670a-146">È necessario decidere, ad esempio, se lo stesso conto viene utilizzato per anticipi di cassa e controversie con carte di credito.</span><span class="sxs-lookup"><span data-stu-id="5670a-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="5670a-147">**Decisioni:**</span><span class="sxs-lookup"><span data-stu-id="5670a-147">**Decisions:**</span></span>

- <span data-ttu-id="5670a-148">In quale giornale di registrazione contabile vengono registrate le note spese approvate?</span><span class="sxs-lookup"><span data-stu-id="5670a-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="5670a-149">Quale conto viene utilizzato per gli anticipi di cassa?</span><span class="sxs-lookup"><span data-stu-id="5670a-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="5670a-150">Gli anticipi di cassa devono essere registrati immediatamente?</span><span class="sxs-lookup"><span data-stu-id="5670a-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="5670a-151">Modalità di pagamento</span><span class="sxs-lookup"><span data-stu-id="5670a-151">Payment methods</span></span>

<span data-ttu-id="5670a-152">Quando si consente ai dipendenti di sostenere spese per conto dell'azienda, è necessario definire i metodi di pagamento che i dipendenti possono utilizzare.</span><span class="sxs-lookup"><span data-stu-id="5670a-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="5670a-153">Ad esempio, potresti consentire ai dipendenti di utilizzare contanti o una carta di credito aziendale.</span><span class="sxs-lookup"><span data-stu-id="5670a-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="5670a-154">Potresti anche consentire ai dipendenti di utilizzare carte di credito personali e quindi rimborsare i dipendenti.</span><span class="sxs-lookup"><span data-stu-id="5670a-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="5670a-155">È necessario prendere le seguenti decisioni per ogni metodo di pagamento consentito.</span><span class="sxs-lookup"><span data-stu-id="5670a-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="5670a-156">**Decisioni:**</span><span class="sxs-lookup"><span data-stu-id="5670a-156">**Decisions:**</span></span>

- <span data-ttu-id="5670a-157">Quali metodi di pagamento sono consentiti?</span><span class="sxs-lookup"><span data-stu-id="5670a-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="5670a-158">A chi spetta le spese del metodo di pagamento?</span><span class="sxs-lookup"><span data-stu-id="5670a-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="5670a-159">Esiste un tipo di conto di compensazione?</span><span class="sxs-lookup"><span data-stu-id="5670a-159">Is there an offset account type?</span></span> <span data-ttu-id="5670a-160">Se esiste un tipo di conto di compensazione, che cos'è?</span><span class="sxs-lookup"><span data-stu-id="5670a-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="5670a-161">Se esiste un conto di compensazione, che cos'è il conto?</span><span class="sxs-lookup"><span data-stu-id="5670a-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="5670a-162">Se il metodo di pagamento è una carta di credito, il metodo di pagamento deve essere utilizzato solo con le transazioni importate?</span><span class="sxs-lookup"><span data-stu-id="5670a-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="5670a-163">Categorie di spesa e categorie condivise</span><span class="sxs-lookup"><span data-stu-id="5670a-163">Expense categories and shared categories</span></span>

<span data-ttu-id="5670a-164">Quando i dipendenti creano una nota spese, ogni spesa che registrano deve essere associata a una categoria di spesa.</span><span class="sxs-lookup"><span data-stu-id="5670a-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="5670a-165">Le categorie di spesa derivano da categorie condivise che possono essere condivise tra le persone giuridiche dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5670a-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="5670a-166">Queste categorie possono anche essere condivise in Gestione progetti e contabilità, a seconda del modo in cui è definita l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5670a-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="5670a-167">In base alla definizione dell'organizzazione e alle linee guida del team di implementazione, è necessario determinare se le categorie utilizzate nella gestione delle spese verranno utilizzate solo in Gestione spese o se debbano essere condivise tra Gestione progetti e contabilità e Gestione spese.</span><span class="sxs-lookup"><span data-stu-id="5670a-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="5670a-168">Nota che queste categorie possono essere condivise tra progetto e spesa o progetto e produzione e non tra spesa e produzione.</span><span class="sxs-lookup"><span data-stu-id="5670a-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="5670a-169">È necessario prendere le seguenti decisioni per ciascuna categoria di spesa.</span><span class="sxs-lookup"><span data-stu-id="5670a-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="5670a-170">**Decisioni:**</span><span class="sxs-lookup"><span data-stu-id="5670a-170">**Decisions:**</span></span>

- <span data-ttu-id="5670a-171">Qual è la categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="5670a-171">What is the expense category?</span></span> <span data-ttu-id="5670a-172">Gli esempi includono categorie per voli, hotel o chilometraggio.</span><span class="sxs-lookup"><span data-stu-id="5670a-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="5670a-173">La categoria di spesa può essere utilizzata anche in Gestione progetti e contabilità?</span><span class="sxs-lookup"><span data-stu-id="5670a-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="5670a-174">Qual è il tipo di spesa?</span><span class="sxs-lookup"><span data-stu-id="5670a-174">What is the expense type?</span></span>
- <span data-ttu-id="5670a-175">Qual è il metodo di pagamento predefinito per la categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="5670a-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="5670a-176">Le spese nella categoria di spesa devono essere dettagliate?</span><span class="sxs-lookup"><span data-stu-id="5670a-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="5670a-177">Qual è il conto predefinito principale per la categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="5670a-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="5670a-178">Qual è la fascia IVA articoli predefinita per la categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="5670a-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="5670a-179">Sono consentiti metodi di pagamento aggiuntivi per la categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="5670a-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="5670a-180">Se sono consentiti metodi di pagamento aggiuntivi, quali sono?</span><span class="sxs-lookup"><span data-stu-id="5670a-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="5670a-181">Ci sono sottocategorie in questa categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="5670a-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="5670a-182">In caso affermativo, devi anche prendere le decisioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5670a-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="5670a-183">Alcune delle sottocategorie sono escluse dal recupero IVA?</span><span class="sxs-lookup"><span data-stu-id="5670a-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="5670a-184">Qual è la fascia IVA articoli delle sottocategorie?</span><span class="sxs-lookup"><span data-stu-id="5670a-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="5670a-185">Se la categoria di spesa viene utilizzata anche in Gestione progetti e contabilità, rispondi alle domande rimanenti.</span><span class="sxs-lookup"><span data-stu-id="5670a-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="5670a-186">Altrimenti, vai alla sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="5670a-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="5670a-187">Quali conti di costo verranno utilizzati per le seguenti spese?</span><span class="sxs-lookup"><span data-stu-id="5670a-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="5670a-188">Costo</span><span class="sxs-lookup"><span data-stu-id="5670a-188">Cost</span></span>
    - <span data-ttu-id="5670a-189">Allocazione retribuzioni</span><span class="sxs-lookup"><span data-stu-id="5670a-189">Payroll allocation</span></span>
    - <span data-ttu-id="5670a-190">WIP - valore costo</span><span class="sxs-lookup"><span data-stu-id="5670a-190">WIP-cost value</span></span>
    - <span data-ttu-id="5670a-191">Elemento di costo</span><span class="sxs-lookup"><span data-stu-id="5670a-191">Cost-item</span></span>
    - <span data-ttu-id="5670a-192">WIP - elemento valore di costo</span><span class="sxs-lookup"><span data-stu-id="5670a-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="5670a-193">Perdita maturata</span><span class="sxs-lookup"><span data-stu-id="5670a-193">Accrued loss</span></span>
    - <span data-ttu-id="5670a-194">WIP - perdita maturata</span><span class="sxs-lookup"><span data-stu-id="5670a-194">WIP-accrued loss</span></span>

- <span data-ttu-id="5670a-195">Quali ricavi di costo verranno utilizzati per le seguenti opzioni?</span><span class="sxs-lookup"><span data-stu-id="5670a-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="5670a-196">Ricavi fatturati</span><span class="sxs-lookup"><span data-stu-id="5670a-196">Invoiced revenue</span></span>
    - <span data-ttu-id="5670a-197">Ricavi maturati - valore delle vendite</span><span class="sxs-lookup"><span data-stu-id="5670a-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="5670a-198">WIP - valore delle vendite</span><span class="sxs-lookup"><span data-stu-id="5670a-198">WIP-sales value</span></span>
    - <span data-ttu-id="5670a-199">Ricavi maturati - produzione</span><span class="sxs-lookup"><span data-stu-id="5670a-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="5670a-200">WIP - produzione</span><span class="sxs-lookup"><span data-stu-id="5670a-200">WIP-production</span></span>
    - <span data-ttu-id="5670a-201">Ricavi maturati - profitti</span><span class="sxs-lookup"><span data-stu-id="5670a-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="5670a-202">WIP - profitti</span><span class="sxs-lookup"><span data-stu-id="5670a-202">WIP-profit</span></span>
    - <span data-ttu-id="5670a-203">Ricavi maturati - abbonamento</span><span class="sxs-lookup"><span data-stu-id="5670a-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="5670a-204">WIP - abbonamento</span><span class="sxs-lookup"><span data-stu-id="5670a-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="5670a-205">Imposte</span><span class="sxs-lookup"><span data-stu-id="5670a-205">Taxes</span></span>

<span data-ttu-id="5670a-206">Per le imposte relative alle spese, è necessario determinare cosa è incluso o abilitato nelle note spese.</span><span class="sxs-lookup"><span data-stu-id="5670a-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="5670a-207">**Decisioni:**</span><span class="sxs-lookup"><span data-stu-id="5670a-207">**Decisions:**</span></span>

- <span data-ttu-id="5670a-208">L'IVA è inclusa negli importi delle spese?</span><span class="sxs-lookup"><span data-stu-id="5670a-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="5670a-209">Il recupero dell'IVA deve essere abilitato sulle spese?</span><span class="sxs-lookup"><span data-stu-id="5670a-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="5670a-210">Se quando hai pianificato la contabilità generale hai deciso di applicare l'IVA statunitense e utilizzare le regole fiscali, non puoi abilitare il recupero dell'IVA sulle spese.</span><span class="sxs-lookup"><span data-stu-id="5670a-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="5670a-211">(Per applicare l'IVA negli Stati Uniti e utilizzare le regole fiscali, imposta l'opzione **Applica le regole di tassazione IVA** su **Sì**.)</span><span class="sxs-lookup"><span data-stu-id="5670a-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="5670a-212">Criteri</span><span class="sxs-lookup"><span data-stu-id="5670a-212">Policies</span></span>

<span data-ttu-id="5670a-213">Creando criteri di nota spese, puoi aiutare la tua organizzazione a risparmiare tempo e denaro quando i dipendenti sostengono le spese per suo conto.</span><span class="sxs-lookup"><span data-stu-id="5670a-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="5670a-214">I criteri aiutano a garantire che i dipendenti rispettino il budget, forniscano tutte le informazioni richieste e spendano denaro solo quando necessario.</span><span class="sxs-lookup"><span data-stu-id="5670a-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="5670a-215">È necessario prendere le seguenti decisioni per ogni criterio della nota spese e ogni criterio di approvazione della nota spese creato.</span><span class="sxs-lookup"><span data-stu-id="5670a-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="5670a-216">**Decisioni:**</span><span class="sxs-lookup"><span data-stu-id="5670a-216">**Decisions:**</span></span>

- <span data-ttu-id="5670a-217">Qual è il nome del criterio?</span><span class="sxs-lookup"><span data-stu-id="5670a-217">What is the name of the policy?</span></span>
- <span data-ttu-id="5670a-218">A cosa serve il criterio di spesa?</span><span class="sxs-lookup"><span data-stu-id="5670a-218">What is the expense policy for?</span></span>
- <span data-ttu-id="5670a-219">Se in precedenza hai deciso di abilitare le spese interaziendali, a quali società della tua organizzazione verrà applicato questo criterio?</span><span class="sxs-lookup"><span data-stu-id="5670a-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="5670a-220">Quando entra in vigore il criterio?</span><span class="sxs-lookup"><span data-stu-id="5670a-220">When does the policy become effective?</span></span>
- <span data-ttu-id="5670a-221">Quando scade il criterio?</span><span class="sxs-lookup"><span data-stu-id="5670a-221">When does the policy expire?</span></span>
- <span data-ttu-id="5670a-222">Qual è la regola dei criteri?</span><span class="sxs-lookup"><span data-stu-id="5670a-222">What is the policy rule?</span></span>
- <span data-ttu-id="5670a-223">Qual è il risultato della regola dei criteri?</span><span class="sxs-lookup"><span data-stu-id="5670a-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]