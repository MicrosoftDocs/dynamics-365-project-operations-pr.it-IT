---
title: Novità o modifiche nella versione di aggiornamento 17 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 17 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bb93208217972639f91b39b7b6705d9897373ef7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126803"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="85b3a-103">Versione di aggiornamento di Project Service Automation 17, V3</span><span class="sxs-lookup"><span data-stu-id="85b3a-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="85b3a-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="85b3a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="85b3a-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="85b3a-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="85b3a-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="85b3a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="85b3a-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="85b3a-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="85b3a-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="85b3a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="85b3a-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 17 di PSA V3.</span><span class="sxs-lookup"><span data-stu-id="85b3a-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="85b3a-110">Questa versione ha il numero di build V3.10.6.34 ed è generalmente disponibile tramite un aggiornamento automatico in marzo 2020.</span><span class="sxs-lookup"><span data-stu-id="85b3a-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="85b3a-111">Rilascio 17 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="85b3a-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="85b3a-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="85b3a-112">Bug fixes</span></span>

<span data-ttu-id="85b3a-113">**Generali**</span><span class="sxs-lookup"><span data-stu-id="85b3a-113">**General**</span></span>

- <span data-ttu-id="85b3a-114">Risolto: aggiornamento di Project Service Automation per applicare le licenze Membro del team (Hub risorse progetto includerà i metadati del piano di servizio Membro del team 3.x)</span><span class="sxs-lookup"><span data-stu-id="85b3a-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="85b3a-115">**Tempo e spesa**</span><span class="sxs-lookup"><span data-stu-id="85b3a-115">**Time and Expense**</span></span>

- <span data-ttu-id="85b3a-116">Risolto: non è possibile modificare una stima spese da un prezzo diverso da zero (0) a zero (0).</span><span class="sxs-lookup"><span data-stu-id="85b3a-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="85b3a-117">La modifica viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="85b3a-117">The change is ignored.</span></span>

<span data-ttu-id="85b3a-118">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="85b3a-118">**Project Management**</span></span>

- <span data-ttu-id="85b3a-119">Risolto: un controllo per i valori null è stato aggiunto sul nome della posizione di un membro del team.</span><span class="sxs-lookup"><span data-stu-id="85b3a-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="85b3a-120">Risolto: campo **msdyn_userresourceid** sull'entità **msdyn_resourceassignment** deprecato.</span><span class="sxs-lookup"><span data-stu-id="85b3a-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="85b3a-121">Risolto: l'aggiornamento da 2.x a 3.x gestisce ora i profili di lavoro sulle assegnazioni delle attività.</span><span class="sxs-lookup"><span data-stu-id="85b3a-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="85b3a-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="85b3a-122">**Sales**</span></span>

- <span data-ttu-id="85b3a-123">Risolto: **Invoice.PreValidateInvoiceUpdate** gestisce ora lo scenario di riassegnazione corretta dei proprietari dei record.</span><span class="sxs-lookup"><span data-stu-id="85b3a-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="85b3a-124">Risolto: quando la classe di transazione è **Ora**, **UnitGroup** non è modificabile per tutte le entità, tra cui **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** e **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="85b3a-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="85b3a-125">Tuttavia, **Unità** non è editabile solo per **JournalLine** e **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="85b3a-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


