---
title: Sincronizzare le stime di progetto direttamente da Project Service Automation a Finance and Operations
description: Questo articolo descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare le stime orarie di progetto e le stime di spesa del progetto direttamente da Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: fb39a377a51b09f04564b4fe8527e34f0ea12682
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920847"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizzare le stime di progetto direttamente da Project Service Automation a Finance and Operations

[!include[banner](../includes/banner.md)]

Questo articolo descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare le stime orarie di progetto e le stime di spesa del progetto direttamente da Dynamics 365 Project Service Automation a Dynamics 365 Finance.

> [!NOTE]
> - L'integrazione delle attività di progetto, le categorie delle transazioni di spesa, le stime delle ore, le stime delle spese e il blocco delle funzionalità sono disponibili nella versione 8.0.
> - L'integrazione dei dati effettivi è disponibile nella versione 8.0.1 o successiva.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flusso di dati per Project Service Automation su Finance

La soluzione di integrazione da Project Service Automation a Finance utilizza la funzionalità di integrazione dei dati per sincronizzare i dati tra le istanze di Project Service Automation e Finance. I modelli di integrazione disponibili con la funzionalità Integrazione dati consentono il flusso di dati sulle stime delle ore di progetto e delle spese del progetto da Project Service Automation a Finance.

La figura seguente mostra come i dati vengono sincronizzati tra Project Service Automation e Finance.

