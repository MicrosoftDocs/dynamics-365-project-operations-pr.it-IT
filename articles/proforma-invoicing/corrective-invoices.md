---
title: Fatture corrette
description: In questo argomento vengono fornite informazioni sulle fatture corrette.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287828"
---
# <a name="corrected-invoices"></a><span data-ttu-id="96021-103">Fatture corrette</span><span class="sxs-lookup"><span data-stu-id="96021-103">Corrected invoices</span></span>

<span data-ttu-id="96021-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="96021-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="96021-105">Le fatture confermate possono essere modificate.</span><span class="sxs-lookup"><span data-stu-id="96021-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="96021-106">Quando modifichi una fattura confermata, viene creata una bozza della fattura corretta.</span><span class="sxs-lookup"><span data-stu-id="96021-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="96021-107">Poiché si presuppone che tu voglia stornare tutte le transazioni e quantità dalla fattura originale, questa fattura corretta include tutte le transazioni della fattura originale e tutte le relative quantità sono pari a zero (0).</span><span class="sxs-lookup"><span data-stu-id="96021-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="96021-108">Se alcune transazioni non richiedono la correzione, puoi rimuoverle dalla bozza di fattura correttiva.</span><span class="sxs-lookup"><span data-stu-id="96021-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="96021-109">Per stornare o restituire solo una quantità parziale, puoi modificare il campo Quantità nel dettaglio della riga.</span><span class="sxs-lookup"><span data-stu-id="96021-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="96021-110">Se apri il dettaglio di riga fattura, puoi vedere la quantità della fattura originale.</span><span class="sxs-lookup"><span data-stu-id="96021-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="96021-111">Puoi quindi modificare la quantità della fattura corrente di modo che sia inferiore o superiore alla quantità della fattura originale.</span><span class="sxs-lookup"><span data-stu-id="96021-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="96021-112">Quando confermi una fattura correttiva, il valore effettivo delle vendite fatturate originali viene stornato e viene creato un nuovo valore effettivo di vendite fatturate.</span><span class="sxs-lookup"><span data-stu-id="96021-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="96021-113">Se la quantità è stata ridotta, la differenza genererà anche la creazione di un nuovo valore effettivo delle vendite.</span><span class="sxs-lookup"><span data-stu-id="96021-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="96021-114">Ad esempio, se lea vendita fatturata originale era per otto ore e il dettaglio di riga di fattura corretta presenta una quantità ridotta di sei ore, la riga delle vendite fatturate originali viene stornata e due nuovi valori effettivi vengono creati:</span><span class="sxs-lookup"><span data-stu-id="96021-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="96021-115">Un valore effettivo delle vendite fatturate per sei ore.</span><span class="sxs-lookup"><span data-stu-id="96021-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="96021-116">Un valore effettivo delle vendite non fatturate per le due ore rimanenti.</span><span class="sxs-lookup"><span data-stu-id="96021-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="96021-117">Questa transazione può essere fatturata successivamente o contrassegnata come non addebitale, a seconda delle negoziazioni con il cliente.</span><span class="sxs-lookup"><span data-stu-id="96021-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]