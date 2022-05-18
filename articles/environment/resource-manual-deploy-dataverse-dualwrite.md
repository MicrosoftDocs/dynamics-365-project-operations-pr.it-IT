---
title: Distribuire manualmente l'app Project Operations Dataverse con supporto doppia scrittura
description: Questo argomento spiega come distribuire manualmente l'app Project Operations Dataverse in modo che supporti la doppia scrittura.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b82eef7b5f64705f37f224172c14f6734612329e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591225"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Distribuire manualmente l'app Project Operations Dataverse con supporto doppia scrittura

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento spiega come distribuire manualmente l'app Microsoft Dynamics 365 Project Operations in Microsoft Dataverse in modo che supporti la doppia scrittura. Project Operations rileva la configurazione dell'ambiente e aggiunge ulteriore supporto per la doppia scrittura se vengono soddisfatti i prerequisiti.

Durante la distribuzione tramite Microsoft Dynamics Lifecycle Services (LCS), se hai seguito le istruzioni in questo argomento, puoi saltare la distribuzione dell'integrazione di Microsoft Power Platform (precedentemente nota come ambiente Common Data Service).

Il processo di distribuzione di Project Operations in Dataverse in modo che supporti la doppia scrittura ha quattro passaggi principali:

1. [Crea un nuovo ambiente in Dataverse che supporta la doppia scrittura](#create).
2. [Aggiungi i prerequisiti di doppia scrittura all'ambiente](#prerequisites).
3. [Aggiungi l'app Project Operations Dataverse](#dataverse).
4. [Collega i tuoi ambienti](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Crea un nuovo ambiente in Dataverse che supporta la doppia scrittura

Per completare questa procedura, devi accedere come amministratore.

1. Apri [l'interfaccia di amministrazione di Power Platform](https://admin.powerplatform.com) e accedi come amministratore.
2. Crea un nuovo ambiente e assegna un nome.
3. Seleziona il tipo di ambiente. Se ti sei registrato per l'offerta della versione di valutazione, seleziona **Versione di valutazione (basata su abbonamento)**.
4. Conferma l'area di distribuzione.
5. Abilita l'opzione **Crea un database per questo ambiente**. 
6. Conferma la lingua, quindi conferma che la valuta corrisponda a quella delle tue app per la finanza e le operazioni.
7. Abilita l'opzione **App Dynamics 365** e conferma che il campo **Distribuisci automaticamente queste app** è impostato su **Nessuna**.
8. Aggiungi un gruppo di sicurezza, se è richiesto un gruppo di sicurezza.
9. Seleziona **Salva** per creare l'ambiente.
10. Attendi fino a quando la distribuzione è completata e l'ambiente raggiunge lo stato di **Pronto**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Aggiungi i prerequisiti di doppia scrittura all'ambiente

Il supporto per la doppia scrittura include campi aggiuntivi che vengono aggiunti alle entità chiave, come l'entità **Società**. Se stai aggiungendo il supporto per la doppia scrittura a un ambiente esistente, potresti dover aggiornare i dati per abilitare il supporto. Per informazioni su come eseguire il bootstrap dei dati, vedi [Bootstrap dei dati della società](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Per ulteriori informazioni sulla doppia scrittura, vedi [Requisiti di sistema per la doppia scrittura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Completa questa procedura per aggiungere i prerequisiti per la doppia scrittura al tuo ambiente.

1. Apri l'ambiente che hai appena creato e poi vai in **Risorsa** \> **App Dynamics 365**.
2. Seleziona **Soluzione di base doppia scrittura** nell'elenco delle app e installala.
3. Attendi fino al completamento dell'installazione. Quindi seleziona **Soluzione di orchestrazione doppia scrittura** nell'elenco delle app e installala.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Aggiungi l'app Project Operations Dataverse

Puoi completare questa procedura solo se hai completato le procedure precedenti prima di installare Project Operations. Durante l'installazione, il sistema analizza la configurazione dell'ambiente e aggiunge il supporto per la doppia scrittura, se necessario.

1. Apri l'ambiente che hai creato prima e poi vai in **Risorsa** \> **App Dynamics 365**.
2. Seleziona **Microsoft Dynamics 365 Project Operations** nell'elenco delle app e installalo.

## <a name="link-your-environments"></a><a name="link"></a>Collega i tuoi ambienti

Dopo che l'ambiente Dataverse è distribuito, è possibile configurare il collegamento nelle app per la finanza e le operazioni. Segui i passaggi in [Usare la procedura guidata doppia scrittura per collegare gli ambienti](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
