---
title: Novità o modifiche nella prima ondata 2020 di Project Service Automation versione 3.x
description: Questo argomento fornisce informazioni sulle novità e sulle modifiche nella prima ondata 2020 di Project Service Automation versione 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2308f83e09c25059b6a36599b04b5b00f66c704f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126488"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="cc20e-103">Novità o modifiche nella prima ondata 2020 di Project Service Automation versione 3</span><span class="sxs-lookup"><span data-stu-id="cc20e-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="cc20e-104">In questo argomento sono presenti considerazioni importanti sull'aggiornamento quando si passa all'ultima versione della prima ondata 2020 di Project Service Automation (PSA) versione 3.x.</span><span class="sxs-lookup"><span data-stu-id="cc20e-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="cc20e-105">Inserimento ore</span><span class="sxs-lookup"><span data-stu-id="cc20e-105">Time entry</span></span>
<span data-ttu-id="cc20e-106">L'esperienza di inserimento ore è stata estesa per offrire le funzionalità per l'estensione dell'inserimento ore in più scenari di clienti.</span><span class="sxs-lookup"><span data-stu-id="cc20e-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="cc20e-107">Ciò include la possibilità di aggiungere tipi di voci che ora guidano comportamenti specifici in base al nome dello schema del campo **Impostazioni di inserimento ore**, visualizzato come **Origine dell'ora**.</span><span class="sxs-lookup"><span data-stu-id="cc20e-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="cc20e-108">Una nuova soluzione, denominata Time, Expense, Statusing and Approvals (TESA) è stata aggiunta per supportare questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="cc20e-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="cc20e-109">Considerazioni sull'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="cc20e-109">Upgrade consideration</span></span>
<span data-ttu-id="cc20e-110">Per supportare questa funzionalità, i ruoli all'interno di PSA sono stati aggiornati per includere nuovi privilegi.</span><span class="sxs-lookup"><span data-stu-id="cc20e-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="cc20e-111">Questi privilegi concedono l'accesso in lettura alla nuova entità, **Impostazioni di inserimento ore**.</span><span class="sxs-lookup"><span data-stu-id="cc20e-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="cc20e-112">Agli utenti che richiedono la possibilità di registrare l'ora deve essere concesso il ruolo utente **Utente con inserimento ore** oltre ai ruoli esistenti.</span><span class="sxs-lookup"><span data-stu-id="cc20e-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="cc20e-113">Questo ruolo include le nuove funzionalità e garantisce che l'inserimento ore continui a funzionare.</span><span class="sxs-lookup"><span data-stu-id="cc20e-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="cc20e-114">Inoltre, se si dispone di moduli di app personalizzati che includono tutti i moduli per l'entità di inserimento ore, dovrai rimuovere il modulo **Modulo di creazione rapida inserimento ore TESA** dal modulo.</span><span class="sxs-lookup"><span data-stu-id="cc20e-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="cc20e-115">Modifiche di inserimento ore attualmente esteso</span><span class="sxs-lookup"><span data-stu-id="cc20e-115">Currently extended time entry changes</span></span>
<span data-ttu-id="cc20e-116">Per ridurre al minimo l'impatto per gli utenti attuali dell'inserimento ore, questo cambio di ruolo è l'unico requisito fondamentale necessario per continuare a utilizzare l'inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="cc20e-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="cc20e-117">Se sono state create visualizzazioni personalizzate o esperienze di inserimento ore separate, è necessario impostare i campi **Impostazioni di inserimento ore** con il valore di PSA corretto.</span><span class="sxs-lookup"><span data-stu-id="cc20e-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
