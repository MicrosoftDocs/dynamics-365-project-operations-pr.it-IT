---
title: Acquistare materiali non stoccati con una fattura fornitore in sospeso
description: Questo argomento spiega come registrare le fatture fornitore in sospeso.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880656"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="40800-103">Acquistare materiali non stoccati con una fattura fornitore in sospeso</span><span class="sxs-lookup"><span data-stu-id="40800-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="40800-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="40800-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="40800-105">Poiché un'azienda acquista materiali non stoccati per un progetto, i costi possono essere immediatamente registrati a fronte del progetto.</span><span class="sxs-lookup"><span data-stu-id="40800-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="40800-106">Per esempio, Contoso Robotics US sta eseguendo un progetto di rinnovo delle apparecchiature e necessita di licenze software.</span><span class="sxs-lookup"><span data-stu-id="40800-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="40800-107">Queste licenze vengono acquistate da un fornitore di terze parti.</span><span class="sxs-lookup"><span data-stu-id="40800-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="40800-108">Utilizzando Dynamics 365 Finance, l'addetto alla contabilità fornitori registra un documento di fattura fornitore in sospeso e attribuisce i costi della licenza direttamente al progetto di rinnovo dell'attrezzatura.</span><span class="sxs-lookup"><span data-stu-id="40800-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="40800-109">Prima di utilizzare la funzionalità descritta in questo argomento, esamina e applica le configurazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="40800-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="40800-110">Per ulteriori informazioni, vedi [Abilitare materiali non stoccati e fatture fornitore in sospeso](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="40800-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="40800-111">Registrare una fattura fornitore in sospeso relativa al progetto</span><span class="sxs-lookup"><span data-stu-id="40800-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="40800-112">Le fatture fornitore in sospeso possono essere registrate nella pagina **Fatture fornitore in sospeso** (**Contabilità fornitori** > **Fatture** > **Fatture fornitore in sospeso**).</span><span class="sxs-lookup"><span data-stu-id="40800-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="40800-113">Completa i seguenti passaggi per registrare una fattura fornitore in sospeso relativa al progetto:</span><span class="sxs-lookup"><span data-stu-id="40800-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="40800-114">Vai a **Contabilità fornitori** > **Fatture** e seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="40800-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="40800-115">Nel campo **Conto fattura** seleziona un fornitore e nel campo **Numero**, immetti l'identificazione della fattura del fornitore.</span><span class="sxs-lookup"><span data-stu-id="40800-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="40800-116">Aggiungi una riga alla fattura fornitore e nel campo **Codice articolo** seleziona l'articolo non stoccato acquistato dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="40800-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="40800-117">Le righe della fattura fornitore basate su una categoria di approvvigionamento non possono essere registrate nel progetto.</span><span class="sxs-lookup"><span data-stu-id="40800-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="40800-118">Aggiungi la quantità acquistata.</span><span class="sxs-lookup"><span data-stu-id="40800-118">Add the quantity purchased.</span></span> <span data-ttu-id="40800-119">Il sistema popolerà il prezzo unitario in base alla configurazione del prezzo dell'articolo non stoccato.</span><span class="sxs-lookup"><span data-stu-id="40800-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="40800-120">Verifica l'importo totale e altri dettagli richiesti sulla riga.</span><span class="sxs-lookup"><span data-stu-id="40800-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="40800-121">Nei dettagli della linea, nella scheda **Progetto** seleziona l'ID del progetto in cui verrà registrato l'elemento.</span><span class="sxs-lookup"><span data-stu-id="40800-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="40800-122">Facoltativamente, seleziona il numero dell'attività e aggiorna la categoria del progetto e la proprietà della riga.</span><span class="sxs-lookup"><span data-stu-id="40800-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="40800-123">Registra la fattura fornitore in sospeso.</span><span class="sxs-lookup"><span data-stu-id="40800-123">Post pending vendor invoice.</span></span> <span data-ttu-id="40800-124">Quando la fattura viene registrata, il sistema registra:</span><span class="sxs-lookup"><span data-stu-id="40800-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="40800-125">L'importo del saldo del fornitore.</span><span class="sxs-lookup"><span data-stu-id="40800-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="40800-126">L'importo dell'IVA.</span><span class="sxs-lookup"><span data-stu-id="40800-126">The sales tax amount.</span></span>
    - <span data-ttu-id="40800-127">Il costo relativo al progetto viene registrato nel conto di integrazione dell'approvvigionamento.</span><span class="sxs-lookup"><span data-stu-id="40800-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="40800-128">La transazione effettiva del progetto in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="40800-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="40800-129">Questa transazione viene ulteriormente elaborata utilizzando il [giornale di integrazione Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="40800-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="40800-130">La registrazione di questo giornale di registrazione sposta l'importo dal conto di integrazione dell'approvvigionamento al conto dei costi del progetto.</span><span class="sxs-lookup"><span data-stu-id="40800-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
