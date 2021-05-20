---
title: Iscriversi per gli abbonamenti in anteprima a Project Operations per scenari basati su risorse/non stoccate
description: Questo argomento fornisce informazioni su come abbonarsi e distribuire Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 917ead8ff6d9d3ef8374f8ccde608b6cebd50c8c
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948469"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Iscriversi per gli abbonamenti in anteprima a Project Operations per scenari basati su risorse/non stoccate

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Questo argomento spiega come abbonarsi all'offerta per i partner/anteprima e distribuire l'ambiente Project Operations per scenari basati su risorse/non stoccate.

## <a name="prerequisites"></a>Prerequisiti

- Riceverai un messaggio e-mail che ti invita a partecipare all'anteprima. È possibile richiedere un'anteprima sul [sito Web di Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- L'utente che distribuisce l'anteprima deve disporre dei diritti di amministratore globale del tenant di Azure.
- La distribuzione di un ambiente Finance richiede una sottoscrizione di Azure valida che verrà fatturata in base all'ambiente. Puoi utilizzare la sottoscrizione esistente della tua organizzazione o utilizzare una [versione di valutazione di Azure](https://azure.microsoft.com/en-us/free/) per iniziare. L'ambiente CDS verrà fornito gratuitamente per un periodo limitato di 30 giorni.

## <a name="subscribe"></a>Sottoscrivi

Quando la [richiesta di anteprima](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) viene approvata, riceverai tre offerte da Microsoft tramite e-mail. Queste offerte consentono di distribuire l'anteprima di Project Operations:

- Versione di valutazione di Dynamics 365 Project Operations (CRM).
- Office 365 Project Operations - Versione di valutazione di anteprima
- Dynamics 365 Finance - Versione di valutazione di anteprima

> [!IMPORTANT]
> Solo una persona, l'amministratore del tenant, in un'organizzazione deve eseguire questa attività. Se non sei abbonato a questa versione, attendi fino a quando la tua organizzazione non è stata iscritta e hai ricevuto le credenziali utente.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Versione di valutazione di Dynamics 365 Project Operations (CRM). 

Prima di iniziare, assicurati di aver effettuato l'accesso a un browser con l'account utente di lavoro nel tenant in cui desideri l'anteprima di Project Operations.

1. Riscatta il primo codice offerta,**Dynamics 365 Project Operations (CRM) - Versione di valutazione** incollandolo nell'URL del browser.

![Riscattare l'offerta](./media/16RedeemFirstOfferNew.png)

2. Conferma l'ordine.

![Conferma l'ordine](./media/17ConfirmOrderNew.png)

Vedrai la conferma che l'offerta è stata riscattata.

![Conferma](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - Versione di valutazione di anteprima

Ripeti gli stessi passaggi del primo codice dell'offerta. Assicurati di aggiungere il secondo codice dell'offerta utilizzando lo stesso account utente utilizzato con il primo codice dell'offerta.

### <a name="dynamics-365-finance-preview-trial"></a>Versione di valutazione di anteprima di Dynamics 365 Finance

Ripeti gli stessi passaggi con l'ultima offerta dal messaggio e-mail di benvenuto.

## <a name="assign-licenses"></a>Assegnare licenze

> [!IMPORTANT]
> Avrai bisogno dell'accesso amministrativo al portale di Microsoft 365 dell'organizzazione per completare i seguenti passaggi.

1. Vai all'[interfaccia di amministrazione di Microsoft 365](https://portal.office.com/) per assegnare le licenze ai tuoi utenti.

![Home page dell'interfaccia di amministrazione](./media/14AdminPortal.png)

2. Nella pagina **Utenti attivi** seleziona gli utenti a cui assegnare una licenza.

![Assegnare licenze](./media/15AssignLicenses.png)

3. Verifica che la licenza **Anteprima di Dynamics 365 Project Operations (CRM)** e **Anteprima di Office 365 Project Operations** sia stata selezionata e seleziona **Salva modifiche**.

> [!NOTE]
> Non è necessario assegnare l'offerta della versione di valutazione di Finance a un utente.

## <a name="start-a-new-project-in-lcs"></a>Avviare un nuovo progetto in LCS

Creare un nuovo progetto LCS come descritto nell'argomento [Avviare un nuovo progetto in LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Aggiungere una sottoscrizione di Azure a un progetto LCS

Per completare questa attività, segui i passaggi nell'argomento [Aggiungere una sottoscrizione di Azure al progetto LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Distribuire l'ambiente demo di Finance con Project Operations per scenari basati su risorse/non stoccate

Segui le indicazioni nell'argomento [Effettuare il provisioning di un nuovo ambiente](resource-provision-new-environment.md) per completare la distribuzione. Utilizza il tipo di distribuzione [ambiente demo](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) per l'anteprima. 

## <a name="install-cds-setup-and-configuration-data"></a>Installare i dati di impostazione e configurazione CDS

Installa i dati di installazione e configurazione CDS come descritto nell'argomento [Impostare e applicare i dati di configurazione in Common Data Service](resource-apply-pro-setup-config-data.md).
Completa questo passaggio solo dopo che l'ambiente demo Finance è stato distribuito e i dati demo in FO sono pronti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]