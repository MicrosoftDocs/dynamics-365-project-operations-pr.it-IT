---
title: Stime di spesa
description: Questo argomento fornisce informazioni sulla definizione o sulla stima delle spese basate sul progetto.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131708"
---
# <a name="expense-estimates"></a><span data-ttu-id="74fc5-103">Stime di spesa</span><span class="sxs-lookup"><span data-stu-id="74fc5-103">Expense estimates</span></span>
<span data-ttu-id="74fc5-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="74fc5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="74fc5-105">Oltre a definire le stime basate sulle risorse, Dynamics 365 Project Operations consente ai Project manager di definire le spese basate sul progetto per ogni progetto.</span><span class="sxs-lookup"><span data-stu-id="74fc5-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="74fc5-106">Ogni voce di spesa può essere associata a una specifica attività di progetto o categoria di spesa.</span><span class="sxs-lookup"><span data-stu-id="74fc5-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="74fc5-107">Le categorie di spesa sono generalmente definite a livello organizzativo.</span><span class="sxs-lookup"><span data-stu-id="74fc5-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="74fc5-108">I prezzi per ciascuna categoria di spesa sono generalmente definiti nella seguente gerarchia:</span><span class="sxs-lookup"><span data-stu-id="74fc5-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="74fc5-109">Azienda</span><span class="sxs-lookup"><span data-stu-id="74fc5-109">Organization</span></span>
- <span data-ttu-id="74fc5-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="74fc5-110">Customer</span></span>
- <span data-ttu-id="74fc5-111">Offerta/contratto</span><span class="sxs-lookup"><span data-stu-id="74fc5-111">Quote/contract</span></span>

<span data-ttu-id="74fc5-112">Completa i seguenti passaggi per visualizzare, aggiungere o eliminare una spesa di progetto.</span><span class="sxs-lookup"><span data-stu-id="74fc5-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="74fc5-113">Vai a **Progetti** e seleziona il progetto su cui vuoi lavorare.</span><span class="sxs-lookup"><span data-stu-id="74fc5-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="74fc5-114">Seleziona la scheda **Stime di progetto** e visualizza l'elenco delle spese di progetto.</span><span class="sxs-lookup"><span data-stu-id="74fc5-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="74fc5-115">Seleziona **Nuova spesa** per aggiungere una spesa.</span><span class="sxs-lookup"><span data-stu-id="74fc5-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="74fc5-116">In alternativa, seleziona una spesa da eliminare, quindi seleziona **Elimina spesa**.</span><span class="sxs-lookup"><span data-stu-id="74fc5-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="74fc5-117">I seguenti attributi sono definiti per ciascuna voce di riga di spesa:</span><span class="sxs-lookup"><span data-stu-id="74fc5-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="74fc5-118">**Categoria**: i raggruppamenti comuni utilizzati per descrivere tutte le spese sostenute per un progetto.</span><span class="sxs-lookup"><span data-stu-id="74fc5-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="74fc5-119">**Data d'inizio**: data in cui si prevede di sostenere la spesa.</span><span class="sxs-lookup"><span data-stu-id="74fc5-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="74fc5-120">**Quantità**: il numero stimato di voci di spesa per una categoria specifica.</span><span class="sxs-lookup"><span data-stu-id="74fc5-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="74fc5-121">**Prezzo di costo unitario**: il prezzo unitario utilizzato per calcolare il costo della spesa.</span><span class="sxs-lookup"><span data-stu-id="74fc5-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="74fc5-122">**Prezzo di vendita unitario**: il prezzo unitario utilizzato per calcolare il prezzo di vendita della spesa.</span><span class="sxs-lookup"><span data-stu-id="74fc5-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

