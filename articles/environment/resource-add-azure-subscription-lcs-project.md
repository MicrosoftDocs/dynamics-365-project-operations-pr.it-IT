---
title: Aggiungere una sottoscrizione di Azure al progetto LCS
description: Questo argomento fornisce informazioni su come connettere la sottoscrizione di Azure a un progetto LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948931"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>Aggiungere una sottoscrizione di Azure al progetto LCS

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Gli ambienti ospitati su cloud devono essere distribuiti utilizzando una sottoscrizione di Azure esistente. Questo argomento descrive come connettere la sottoscrizione di Azure esistente a un progetto LCS. 

## <a name="grant-admin-consent"></a>Concedere il consenso amministratore

1. Nel progetto LCS, nella sezione **Ambienti**, seleziona **Impostazioni di Microsoft Azure**.

![Impostazioni Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Nella pagina **Impostazioni progetto**, nella scheda **Connettori di Azure**, seleziona **Autorizza**. Ciò consente di distribuire gli ambienti a questo progetto.

![Connettori di Azure](./media/2AzureConnectors.png)

3. Seleziona **Autorizza** di nuovo per fornire il consenso amministratore.

![Concedi consenso amministratore](./media/3GrantAdminConsent.png)

4. Accetta la richiesta di autorizzazione.

![Accetta richiesta di autorizzazione](./media/4AcceptPermissionRequest.png)

L'autorizzazione è ora completa. 

![Autorizzazione completata](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Fornire l'accesso a Servizi di distribuzione Dynamics alla sottoscrizione di Azure

1. Vai a [Fatturazione di Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) e seleziona la sottoscrizione. Servizi di distribuzione Dynamics deve accedere a questa sottoscrizione per poter distribuire gli ambienti.

![Dettagli sottoscrizione di Azure](./media/6AzureSubscription.png)

2. Seleziona **Controllo di accesso (IAM)** nel riquadro di spostamento, quindi seleziona **Aggiungi assegnazione di ruolo**.
3. Nel dispositivo di scorrimento sul lato destro, seleziona **Ruolo collaboratore** e nell'elenco fornito trova e seleziona **Servizi di distribuzione Dynamics**. 
4. Seleziona **Salva**.

![Accesso sottoscrizione](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Aggiungere un connettore di sottoscrizione a un progetto LCS

1. Nel progetto LCS, nella pagina **Impostazioni di Microsoft Azure**, seleziona **Aggiungi** per aggiungere un nuovo connettore.
2. Immetti l'ID sottoscrizione di Azure. È possibile trovare l'ID della sottoscrizione di Azure nel [portale di Azure](https://ms.portal.azure.com/), sotto **Impostazioni** in basso a sinistra dello schermo.
3. Nel campo **Configura per l'utilizzo di Azure Resource Manager**, seleziona **Sì**.
4. Assicurati che il dominio tenant AAD della sottoscrizione di Azure corrisponda alla sottoscrizione di Azure proprietaria del dominio che stai utilizzando e seleziona **Avanti**.
5. Nella schermata **Impostazione di Microsoft Azure**, seleziona **Avanti** per confermare. Se ricevi un errore in questa schermata, torna alla sezione [Fornire l'accesso a Servizi di distribuzione Dynamics alla sottoscrizione di Azure](#provide) in questo argomento e assicurati di aver completato tutti i passaggi.
6. Scarica il certificato di gestione di Azure in una cartella locale nel computer e quindi caricalo nel portale di gestione di Azure andando a **Impostazioni** > **Certificati di gestione**. Questo certificato consentirà a LCS di comunicare con Azure. Puoi saltare questo passaggio se il tuo utente ha accesso alla sottoscrizione.
7. Seleziona **Avanti**.
8. Seleziona l'area di Azure in cui eseguire la distribuzione e seleziona un data center vicino al luogo in cui prevedi di utilizzare questo sistema.
9.  Seleziona **Connetti**.

La sottoscrizione di Azure è stata connessa in modo corretto. Ora puoi distribuire ambienti ospitati su cloud di Dynamics 365 Finance.


