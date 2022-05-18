---
title: Iscriversi a un abbonamento di anteprima - semplice
description: 'Questo argomento fornisce informazioni su come iscriversi alla distribuzione semplice di Project Operations: accordo per la fatturazione proforma.'
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3b06ac29e8021967490534d3aefc8b5ce733413b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588005"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Iscriversi a un abbonamento di anteprima - semplice 

Questo argomento spiega come sottoscrivere l'offerta della versione di valutazione e distribuire Dynamics 365 Project Operations, distribuzione semplice: dalla transazione alla fatturazione proforma.

> [!NOTE]
> Questo processo cambierà nelle prossime versioni di Project Operations.

## <a name="prerequisites"></a>Prerequisiti
- L'utente che distribuisce l'anteprima deve disporre dei diritti di amministratore globale del tenant di Azure. Puoi creare un tenant durante il primo riscatto dell'offerta.

> [!IMPORTANT]
> Solo una persona, l'amministratore del tenant, in un'organizzazione deve eseguire questa attività. Se non sei abbonato a questa versione, attendi fino a quando la tua organizzazione non è stata iscritta e hai ricevuto le credenziali utente.
> 
> Le versioni di valutazione sono per uso singolo nel tenant. Puoi eseguire una versione di valutazione solo una volta. Ti consigliamo di creare un nuovo tenant ai fini della versione di valutazione.

### <a name="dynamics-365-project-operations-trial"></a>Versione di valutazione di Dynamics 365 Project Operations 

Prima di iniziare, assicurati di aver effettuato l'accesso a un browser con l'account utente di lavoro nel tenant in cui desideri l'anteprima di Project Operations.

1. Vai a [Versione di valutazione di Project Operations](https://aka.ms/try-po) per riscattare il primo codice dell'offerta, **Dynamics 365 Project Operations**.
2. Conferma l'ordine.

  Vedrai che la conferma che l'offerta è stata riscossa con successo.

## <a name="assign-licenses"></a>Assegnare licenze

> [!IMPORTANT]
> Avrai bisogno dell'accesso amministrativo al portale di Microsoft 365 dell'organizzazione per completare i seguenti passaggi.


1. Vai all'[interfaccia di amministrazione di Microsoft 365](https://portal.office.com/) per assegnare le licenze ai tuoi utenti.
2. Nella pagina **Utenti attivi** seleziona gli utenti a cui assegnare una licenza.
3. Verifica che la licenza **Dynamics 365 Project Operations** sia selezionata. 
4. Seleziona **Salva modifiche**.

## <a name="create-a-new-dataverse-environment"></a>Creare un nuovo ambiente Dataverse

1. Esegui il provisioning di un nuovo ambiente di distribuzione Dataverse di Project Operations seguendo le istruzioni nell'argomento [Modello di distribuzione Dataverse](lite-deployment.md). Quando selezioni il tipo di ambiente, assicurati di utilizzare **Versione di valutazione (basata su abbonamento)**.

  ![Nuovo ambiente.](./media/19CreateEnvironment.png)

2. Seleziona l'impostazione **Abilita app Dynamics 365** e lascia **Distribuisci automaticamente queste app** vuoto.  
3. Seleziona **Salva** per creare l'ambiente.

  ![Aggiungere il database.](./media/20CreateEnvironment1.png)

4. Dopo aver creato l'ambiente, installa la soluzione **Microsoft Dynamics 365 Project Operations**. 

![Installare la soluzione.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installare i dati dimostrativi di installazione e configurazione CDS

Installa i dati dimostrativi di installazione e configurazione CDS seguendo le istruzioni nell'argomento [Applicare i dati di installazione e configurazione dimostrativi](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
