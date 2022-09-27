---
title: Iscrizione alle versioni di valutazione di Project Operations
description: In questo articolo sono riportate informazioni su come distribuire una versione di valutazione di Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 60790d83d5fcc8c75fef8eac2877d1ca14a761f2
ms.sourcegitcommit: 385081ecc839d7d4a557eda2bb1578ca073f7e41
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528013"
---
# <a name="sign-up-for-project-operations-trials"></a>Iscrizione alle versioni di valutazione di Project Operations 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, distribuzione lite: transazioni di fatturazione proforma e Project Operations per scenari basati su materiali stoccati/produzione_ 



Questo articolo spiega come iscriversi all'offerta partner di anteprima e distribuire un ambiente Dynamics 365 Project Operations.

Con la nuova versione di valutazione di Project Operations, puoi distribuire automaticamente uno dei tre scenari di distribuzione supportati completando un questionario che consiglia l'approccio di distribuzione migliore. In questo articolo sono riportate informazioni su come:

- riscattare la tua offerta di prova.
- avviare il provisioning.
- Configurare la doppia scrittura.
- Altre informazioni su Project Operations. 

La tabella seguente illustra i dettagli della nuova offerta di prova.

| **Articolo offerta**               | **Dettagli**                                  |
|------------------------------|----------------------------------------------|
| Tipo di offerta                   | Questo tipo di offerta è amministratore, quindi è necessario un amministratore del tenant per riscattarla. |
| Utilizzo dell'offerta                    | Una volta per tenant                          |
| Durata dell'offerta               | 30 giorni di calendario                             |
| Riscatti per tenant       | 1                                            |
| Interno                    | 1 estensione, 30 giorni di calendario               |
| Numero di ambienti di prova | 3                                            |


## <a name="admin-trial-details"></a>Dettagli dell'amministratore della versione di prova
La tabella seguente elenca i dettagli della versione di prova e come si applicano a ciascun tipo di distribuzione.

| **Articolo**                      | **Lite**                                     | **Materiali non stoccati** | **Materiali stoccati** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Dati di configurazione forniti           | Sì                                          | Sì                       | Sì (USSI)            |
| Dati delle transazioni            | No                                           | No                        | No                    |
| Tempo di approvvigionamento in minuti  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Prerequisiti
Sono richiesti i seguenti prerequisitivi per distribuire una versione di prova di Dynamics 365 Project Operations.

