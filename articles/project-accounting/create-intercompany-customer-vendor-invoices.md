---
title: Creare fatture interaziendali per clienti e fornitori
description: Questo argomento fornisce informazioni su come creare fatture fornitori e clienti interaziendali.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595496"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a><span data-ttu-id="93c05-103">Creare fatture interaziendali per clienti e fornitori</span><span class="sxs-lookup"><span data-stu-id="93c05-103">Create intercompany customer and vendor invoices</span></span>

<span data-ttu-id="93c05-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="93c05-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="93c05-105">Un contabile di progetto in una persona giuridica che effettua la concessione crea una fattura cliente interaziendale per i costi del progetto che vengono trasferiti all'entità richiedente.</span><span class="sxs-lookup"><span data-stu-id="93c05-105">A project accountant in a lending legal entity creates an intercompany customer invoice for the project costs that are being transferred to the borrowing entity.</span></span> <span data-ttu-id="93c05-106">Dopo che la fattura cliente interaziendale è stata approvata e registrata, la persona giuridica che effettua la concessione invia la fattura interaziendale alla persona giuridica richiedente.</span><span class="sxs-lookup"><span data-stu-id="93c05-106">After the intercompany customer invoice is approved and posted, the lending legal entity sends the intercompany invoice to the borrowing legal entity.</span></span>

<span data-ttu-id="93c05-107">Il contabile di progetto per la persona giuridica che effettua la concessione può impostare un processo batch per generare fatture interaziendali su base ricorrente.</span><span class="sxs-lookup"><span data-stu-id="93c05-107">The project accountant for the lending legal entity can set up a batch process to generate intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="93c05-108">Il contabile di progetto specifica i criteri, ad esempio progetti specifici, per creare fatture interaziendali in un batch.</span><span class="sxs-lookup"><span data-stu-id="93c05-108">The project accountant specifies the criteria, such as specific projects, to create intercompany invoices in a batch.</span></span>

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a><span data-ttu-id="93c05-109">Creare manualmente una fattura cliente interaziendale per le transazioni di progetto</span><span class="sxs-lookup"><span data-stu-id="93c05-109">Manually create an intercompany customer invoice for project transactions</span></span> 

<span data-ttu-id="93c05-110">Utilizzare questa procedura per creare manualmente una fattura cliente interaziendale per le transazioni di progetto.</span><span class="sxs-lookup"><span data-stu-id="93c05-110">Use this procedure to manually create an intercompany customer invoice for project transactions.</span></span> <span data-ttu-id="93c05-111">Cerca le ore registrate dai lavoratori sui progetti nelle persone giuridiche che effettuano la concessione e le spese sostenute dalla persona giuridica per conto delle persone giuridiche richiedenti.</span><span class="sxs-lookup"><span data-stu-id="93c05-111">Search for hours that were posted by workers on projects in the borrowing legal entities and for expenses that were incurred by your legal entity on behalf of borrowing legal entities.</span></span> <span data-ttu-id="93c05-112">È possibile eseguire la ricerca per nome della persona giuridica, numero di contratto di progetto, numero di progetto, intervallo di date o qualsiasi combinazione di queste opzioni.</span><span class="sxs-lookup"><span data-stu-id="93c05-112">You can search by legal entity name, project contract number, project number, date range, or any combination of these options.</span></span> <span data-ttu-id="93c05-113">Nei risultati della ricerca selezionare le transazioni da aggiungere a una fattura interaziendale.</span><span class="sxs-lookup"><span data-stu-id="93c05-113">In the search results, select the transactions to add to an intercompany invoice.</span></span>

