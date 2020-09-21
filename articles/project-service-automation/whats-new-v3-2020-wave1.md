---
title: Novità o modifiche nella prima ondata 2020 di Project Service Automation versione 3.x
description: Questo argomento fornisce informazioni sulle novità e sulle modifiche nella prima ondata 2020 di Project Service Automation versione 3.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752641"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="2456e-103">Novità o modifiche nella prima ondata 2020 di Project Service Automation versione 3</span><span class="sxs-lookup"><span data-stu-id="2456e-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="2456e-104">In questo argomento sono presenti considerazioni importanti sull'aggiornamento quando si passa all'ultima versione della prima ondata 2020 di Project Service Automation (PSA) versione 3.x.</span><span class="sxs-lookup"><span data-stu-id="2456e-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="2456e-105">Inserimento ore</span><span class="sxs-lookup"><span data-stu-id="2456e-105">Time entry</span></span>
<span data-ttu-id="2456e-106">L'esperienza di inserimento ore è stata estesa per offrire le funzionalità per l'estensione dell'inserimento ore in più scenari di clienti.</span><span class="sxs-lookup"><span data-stu-id="2456e-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="2456e-107">Ciò include la possibilità di aggiungere tipi di voci che ora guidano comportamenti specifici in base al nome dello schema del campo **Impostazioni di inserimento ore**, visualizzato come **Origine dell'ora**.</span><span class="sxs-lookup"><span data-stu-id="2456e-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="2456e-108">Considerazioni sull'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2456e-108">Upgrade consideration</span></span>
<span data-ttu-id="2456e-109">Per supportare questa funzionalità, i ruoli all'interno di PSA sono stati aggiornati per includere nuovi privilegi.</span><span class="sxs-lookup"><span data-stu-id="2456e-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="2456e-110">Questi privilegi concedono l'accesso in lettura alla nuova entità, **Impostazioni di inserimento ore**.</span><span class="sxs-lookup"><span data-stu-id="2456e-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="2456e-111">Agli utenti che richiedono la possibilità di registrare l'ora deve essere concesso il ruolo utente **Utente con inserimento ore** oltre ai ruoli esistenti.</span><span class="sxs-lookup"><span data-stu-id="2456e-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="2456e-112">Questo ruolo include le nuove funzionalità e garantisce che l'inserimento ore continui a funzionare.</span><span class="sxs-lookup"><span data-stu-id="2456e-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="2456e-113">Modifiche di inserimento ore attualmente esteso</span><span class="sxs-lookup"><span data-stu-id="2456e-113">Currently extended time entry changes</span></span>
<span data-ttu-id="2456e-114">Per ridurre al minimo l'impatto per gli utenti attuali dell'inserimento ore, questo cambio di ruolo è l'unico requisito fondamentale necessario per continuare a utilizzare l'inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="2456e-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="2456e-115">Se sono state create visualizzazioni personalizzate o esperienze di inserimento ore separate, è necessario impostare i campi **Impostazioni di inserimento ore** con il valore di PSA corretto.</span><span class="sxs-lookup"><span data-stu-id="2456e-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
