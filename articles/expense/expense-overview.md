---
title: Panoramica della spesa
description: Questo argomento fornisce informazioni su come utilizzare la funzionalità Spesa in Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c4e2f441e1c4b1bcba5bca292b8075b4334a004d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276578"
---
# <a name="expense-home-page"></a><span data-ttu-id="1a4f1-103">Home page di Spesa</span><span class="sxs-lookup"><span data-stu-id="1a4f1-103">Expense home page</span></span>

<span data-ttu-id="1a4f1-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="1a4f1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1a4f1-105">Dynamics 365 Project Operations supporta la capacità di elaborare le spese.</span><span class="sxs-lookup"><span data-stu-id="1a4f1-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="1a4f1-106">L'elaborazione delle spese avviene con o senza progetti utilizzando un flusso di lavoro personalizzabile di criteri, categorie di transazioni e approvazioni.</span><span class="sxs-lookup"><span data-stu-id="1a4f1-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="1a4f1-107">In Project Operations, sono disponibili due modelli di distribuzione supportati per spesa:</span><span class="sxs-lookup"><span data-stu-id="1a4f1-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="1a4f1-108">**Completo**: la distribuzione completa è disponibile per **Project Operations per scenari basati su risorse/materiali non stoccati** o **Project Operations per scenari basati su ordini di produzione**.</span><span class="sxs-lookup"><span data-stu-id="1a4f1-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="1a4f1-109">**Di base**: la distribuzione di base è disponibile per **Project Operations per scenari basati su risorse/materiali non stoccati** e **Distribuzione semplice: dalla transazione alla fatturazione proforma**.</span><span class="sxs-lookup"><span data-stu-id="1a4f1-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="1a4f1-110">Completa</span><span class="sxs-lookup"><span data-stu-id="1a4f1-110">Full</span></span> 
<span data-ttu-id="1a4f1-111">L'implementazione Spesa completa fornisce un'applicazione completa dei criteri che include la possibilità di creare criteri, come:</span><span class="sxs-lookup"><span data-stu-id="1a4f1-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="1a4f1-112">Limiti di categoria di spesa</span><span class="sxs-lookup"><span data-stu-id="1a4f1-112">Expense category limits</span></span>
  - <span data-ttu-id="1a4f1-113">Viaggi</span><span class="sxs-lookup"><span data-stu-id="1a4f1-113">Travel</span></span>
  - <span data-ttu-id="1a4f1-114">Diaria</span><span class="sxs-lookup"><span data-stu-id="1a4f1-114">Per diem</span></span>
  - <span data-ttu-id="1a4f1-115">Importi della carta di credito</span><span class="sxs-lookup"><span data-stu-id="1a4f1-115">Credit card imports</span></span>
  - <span data-ttu-id="1a4f1-116">Riconoscimento ottico dei caratteri della ricevuta</span><span class="sxs-lookup"><span data-stu-id="1a4f1-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="1a4f1-117">Basic</span><span class="sxs-lookup"><span data-stu-id="1a4f1-117">Basic</span></span> 
<span data-ttu-id="1a4f1-118">Lo scenario di distribuzione delle spese di base consente solo di registrare le spese di base rispetto a un progetto.</span><span class="sxs-lookup"><span data-stu-id="1a4f1-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="1a4f1-119">Per ulteriori informazioni, vedi [Voce di spesa (semplice)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="1a4f1-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="1a4f1-120">Determinare la distribuzione della spesa</span><span class="sxs-lookup"><span data-stu-id="1a4f1-120">Determine your Expense deployment</span></span>
<span data-ttu-id="1a4f1-121">Per determinare se stai eseguendo la distribuzione di gestione delle spese di base, verifica che l'URL dell'indirizzo termini con **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="1a4f1-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]