[![Flusso di dati per l'integrazione di Project Service Automation con Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Stime delle ore di progetto

### <a name="template-and-tasks"></a>Modelli e attività

Per accedere ai modelli disponibili, nell'interfaccia di amministrazione di Microsoft Power Apps, seleziona **Progetti**, quindi, nell'angolo in alto a destra, seleziona **Nuovo progetto** per selezionare modelli pubblici.

Il modello seguente e le attività sottostanti vengono utilizzati per sincronizzare le stime delle ore di progetto da Project Service Automation a Finance:

- **Nome del modello in Integrazione dati:** stime delle ore di progetto (da PSA a Fin e Ops)
- **Nome delle attività nel progetto:**

    - Relazioni transazione
    - Stime di spesa

### <a name="entity-set"></a>Set di entità

| Project Service Automation | Finanza                                       |
|----------------------------|-----------------------------------------------|
| Attività di progetto              | Entità di integrazione per le stime delle ore di progetto |

### <a name="entity-flow"></a>Flusso di entità

Le stime delle ore di progetto vengono gestite in Project Service Automation e vengono sincronizzate con Finance come previsioni delle ore di progetto.

### <a name="prerequisites"></a>Prerequisiti

Prima di poter sincronizzare le stime delle ore di progetto, è necessario sincronizzare i progetti, le attività di progetto e le categorie di transazioni di spesa del progetto.

### <a name="power-query"></a>Power Query

Nel modello di stime di ore del progetto, è necessario utilizzare Microsoft Power Query per Excel per completare queste attività:

- Impostare l'ID modello di previsione predefinito che verrà utilizzato quando l'integrazione crea nuove previsioni orarie.
- Filtrare tutti i record specifici della risorsa nell'attività che non riusciranno a integrare le previsioni orarie.
- Filtrare tutte le righe di categorie di transazioni vuote. Il mancato completamento di questa attività potrebbe causare previsioni orarie errate.

#### <a name="set-the-default-forecast-model-id"></a>Impostare l'ID modello di previsione predefinito

Per aggiornare l'ID modello di previsione predefinito nel modello, fai clic sula freccia **Mappa** per aprire il mapping. Quindi seleziona il collegamento **Filtro e query avanzati**.

- Se stai utilizzando il modello di stima delle ore di progetto predefinito (da PSA a Fin e Ops), seleziona **Condizione inserita** nell'elenco di **Passaggi applicati**. Nella voce **Funzione**, sostituisci **O\_previsione** con il nome dell'ID del modello di previsione da utilizzare con l'integrazione. Il modello predefinito ha un ID modello di previsione dai dati demo.
- Se stai creando un nuovo modello, devi aggiungere questa colonna. In Power Query seleziona **Aggiungi colonna condizionale** e assegna un nome alla nuova colonna, ad esempio **ModelID**. Immetti la condizione per la colonna, dove, se Project task è null, quindi \<enter the forecast model ID\>; in caso contrario null.

#### <a name="filter-out-resource-specific-records"></a>Filtrare i record specifici delle risorse

Il modello Stime delle ore di progetto (da PSA a Fin e Ops) ha un filtro predefinito che rimuove tutti i record specifici della risorsa. Se crei il tuo modello, devi aggiungere questo filtro. Seleziona il collegamento **Filtro e query avanzati** per filtrare la colonna **msdyn\_islinetask** in modo che solo i record **Falso** siano inclusi.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrare le righe di categorie di transazioni vuote

Devi aggiungere un filtro per rimuovere tutte le righe con categorie di transazioni vuote. Questa attività è obbligatoria, indipendentemente dal fatto che tu stia utilizzando il modello predefinito o creando il tuo modello. Questo filtro rimuove le righe di riepilogo da Project Service Automation che potrebbero causare errori nelle previsioni orarie in Finance. Seleziona il collegamento **Filtro e query avanzati** per filtrare i record Null nella colonna **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mapping dei modelli nell'integrazione dei dati

La figura seguente mostra un esempio del mapping delle attività del modello in Integrazione dati. Il mapping mostra le informazioni sui campi che verranno sincronizzate da Project Service Automation a Finance.

[![Mapping dei modelli di attività nell'integrazione dei dati.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Stime di spesa del progetto

### <a name="template-and-tasks"></a>Modelli e attività

Il modello seguente e le attività sottostanti vengono utilizzati per sincronizzare le stime di spesa del progetto da Project Service Automation a Finance:

- **Nome del modello in Integrazione dati:** stime di spesa del progetto (da PSA a Fin e Ops)
- **Nome delle attività nel progetto:**

    - Relazioni transazione 
    - Stime di spesa

### <a name="entity-set"></a>Set di entità

| Project Service Automation | Finanza                                                  |
|----------------------------|----------------------------------------------------------|
| Connessioni delle transazioni    | Entità di integrazione per le relazioni di transazione del progetto |
| Righe di stima             | Entità di integrazione per le stime di spesa del progetto         |

### <a name="entity-flow"></a>Flusso di entità

Le stime di spesa del progetto vengono gestite in Project Service Automation e vengono sincronizzate con Finance come previsioni di spesa del progetto.

### <a name="prerequisites"></a>Prerequisiti

Prima di poter sincronizzare le stime di spesa del progetto, è necessario sincronizzare i progetti, le attività di progetto e le categorie di transazioni di spesa del progetto.

### <a name="power-query"></a>Power Query

Nel modello delle stime di spesa del progetto, è necessario utilizzare Power Query per completare queste attività:

- Filtra per includere solo i record di riga di stima di spesa.
- Impostare l'ID modello di previsione predefinito che verrà utilizzato quando l'integrazione crea nuove previsioni orarie.
- Trasforma i tipi di fatturazione.
- Trasforma i tipi di transazione.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrare per includere solo le righe di stima di spesa

Il modello Stime di spesa del progetto (da PSA a Fin e Ops) ha un filtro predefinito che include solo le righe di spesa nell'integrazione. Se crei il tuo modello, devi aggiungere questo filtro. Seleziona l'attività **Relazioni transazione**, quindi fai clic sulla freccia **Mapping** per aprire il mapping. Seleziona il collegamento **Filtro e query avanzati**. Filtra la colonna **msdyn\_transactiontype1** in modo da includere solo **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Impostare l'ID modello di previsione predefinito

Per aggiornare l'ID modello di previsione predefinito nel modello, seleziona l'attività **Stime di spesa**, quindi fai clic sula freccia **Mappa** per aprire il mapping. Seleziona il collegamento **Filtro e query avanzati**.

- Se si utilizza il modello predefinito Stime di spesa (da PSA a Fin and Ops), in Power Query seleziona la prima **Condizione inserita** nella sezione **Passaggi applicati**. Nella voce **Funzione**, sostituisci **O\_previsione** con il nome dell'ID del modello di previsione da utilizzare con l'integrazione. Il modello predefinito ha un ID modello di previsione dai dati demo.
- Se stai creando un nuovo modello, devi aggiungere questa colonna. In Power Query seleziona **Aggiungi colonna condizionale** e assegna un nome alla nuova colonna, ad esempio **ModelID**. Immetti la condizione per la colonna, dove, se ID riga di stima è null, quindi \<enter the forecast model ID\>; in caso contrario null.

#### <a name="transform-the-billing-types"></a>Trasformare i tipi di fatturazione

Il modello Stime di spesa del progetto (da PSA a Fin e Ops) include una colonna condizionale utilizzata per trasformare i tipi di fatturazione ricevuti da Project Service Automation durante l'integrazione. Se crei il tuo modello, devi aggiungere questa colonna condizionale. Seleziona il collegamento **Filtro e query avanzati**, quindi seleziona **Aggiungi colonna condizionale**. Immetti un nome per la nuova colonna, ad esempio **BillingType**. Quindi, immetti la condizione seguente:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Trasformare i tipi di transazione

Il modello Stime di spesa del progetto (da PSA a Fin e Ops) include una colonna condizionale utilizzata per trasformare i tipi di transazione ricevuti da Project Service Automation durante l'integrazione. Se crei il tuo modello, devi aggiungere questa colonna condizionale. Seleziona il collegamento **Filtro e query avanzati**, quindi seleziona **Aggiungi colonna condizionale**. Immetti un nome per la nuova colonna, ad esempio **TransactionType**. Quindi, immetti la condizione seguente:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Mapping dei modelli nell'integrazione dei dati

La figura seguente mostra esempi di mapping delle attività del modello in Integrazione dati. Il mapping mostra le informazioni sui campi che verranno sincronizzate da Project Service Automation a Finance.

[![Mappatura del modello delle transazioni di stima di spesa.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mappatura del modello delle stime di spesa.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]