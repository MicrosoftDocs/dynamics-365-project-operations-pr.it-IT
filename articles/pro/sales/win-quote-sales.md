---
title: Chiudere un'offerta - semplice
description: Questo argomento fornisce informazioni sulla chiusura di un'offerta in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272283"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="73651-103">Chiudere un'offerta - semplice</span><span class="sxs-lookup"><span data-stu-id="73651-103">Close a quote - lite</span></span>

<span data-ttu-id="73651-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="73651-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="73651-105">Un'offerta di progetto può essere chiusa come acquisita o persa.</span><span class="sxs-lookup"><span data-stu-id="73651-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="73651-106">Una bozza di offerta può essere chiusa perché le operazioni di attivazione e revisione sulle offerte non sono supportate in Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="73651-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="73651-107">Chiudere un'offerta come acquisita</span><span class="sxs-lookup"><span data-stu-id="73651-107">Close a quote as Won</span></span>

<span data-ttu-id="73651-108">Quando chiudi un'offerta di progetto come Acquisita, lo stato viene impostato su Chiuso e il motivo dello stato è Acquisito.</span><span class="sxs-lookup"><span data-stu-id="73651-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="73651-109">La chiusura dell'offerta rende l'offerta di progetto di sola lettura e crea un contratto di progetto in bozza che contiene le informazioni sull'offerta.</span><span class="sxs-lookup"><span data-stu-id="73651-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="73651-110">Poiché un'offerta chiusa non può essere riaperta, una finestra di dialogo chiederà di confermare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="73651-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="73651-111">Se l'offerta è collegata a un'opportunità, qualsiasi altra offerta di progetto dell'opportunità viene automaticamente chiusa come persa.</span><span class="sxs-lookup"><span data-stu-id="73651-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="73651-112">Impatto finanziario della chiusura di un'offerta come acquisita</span><span class="sxs-lookup"><span data-stu-id="73651-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="73651-113">Se sono presenti valori effettivi per l'ora in un progetto mentre è ancora collegato a una bozza di offerta, viene registrato solo il costo dell'ora o della spesa.</span><span class="sxs-lookup"><span data-stu-id="73651-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="73651-114">Dopo che un'offerta è stata chiusa come acquisita, l'applicazione effettuerà il refactoring dei costi annullando i valori effettivi di costo precedenti e ricreando nuovi valori effettivi di costo.</span><span class="sxs-lookup"><span data-stu-id="73651-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="73651-115">L'applicazione elaborerà questi valori effettivi di costo in base al metodo di fatturazione della voce di contratto di progetto associata.</span><span class="sxs-lookup"><span data-stu-id="73651-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="73651-116">Se i valori effettivi dei costi fanno riferimento a una riga di contratto di tempo e materiali, vengono creati i valori effettivi di vendita non fatturati corrispondenti per quando l'offerta viene chiusa e il contratto di progetto viene creato.</span><span class="sxs-lookup"><span data-stu-id="73651-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="73651-117">Se i costi effettivi fanno riferimento a una riga di contratto a prezzo fisso, l'applicazione interromperà la rielaborazione dei costi effettivi basati sulle regole di fatturazione suddivisa per i clienti del contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="73651-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="73651-118">Chiusura di un'offerta come persa:</span><span class="sxs-lookup"><span data-stu-id="73651-118">Closing a quote as lost:</span></span>

<span data-ttu-id="73651-119">Quando chiudi un'offerta di progetto come Persa, lo stato viene impostato su Chiuso e il motivo dello stato è Perso.</span><span class="sxs-lookup"><span data-stu-id="73651-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="73651-120">La chiusura dell'offerta rende l'offerta di progetto di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="73651-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="73651-121">Poiché un'offerta chiusa non può essere riaperta, prima di chiudere un'offerta una finestra di dialogo di conferma confermerà le modifiche.</span><span class="sxs-lookup"><span data-stu-id="73651-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="73651-122">Se l'offerta di progetto chiusa come Persa fa riferimento a un progetto in una delle sue righe, anche quel progetto viene contrassegnato come Chiuso.</span><span class="sxs-lookup"><span data-stu-id="73651-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="73651-123">Qualsiasi prenotazione di risorse da quel giorno in poi viene annullata.</span><span class="sxs-lookup"><span data-stu-id="73651-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="73651-124">In Project Operations, la chiusura di un'offerta come acquisita o persa non influirà sullo stato dell'opportunità, che rimarrà aperta fino a quando non verrà chiusa manualmente.</span><span class="sxs-lookup"><span data-stu-id="73651-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]