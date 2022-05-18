---
title: Gestire progetti e prenotazioni nel calendario di Office 365
description: Come gestire progetti e prenotazioni nel calendario di Office 365
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: cf51333179d2d972af84de7adb4b718b6e17d038
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598907"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Gestire progetti e prenotazioni nel calendario (Project Service)

> [!Note]
> DEPRECATA: questa funzionalità è stata deprecata e non è più disponibile.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Visualizza gli appuntamenti, le prenotazioni di progetto- lavoro e le assegnazioni di ordini di lavoro di Field Service utilizzando il calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Con tutto in un'unica posizione, è semplice la gestione delle giornate. Le riunioni, le prenotazioni, gli appuntamenti e le attività sono tutti disponibili nel calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Se utilizzi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], puoi anche registrare gli appuntamenti personali nella visualizzazione di voce di tempo Project Service. In questo modo i responsabili della risorsa e di progetto conoscono la tua disponibilità per i progetti. Verrà inoltre salvato tempo, poiché non sarà necessario specificare due volte informazioni sugli appuntamenti personali. Puoi semplicemente importare gli appuntamenti personali dal calendario nella visualizzazione di voce di tempo Project Service.  
  
 Il calendario sincronizzerà le prenotazioni di progetto e ordine di lavoro dalla data corrente fino alle quattro settimane successive. Questa impostazione non può essere modificata.  
  
 La sincronizzazione è supportata solo in una direzione, da PSA al calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. È possibile sincronizzare in ordine inverso. 
  
 Per informazioni su come utilizzare il calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] vedi [Calendario in Outlook sul Web per ufficio](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)  
  
## <a name="setup"></a>Configurazione  
 Prima di poter visualizzare e gestire le prenotazioni nel calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], devi impostare alcune cose.  
  
- È necessario disporre delle credenziali di amministratore globale [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] o di amministratore di sistema .  
  
- L'amministratore dovrà configurare il profilo di server e-mail e ogni utente dovrà configurare la propria cassetta postale. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configurare l'elaborazione dei messaggi e-mail tramite la sincronizzazione lato server](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Abilitare la sincronizzazione per l'organizzazione (attività di amministrazione)  
  
1.  Nel menu principale fai clic su **Impostazioni** > **Amministrazione**.  
  
2.  Fare clic su **Impostazioni di sistema**.  
  
3.  Fai clic sulla scheda **Sincronizzazione**.  
  
4.  In **Scegli se abilitare la sincronizzazione delle prenotazioni risorse con Outlook** seleziona **Sincronizza prenotazioni risorse con Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Abilitare la sincronizzazione per il profilo utente (attività utente)  
  
1.  Fai clic sul pulsante **Impostazioni** nell'angolo in alto a destra dello schermo.  
  
2.  Fare clic su **Opzioni**.  
  
3.  Fai clic sulla scheda **Sincronizzazione**.  
  
4.  In **Sincronizzazione di prenotazione delle risorse per Outlook** seleziona **Prenotazione delle risorse sincronizzazione con Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importare gli appuntamenti personali (attività utente)  
 Puoi importare gli appuntamenti personali dal calendario nella visualizzazione di voce di tempo Project Service Automation.  
  
1. Apri il calendario di [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] e fai clic su **Importa dati**.  
  
2. Nella schermata Filtri seleziona **Appuntamenti di Exchange**, quindi fai clic su **Applica**.  
  
3. Il sistema sposterà gli appuntamenti nella visualizzazione di voce di tempo come voci suggerite della settimana corrente. Per aggiungere le voci di un'altra settimana, fai clic su **Precedente** o **Successiva**.  
  
4. Seleziona l'appuntamento che desideri aggiungere alla visualizzazione di voce di tempo Project Service Automation.  
  
5. Nella finestra popup **Inserimento ore** seleziona le opzioni appropriate per convertire l'appuntamento in una visualizzazione di voce di tempo Project Service Automation.  
  
6. Fai clic su **Salva**.  
  
### <a name="see-also"></a>Vedi anche  
 [Guida per tempo, spese e collaborazione](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
