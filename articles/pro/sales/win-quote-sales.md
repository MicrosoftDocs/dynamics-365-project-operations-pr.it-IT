---
title: Chiudere le offerte
description: Questo argomento fornisce informazioni sulla chiusura di un'offerta in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078797"
---
# <a name="close-quotes"></a><span data-ttu-id="10ba2-103">Chiudere le offerte</span><span class="sxs-lookup"><span data-stu-id="10ba2-103">Close quotes</span></span> 

<span data-ttu-id="10ba2-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="10ba2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="10ba2-105">Un'offerta di progetto può essere chiusa come acquisita o persa.</span><span class="sxs-lookup"><span data-stu-id="10ba2-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="10ba2-106">Le operazioni Attiva e Aggiorna sulle offerte non sono supportate in Microsoft Dynamics 365 Project Operations, quindi è possibile chiudere un'offerta in bozza.</span><span class="sxs-lookup"><span data-stu-id="10ba2-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="10ba2-107">Chiudere un'offerta come acquisita</span><span class="sxs-lookup"><span data-stu-id="10ba2-107">Close a quote as Won</span></span>

<span data-ttu-id="10ba2-108">La chiusura di un'offerta di progetto come acquisita chiuderà l'offerta con lo stato impostato su Chiusa e il motivo stato impostato su Acquisita.</span><span class="sxs-lookup"><span data-stu-id="10ba2-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="10ba2-109">La chiusura dell'offerta rende l'offerta di progetto di sola lettura e crea un contratto di progetto in bozza che contiene le informazioni sull'offerta.</span><span class="sxs-lookup"><span data-stu-id="10ba2-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="10ba2-110">Viene visualizzata una finestra di dialogo di conferma prima che vengano apportate le modifiche poiché un'offerta chiusa non può essere riaperta e le modifiche sono irreversibili.</span><span class="sxs-lookup"><span data-stu-id="10ba2-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="10ba2-111">Se l'offerta è collegata a un'opportunità, qualsiasi altra offerta di progetto dell'opportunità viene automaticamente chiusa come persa.</span><span class="sxs-lookup"><span data-stu-id="10ba2-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="10ba2-112">Impatto finanziario della chiusura di un'offerta come acquisita</span><span class="sxs-lookup"><span data-stu-id="10ba2-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="10ba2-113">Se sono stati registrati dei valori effettivi per il tempo in un progetto mentre è ancora collegato a un'offerta in bozza, viene registrato solo il costo del tempo o della spesa.</span><span class="sxs-lookup"><span data-stu-id="10ba2-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="10ba2-114">Dopo che un'offerta è stata chiusa come acquisita, l'applicazione effettuerà il refactoring dei costi annullando i valori effettivi di costo precedenti e ricreando nuovi valori effettivi di costo.</span><span class="sxs-lookup"><span data-stu-id="10ba2-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="10ba2-115">L'applicazione elaborerà questi valori effettivi di costo in base al metodo di fatturazione della voce di contratto di progetto associata.</span><span class="sxs-lookup"><span data-stu-id="10ba2-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="10ba2-116">Se i valori effettivi di costo fanno riferimento a una voce di contratto di tempistica e materiali, il sistema creerà automaticamente i valori effettivi di vendita non fatturati corrispondenti quando l'offerta viene chiusa e il contratto di progetto viene creato.</span><span class="sxs-lookup"><span data-stu-id="10ba2-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="10ba2-117">Se i valori effettivi di costo fanno riferimento a una voce di contratto a prezzo fisso, l'applicazione interromperà la rielaborazione dei valori effettivi di costo in base alle regole di fatturazione separata per i clienti del contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="10ba2-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="10ba2-118">Chiusura di un'offerta come persa:</span><span class="sxs-lookup"><span data-stu-id="10ba2-118">Closing a quote as lost:</span></span>

<span data-ttu-id="10ba2-119">La chiusura di un'offerta come persa imposterà lo stato su Chiusa e il motivo stato su Persa.</span><span class="sxs-lookup"><span data-stu-id="10ba2-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="10ba2-120">La chiusura dell'offerta rende l'offerta di progetto di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="10ba2-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="10ba2-121">Poiché un'offerta chiusa non può essere riaperta, prima di chiudere un'offerta una finestra di dialogo di conferma confermerà le modifiche.</span><span class="sxs-lookup"><span data-stu-id="10ba2-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="10ba2-122">Se l'offerta di progetto chiusa come persa fa riferimento a un progetto in una delle sue righe, anche quel progetto viene contrassegnato come chiuso e tutte le prenotazioni di risorse da quel giorno in poi vengono annullate.</span><span class="sxs-lookup"><span data-stu-id="10ba2-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="10ba2-123">In Project Operations, la chiusura di un'offerta come acquisita o persa non influirà sullo stato dell'opportunità, che rimarrà aperta fino a quando non verrà chiusa manualmente.</span><span class="sxs-lookup"><span data-stu-id="10ba2-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
