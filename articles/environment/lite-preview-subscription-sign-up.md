---
title: Iscriversi a un abbonamento di anteprima - semplice
description: 'Questo argomento fornisce informazioni su come iscriversi alla distribuzione semplice di Project Operations: accordo per la fatturazione proforma.'
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 44edf2613ea4b26dadbd9edc47c784c488c577de
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290049"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Iscriversi a un abbonamento di anteprima - semplice 

Questo argomento spiega come iscriversi all'offerta di anteprima per i partner e implementare la distribuzione semplice Dynamics 365 Project Operations: dalla transazione alla fatturazione proforma.

> [!NOTE]
> Questo processo cambierà nelle prossime versioni di Project Operations.

## <a name="prerequisites"></a>Prerequisiti

- Riceverai un messaggio e-mail che ti invita a partecipare all'anteprima. È possibile richiedere un'anteprima sul [sito Web di Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- L'utente che distribuisce l'anteprima deve disporre dei diritti di amministratore globale del tenant di Azure.
- Rivedi tutti i termini e le condizioni.

## <a name="subscribe"></a>Sottoscrivi

Quando ricevi l'approvazione per una [richiesta di anteprima](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), riceverai due offerte da Microsoft tramite e-mail. Queste offerte consentono di distribuire l'anteprima di Project Operations:

- Versione di valutazione di Dynamics 365 Project Operations (CRM).
- Office 365 Project Operations - Versione di valutazione di anteprima

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

## <a name="assign-licenses"></a>Assegnare licenze

> [!IMPORTANT]
> Avrai bisogno dell'accesso amministrativo al portale di Microsoft 365 dell'organizzazione per completare i seguenti passaggi.


1. Vai all'[interfaccia di amministrazione di Microsoft 365](https://portal.office.com/) per assegnare le licenze ai tuoi utenti.

![Home page dell'interfaccia di amministrazione](./media/14AdminPortal.png)

2. Nella pagina **Utenti attivi** seleziona gli utenti a cui assegnare una licenza.

![Assegnare licenze](./media/15AssignLicenses.png)

3. Verifica che le licenze **Dynamics 365 Project Operations (CRM) Anteprima** e **Office 365 Project Operations - Anteprima** siano selezionate. 
4. Seleziona **Salva modifiche**.

## <a name="create-a-new-cds-environment"></a>Creare un nuovo ambiente CDS

1. Esegui il provisioning di un nuovo ambiente di distribuzione CDS di Project Operations seguendo le istruzioni nell'argomento [Modello di distribuzione CDS](lite-deployment.md). Quando selezioni il tipo di ambiente, assicurati di utilizzare **Versione di valutazione (basata su abbonamento)**.
![Nuovo ambiente](./media/19CreateEnvironment.png)

2. Seleziona l'impostazione **Abilita app Dynamics 365** e lascia **Distribuisci automaticamente queste app** vuoto.  
3. Seleziona **Salva** per creare l'ambiente.

![Aggiungi database](./media/20CreateEnvironment1.png)

4. Dopo aver creato l'ambiente, installa la soluzione **Microsoft Dynamics 365 Project Operations**. 

![Installare la soluzione](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installare i dati dimostrativi di installazione e configurazione CDS

Installa i dati dimostrativi di installazione e configurazione CDS seguendo le istruzioni nell'argomento [Applicare i dati di installazione e configurazione dimostrativi](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]