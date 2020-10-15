---
title: Iscriversi per gli abbonamenti in anteprima a Project Operations per scenari basati su risorse/non stoccate
description: Questo argomento fornisce informazioni su come abbonarsi e distribuire Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948932"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Iscriversi per gli abbonamenti in anteprima a Project Operations per scenari basati su risorse/non stoccate

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento spiega come abbonarsi all'offerta per i partner/anteprima e distribuire l'ambiente Project Operations per scenari basati su risorse/non stoccate.

## <a name="prerequisites"></a>Prerequisiti

- Riceverai un messaggio e-mail che ti invita a partecipare all'anteprima. È possibile richiedere un'anteprima sul [sito Web di Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- L'utente che distribuisce l'anteprima deve disporre dei diritti di amministratore globale del tenant di Azure.
- La distribuzione di un ambiente Finance richiede una sottoscrizione di Azure valida che verrà fatturata in base all'ambiente. Puoi utilizzare la sottoscrizione esistente della tua organizzazione o utilizzare una [versione di valutazione di Azure](https://azure.microsoft.com/en-us/free/) per iniziare. L'ambiente CDS verrà fornito gratuitamente per un periodo limitato di 30 giorni.

## <a name="subscribe"></a>Sottoscrivi

Quando la [richiesta di anteprima](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) viene approvata, riceverai due offerte da Microsoft tramite e-mail. Queste offerte consentono di distribuire l'anteprima di Project Operations:

- Dynamics 365 Project Operations: versione di valutazione di anteprima
- Versione di valutazione di anteprima di Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Solo una persona, l'amministratore del tenant, in un'organizzazione deve eseguire questa attività. Se non sei abbonato a questa versione, attendi fino a quando la tua organizzazione non è stata iscritta e hai ricevuto le credenziali utente.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations: versione di valutazione di anteprima

1. Riscatta la prima offerta, **Versione di valutazione di Dynamics 365 Project Operations**, con l'URL fornito nel messaggio e-mail di benvenuto.

![Prima offerta](./media/1FirstOffer.png)

2. Verifica di aver effettuato l'accesso come utente appartenente all'organizzazione che si abbonerà al servizio.
3. Procedi con il riscatto dell'offerta. 
4. Seleziona **Sì, aggiungilo al mio account**.

![Riscattare l'offerta](./media/2RedeemFirstOffer.png)

![Confermare l'offerta](./media/3ConfirmFirstOffer.png)

![Offerta riscattata](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Versione di valutazione di anteprima di Dynamics 365 Finance

Ripeti gli stessi passaggi con la seconda offerta dal messaggio e-mail di benvenuto.

## <a name="assign-licenses"></a>Assegnare licenze

> [!IMPORTANT]
> Avrai bisogno dell'accesso amministrativo al portale di Office 365 dell'organizzazione per completare i seguenti passaggi.

1. Vai all'[interfaccia di amministrazione di Microsoft 365](https://portal.office.com/) per assegnare le licenze ai tuoi utenti.

![Portale di amministrazione di Office](./media/5OfficeAdminPortal.png)

2. Nella pagina **Utenti attivi** seleziona gli utenti a cui assegnare una licenza.

![Assegnare licenze](./media/6AssignLicenses.png)

3. Verifica che la licenza di Project Operations sia stata selezionata e seleziona **Salva modifiche**. 

> [!NOTE]
> Non è necessario assegnare l'offerta della versione di valutazione di Finance a un utente.

## <a name="start-a-new-project-in-lcs"></a>Avviare un nuovo progetto in LCS

Creare un nuovo progetto LCS come descritto nell'argomento [Avviare un nuovo progetto in LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Aggiungere una sottoscrizione di Azure a un progetto LCS

Per completare questa attività, segui i passaggi nell'argomento [Aggiungere una sottoscrizione di Azure al progetto LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Distribuire l'ambiente demo di Finance con Project Operations per scenari basati su risorse/non stoccate

Segui le indicazioni nell'argomento [Effettuare il provisioning di un nuovo ambiente](resource-provision-new-environment.md) per completare la distribuzione. Utilizza il tipo di distribuzione [ambiente demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) per l'anteprima.

## <a name="install-cds-setup-and-configuration-data"></a>Installare i dati di impostazione e configurazione CDS

Installa i dati di installazione e configurazione CDS come descritto nell'argomento [Impostare e applicare i dati di configurazione in Common Data Service](resource-apply-pro-setup-config-data.md).