1. <span data-ttu-id="93c05-114">In Dynamics 365 Finance, vai a **Contabilità e gestione dei progetti** > **Fatture di progetto** > **Fatture cliente interaziendale**.</span><span class="sxs-lookup"><span data-stu-id="93c05-114">In Dynamics 365 Finance, go to **Project management and accounting** > **Project invoices** > **Intercompany customer invoices**.</span></span> <span data-ttu-id="93c05-115">Nella pagina dell'elenco **Fatture clienti interaziendali**, nel riquadro azioni selezionare **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="93c05-115">On the **Intercompany customer invoices**  list page, on the Action Pane, select **New.**</span></span>
2. <span data-ttu-id="93c05-116">Nella pagina **Crea fattura interaziendale**, nel campo **Entità legale**, selezionare una persona giuridica richiedente.</span><span class="sxs-lookup"><span data-stu-id="93c05-116">On the **Create intercompany invoice** page, in the **Legal entity** field, select a borrowing legal entity.</span></span>
3. <span data-ttu-id="93c05-117">Facoltativo: immettere un contratto di progetto specifico e un numero di progetto.</span><span class="sxs-lookup"><span data-stu-id="93c05-117">Optional: Enter a specific project contract and project number.</span></span>
4. <span data-ttu-id="93c05-118">Restringere la ricerca selezionando un intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="93c05-118">Narrow the search by selecting a date range.</span></span> <span data-ttu-id="93c05-119">Immettere date specifiche nei campi **Data d'inizio** e **Data di fine**.</span><span class="sxs-lookup"><span data-stu-id="93c05-119">Enter specific dates in the **Start date** and **End date** fields.</span></span> <span data-ttu-id="93c05-120">Nei risultati della ricerca vengono visualizzate solo le transazioni interaziendali registrate in questo intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="93c05-120">Only intercompany transactions that are posted within this date range are displayed in the search results.</span></span>
5. <span data-ttu-id="93c05-121">Imposta **Parametro della riga di giornale di registrazione avanzata del progetto** su **Sì** e seleziona **Ricerca**.</span><span class="sxs-lookup"><span data-stu-id="93c05-121">Set **Project advanced journal line parameter** to **Yes** and select **Search**.</span></span>
6. <span data-ttu-id="93c05-122">Nei risultati della ricerca, seleziona le transazioni da includere nella proposta di fatturazione interaziendale, quindi seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c05-122">In the search results, select the transactions to include in the intercompany invoice proposal, and then select **OK**.</span></span>
7. <span data-ttu-id="93c05-123">Nella pagina **Fattura cliente interaziendale**, vengono visualizzate le transazioni del progetto interaziendale selezionate dai risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="93c05-123">On the **Intercompany customer invoice** page, the intercompany project transactions that you selected from the search results are displayed.</span></span> <span data-ttu-id="93c05-124">Per modificare le transazioni prima di inviare la fattura alla persona giuridica richiedente, effettuare le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="93c05-124">To modify the transactions before you send the invoice to the borrowing legal entity, do the following:</span></span>
  
    1. <span data-ttu-id="93c05-125">Aprire la pagina **Crea proposta di fattura**.</span><span class="sxs-lookup"><span data-stu-id="93c05-125">Open the **Create invoice proposal** page.</span></span> <span data-ttu-id="93c05-126">Seleziona ulteriori transazioni interaziendali per la fattura corrente, quindi seleziona **Aggiungi riga**.</span><span class="sxs-lookup"><span data-stu-id="93c05-126">Select additional intercompany transactions for the current invoice, and then select **Add line**.</span></span>
    2. <span data-ttu-id="93c05-127">Per rimuovere una riga, selezionarla, quindi selezionare **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="93c05-127">To remove a line, select it, and then select **Remove**.</span></span>
    3. <span data-ttu-id="93c05-128">Visualizza commenti, motivi, dimensioni finanziarie e altre informazioni su una selezionata nella scheda dettaglio **Righe fattura**.</span><span class="sxs-lookup"><span data-stu-id="93c05-128">View comments, reasons, financial dimensions, and other information about a selected line on the  **Invoice lines**  FastTab.</span></span>
    
8. <span data-ttu-id="93c05-129">Per registrare la fattura cliente interaziendale, nel riquadro azioni, seleziona **Registra**.</span><span class="sxs-lookup"><span data-stu-id="93c05-129">To post the intercompany customer invoice, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="93c05-130">Se la tua organizzazione richiede che le fatture interaziendali vengano riviste prima di essere registrate, un amministratore di sistema potrebbe impostare un flusso di lavoro per le fatture interaziendali.</span><span class="sxs-lookup"><span data-stu-id="93c05-130">If your organization requires that intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="93c05-131">Se un flusso di lavoro non è impostato per le fatture interaziendali, è possibile registrare la fattura interaziendale.</span><span class="sxs-lookup"><span data-stu-id="93c05-131">If a workflow is not set up for intercompany invoices, you can post the intercompany invoice.</span></span>

## <a name="create-a-batch-job-for-intercompany-invoices"></a><span data-ttu-id="93c05-132">Crea un processo batch per le fatture interaziendali</span><span class="sxs-lookup"><span data-stu-id="93c05-132">Create a batch job for intercompany invoices</span></span>

<span data-ttu-id="93c05-133">Puoi creare più fatture interaziendali contemporaneamente per tutte le persone giuridiche che effettuano la concessione.</span><span class="sxs-lookup"><span data-stu-id="93c05-133">You can create multiple intercompany invoices at the same time for all borrowing legal entities.</span></span> <span data-ttu-id="93c05-134">Utilizzando la funzionalità di ricerca, è possibile, ad esempio, cercare tutte le transazioni registrate da lavoratori in prestito e correlate a progetti gestiti da altre persone giuridiche.</span><span class="sxs-lookup"><span data-stu-id="93c05-134">Using search functionality, you can for example, search for all transactions that are posted by borrowed workers and related to projects that are managed by other legal entities.</span></span> <span data-ttu-id="93c05-135">Quindi, per ciascuna persona giuridica che richiedente, è possibile creare una fattura interaziendale per le transazioni fornite nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="93c05-135">Then, for each borrowing legal entity, you can create an intercompany invoice for the transactions provided in the search results.</span></span>

