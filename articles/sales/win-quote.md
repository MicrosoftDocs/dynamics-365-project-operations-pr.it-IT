---
title: Chiudere un'offerta
description: Questo argomento fornisce informazioni sulla chiusura delle offerte in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2c752ba6395ed4bf025092219350dc245f7428f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277253"
---
# <a name="close-a-quote"></a><span data-ttu-id="c32f2-103">Chiudere un'offerta</span><span class="sxs-lookup"><span data-stu-id="c32f2-103">Close a quote</span></span>

<span data-ttu-id="c32f2-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="c32f2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c32f2-105">Un'offerta di progetto può essere chiusa come acquisita o persa.</span><span class="sxs-lookup"><span data-stu-id="c32f2-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="c32f2-106">Dal momento che le funzioni Attiva e Revisiona non sono supportate nelle offerte in Microsoft Dynamics 365 Project Operations, puoi chiudere un'offerta in bozza.</span><span class="sxs-lookup"><span data-stu-id="c32f2-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="c32f2-107">Chiudere un'offerta come acquisita</span><span class="sxs-lookup"><span data-stu-id="c32f2-107">Close a quote as Won</span></span>

<span data-ttu-id="c32f2-108">La chiusura di un'offerta di progetto come acquisita imposterà lo stato dell'offerta su **Chiusa** e il motivo stato **Acquisita**.</span><span class="sxs-lookup"><span data-stu-id="c32f2-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="c32f2-109">La chiusura dell'offerta la rende di sola lettura e crea un contratto di progetto in bozza con tutte le informazioni sull'offerta.</span><span class="sxs-lookup"><span data-stu-id="c32f2-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="c32f2-110">Poiché un'offerta chiusa non può essere riaperta, prima di chiudere un'offerta una finestra di dialogo di conferma confermerà le modifiche.</span><span class="sxs-lookup"><span data-stu-id="c32f2-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="c32f2-111">Il contratto di progetto creato da un'offerta di progetto è disponibile anche nel modulo Gestione progetti e contabilità di Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c32f2-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="c32f2-112">Se un contratto di progetto non è mappato a un progetto su nessuna delle voci, questo contratto di progetto viene reso disponibile come contratto di progetto inattivo e diventa attivo non appena un progetto viene mappato su almeno una delle voci di contratto.</span><span class="sxs-lookup"><span data-stu-id="c32f2-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="c32f2-113">Se l'offerta è collegata a un'opportunità, qualsiasi altra offerta di progetto dell'opportunità viene automaticamente chiusa come persa.</span><span class="sxs-lookup"><span data-stu-id="c32f2-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="c32f2-114">Impatto finanziario della chiusura di un'offerta come acquisita</span><span class="sxs-lookup"><span data-stu-id="c32f2-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="c32f2-115">Se sono stati registrati dei valori effettivi per il tempo in un progetto mentre è ancora collegato a un'offerta in bozza, viene registrato solo il costo del tempo o della spesa.</span><span class="sxs-lookup"><span data-stu-id="c32f2-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="c32f2-116">Dopo che un'offerta è stata chiusa come acquisita, l'applicazione effettuerà il refactoring dei costi annullando i valori effettivi di costo precedenti e ricreando nuovi valori effettivi di costo.</span><span class="sxs-lookup"><span data-stu-id="c32f2-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="c32f2-117">L'applicazione elaborerà questi valori effettivi di costo in base al metodo di fatturazione della voce di contratto di progetto associata.</span><span class="sxs-lookup"><span data-stu-id="c32f2-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="c32f2-118">Se i valori effettivi di costo fanno riferimento a una voce di contratto di tempistica e materiali, il sistema creerà automaticamente i valori effettivi di vendita non fatturati corrispondenti quando l'offerta viene chiusa e il contratto di progetto viene creato.</span><span class="sxs-lookup"><span data-stu-id="c32f2-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="c32f2-119">Se i valori effettivi di costo fanno riferimento a una voce di contratto a prezzo fisso, l'applicazione interromperà la rielaborazione dei valori effettivi di costo in base alle regole di fatturazione separata per i clienti del contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="c32f2-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="c32f2-120">Tutti i valori effettivi rielaborati sono disponibili nel modulo Gestione progetti e contabilità affinché il contabile del progetto possa rivederli, aggiornarli e registrarli nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="c32f2-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="c32f2-121">Chiudere un'offerta come persa</span><span class="sxs-lookup"><span data-stu-id="c32f2-121">Close a quote as Lost</span></span>

<span data-ttu-id="c32f2-122">La chiusura di un'offerta come persa imposterà lo stato su **Chiusa** e il motivo stato su **Persa**.</span><span class="sxs-lookup"><span data-stu-id="c32f2-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="c32f2-123">La chiusura dell'offerta la rende di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c32f2-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="c32f2-124">Poiché un'offerta chiusa non può essere riaperta, prima di chiudere un'offerta una finestra di dialogo di conferma confermerà le modifiche.</span><span class="sxs-lookup"><span data-stu-id="c32f2-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="c32f2-125">Se l'offerta di progetto chiusa come persa fa riferimento a un progetto in una delle sue righe, anche quel progetto viene contrassegnato come chiuso e tutte le prenotazioni di risorse da quel giorno in poi vengono annullate.</span><span class="sxs-lookup"><span data-stu-id="c32f2-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="c32f2-126">In Project Operations, la chiusura di un'offerta come acquisita o persa non influirà sullo stato dell'opportunità, che rimarrà aperta fino a quando non verrà chiusa manualmente.</span><span class="sxs-lookup"><span data-stu-id="c32f2-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]