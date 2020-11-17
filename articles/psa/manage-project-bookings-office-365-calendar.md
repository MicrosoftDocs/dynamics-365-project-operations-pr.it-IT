---
title: Gestire progetti e prenotazioni nel calendario di Office 365
description: Come gestire progetti e prenotazioni nel calendario di Office 365
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 31ff541f5b817c29b162c38c282df8cfd866e375
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129053"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a><span data-ttu-id="21dbc-103">Gestire progetti e prenotazioni nel calendario (Project Service)</span><span class="sxs-lookup"><span data-stu-id="21dbc-103">Manage projects and bookings in your calendar (Project Service)</span></span>

> [!Note]
> <span data-ttu-id="21dbc-104">DEPRECATA: questa funzionalità è stata deprecata e non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="21dbc-104">DEPRECATED: This feature has been deprecated and is no longer available.</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

<span data-ttu-id="21dbc-105">Visualizza gli appuntamenti, le prenotazioni di progetto- lavoro e le assegnazioni di ordini di lavoro di Field Service utilizzando il calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].</span><span class="sxs-lookup"><span data-stu-id="21dbc-105">View personal appointments, project-work bookings, and field service work order assignments using the [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="21dbc-106">Con tutto in un'unica posizione, è semplice la gestione delle giornate.</span><span class="sxs-lookup"><span data-stu-id="21dbc-106">With everything in one place, it’s easy to manage your day.</span></span> <span data-ttu-id="21dbc-107">Le riunioni, le prenotazioni, gli appuntamenti e le attività sono tutti disponibili nel calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].</span><span class="sxs-lookup"><span data-stu-id="21dbc-107">Your meetings, appointments, bookings, and tasks are all available in your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="21dbc-108">Se utilizzi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], puoi anche registrare gli appuntamenti personali nella visualizzazione di voce di tempo Project Service.</span><span class="sxs-lookup"><span data-stu-id="21dbc-108">If you’re using [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you can also enter your personal appointments in the Project Service time entry view.</span></span> <span data-ttu-id="21dbc-109">In questo modo i responsabili della risorsa e di progetto conoscono la tua disponibilità per i progetti.</span><span class="sxs-lookup"><span data-stu-id="21dbc-109">This lets project and resource managers know your availability for projects.</span></span> <span data-ttu-id="21dbc-110">Verrà inoltre salvato tempo, poiché non sarà necessario specificare due volte informazioni sugli appuntamenti personali.</span><span class="sxs-lookup"><span data-stu-id="21dbc-110">It also saves you time, because you don’t have to enter info about your personal appointments twice.</span></span> <span data-ttu-id="21dbc-111">Puoi semplicemente importare gli appuntamenti personali dal calendario nella visualizzazione di voce di tempo Project Service.</span><span class="sxs-lookup"><span data-stu-id="21dbc-111">You can simply import your personal appointments from your calendar to Project Service time entry view.</span></span>  
  
 <span data-ttu-id="21dbc-112">Il calendario sincronizzerà le prenotazioni di progetto e ordine di lavoro dalla data corrente fino alle quattro settimane successive.</span><span class="sxs-lookup"><span data-stu-id="21dbc-112">Your calendar will sync project and work order bookings from today to upcoming four weeks.</span></span> <span data-ttu-id="21dbc-113">Questa impostazione non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="21dbc-113">This setting can’t be changed.</span></span>  
  
 <span data-ttu-id="21dbc-114">La sincronizzazione è supportata solo in una direzione, da PSA al calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].</span><span class="sxs-lookup"><span data-stu-id="21dbc-114">Syncing is only supported one way, from PSA to your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span> <span data-ttu-id="21dbc-115">È possibile sincronizzare in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="21dbc-115">You can sync in the reverse order.</span></span> 
  
 <span data-ttu-id="21dbc-116">Per informazioni su come utilizzare il calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] vedi [Calendario in Outlook sul Web per ufficio](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)</span><span class="sxs-lookup"><span data-stu-id="21dbc-116">To learn how to use your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, see [Calendar in Outlook on the web for business](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span></span>  
  
## <a name="setup"></a><span data-ttu-id="21dbc-117">Configurazione</span><span class="sxs-lookup"><span data-stu-id="21dbc-117">Setup</span></span>  
 <span data-ttu-id="21dbc-118">Prima di poter visualizzare e gestire le prenotazioni nel calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], devi impostare alcune cose.</span><span class="sxs-lookup"><span data-stu-id="21dbc-118">Before you can see and manage your bookings on your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, you need to set a few things up.</span></span>  
  