- Iscriviti a [Dynamics 365 Project Operations - Versione di valutazione](https://www.aka.ms/try-po).
- L'utente che distribuisce l'anteprima deve disporre dei diritti di amministratore globale del tenant di Azure.

> [!IMPORTANT]
> Solo una persona in un'organizzazione, l'amministratore del tenant, deve svolgere questa attività. Se non sei abbonato a questa versione, attendi fino a quando la tua organizzazione non è stata iscritta e hai ricevuto le credenziali utente.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - Versione di valutazione 

Prima di iniziare, accedi a un browser con l'account di lavoro dell'utente nel tenant in cui desideri visualizzare l'anteprima di Project Operations.

1. Riscatta il primo codice offerta, **Dynamics 365 Project Operations - Versione di valutazione** incollandolo nell'URL del browser.

    ![Riscattare l'offerta](./media/16RedeemFirstOfferNew.png)

2. Conferma l'ordine.

    ![Conferma l'ordine](./media/17ConfirmOrderNew.png)

  Vedrai che la conferma dell'offerta è stata riscossa con successo.

   ![Conferma](./media/18OrderConfirmationNew.png)

  Verrai reindirizzato all'[interfaccia di amministrazione di Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Questionario e provisioning

1.  Vai all'[interfaccia di amministrazione di Power Platform](https://admin.powerplatform.com/projectoperationstrial) e completa il questionario.  
2.  Rivedi il tipo di distribuzione consigliato e seleziona **Inizia installazione** per avviare il provisioning.
3.  Esamina le condizioni, quindi seleziona **Avvia**.

   Dopo l'avvio del provisioning, verrai reindirizzato all'elenco degli ambienti nell'interfaccia di amministrazione di Power Platform. Durante il provisioning, lo stato del tuo ambiente è **PreparingInstance**.
 
  Al termine del provisioning, lo stato del tuo ambiente è **Pronto**. Il provisioning dell'ambiente include la distribuzione di dati dimostrativi.
 
4.  Seleziona il rispettivo URL Microsoft Dataverse e gli URL delle app per la finanza e le operazioni per convalidare la distribuzione.

## <a name="configuring-dual-write"></a>Configurazione della doppia scrittura
- Per configurare i ruoli di sicurezza per la doppia scrittura, vedi [Aggiornare le impostazioni di sicurezza su Project Operations in Dataverse](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- Per accedere alla configurazione della doppia scrittura, vai all'istanza delle app per la finanza e le operazioni, quindi vai a **Gestione dati** > **Doppia scrittura**.
- Per configurare le mappe a doppia scrittura, vedi [Eseguire le mappe a doppia scrittura di Project Operations](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Assegnare licenze

Avrai bisogno dell'accesso amministrativo al portale di Microsoft 365 dell'organizzazione per completare i seguenti passaggi.

1. Vai all'[interfaccia di amministrazione di Microsoft 365](https://portal.office.com/) per assegnare le licenze ai tuoi utenti.

   ![Home page dell'interfaccia di amministrazione](./media/14AdminPortal.png)

2. Nella pagina **Utenti attivi** seleziona gli utenti a cui assegnare una licenza.

   ![Assegnare licenze](./media/15AssignLicenses.png)

3. Verifica che la licenza di **Anteprima di Dynamics 365 Project Operations** sia stata selezionata e seleziona **Salva modifiche**.

## <a name="additional-resources"></a>Risorse aggiuntive

Le seguenti risorse forniscono una guida utile quando inizi il tuo viaggio con Project Operations:

- [Serie di video -Panoramica di Project Operations, con approfondimenti e roadmap](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/training/modules/examine-dynamics-365-project-operations/)
- [Determinare il tipo di distribuzione](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Domande frequenti

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Cosa succede se ho bisogno di ALM o ELM per il mio ambiente delle app per la finanza e le operazioni?

- Per i partner che richiedono funzionalità di gestione del ciclo di vita dell'ambiente completo, vedi [Richiesta di licenza sandbox partner](https://experience.dynamics.com/requestlicense) per esaminare la nuova offerta del partner. 
- Per i partner che cercano maggiori informazioni su Internal Use Rights, vedi [Vantaggio cloud e software per Internal Use Rights (microsoft.com)](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Posso estendere la mia prova oltre i 30 giorni?
Per estendere la tua prova, completa i seguenti passaggi.

1. Nell'**interfaccia di amministrazione di Microsoft 365**, vai a **Fatturazione** > **Prodotti personali**.
2. Seleziona **Dynamics 365 Project Operations (CE) - Versione di valutazione**.
3. In **Data di scadenza**, seleziona **Data estensione**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Posso eseguire l'aggiornamento dalla distribuzione lite alla distribuzione degli scenari basati su risorse/materiali non stoccati?
Attualmente, non è disponibile alcun supporto per l'aggiornamento di un ambiente da un'implementazione lite a una distribuzione non fornita.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Posso accedere a Lifecycle Services (LCS) per i miei ambienti Finance?  
Nr. Per queste versioni di valutazione, la distribuzione viene gestita tramite l'interfaccia di amministrazione di Power Platform. L'accesso all'ambiente Finance viene limitato.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Posso installare la mia versione di prova in un ambiente esistente?
Se disponi di un ambiente esistente, ti sarà consentito installare la distribuzione lite su un ambiente di vendita Dataverse esistente dall'interfaccia di amministrazione Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
