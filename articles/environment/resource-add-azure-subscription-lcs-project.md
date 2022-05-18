---
title: Aggiungere una sottoscrizione di Azure a un progetto LCS
description: Questo argomento fornisce informazioni su come connettere la sottoscrizione di Azure a un progetto LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 839c510838b0bccb718b8ca8a4f71a1c46e7ea3f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595917"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Aggiungere una sottoscrizione di Azure a un progetto LCS

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Gli ambienti ospitati su cloud devono essere distribuiti utilizzando una sottoscrizione di Azure esistente. Questo argomento descrive come connettere la sottoscrizione di Azure esistente a un progetto LCS. 

## <a name="grant-admin-consent"></a>Concedere il consenso amministratore

1. Nel progetto LCS, nella sezione **Ambienti**, seleziona **Impostazioni di Microsoft Azure**.

![Impostazioni di Microsoft Azure.](./media/1MicrosoftAzureSettings.png)

2. Nella pagina **Impostazioni progetto**, nella scheda **Connettori di Azure**, seleziona **Autorizza**. Ciò consente di distribuire gli ambienti a questo progetto.

![Connettori di Azure.](./media/2AzureConnectors.png)

3. Seleziona **Autorizza** di nuovo per fornire il consenso amministratore.

![Concedere il consenso amministratore.](./media/3GrantAdminConsent.png)

4. Accetta la richiesta di autorizzazione.

![Accettare la richiesta di autorizzazione.](./media/4AcceptPermissionRequest.png)

L'autorizzazione è ora completa. 

![Autorizzazione completata.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Fornire l'accesso a Servizi di distribuzione Dynamics alla sottoscrizione di Azure

1. Vai a [Fatturazione di Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) e seleziona la sottoscrizione. Servizi di distribuzione Dynamics deve accedere a questa sottoscrizione per poter distribuire gli ambienti.

![Dettagli sottoscrizione di Azure.](./media/6AzureSubscription.png)

2. Seleziona **Controllo di accesso (IAM)** nel riquadro di spostamento, quindi seleziona **Aggiungi assegnazione di ruolo**.
3. Nel dispositivo di scorrimento sul lato destro, seleziona **Ruolo collaboratore** e nell'elenco fornito trova e seleziona **Servizi di distribuzione Dynamics**. 
4. Seleziona **Salva**.

![Accesso sottoscrizione.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Aggiungere un connettore di sottoscrizione a un progetto LCS

1. Nel progetto LCS, nella pagina **Impostazioni di Microsoft Azure**, seleziona **Aggiungi** per aggiungere un nuovo connettore.
2. Immetti l'ID sottoscrizione di Azure. È possibile trovare l'ID della sottoscrizione di Azure nel [portale di Azure](https://ms.portal.azure.com/), sotto **Impostazioni** in basso a sinistra dello schermo.
3. Nel campo **Configura per l'utilizzo di Azure Resource Manager**, seleziona **Sì**.
4. Assicurati che il dominio tenant AAD della sottoscrizione di Azure corrisponda alla sottoscrizione di Azure proprietaria del dominio che stai utilizzando e seleziona **Avanti**.
5. Nella schermata **Impostazione di Microsoft Azure**, seleziona **Avanti** per confermare. Se ricevi un errore in questa schermata, torna alla sezione [Fornire l'accesso a Servizi di distribuzione Dynamics alla sottoscrizione di Azure](#provide) in questo argomento e assicurati di aver completato tutti i passaggi.
6. Scarica il certificato di gestione di Azure in una cartella locale sul tuo computer. Chiedi all'amministratore della tua sottoscrizione di Azure di caricare il certificato nel portale di gestione di Azure selezionando la sottoscrizione e andando in **Impostazioni** > **Certificati di gestione**. Questo certificato consente a LCS di comunicare con Azure per tuo conto. Puoi saltare questo passaggio se il tuo utente ha accesso alla sottoscrizione.
7. Seleziona **Avanti**.
8. Seleziona l'area di Azure in cui eseguire la distribuzione e seleziona un data center vicino al luogo in cui prevedi di utilizzare questo sistema.
9.  Seleziona **Connetti**.

La sottoscrizione di Azure è stata connessa in modo corretto. Ora puoi distribuire gli ambienti ospitati nel cloud di Dynamics 365 Finance.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
