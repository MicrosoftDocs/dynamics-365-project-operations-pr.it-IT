---
title: Informazioni sullo stato del progetto
description: Questo argomento fornisce informazioni sullo stato assegnato ai progetti in Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965681"
---
# <a name="understand-project-status"></a><span data-ttu-id="73a92-103">Informazioni sullo stato del progetto</span><span class="sxs-lookup"><span data-stu-id="73a92-103">Understand project status</span></span>

<span data-ttu-id="73a92-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="73a92-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="73a92-105">La sezione **Stato** nella pagina **Entità progetto** fornisce un riepilogo dello stato di un progetto in base al costo e al lavoro richiesto.</span><span class="sxs-lookup"><span data-stu-id="73a92-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="73a92-106">Campi di riepilogo dello stato</span><span class="sxs-lookup"><span data-stu-id="73a92-106">Status summary fields</span></span>

- <span data-ttu-id="73a92-107">Il campo **Stato di progetto generale** è un campo modificabile che mostra lo stato globale del progetto.</span><span class="sxs-lookup"><span data-stu-id="73a92-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="73a92-108">Questo campo utilizza la codifica con colori, come verde, giallo e rosso, per indicare il rischio crescente.</span><span class="sxs-lookup"><span data-stu-id="73a92-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="73a92-109">Il campo **Commenti** consente al responsabile di progetto di immettere commenti specifici sullo stato.</span><span class="sxs-lookup"><span data-stu-id="73a92-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="73a92-110">Il campo **Data aggiornamento stato** non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="73a92-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="73a92-111">Il valore in questo campo è un timestamp che indica quando lo stato è stato aggiornato l'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="73a92-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="73a92-112">I campie **Prestazioni di pianificazione** e **Prestazioni costo** sono impostati in base alla griglia di registrazione.</span><span class="sxs-lookup"><span data-stu-id="73a92-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="73a92-113">Quando lo scostamento pianificazione e lo scostamento costo per il nodo radice nella vista **Registrazione lavoro richiesto** sono positivi, questi campi vengono aggiornati su **In anticipo**.</span><span class="sxs-lookup"><span data-stu-id="73a92-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="73a92-114">Quando lo scostamento pianificazione e lo scostamento costo per il nodo radice sono negativi, questi campi vengono impostati su **In ritardo**.</span><span class="sxs-lookup"><span data-stu-id="73a92-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
