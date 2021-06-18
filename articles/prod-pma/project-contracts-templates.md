---
title: Sincronizzare i contratti di progetto e i progetti direttamente da Project Service Automation a Finance
description: Questo argomento descrive il modello e le attività sottostanti che vengono utilizzati per sincronizzare i progetti e i contratti del del progetto direttamente da Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: Yowelle
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 2f5fa0143c903f08b3937426805cb43d5d6109e3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999811"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Sincronizzare i contratti di progetto e i progetti direttamente da Project Service Automation a Finance 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Questo argomento descrive il modello e le attività sottostanti che vengono utilizzati per sincronizzare i progetti e i contratti del del progetto direttamente da Dynamics 365 Project Service Automation a Dynamics 365 Finance.

> [!NOTE] 
> Se utilizzi Enterprise Edition 7.3.0, devi installare KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flusso di dati per Project Service Automation su Finance

> [!NOTE]
> Prima di poter utilizzare la soluzione di integrazione di Project Service Automation con Finance, è necessario acquisire familiarità con la funzionalità di integrazione dei dati di Dynamics 365.

La soluzione di integrazione da Project Service Automation a Finance utilizza la funzionalità di integrazione dei dati per sincronizzare i dati tra le istanze di Project Service Automation e Finance. Il modello di integrazione disponibile con la funzionalità Integrazione dati consente il flusso di dati su contratti di progetto, progetti, voci di contratto di progetto e fasi delle voci di contratto di progetto da Project Service Automation a Finance.

La figura seguente mostra come i dati vengono sincronizzati tra Project Service Automation e Finance.

