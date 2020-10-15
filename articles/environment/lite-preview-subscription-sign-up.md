---
title: Iscriversi a un abbonamento di anteprima
description: 'Questo argomento fornisce informazioni su come iscriversi alla distribuzione semplice di Project Operations: accordo per la fatturazione proforma.'
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948929"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Iscriversi a un abbonamento in anteprima per la distribuzione semplice: accordo per la fatturazione proforma

Questo argomento spiega come iscriversi all'offerta per i partner di anteprima e applicare la distribuzione semplice di Dynamics 365 Project Operations: accordo per la fatturazione proforma.

> [!NOTE]
> Questo processo cambierà nelle prossime versioni di Project Operations.

## <a name="prerequisites"></a>Prerequisiti

- Riceverai un messaggio e-mail che ti invita a partecipare all'anteprima. È possibile richiedere un'anteprima sul [sito Web di Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- L'utente che distribuisce l'anteprima deve disporre dei diritti di amministratore globale del tenant di Azure.
- L'utente che distribuisce l'anteprima avrà bisogno di un numero di telefono e di una carta di credito valida. Durante la registrazione, non ci saranno addebiti sulla carta per sei mesi. Dopo sei mesi, è necessario annullare l'abbonamento. 
- Rivedi tutti i termini e le condizioni.

## <a name="subscribe"></a>Sottoscrivi

Quando ricevi l'approvazione per una [richiesta di anteprima](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), riceverai due offerte da Microsoft tramite e-mail. Queste offerte consentono di distribuire l'anteprima di Project Operations:

- Versione di valutazione di anteprima Dynamics 365 Customer Service: codice monouso
- Dynamics 365 Project Operations: versione di valutazione di anteprima

### <a name="dynamics-365-customer-service-paid-offer"></a>Offerta a pagamento di Dynamics 365 Customer Service

1. Utilizzando una finestra del browser InPrivate/Incognito, riscatta il primo codice offerta per Dynamics 365 Customer Service. Per iscriverti a Customer Service, avrai bisogno di:

- Un numero di telefono
- Una carta di credito. Durante la registrazione, non ci saranno addebiti sulla carta per sei mesi. Dopo sei mesi, è necessario annullare l'abbonamento.
- Rivedi tutti i termini e le condizioni.

2. Fornisci le tue informazioni di contatto.

![Informazioni di contatto](./media/1ContactInformation.png)

3. Fornisci i dettagli del nuovo tenant.

![Creare l'ID utente](./media/2CreateUserID.png)

4. Verifica la tua identità, salva il nuovo ID utente e quindi seleziona **Configura**.

![Salvare le informazioni](./media/3SaveInfo.png)

5. Completa la registrazione con carta di credito e rivedi tutti i termini e le condizioni. 

![Completare con carta di credito](./media/4CompleteCreditCard.png)

![Completamento della transazione con carta di credito](./media/5CreditCardCheckout.png)

![Salvare l'ordine](./media/6SaveOrder.png)

![Conferma della carta di credito](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Annullare l'offerta di Dynamics 365 Customer Service Enterprise

L'offerta Dynamics 365 Customer Service Enterprise viene fornita gratuitamente per sei mesi. L'offerta si rinnoverà a tariffa piena al termine del semestre. Per annullare prima della data di rinnovo, completa le seguenti istruzioni. 

> [!NOTE]
> Dopo aver completato questi passaggi, non sarà più possibile utilizzare l'ambiente di anteprima pubblica di Project Operations.

1. Vai al [Portale di amministrazione](https://admin.microsoft.com/) e sotto **Fatturazione** seleziona **I tuoi prodotti**.

![Portale di amministrazione, pagina I tuoi prodotti](./media/8AdminPortal.png)

2. Seleziona l'**offerta Dynamics 365 Customer Service Enterprise**.

![Annullare la sottoscrizione](./media/9CancelSubscription.png)

3. Seleziona **Impostazioni** > **Azioni** > **Annulla abbonamento**.
4. Nel modulo **Annulla abbonamento**, inserisci le informazioni nei campi obbligatori.
5. Seleziona **Annulla** > **Abbonamento.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations: versione di valutazione di anteprima

1. Riscatta la seconda offerta, versione di valutazione di Dynamics 365 Project Operations con l'URL fornito nel messaggio e-mail di benvenuto.

![Riscattare l'offerta 2](./media/10RedeemOffer2.png)

2. Verifica di aver effettuato l'accesso come utente che appartiene alla stessa organizzazione che è stata sottoscritta utilizzando il primo codice offerta e quindi procedi con il riscatto dell'offerta. 
3. Seleziona **Sì, aggiungilo al mio account**.

![Aggiungere all'account](./media/11AddToAccount.png)

![Schermata Prova ora](./media/12TryNow.png)

![Dettagli ordine](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Assegnare licenze

> [!IMPORTANT]
> Avrai bisogno dell'accesso amministrativo al portale di Office 365 dell'organizzazione per completare i seguenti passaggi.

1. Vai all'[interfaccia di amministrazione di Microsoft 365](https://portal.office.com/) per assegnare le licenze ai tuoi utenti.

![Home page dell'interfaccia di amministrazione](./media/14AdminPortal.png)

2. Nella pagina **Utenti attivi** seleziona gli utenti a cui assegnare una licenza.

![Assegnare licenze](./media/15AssignLicenses.png)

3. Verifica che la licenza di **Customer Service Enterprise** e **Project Operations** siano state selezionate e seleziona **Salva modifiche**.

## <a name="create-a-new-cds-environment"></a>Creare un nuovo ambiente CDS

Esegui il provisioning di un nuovo ambiente di distribuzione CDS di Project Operations seguendo le istruzioni nell'argomento [Modello di distribuzione CDS](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installare i dati dimostrativi di installazione e configurazione CDS

Installa i dati dimostrativi di installazione e configurazione CDS seguendo le istruzioni nell'argomento [Applicare i dati di installazione e configurazione dimostrativi](lite-apply-demo-setup-config-data.md).