1. <span data-ttu-id="93c05-136">Vai a **Contabilità e gestione dei progetti** > **Periodico** > **Fatture progetto** > **Crea fatture interaziendali per clienti**.</span><span class="sxs-lookup"><span data-stu-id="93c05-136">Go to **Project management and accounting** > **Periodic** > **Project invoices** > **Create intercompany customer invoices**.</span></span>
2. <span data-ttu-id="93c05-137">Nella pagina **Crea fatture cliente interaziendali**, nel campo **Azienda**, selezionare una persona giuridica da fatturare.</span><span class="sxs-lookup"><span data-stu-id="93c05-137">On the **Create intercompany customer invoices** page, in the **Company**  field, select a legal entity to invoice.</span></span> <span data-ttu-id="93c05-138">Se non si seleziona una società, tutte le transazioni che soddisfano i criteri di ricerca vengono visualizzate per tutte le persone giuridiche che effettuano la concessione.</span><span class="sxs-lookup"><span data-stu-id="93c05-138">If you don't select a company, all transactions that meet the search criteria are displayed for all borrowing legal entities.</span></span>
3. <span data-ttu-id="93c05-139">In **Crea una fattura per**, seleziona se creare una fattura per transazioni interaziendali basate su un progetto o su una persona giuridica richiedente.</span><span class="sxs-lookup"><span data-stu-id="93c05-139">In **Create one invoice per**, select whether to create an invoice for intercompany transactions based on a project or based on a borrowing legal entity.</span></span>
4. <span data-ttu-id="93c05-140">Facoltativo: per selezionare un progetto specifico e un contratto di progetto per cui creare fatture interaziendali, fare clic su **Seleziona**.</span><span class="sxs-lookup"><span data-stu-id="93c05-140">Optional: To select a specific project and project contract to create intercompany invoices for, click **Select**.</span></span> <span data-ttu-id="93c05-141">Nella pagina **Richiesta di informazioni**, nel campo **Criteri**, seleziona il contratto di progetto, il numero di progetto o entrambi, quindi seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c05-141">On the **Inquiry** page, in the **Criteria** field, select the project contract, project number, or both, and then select **OK**.</span></span>
5. <span data-ttu-id="93c05-142">Nella scheda **Batch**, imposta un processo batch per creare fatture interaziendali su base ricorrente.</span><span class="sxs-lookup"><span data-stu-id="93c05-142">On the **Batch** tab, set up a batch process to create intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="93c05-143">Per ulteriori informazioni, vedi [Invia un processo di elaborazione batch da un modulo](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).</span><span class="sxs-lookup"><span data-stu-id="93c05-143">For more information, see [Submit a batch processing job from a form](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).</span></span>
6. <span data-ttu-id="93c05-144">Per registrare le fatture interaziendali, nel riquadro azioni, seleziona **Registra**.</span><span class="sxs-lookup"><span data-stu-id="93c05-144">To post the intercompany invoices, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="93c05-145">Se la tua organizzazione richiede che le fatture interaziendali vengano riviste prima di essere registrate, un amministratore di sistema potrebbe impostare un flusso di lavoro per le fatture interaziendali.</span><span class="sxs-lookup"><span data-stu-id="93c05-145">If your organization requires intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="93c05-146">Se un flusso di lavoro non è impostato per le fatture interaziendali, è possibile registrare le fatture interaziendali.</span><span class="sxs-lookup"><span data-stu-id="93c05-146">If a workflow is not set up for intercompany invoices, you can post the intercompany invoices.</span></span>

## <a name="post-the-intercompany-vendor-invoice"></a><span data-ttu-id="93c05-147">Registrare la fattura fornitore interaziendale</span><span class="sxs-lookup"><span data-stu-id="93c05-147">Post the intercompany vendor invoice</span></span>

<span data-ttu-id="93c05-148">Un contabile di progetto nella persona giuridica richiedente può rivedere le fatture fornitore interaziendali in sospeso quando viene registrata la fattura cliente interaziendale corrispondente.</span><span class="sxs-lookup"><span data-stu-id="93c05-148">A project accountant in the borrowing legal entity can review intercompany pending vendor invoices when the corresponding intercompany customer invoice is posted.</span></span> <span data-ttu-id="93c05-149">In Finance, nella persona giuridica richiedente, vai a **Contabilità fornitori** > **Fatture** > **Fattura fornitore in sospeso**.</span><span class="sxs-lookup"><span data-stu-id="93c05-149">In Finance, in the borrowing legal entity, go to **Accounts payable** > **Invoices** > **Pending vendor invoice**.</span></span> <span data-ttu-id="93c05-150">Il numero della fattura in sospeso corrisponderà al numero della fattura del cliente interaziendale.</span><span class="sxs-lookup"><span data-stu-id="93c05-150">The pending invoice number will match the intercompany customer invoice number.</span></span> <span data-ttu-id="93c05-151">Verifica che la fattura sia corretta, quindi registra la fattura.</span><span class="sxs-lookup"><span data-stu-id="93c05-151">Verify that the invoice is correct and then post the invoice.</span></span> <span data-ttu-id="93c05-152">La registrazione di una fattura fornitore interaziendale crea un registro secondario del progetto e una transazione di contabilità generale che riflette i costi di transazione nella persona giuridica debitrice.</span><span class="sxs-lookup"><span data-stu-id="93c05-152">Posting intercompany vendor invoice creates a project subledger and a general ledger transaction that reflects the transaction costs in the borrowing legal entity.</span></span>