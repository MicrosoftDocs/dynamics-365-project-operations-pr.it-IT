---
title: Progetti di stima dei ricavi a prezzo fisso
description: In questo argomento vengono fornite informazioni sui ricavi a prezzo fisso nei progetti.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013806"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="14164-103">Progetti di stima dei ricavi a prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="14164-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="14164-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="14164-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="14164-105">Quando crei una riga di contratto di progetto con i seguenti attributi in Dynamics 365 Project Operations in Microsoft Dataverse, il sistema crea automaticamente un progetto di stima dei ricavi a prezzo fisso.</span><span class="sxs-lookup"><span data-stu-id="14164-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="14164-106">Le informazioni in questo progetto si basano su quanto segue:</span><span class="sxs-lookup"><span data-stu-id="14164-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="14164-107">Un metodo di fatturazione a prezzo fisso.</span><span class="sxs-lookup"><span data-stu-id="14164-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="14164-108">Un progetto associato.</span><span class="sxs-lookup"><span data-stu-id="14164-108">An associated project.</span></span>
  - <span data-ttu-id="14164-109">Almeno una passaggio fondamentale definito nella scheda **Pianificazione fatture** nella pagina **Riga contratto di progetto**.</span><span class="sxs-lookup"><span data-stu-id="14164-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="14164-110">Revisione dei progetti delle stime dei ricavi a prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="14164-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="14164-111">Per rivedere i progetti delle stime dei ricavi a prezzo fisso, completare i seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="14164-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="14164-112">Nell'ambiente Dynamics 365 Finance, vai a **Contabilità e gestione progetti** > **Progetti** > **Progetti di stima dei ricavi a prezzo fisso**.</span><span class="sxs-lookup"><span data-stu-id="14164-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="14164-113">Seleziona il progetto che desideri visualizzare e fai doppio clic su **Stima ID del progetto** per aprire il record e rivedere i dettagli del progetto.</span><span class="sxs-lookup"><span data-stu-id="14164-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="14164-114">Espandi la schedaa **Progetto**. Vedrai un progetto nella griglia **Progetti selezionati**.</span><span class="sxs-lookup"><span data-stu-id="14164-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="14164-115">Il sistema utilizza questo progetto come predefinito perché è il progetto associato alla riga di contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="14164-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="14164-116">Per modificare l'associazione, seleziona altri progetti e aggiungili alla griglia **Progetti selezionati**.</span><span class="sxs-lookup"><span data-stu-id="14164-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="14164-117">Se in questa griglia vengono selezionati più progetti, la percentuale di completamento del progetto e le stime dei ricavi vengono calcolate insieme per tutti i progetti selezionati.</span><span class="sxs-lookup"><span data-stu-id="14164-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="14164-118">Il costo del progetto, il profilo dei ricavi, il modello di costo e il codice del periodo possono essere impostati manualmente.</span><span class="sxs-lookup"><span data-stu-id="14164-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="14164-119">Se non vengono impostati manualmente, i valori vengono impostati come predefiniti durante il primo calcolo della stima per il progetto utilizzando le regole configurate per i profili di costi e ricavi del progetto.</span><span class="sxs-lookup"><span data-stu-id="14164-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]