- <span data-ttu-id="21dbc-119">È necessario disporre delle credenziali di amministratore globale [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] o di amministratore di sistema .</span><span class="sxs-lookup"><span data-stu-id="21dbc-119">You will need to have [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Global Administrator or System Administrator credentials.</span></span>  
  
- <span data-ttu-id="21dbc-120">L'amministratore dovrà configurare il profilo di server e-mail e ogni utente dovrà configurare la propria cassetta postale.</span><span class="sxs-lookup"><span data-stu-id="21dbc-120">Your Admin will need to configure the email server profile and each user will need to configure their mailbox.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="21dbc-121">[Configurare l'elaborazione dei messaggi e-mail tramite la sincronizzazione lato server](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span><span class="sxs-lookup"><span data-stu-id="21dbc-121">[Set up email processing through server-side synchronization](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span></span>  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a><span data-ttu-id="21dbc-122">Abilitare la sincronizzazione per l'organizzazione (attività di amministrazione)</span><span class="sxs-lookup"><span data-stu-id="21dbc-122">Turn on synchronization for your organization (admin task)</span></span>  
  
1.  <span data-ttu-id="21dbc-123">Nel menu principale fai clic su **Impostazioni** > **Amministrazione**.</span><span class="sxs-lookup"><span data-stu-id="21dbc-123">From the main menu, click **Settings** > **Administration**.</span></span>  
  
2.  <span data-ttu-id="21dbc-124">Fare clic su **Impostazioni di sistema**.</span><span class="sxs-lookup"><span data-stu-id="21dbc-124">Click **System Settings**.</span></span>  
  
3.  <span data-ttu-id="21dbc-125">Fai clic sulla scheda **Sincronizzazione**.</span><span class="sxs-lookup"><span data-stu-id="21dbc-125">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="21dbc-126">In **Scegli se abilitare la sincronizzazione delle prenotazioni risorse con Outlook** seleziona **Sincronizza prenotazioni risorse con Outlook**.</span><span class="sxs-lookup"><span data-stu-id="21dbc-126">Under **Select whether to enable syncing of resource booking with**, check the **Synchronize resource booking with Outlook**.</span></span>  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a><span data-ttu-id="21dbc-127">Abilitare la sincronizzazione per il profilo utente (attività utente)</span><span class="sxs-lookup"><span data-stu-id="21dbc-127">Turn on synchronization for your user profile (user task)</span></span>  
  
1.  <span data-ttu-id="21dbc-128">Fai clic sul pulsante **Impostazioni** nell'angolo in alto a destra dello schermo.</span><span class="sxs-lookup"><span data-stu-id="21dbc-128">Click the **Settings** button in the upper-right corner of the screen.</span></span>  
  
2.  <span data-ttu-id="21dbc-129">Fare clic su **Opzioni**.</span><span class="sxs-lookup"><span data-stu-id="21dbc-129">Click **Options**.</span></span>  
  
3.  <span data-ttu-id="21dbc-130">Fai clic sulla scheda **Sincronizzazione**.</span><span class="sxs-lookup"><span data-stu-id="21dbc-130">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="21dbc-131">In **Sincronizzazione di prenotazione delle risorse per Outlook** seleziona **Prenotazione delle risorse sincronizzazione con Outlook**.</span><span class="sxs-lookup"><span data-stu-id="21dbc-131">Under **Resource booking sync with Outlook**, check the **Synchronization resource booking with Outlook**.</span></span>  
  
## <a name="import-your-personal-appointments-user-task"></a><span data-ttu-id="21dbc-132">Importare gli appuntamenti personali (attività utente)</span><span class="sxs-lookup"><span data-stu-id="21dbc-132">Import your personal appointments (user task)</span></span>  
 <span data-ttu-id="21dbc-133">Puoi importare gli appuntamenti personali dal calendario nella visualizzazione di voce di tempo Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="21dbc-133">You can import your personal appointments from your calendar to Project Service Automation time entry view.</span></span>  
  
1. <span data-ttu-id="21dbc-134">Apri il calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] e fai clic su **Importa dati**.</span><span class="sxs-lookup"><span data-stu-id="21dbc-134">Open [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar and click **Import Data**.</span></span>  
  
2. <span data-ttu-id="21dbc-135">Nella schermata Filtri seleziona **Appuntamenti di Exchange**, quindi fai clic su **Applica**.</span><span class="sxs-lookup"><span data-stu-id="21dbc-135">On the Filters screen, select **Appointments from Exchange** and then click **Apply**.</span></span>  
  
3. <span data-ttu-id="21dbc-136">Il sistema sposterà gli appuntamenti nella visualizzazione di voce di tempo come voci suggerite della settimana corrente.</span><span class="sxs-lookup"><span data-stu-id="21dbc-136">The system will pull appointments into time entry view as suggested entries from the current week.</span></span> <span data-ttu-id="21dbc-137">Per aggiungere le voci di un'altra settimana, fai clic su **Precedente** o **Successiva**.</span><span class="sxs-lookup"><span data-stu-id="21dbc-137">To add entries for another week, click **Previous** or **Next**.</span></span>  
  
4. <span data-ttu-id="21dbc-138">Seleziona l'appuntamento che desideri aggiungere alla visualizzazione di voce di tempo Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="21dbc-138">Select the appointment that you want to add to Project Service Automation time entry view.</span></span>  
  
5. <span data-ttu-id="21dbc-139">Nella finestra popup **Inserimento ore** seleziona le opzioni appropriate per convertire l'appuntamento in una visualizzazione di voce di tempo Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="21dbc-139">On the **Time Entry** popup box, select the appropriate options to convert the appointment to a Project Service Automation time entry view.</span></span>  
  
6. <span data-ttu-id="21dbc-140">Fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="21dbc-140">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="21dbc-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21dbc-141">See Also</span></span>  
 [<span data-ttu-id="21dbc-142">Guida per tempo, spese e collaborazione</span><span class="sxs-lookup"><span data-stu-id="21dbc-142">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
