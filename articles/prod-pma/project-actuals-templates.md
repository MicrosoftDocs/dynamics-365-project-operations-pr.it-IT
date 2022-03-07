---
title: Sincronizzare i valori effettivi del progetto direttamente da Project Service Automation con il giornale di registrazione dell'integrazione del progetto per la registrazione in Finance and Operations
description: Questo argomento descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare i valori effettivi del progetto direttamente da Microsoft Dynamics 365 Project Service Automation con Finance and Operations.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 11ccbd64c37341b2969e10e9a737f1aa4b4a61f9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289689"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Sincronizzare i valori effettivi del progetto direttamente da Project Service Automation con il giornale di registrazione dell'integrazione del progetto per la registrazione in Finance and Operations

[!include[banner](../includes/banner.md)]

Questo argomento descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare i valori effettivi del progetto direttamente da Dynamics 365 Project Service Automation con Dynamics 365 Finance.

Il modello sincronizza le transazioni da Project Service Automation in una tabella di staging in Finance. Dopo che la sincronizzazione è completata, **devi** importare i dati dalla tabella di staging nel giornale di integrazione.

> [!NOTE]
> - L'integrazione dei dati effettivi del progetto è disponibile a partire dalla versione 8.0.1.
> - Se stai utilizzando Enterprise Edition 7.3.0 dopo aver installato KB 4132657 e KB 4132660, potrai utilizzare i modelli per integrare attività di progetto, categorie di transazioni di spesa, stime di ore, stime di spesa e valori effettivi e per configurare il blocco delle funzionalità. Se devi reimpostare le distribuzioni contabili, è consigliabile installare anche KB 4131710.
> - Se stai utilizzando la versione 7.3.0 e stai trasferendo le transazioni delle commissioni da Project Service Automation, devi installare KB 4345320 per includere tali commissioni nella fattura del progetto.
> - Se stai immettendo importi IVA su transazioni di tempo o spese in Project Service Automation, devi installare Project Service Automation Update 7. In caso contrario, i valori effettivi delle imposte non saranno collegati ai valori effettivi di tempo o di spesa associati e non verranno sincronizzati con Finance. Per altre informazioni, contatta il supporto.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flusso di dati per Project Service Automation su Finance

La soluzione di integrazione da Project Service Automation a Finance utilizza la funzionalità di integrazione dei dati per sincronizzare i dati tra le istanze di Project Service Automation e Finance. I modelli di integrazione disponibili con la funzionalità Integrazione dati consentono il flusso di dati sui dati effettivi del progetto da Project Service Automation a Finance.

La figura seguente mostra come i dati vengono sincronizzati tra Project Service Automation e Finance.

