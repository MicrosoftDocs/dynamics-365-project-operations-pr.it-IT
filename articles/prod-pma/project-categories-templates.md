---
title: Sincronizzare le categorie di spesa del progetto tra Finance and Operations e Project Service Automation
description: Questo argomento descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare le categorie di spesa del progetto tra Microsoft Dynamics 365 Finance e Dynamics 365 Project Service Automation.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079015"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Sincronizzare le categorie di spesa del progetto tra Finance and Operations e Project Service Automation

[!include[banner](../includes/banner.md)]

Questo argomento descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare le categorie di spesa del progetto tra Dynamics 365 Finance e Dynamics 365 Project Service Automation.

> [!NOTE]
> - L'integrazione delle attività di progetto, le categorie delle transazioni di spesa, le stime delle ore, le stime delle spese e il blocco delle funzionalità sono disponibili nella versione 8.0.
> - L'integrazione dei dati effettivi è disponibile nella versione 8.0.1 o successiva.
> - Se stai utilizzando Enterprise Edition 7.3.0 dopo aver installato KB 4132657 e KB 4132660, potrai utilizzare i modelli per integrare attività di progetto, categorie di transazioni di spesa, stime di ore, stime di spesa e valori effettivi e per configurare il blocco delle funzionalità. Se devi reimpostare le distribuzioni contabili, è consigliabile installare anche KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Flusso di dati per Project Service Automation e Finance

La soluzione di integrazione tra Project Service Automation e Finance utilizza la funzionalità di integrazione dei dati per sincronizzare i dati tra le istanze di Project Service Automation e Finance. I modelli di integrazione disponibili con la funzionalità Integrazione dati consentono il flusso di dati sulle categorie di transazione di spesa del progetto tra Finance e Project Service Automation.

Se le categorie di spesa del progetto vengono gestite in Finance, il flusso di integrazione viene prima da Finance a Project Service Automation. Gli ID integrazione delle categorie di spesa del progetto vengono quindi aggiornati tramite la sincronizzazione da Project Service Automation a Finance.

Se le categorie di spesa del progetto vengono gestite in Project Service Automation, il flusso di integrazione viene prima da Project Service Automation a Finance. Le categorie di progetto devono essere già configurate in Finance prima della sincronizzazione da Project Service Automation. Quindi sincronizza di nuovo da Finance a Project Service Automation e quindi da Project Service Automation di nuovo a Finance. In questo modo, contribuisci a garantire che le categorie siano collegate e che non vengano creati duplicati.

> [!NOTE]
> In genere, le categorie di spesa del progetto vengono gestite in Finance. Tuttavia, se non lo sono o se le categorie di spesa sono già state create in Project Service Automation, è necessario prima sincronizzare utilizzando il modello Categorie di transazione di spesa del progetto (da PSA a Fin e Ops). Quindi sincronizza utilizzando il modello delle categorie di transazioni di spesa del progetto (Da Fin e Ops a PSA). È consiglibile quindi eseguire ancora una volta la sincronizzazione da Project Service Automation a Finance.
>
> Se esegui la sincronizzazione prima da Project Service Automation, è necessario soddisfare i seguenti requisiti in Finance prima di eseguire la sincronizzazione:
>
> - La categoria condivisa che corrisponde alla categoria di progetto configurata in Project Service Automation deve esistere e deve essere abilitata per entrambi **Progetto** e **Spesa**.
> - Per ogni persona giuridica Finance con cui deve essere effettuata l'integrazione, devono esistere le seguenti categorie di progetto:
>
>     - **Categoria progetto** esiste. 
>     - **Usa in Gestione spese** è abilitata.
>     - **Attivo nella giornale di registrazione** è abilitata.
>     - **Tipo di transazione** è impostata su **Gerstione spese**.

La figura seguente mostra come i dati vengono sincronizzati tra Project Service Automation e Finance.

[![Flusso di dati per l'integrazione di Project Service Automation con Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Sincronizzazione delle categorie di spesa del progetto tra Finance e Project Service Automation

### <a name="template-and-task"></a>Modello e attività

Per accedere al modello, nell'interfaccia di amministrazione di Microsoft Power Apps, seleziona **Progetti**, quindi, nell'angolo in alto a destra, seleziona **Nuovo progetto** per selezionare modelli pubblici.

Il modello seguente e l'attività sottostante vengono utilizzati per sincronizzare le categorie di spesa del progetto da Finance a Project Service Automation:

- **Nome del modello in Integrazione dati:** categorie di transazioni di spesa del progetto (da Fin e Ops a PSA)
- **Nome dell'attività nel progetto:** sincronizza le categorie con PSA

### <a name="entity-set"></a>Set di entità

| Finanza                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entità di integrazione per le categorie | Categorie di transazioni     |

### <a name="entity-flow"></a>Flusso di entità

Le categorie di spesa del progetto vengono gestite in Finance e vengono sincronizzate con Project Service Automation come categorie di transazioni.

### <a name="power-query"></a>Power Query

Quando esegui la sincronizzazione con Project Service Automation, devi utilizzare Microsoft Power Query per Excel per impostare il tipo di fatturazione nella categoria della transazione. Il modello delle categorie di transazioni di spesa del progetto (da Fin e Ops a PSA) fornisce una colonna e una mappatura predefinite. Se crei il tuo modello, devi aggiungere una colonna aggiuntiva in Power Query. Effettuare i passaggi seguenti.

1. Fai clic sulla freccia per aprire il mapping dell'attività delle categorie di spesa del progetto nel modello Categorie delle transazioni di spesa del progetto (da Fin e Ops a PSA).
2. Fai clic sul collegamento **Filtro e query avanzati** per aprire Power Query.
2. Seleziona **Aggiungi colonna condizionale**.
3. Immetti un nome per la nuova colonna, ad esempio **BillingType**.
4. Immetti la seguente condizione: **Se CATEGORYID non è uguale a Null, allora 19235001, altrimenti null**.
5. Fai clic su **OK** nella colonna.
6. Assicurati di mappare questa nuova colonna nella pagina di mapping.

La figura seguente mostra un esempio del mapping delle attività del modello in Integrazione dati. Il mapping mostra le informazioni sui campi che verranno sincronizzate da Finance a Project Service Automation.

[![Mapping di modello della categoria di spesa del progetto a Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Sincronizzazione delle categorie di spesa del progetto tra Project Service Automation e Finance

### <a name="template-and-task"></a>Modello e attività

Il modello seguente e l'attività sottostante vengono utilizzati per sincronizzare le categorie di spesa del progetto da Project Service Automation a Finance:

- **Nome del modello in Integrazione dati:** categorie di transazioni di spesa del progetto (da PSA a Fin e Ops)
- **Nome dell'attività nel progetto:** sincronizza le categorie con Fin Ops

### <a name="entity-set"></a>Set di entità

| Project Service Automation | Finanza                           |
|----------------------------|-----------------------------------|
| Categorie di transazioni     | Entità di integrazione per le categorie |

### <a name="entity-flow"></a>Flusso di entità

Le categorie di spesa del progetto vengono gestite in Finance e vengono sincronizzate con Project Service Automation come categorie di transazioni. La sincronizzazione con gli aggiornamenti di Finance aggiorna la categoria di progetto in Finance con l'ID integrazione da Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Mapping dei modelli nell'integrazione dei dati

La figura seguente mostra un esempio del mapping delle attività del modello in Integrazione dati.

> [!NOTE]
> Il mapping mostra le informazioni sui campi che verranno sincronizzate da Project Service Automation a Finance.

[![Mapping di modello da Project Service Automation a Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
