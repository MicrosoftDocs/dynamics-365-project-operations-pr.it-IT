---
title: Gestire contratti di progetto
description: Questo argomento fornisce informazioni sulla visualizzazione dei contratti basati su progetto.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441fbc378a423334f45bc65658811ef238515393
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177336"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="16f33-103">Gestire contratti di progetto</span><span class="sxs-lookup"><span data-stu-id="16f33-103">Manage project contracts</span></span>

<span data-ttu-id="16f33-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="16f33-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="16f33-105">I contratti di progetto in Dynamics 365 Project Operations acquisiscono e gestiscono gli impegni di contratto concordati e i dettagli di fatturazione di un progetto.</span><span class="sxs-lookup"><span data-stu-id="16f33-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="16f33-106">La struttura di un contratto di progetto in Project Operations è adattata per il lavoro basato su progetto con i seguenti componenti:</span><span class="sxs-lookup"><span data-stu-id="16f33-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="16f33-107">Voci di contratto che identificano i componenti discreti del lavoro che verranno presentati come componenti di alto livello in una fattura di progetto.</span><span class="sxs-lookup"><span data-stu-id="16f33-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="16f33-108">Dettagli della voce di contratto che identificano e stimano il lavoro per ogni componente di alto livello o voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="16f33-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="16f33-109">La stima include la pianificazione e gli aspetti finanziari del lavoro legati a quella voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="16f33-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="16f33-110">I modelli di contratto e i componenti addebitabili vengono impostati per ciascuna voce di contratto che contiene il contratto di fatturazione per ciascuna voce di contratto e il contratto complessivo.</span><span class="sxs-lookup"><span data-stu-id="16f33-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="16f33-111">Visualizzare tutti i contratti basati su progetto</span><span class="sxs-lookup"><span data-stu-id="16f33-111">View all project-based contracts</span></span>

<span data-ttu-id="16f33-112">Un elenco di tutti i contratti di progetto può essere visualizzato dalla pagina elenco **Contratti**.</span><span class="sxs-lookup"><span data-stu-id="16f33-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="16f33-113">Vai a **Vendite** > **Contratti**.</span><span class="sxs-lookup"><span data-stu-id="16f33-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="16f33-114">Viene visualizzato un elenco di tutti i contratti di progetto nel sistema.</span><span class="sxs-lookup"><span data-stu-id="16f33-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="16f33-115">Seleziona **Cambia vista** (la freccia a discesa accanto al nome della visualizzazione) per selezionare altre visualizzazioni filtrate.</span><span class="sxs-lookup"><span data-stu-id="16f33-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="16f33-116">Puoi creare le tue visualizzazioni con criteri di filtro personalizzati.</span><span class="sxs-lookup"><span data-stu-id="16f33-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="16f33-117">I contratti possono essere creati o eliminati da questa pagina elenco o dalle pagine dei dettagli.</span><span class="sxs-lookup"><span data-stu-id="16f33-117">Contracts can be created or deleted from this list page or detail pages.</span></span>