[![Flusso di dati per l'integrazione di Project Service Automation con Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Valori effettivi di progetto da Project Service Automation

### <a name="template-and-tasks"></a>Modelli e attività

Per accedere ai modelli disponibili, nell'interfaccia di amministrazione di Microsoft Power Apps, seleziona **Progetti**, quindi, nell'angolo in alto a destra, seleziona **Nuovo progetto** per selezionare modelli pubblici.

Il modello seguente e le attività sottostanti vengono utilizzati per sincronizzare i valori effettivi di progetto da Project Service Automation a Finance:

- **Nome del modello in Integrazione dati:** valori effettivi di progetto (da PSA a Fin e Ops)
- **Nome delle attività nel progetto:**

    - Valori effettivi
    - TransactionConnections

### <a name="entity-set"></a>Set di entità

| Project Service Automation | Finanza                                   |
|----------------------------|----------------------------------------------------------|
| Valori effettivi                    | Entità di integrazione per i valori effettivi di progetto                   |
| Connessioni delle transazioni    | Entità di integrazione per le relazioni di transazione del progetto |

### <a name="entity-flow"></a>Flusso di entità

I valori effettivi di progetto vengono gestiti in Project Service Automation e vengono sincronizzati con il giornale di integrazione del progetto in Finance. La contabilità verrà applicata in base alle dimensioni finanziarie predefinite e alla configurazione della registrazione.

### <a name="prerequisites"></a>Prerequisiti

Prima che possa verificarsi la sincronizzazione dei valori effettivi, devi configurare i parametri di integrazione di Project Service Automation e sincronizzare i progetti, le attività di progetto e le categorie di transazioni di spesa del progetto.

### <a name="power-query"></a>Power Query

Nel modello dei valori effetti di progetto, è necessario utilizzare Microsoft Power Query per Excel per completare queste attività:

- Trasforma il tipo di transazione in Project Service Automation nel tipo di transazione corretto in Finance. Questa trasformazione è già definita nel modello di valori effettivi di progetto (da PSA a Fin and Ops).
- Trasforma il tipo di fatturazione in Project Service Automation nel tipo di fatturazione corretto in Finance. Questa trasformazione è già definita nel modello di valori effettivi di progetto (da PSA a Fin and Ops). Il tipo di fatturazione viene quindi mappato alla proprietà della riga, in base alla configurazione nella pagina **Parametri di integrazione di Project Service Automation**.
- Filtra per unità organizzative di risorse specifiche che devono essere sincronizzate con questo modello.
- Se i valori effettivi del tempo interaziendale o delle spese interaziendali verranno sincronizzati in Finance, devi trasformare l'unità organizzativa del contratto nella persona giuridica corretta in Finance. Nel modello Valori effettivi del progetto (da PSA a Fin e Ops), viene definita una colonna condizionale in base ai dati dimostrativi. Devi aggiornare l'ultima colonna condizionale inserita alle persone giuridiche corrette. In caso contrario, potrebbe verificarsi un errore di integrazione o potrebbero essere importate transazioni effettive errate in Finance.
- Se i valori effettivi del tempo interaziendale o delle spese interaziendali non verranno sincronizzati in Finance, è necessario eliminare l'ultima colonna condizionale inserita dal modello. In caso contrario, potrebbe verificarsi un errore di integrazione o potrebbero essere importate transazioni effettive errate in Finance.

#### <a name="contract-organizational-unit"></a>Unità organizzativa del contratto
Per aggiornare la colonna condizionale inserita nel modello, fai clic sula freccia **Mappa** per aprire il mapping. Seleziona il collegamento **Filtro e query avanzati** per aprire Power Query.

- Se stai utilizzando il modello di valori effettivi del progetto predefinito (da PSA a Fin e Ops), in Power Query seleziona l'ultima **Condizione inserita** dalla sezione **Passaggi applicati**. Nella voce **Funzione**, sostituisci **USSI** con il nome della persona giuridica da utilizzare con l'integrazione. Aggiungi condizioni aggiuntive alla voce **Funzione** come richiesto e aggiorna la condizione **else** da **USMF** alla persona giuridica corretta.
- Se stai creando un nuovo modello, devi aggiungere la colonna per supportare i tempi e le spese interaziendali. Seleziona **Aggiungi colonna condizionale** e inserisci un nome per la nuova colonna, ad esempio **LegalEntity**. Immetti una condizione per la colonna, dove, se **msdyn\_contractorganizationalunitid.msdyn\_name** è \<organizational unit\>, quindi \<enter the legal entity\>; in caso contrario null.

### <a name="template-mapping-in-data-integration"></a>Mapping dei modelli nell'integrazione dei dati

Le figure seguenti mostrano un esempio del mapping delle attività del modello in Integrazione dati. Il mapping mostra le informazioni sui campi che verranno sincronizzate da Project Service Automation a Finance.

[![Mappatura dei modelli - Valori effettivi](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mappatura dei modelli - Connessioni di transazione](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importazione dalla tabella di staging dopo l'integrazione da Project Service Automation

Il processo periodico di importazione dalla tabella di staging deve essere eseguito dopo la sincronizzazione dei valori effettivi da Project Service Automation a Finance. Questo processo importerà le transazioni del progetto dalla tabella di staging nel giornale di registrazione dell'integrazione di Project Service Automation, dove viene applicata la contabilità e le transazioni importate possono essere registrate. Si consiglia di eseguire questo processo in modalità batch; opzionalmente può essere configurato per essere eseguito come batch ricorrente.

## <a name="update-actuals-from-finance"></a>Aggiornare i valori effettivi da Finance

### <a name="template-and-tasks"></a>Modelli e attività

Il modello seguente e le attività sottostanti vengono utilizzati per sincronizzare il numero di giustificativo e le imposte sulle vendite per le transazioni di progetto registrate da Finance a Project Service Automation:

- **Nome del modello in Integrazione dati:** aggiornamento dei valori effettivi di progetto (da Fin Ops a PSA)
- **Nome delle attività nel progetto:**

    - Valori effettivi 
    - TransactionConnections

### <a name="entity-set"></a>Set di entità

| Finanza                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entità di integrazione per i valori effettivi di progetto                   | Valori effettivi                    |
| Entità di integrazione per le relazioni di transazione del progetto | Connessioni delle transazioni    |

### <a name="entity-flow"></a>Flusso di entità

I valori effettivi di progetto vengono gestiti in Project Service Automation e vengono sincronizzati con il giornale di integrazione del progetto in Finance. Dopo che i valori effettivi sono stati registrati in Finance, vengono aggiornati in Project Service Automation con il numero di giustificativo di Finance. Se le imposte sulle vendite sono state aggiunte in Finance, vengono creati nuovi valori effettivi fiscali in Project Service Automation.

### <a name="power-query"></a>Power Query

Nel modello di aggiornamento dei valori effetti di progetto, è necessario utilizzare Power Query per completare queste attività:

- Trasforma il tipo di transazione in Finance nel tipo di transazione corretto in Project Service Automation. Questa trasformazione è già definita nel modello di aggiornamento dei valori effettivi di progetto (da Fin Ops a PSA).
- Trasforma il tipo di fatturazione in Finance nel tipo di fatturazione corretto in Project Service Automation. Questa trasformazione è già definita nel modello di aggiornamento dei valori effettivi di progetto (da Fin Ops a PSA).

### <a name="template-mapping-in-data-integration"></a>Mapping dei modelli nell'integrazione dei dati

La figura seguente mostra esempi di mapping delle attività del modello in Integrazione dati. Il mapping mostra le informazioni sui campi che verranno sincronizzate da Finance a Project Service Automation.

[![Mappatura dei modelli - Aggiornamento dei valori effettivi](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mappatura dei modelli - Aggiornamento della transazione](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]