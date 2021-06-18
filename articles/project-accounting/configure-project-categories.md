---
title: Configurare categorie di progetto
description: In questo argomento vengono fornite informazioni sulla configurazione delle categorie di progetto.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d82302f12ba75a92f2de0e9746ad7e61ce0cdc6b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995176"
---
# <a name="configure-project-categories"></a>Configurare categorie di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Project Operations offre solide funzionalità per la categorizzazione dei ricavi e delle spese sui progetti. Le categorie consentono di creare report e analizzare le transazioni di progetto e di guidare la registrazione nella contabilità generale.

Il diagramma seguente illustra la correlazione tra categorie di transazioni, categorie condivise e categorie di progetto. 

Le categorie di transazioni sono il raggruppamento di base per le transazioni di progetto. All'interno di quel raggruppamento, c'è un insieme di categorie condivise che possono essere condivise tra applicazioni e moduli. Entrando ancora più nello specifico, le categorie di progetto sono il livello di categorie più granulare. Le categorie di progetto sono specifiche per persona giuridica, modulo e applicazione.

![Correlazione tra categorie di transazioni, categorie condivise e categorie di progetto](media/project-categories.png)

## <a name="transaction-categories"></a>Categorie di transazioni

Le categorie di transazioni rappresentano il raggruppamento di base per le transazioni di progetto e non sono specifiche della società o del tipo di transazione. Ad esempio, Contoso Robotics utilizza le categorie Progettazione, Viaggio, Installazione e Transazione del servizio per raggruppare le transazioni del progetto.

Le categorie di transazione sono definite nel modulo Project Operations. 
1. Vai a **Impostazioni** \> **Categorie di transazione** per aprire il modulo. 
2. Crea una nuova categoria di transazione selezionando **Nuovo** o selezionando **Importa da Excel**.

## <a name="shared-categories"></a>Categorie condivise

Dynamics 365 utilizza il concetto di categorie condivise per classificare le spese in diverse applicazioni, ad esempio Dynamics 365 Finance, Dynamics 365 Supply Chain e Dynamics 365 Project Operations. Per ogni categoria di transazione creata, Project Operations crea automaticamente quattro categorie condivise correlate: ore, spese, commissioni e articolo. Puoi rivedere e modificare le categorie condivise andando su **Gestione progetti e contabilità** \> **Configura** \> **Categorie** \> **Categorie condivise**.

## <a name="project-categories"></a>Categorie progetti

Le categorie di progetto rappresentano il livello più granulare di configurazione delle categorie e devono essere configurate separatamente, e per ogni azienda, da un contabile di progetto.

1. Vai a **Gestione progetti e contabilità** \> **Configura** \> **Categorie** \> **Categorie di progetto**.
2. Seleziona **Nuovo**.
3. Seleziona l'**ID categoria** della categoria condivisa creata nella sezione precedente. Project Operations consente di utilizzare solo le categorie condivise associate alle categorie di transazione.
4. Seleziona un gruppo di categorie.

## <a name="category-groups"></a>Gruppi di categorie

I gruppi di categorie vengono utilizzati per condividere proprietà, principalmente profili di registrazione, tra le categorie di progetto correlate. Deve essere presente almeno un gruppo di categorie per ogni tipo di transazione e ad ogni categoria di progetto è assegnato un gruppo.

Le specifiche di registrazione in Project Operations sono definite dalle regole del profilo dei costi e dei ricavi del progetto, dalle categorie di progetto e dai gruppi di categorie. Puoi configurare gruppi di categorie andando a **Gestione progetti e contabilità** \> **Configura** \> **Categorie** \> **Gruppi di categorie**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]