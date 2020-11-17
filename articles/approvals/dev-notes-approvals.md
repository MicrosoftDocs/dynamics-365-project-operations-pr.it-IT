---
title: Note sulle approvazioni per gli sviluppatori
description: Questo argomento fornisce ulteriori informazioni per gli sviluppatori su come utilizzare le approvazioni.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483953"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="d04eb-103">Note sulle approvazioni per gli sviluppatori</span><span class="sxs-lookup"><span data-stu-id="d04eb-103">Developer notes for Approvals</span></span>

<span data-ttu-id="d04eb-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="d04eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d04eb-105">Dynamics 365 Project Operations include la logica di convalida che garantisce la corretta transizione dei record attraverso le fasi di approvazione.</span><span class="sxs-lookup"><span data-stu-id="d04eb-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="d04eb-106">Le corrette transizioni dei record garantiscono:</span><span class="sxs-lookup"><span data-stu-id="d04eb-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="d04eb-107">Tutte le righe di supporto vengono create nelle tabelle correlate, come giornali di registrazione e valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="d04eb-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="d04eb-108">Il responsabile approvazione di progetto è contrassegnato come **Responsabile approvazione di progetto** nel progetto prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="d04eb-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
