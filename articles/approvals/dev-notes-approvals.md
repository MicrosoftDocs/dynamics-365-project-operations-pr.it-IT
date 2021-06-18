---
title: Note sulle approvazioni per gli sviluppatori
description: Questo argomento fornisce ulteriori informazioni per gli sviluppatori su come utilizzare le approvazioni.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996796"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="96ab9-103">Note sulle approvazioni per gli sviluppatori</span><span class="sxs-lookup"><span data-stu-id="96ab9-103">Developer notes for Approvals</span></span>

<span data-ttu-id="96ab9-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="96ab9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="96ab9-105">Dynamics 365 Project Operations include la logica di convalida che garantisce la corretta transizione dei record attraverso le fasi di approvazione.</span><span class="sxs-lookup"><span data-stu-id="96ab9-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="96ab9-106">Le corrette transizioni dei record garantiscono:</span><span class="sxs-lookup"><span data-stu-id="96ab9-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="96ab9-107">Tutte le righe di supporto vengono create nelle tabelle correlate, come giornali di registrazione e valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="96ab9-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="96ab9-108">Il responsabile approvazione di progetto è contrassegnato come **Responsabile approvazione di progetto** nel progetto prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="96ab9-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]