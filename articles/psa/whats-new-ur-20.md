---
title: Novità o modifiche nella versione di aggiornamento 20 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 20 di Project Service Automation V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147118"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="30040-103">Versione di aggiornamento di Project Service Automation 20, V3</span><span class="sxs-lookup"><span data-stu-id="30040-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="30040-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="30040-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="30040-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="30040-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="30040-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="30040-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="30040-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="30040-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="30040-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="30040-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="30040-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 20 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="30040-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="30040-110">Questa versione ha il numero di build V 3.10.31.37 ed è generalmente disponibile tramite un aggiornamento automatico a giugno 2020.</span><span class="sxs-lookup"><span data-stu-id="30040-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="30040-111">Rilascio 20 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="30040-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="30040-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="30040-112">Bug fixes</span></span>

<span data-ttu-id="30040-113">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="30040-113">**Project Management**</span></span>

<span data-ttu-id="30040-114">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="30040-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="30040-115">L'importazione dei membri del team di progetto con un metodo di allocazione che richiede ore genera un messaggio di errore non chiaro quando le ore specificate sono zero.</span><span class="sxs-lookup"><span data-stu-id="30040-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="30040-116">Gli utenti ricevono un errore non corretto quando il numero massimo di caratteri è stato inserito nel campo **Descrizione** per un'attività di progetto.</span><span class="sxs-lookup"><span data-stu-id="30040-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="30040-117">La pagina **download del componente aggiuntivo Microsoft Dynamics 365 Project Service Automation** reindirizza alla pagina di download in inglese quando le impostazioni della lingua dell'utente sono impostate sul giapponese.</span><span class="sxs-lookup"><span data-stu-id="30040-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="30040-118">Quando si verifica un errore del server, l'etichetta di sincronizzazione sulla scheda **Pianifica** del modulo **Progetti** a volte rimane.</span><span class="sxs-lookup"><span data-stu-id="30040-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="30040-119">Gli aggiornamenti delle attività ridondanti vengono inviati al server quando un'attività viene modificata.</span><span class="sxs-lookup"><span data-stu-id="30040-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="30040-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="30040-120">**Sales**</span></span>

<span data-ttu-id="30040-121">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="30040-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="30040-122">Sul modulo **Contratto**, fai doppio clic su **Crea fattura** crea due fatture per un singolo record effettivo.</span><span class="sxs-lookup"><span data-stu-id="30040-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="30040-123">In Internet Explorer 11, gli utenti non sono in grado di creare voci di spesa.</span><span class="sxs-lookup"><span data-stu-id="30040-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="30040-124">Lo storno del costo e lo storno dei valori effettivi di vendita non fatturati non sono collegati.</span><span class="sxs-lookup"><span data-stu-id="30040-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="30040-125">Il pulsante **Aggiorna valori effettivi** sul modulo **Progetto** non aggiorna **Ore effettive attività**.</span><span class="sxs-lookup"><span data-stu-id="30040-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="30040-126">Il plug-in **PreValidateProjectTeamMemberCreate** può creare risorse prenotabili generiche duplicate quando l'attributo **msdyn_isgenericresourceprojectscoped** è impostato su **False**.</span><span class="sxs-lookup"><span data-stu-id="30040-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="30040-127">**Ricalcola** cancella i costi addebitabili dei dettagli della riga di offerta basata sul prodotto e dei dettagli della voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="30040-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="30040-128">In scenari specifici, il plug-in **PostEstimateLineUpdate** visualizza un errore di eccezione di riferimento Null.</span><span class="sxs-lookup"><span data-stu-id="30040-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="30040-129">Durata della scala cronologica sul **Grafico Analisi redditività** non corrisponde alla durata dei costi nel dettaglio della riga di offerta a prezzo fisso dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="30040-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="30040-130">Le impostazioni predefinite per i valori delle unità e delle unità di vendita non vengono applicate correttamente per le categorie di spesa nei moduli **Dettagli voce di contratto** e **Dettagli riga di offerta**.</span><span class="sxs-lookup"><span data-stu-id="30040-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="30040-131">Gli elenchi **Prezzo di costo unità organizzativa** consentono sovrapposizioni della data di validità.</span><span class="sxs-lookup"><span data-stu-id="30040-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="30040-132">Gli utenti non sono autorizzati a modificare **OrgUnit** quando il tipo di ordine non è basato sul lavoro perché questa operazione genererà un errore di eccezione di riferimento Null.</span><span class="sxs-lookup"><span data-stu-id="30040-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="30040-133">Quando si tenta di passare dal modulo **Dettagli riga di offerta**, indietro nella scheda **Offerta**, il modulo si aggiorna e visualizza la scheda **Riepilogo**.</span><span class="sxs-lookup"><span data-stu-id="30040-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
