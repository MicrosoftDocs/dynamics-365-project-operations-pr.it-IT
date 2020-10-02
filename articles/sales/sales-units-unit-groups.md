---
title: Unità e unità di vendita
description: Questo argomento fornisce informazioni su come creare unità e unità di vendita in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898761"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="3a007-103">Unità e unità di vendita</span><span class="sxs-lookup"><span data-stu-id="3a007-103">Units and unit groups</span></span>

<span data-ttu-id="3a007-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="3a007-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3a007-105">Le unità sono le quantità o le misure in cui vengono venduti i prodotti o i servizi.</span><span class="sxs-lookup"><span data-stu-id="3a007-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="3a007-106">Ad esempio, se si vendono forniture di giardinaggio, si potrebbero vendere i semi in unità tipo pacchetti, scatole e pallet.</span><span class="sxs-lookup"><span data-stu-id="3a007-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="3a007-107">Un'unità di vendita è una raccolta di tali diverse unità.</span><span class="sxs-lookup"><span data-stu-id="3a007-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="3a007-108">Per completare i passaggi in questo argomento, assicurati di essere stato assegnato al ruolo Amministratore di sistema o Responsabile Sales Professional o di disporre di autorizzazioni equivalenti.</span><span class="sxs-lookup"><span data-stu-id="3a007-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="3a007-109">Creare un'unità di vendita</span><span class="sxs-lookup"><span data-stu-id="3a007-109">Create a unit group</span></span>

1. <span data-ttu-id="3a007-110">Nella mappa del sito, seleziona **Unità**.</span><span class="sxs-lookup"><span data-stu-id="3a007-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="3a007-111">Seleziona **Nuovo** e nella finestra di dialogo **Crea unità di vendita** immetti il nome dell'unità.</span><span class="sxs-lookup"><span data-stu-id="3a007-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="3a007-112">Nel campo**Unità primaria** immetti l'unità di misura comune più piccola che verrà utilizzata per la vendita del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3a007-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="3a007-113">Ad esempio, potresti inserire "pezzo" o "oncia".</span><span class="sxs-lookup"><span data-stu-id="3a007-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="3a007-114">Seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a007-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="3a007-115">Aggiungere unità a un'unità di vendita</span><span class="sxs-lookup"><span data-stu-id="3a007-115">Add units to a unit group</span></span>

1. <span data-ttu-id="3a007-116">Apri un'unità di vendita e nella scheda **Correlato** seleziona **Unità**.</span><span class="sxs-lookup"><span data-stu-id="3a007-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="3a007-117">Vedrai che l'unità primaria è già aggiunta.</span><span class="sxs-lookup"><span data-stu-id="3a007-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="3a007-118">Seleziona **Aggiungi nuova unità** e nella pagina **Creazione rapida: unità** nel campo **Nome** inserisci il nome dell'unità.</span><span class="sxs-lookup"><span data-stu-id="3a007-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="3a007-119">Nel campo **Quantità** immetti la quantità che l'unità conterrà.</span><span class="sxs-lookup"><span data-stu-id="3a007-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="3a007-120">Ad esempio, se una scatola contiene 2 pezzi, immetti "2".</span><span class="sxs-lookup"><span data-stu-id="3a007-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="3a007-121">Nel campo **Unità base** seleziona un'unità di base per stabilire l'unità di misura più bassa per l'unità.</span><span class="sxs-lookup"><span data-stu-id="3a007-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="3a007-122">Ad esempio, potresti selezionare "Pezzo".</span><span class="sxs-lookup"><span data-stu-id="3a007-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="3a007-123">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="3a007-123">Select **Save**:</span></span>