[![Flusso di dati per l'integrazione di Project Service Automation con Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Modelli e attività

Per accedere ai modelli disponibili, nell'interfaccia di amministrazione di Microsoft Power Apps, seleziona **Progetti**, quindi, nell'angolo in alto a destra, seleziona **Nuovo progetto** per selezionare modelli pubblici.

I modelli seguenti e le attività sottostanti vengono utilizzati per sincronizzare i progetti e i contratti di progetto da Project Service Automation a Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrazione con Dynamics 365 Project Service Automation v2.x
- **Nome del modello in Integrazione dati:** Progetti e contratti (da Project Service Automation a Finance)
- **Nome delle attività nel progetto:**

    - Contratti di progetto da Project Service Automation a Finance
    - Progetti da Project Service Automation a Finance
    - Righe di contratto di progetto da Project Service Automation a Finance
    - Passaggi fondamentali righe di contratto di progetto da Project Service Automation a Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrazione con Dynamics 365 Project Service Automation v3.x
È stata apportata una modifica allo schema in Project Service Automation che influisce sul modello di fase della riga del contratto di progetto e l'utilizzo della versione v2 del modello è necessario per integrare Project Service Automation v3.x con Dynamics 365.

- **Nome del modello in Integrazione dati:** Progetti e contratti (da Project Service Automation 3.x a Finance) - v2
- **Nome delle attività nel progetto:**

    - Contratti di progetto da Project Service Automation a Finance
    - Progetti da Project Service Automation a Finance
    - Righe di contratto di progetto da Project Service Automation a Finance
    - Passaggi fondamentali righe di contratto di progetto da Project Service Automation a Finance

Prima di sincronizzare i contratti di progetto e i progetti, è necessario sincronizzare gli account.

## <a name="entity-set"></a>Set di entità

| Project Service Automation       | Finanza                                                |
|----------------------------------|--------------------------------------------------------|
| Ordini                           | Entità di integrazione per contratto di progetto                |
| Progetti                         | Entità di integrazione per progetto                         |
| Righe ordine                      | Entità di integrazione per voce di contratto di progetto           |
| Fasi delle voci di contratto di progetto | Entità di integrazione per fase di voce di contratto di progetto |

## <a name="entity-flow"></a>Flusso di entità

I contratti di progetto vengono gestiti in Project Service Automation e vengono sincronizzati con Finance come contratti di progetto. Come parte del modello di integrazione, puoi impostare l'origine dell'integrazione in Finance per il contratto di progetto.

I progetti tempi e materiali e prezzo fisso vengono gestiti in Project Service Automation e sincronizzati con Finance come progetti. Come parte dell'integrazione del modello, puoi impostare l'origine dell'integrazione per il progetto in Finance. Attualmente, sono supportati solo progetti tempo e materiali e prezzo fisso.


Le voci di contratto di progetto vengono gestite in Project Service Automation e vengono sincronizzate con Finance come regole di fatturazione del contratto di progetto. Se il metodo di fatturazione è diverso dal tipo di progetto predefinito, la sincronizzazione aggiorna il tipo di progetto per il progetto della voce di contratto e il gruppo di progetti.

Le fasi di voci di contratto di progetto vengono gestite in Project Service Automation e vengono sincronizzate con Finance come fasi di regole di fatturazione del contratto di progetto.

## <a name="project-service-automation-to-finance-integration-solution"></a>Soluzione di integrazione da Project Service Automation a Finance

Il campo **ID contratto di progetto** è disponibile nella pagina **Contratti di progetto**. Questo campo è stato convertito in una chiave naturale e univoca per supportare l'integrazione.

Quando viene creato un nuovo contratto di progetto, se un valore **ID contratto di progetto** non esiste già, viene generato automaticamente utilizzando una sequenza numerica. Il valore è costituito da **ORD** seguito da una sequenza numerica crescente e quindi da un suffisso di sei caratteri. Di seguito è riportato un esempio: **ORD-01022-Z4M9Q0**.

Il campo **Numero di progetto** è disponibile nella pagina **Progetti**. Questo campo è stato convertito in una chiave naturale e univoca per supportare l'integrazione.

Quando viene creato un nuovo progetto, se un valore **Numero di progetto** non esiste già, viene generato automaticamente utilizzando una sequenza numerica. Il valore è costituito da **PRJ** seguito da una sequenza numerica crescente e quindi da un suffisso di sei caratteri. Di seguito è riportato un esempio: **PRJ-01049-CCNID0**.

Quando viene applicata la soluzione di integrazione da Project Service Automation a Finance, uno script di aggiornamento imposta il campo **ID contratto di progetto** per contratti di progetto esistenti e il campo **Numero di progetto** per i progetti esistenti in Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Configurazione di prerequisiti e mapping

- Prima di sincronizzare i contratti di progetto e i progetti, è necessario sincronizzare gli account.
- Nel set di connessione, aggiungi un mapping del campo della chiave di integrazione per **msdyn\_organizationalunits** su **msdyn\_name\[Nome \]**. Potrebbe essere necessario prima aggiungere un progetto al set di connessione. Per altre informazioni, vedi [Integrare i dati in Common Data Service per le app](/powerapps/administrator/data-integrator).
- Nel set di connessione, aggiungi un mapping del campo della chiave di integrazione per **msdyn\_projects** su **msdynce\_projectnumber\[Numero di progetto\]**. Potrebbe essere necessario prima aggiungere un progetto al set di connessione. Per altre informazioni, vedi [Integrare i dati in Common Data Service per le app](/powerapps/administrator/data-integrator).
- **SourceDataID** per i contratti di progetto e i progetti possono essere aggiornati su un valore diverso o rimossi dal mapping. Il valore del modello predefinito è **Project Service Automation**.
- Il mapping **PaymentTerms** deve essere aggiornato in modo che rifletta i termini di pagamento validi in Finance. Puoi inoltre rimuovere il mapping dall'attività del progetto. Il mapping di valori predefinito ha valori predefiniti per i dati demo. La tabella seguente mostra i valori in Project Service Automation.

    | Value | Descrizione   |
    |-------|---------------|
    | 1     | 30 gg.        |
    | 2     | 30 gg. (10 gg. sconto 2%) |
    | 3     | 45 gg.        |
    | 4     | 60 gg.        |

## <a name="power-query"></a>Power Query

Utilizza Microsoft Power Query per Excel per filtrare i dati se sono soddisfatte le seguenti condizioni:

- Hai ordini cliente in Dynamics 365 Sales.
- Hai più unità organizzative in Project Service Automation e queste unità organizzative verranno associate a più persone giuridiche in Finance.

Se devi utilizzare Power Query, segui queste linee guida:

- Il modello Progetti e contratti (da PSA a Fin e Ops) ha un filtro predefinito che include solo gli ordini di vendita del tipo **Elemento di di lavoro (msdyn\_ordertype = 192350001)**. Questo filtro consente di garantire che i contratti di progetto non vengano creati per gli ordini di vendita in Finance. Se crei il tuo modello, devi aggiungere questo filtro.
- Crea un filtro Power Query che includa solo le organizzazioni di contratto che devono essere sincronizzate con la persona giuridica del set di connessione di integrazione. Ad esempio, i contratti di progetto che hai con l'unità organizzativa del contratto di Contoso US devono essere sincronizzati con la persona giuridica USSI, ma i contratti di progetto che hai con l'unità organizzativa del contratto di Contoso Global devono essere sincronizzati con la persona giuridica USMF. Se non aggiungi questo filtro al mapping delle attività, tutti i contratti di progetto verranno sincronizzati con la persona giuridica definita per il set di connessione, indipendentemente dall'unità organizzativa del contratto.

## <a name="template-mapping-in-data-integration"></a>Mapping dei modelli nell'integrazione dei dati

> [!NOTE] 
> I campi **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** e **AddressZipCode** non sono inclusi nel mapping predefinito per i contratti di progetto. Puoi aggiungere i mapping se vuoi che questi dati vengano sincronizzati per i contratti di progetto.
>
> I campi **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** e **ProjectType** non sono inclusi nel mapping predefinito per i progetti. Puoi aggiungere i mapping se vuoi che questi dati vengano sincronizzati per i progetti.

La figura seguente mostra esempi di mapping delle attività del modello in Integrazione dati. Il mapping mostra le informazioni sui campi che verranno sincronizzate da Project Service Automation a Finance.

[![Mapping di modello di contratto di progetto](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mapping di modello di progetto](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mapping di modello di voci di contratto di progetto](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mapping di modello di passaggio fondamentale di voce di contratto di progetto](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Mapping delle fasi di voce contratto di progetto nel modello di progetti e contratti (da PSA 3.x a Dynamics) - v2:

[![Mapping di passaggio fondamentale di voce di contratto di progetto con modello a due versioni](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]