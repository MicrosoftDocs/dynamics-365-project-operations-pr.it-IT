---
title: Iscriversi per gli abbonamenti in anteprima a Project Operations per scenari basati su risorse/non stoccate
description: Questo articolo fornisce informazioni su come iscriversi e distribuire Project Operations per scenari basati su risorse non stoccate.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842020"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Iscriversi per gli abbonamenti in anteprima a Project Operations per scenari basati su risorse/non stoccate

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_



Questo articolo spiega come sottoscrivere l'offerta di prova e distribuire l'ambiente Project Operations per scenari basati su risorse/non stoccate.

## <a name="prerequisites"></a>Prerequisiti
- L'utente che distribuisce l'anteprima deve disporre dei diritti di amministratore globale del tenant di Azure. Puoi creare un tenant durante il primo riscatto dell'offerta. 
- La distribuzione di un ambiente Finance richiede una sottoscrizione di Azure valida che verrà fatturata in base all'ambiente. Puoi utilizzare la sottoscrizione esistente della tua organizzazione o utilizzare una [versione di valutazione di Azure](https://azure.microsoft.com/free/) per iniziare. L'ambiente CDS verrà fornito gratuitamente per un periodo limitato di 30 giorni.

> [!IMPORTANT]
> Solo una persona, l'amministratore del tenant, in un'organizzazione deve eseguire questa attività. Se non sei abbonato a questa versione, attendi fino a quando la tua organizzazione non è stata iscritta e hai ricevuto le credenziali utente.
> 
> Le versioni di valutazione sono per uso singolo nel tenant. Puoi eseguire una versione di valutazione solo una volta. Ti consigliamo di creare un nuovo tenant ai fini della versione di valutazione.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Versione di valutazione di Dynamics 365 Project Operations(CE) - Anteprima 

Prima di iniziare, assicurati di aver effettuato l'accesso a un browser con l'account utente di lavoro nel tenant in cui desideri l'anteprima di Project Operations.

1. Riscatta il primo codice offerta, **Dynamics 365 Project Operations** qui [Versione di valutazione di Project Operations](https://aka.ms/try-po).
2. Conferma l'ordine.

  Vedrai la conferma che l'offerta è stata riscattata.

### <a name="dynamics-365-finance-preview-trial"></a>Versione di valutazione in anteprima di Dynamics 365 Finance

Vai a [Versione di valutazione Dynamics 365 for Finance Anteprima](https://aka.ms/trypoche) e ripeti i passaggi della sezione precedente con l'offerta. Registrati per l'ambiente ospitato nel cloud.  

## <a name="assign-licenses"></a>Assegnare licenze

> [!IMPORTANT]
> Avrai bisogno dell'accesso amministrativo al portale di Microsoft 365 dell'organizzazione per completare i seguenti passaggi.

1. Vai all'[interfaccia di amministrazione di Microsoft 365](https://portal.office.com/) per assegnare le licenze ai tuoi utenti.

2. Nella pagina **Utenti attivi** seleziona gli utenti a cui assegnare una licenza.

3. Verifica che la licenza **Dynamics 365 Project Operations** sia stata selezionata e seleziona **Salva le modifiche**.

> [!NOTE]
> Non è necessario assegnare l'offerta della versione di valutazione di Finance a un utente.

## <a name="start-a-new-project-in-lcs"></a>Avviare un nuovo progetto in LCS

Crea un nuovo progetto LCS come descritto nell'articolo [Avviare un nuovo progetto in LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Aggiungere una sottoscrizione di Azure a un progetto LCS

Per completare questa attività, segui i passaggi nell'articolo, [Aggiungere una sottoscrizione di Azure al progetto LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Distribuire l'ambiente demo di Finance con Project Operations per scenari basati su risorse/non stoccate

Segui la guida nell'articolo, [Fornire un nuovo ambiente](resource-provision-new-environment.md) per completare la distribuzione. Utilizza il tipo di distribuzione [ambiente demo](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) per l'anteprima. 

## <a name="install-cds-setup-and-configuration-data"></a>Installare i dati di impostazione e configurazione CDS

Installa i dati di installazione e configurazione di CDS come descritto nell'articolo, [Impostare e applicare i dati di configurazione in Common Data Service](resource-apply-pro-setup-config-data.md).
Completa questo passaggio solo dopo che l'ambiente demo di Finance è stato distribuito e i dati demo sono pronti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
