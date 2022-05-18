---
title: Integrazione di stime e valori effettivi di progetto
description: Questo argomento fornisce informazioni sull'integrazione a doppia scrittura di Project Operations per le stime e i valori effettivi di progetto.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5aaa59020427438fa6ebab3789fbb70c5b86e272
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577195"
---
# <a name="project-estimates-and-actuals-integration"></a>Integrazione di stime e valori effettivi di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento fornisce informazioni sull'integrazione a doppia scrittura di Project Operations per le stime e i valori effettivi di progetto.

## <a name="project-estimates"></a>Stime di progetto

Le stime di manodopera, spese e materiali di progetto vengono create e mantenute in Microsoft Dataverse e sincronizzate con le app per la finanza e le operazioni a fini contabili. La creazione, l'aggiornamento e l'eliminazione di operazioni non sono supportati tramite le app per la finanza e le operazioni.

La creazione di stime richiede una configurazione contabile valida per il progetto. I progetti associati alle righe di contratto devono avere un profilo di costi e ricavi del progetto valido definito nelle regole del profilo dei ricavi e dei costi del progetto. Per ulteriori informazioni, vedi [Configurare la contabilità per i progetti fatturabili](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Stime di manodopera

Le stime di manodopera vengono create dal responsabile di progetto o dal responsabile delle risorse che assegna una risorsa generica o denominata all'attività del progetto. I record di assegnazione delle risorse possono essere esaminati nella scheda **Assegnazioni risorse** della pagina **Dettagli progetto** in Dataverse. I record di assegnazione delle risorse in Dataverse creano record di previsioni orarie nelle app per la finanza e le operazioni utilizzando **Entità di integrazione per stime orarie di Project Operations (msdyn\_resourceassignments)**.

   ![Integrazione di stime di manodopera.](./Media/DW4LaborEstimates.png)

La doppia scrittura sincronizza i record di assegnazione delle risorse alla tabella di gestione temporanea (**ProjCDSEstimateHoursImport**), quindi utilizza la logica aziendale per creare e aggiornare i record delle previsioni orarie (**ProjForecastEmpl**).

Il contabile di progetto esamina i record delle ore di previsione creati nelle app per la finanza e le operazioni andando in **Gestione progetti e contabilità** > **Tutti i progetti** > **Piano** > **Previsioni ore**.

## <a name="expense-estimates"></a>Stime di spesa

Le stime di spesa vengono create dal responsabile di progetto nella scheda **Stime di spesa** della pagina **Dettagli progetto** in Dataverse. I record delle stime di spesa vengono archiviati nell'entità **Riga di stima** in Dataverse. Questi record di stima hanno una classe di transazione, **Spese** e sono sincronizzati con i record di previsione delle spese nelle app per la finanza e le operazioni usando **Entità dell'integrazione di Project Operations per stime delle spese (msdyn\_estimatelines)**.

   ![Integrazione di stime di spesa.](./Media/DW4ExpenseEstimates.png)

La doppia scrittura sincronizza i record di stima di spesa alla tabella di gestione temporanea **ProjCDSEstimateExpenseImport**, quindi utilizza la logica aziendale per creare e aggiornare i record delle previsioni di spesa (**ProjForecastCost**). Le righe di stima memorizzano la stima delle vendite e i record della stima dei costi separatamente. La logica di business nelle app per la finanza e le operazioni compila un singolo record di previsione delle spese utilizzando questo dettaglio nella tabella di gestione temporanea.

Il contabile di progetto può esaminare i record delle previsioni di spesa creati nelle app per la finanza e le operazioni andando in **Gestione progetti e contabilità** > **Tutti i progetti** > **Piano** > **Previsioni spesa**.

## <a name="material-estimates"></a>Stime di materiale

Le stime di materiale vengono create dal responsabile di progetto nella scheda **Stime di materiale** della pagina **Dettagli progetto** in Dataverse. I record delle stime di materiale vengono archiviati nell'entità **Riga di stima** in Dataverse. Questi record di stima hanno la classe di transazione, **Materiale** e sono sincronizzati con i record di previsione articoli nelle app per la finanza e le operazioni usando **Tabella di integrazione di progetto per stime di materiali (msdyn\_estimatelines)**.

   ![Integrazione di stime di materiale.](./Media/DW4MaterialEstimates.png)

La doppia scrittura sincronizza i record di stima di materiale alla tabella di gestione temporanea **ProjForecastSalesImpor**, quindi utilizza la logica aziendale per creare e aggiornare i record delle previsioni di articolo (**ForecastSales**). Le righe di stima memorizzano la stima delle vendite e i record della stima dei costi separatamente. La logica di business nelle app per la finanza e le operazioni compila un singolo record di previsione dell'articolo utilizzando questo dettaglio nella tabella di gestione temporanea.

Il contabile di progetto può esaminare i record delle previsioni dell'articolo creati nelle app per la finanza e le operazioni andando in **Gestione progetti e contabilità** > **Tutti i progetti** > **Piano** > **Previsioni articolo**.

## <a name="project-actuals"></a>Valori effettivi di progetto

I valori effettivi di progetto vengono creati in Dataverse, in base a tempo, spesa, materiale e attività di fatturazione. Tutti gli attributi operativi di queste transazioni, tra cui quantità, prezzo di costo, prezzo di vendita e progetto, vengono acquisiti in questa entità Dataverse. Per ulteriori informazioni, vedi [Valori effettivi](../actuals/actuals-overview.md). I record effettivi vengono sincronizzati con le app per la finanza e le operazioni utilizzando la mappa tabella a doppia scrittura **Valori effettivi per l'integrazione di Project Operations (msdyn\_actuals)** per la contabilità a valle.

   ![Integrazione di valori effettivi.](./Media/DW4Actuals.png)

La mappa della tabella **Valori effettivi di integrazione di Project Operations** sincronizza tutti i record dall'entità **Valori effettivi** in Dataverse, con l'attributo **Ignora sincronizzazione (solo per uso interno)** impostato su **Falso**. Questo valore dell'attributo è impostato in Dataverse automaticamente quando viene creato il record. Esempi in cui questo attributo è impostato su **Vero** sono:

  - Valori effettivi dei costi di progetto per le transazioni interaziendali. Per ulteriori informazioni, vedi [Creare transazioni interaziendali](../project-accounting/create-intercompany-transactions.md). Questi record vengono ignorati perché il sistema ricrea il costo del progetto effettivo nelle app per la finanza e le operazioni quando viene registrata la fattura fornitore interaziendale.
  - Record di vendita non fatturati negativi creati quando la fattura proforma viene confermata. Questi record vengono ignorati perché il giornale di registrazione secondario di progetto nelle app per la finanza e le operazioni non annulla il record delle vendite non fatturate al momento della fatturazione, ma modifica lo stato in completamente fatturato.

La mappa della tabella a doppia scrittura sincronizza i record effettivi con la tabella di gestione temporanea **ProjCDSActualsImport**. Questi record vengono elaborati dal processo periodico **Importa dalla tabella di gestione temporanea** durante la creazione di righe del giornale di registrazione di integrazione di Project Operations e righe della proposta fattura di progetto. Per ulteriori informazioni, vedi [Giornale di registrazione integrazione in Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse acquisisce anche i collegamenti tra le transazioni effettive del progetto nell'entità **Connessione di transazione**. Per ulteriori informazioni, vedi [Collegare i valori effettivi ai record originali](../actuals/linkingactuals.md). I collegamenti tra le transazioni effettive vengono sincronizzati anche con le app per la finanza e le operazioni utilizzando la mappa tabella a doppia scrittura, **Entità di integrazione per relazioni tra transazione del progetto (msdyn\_transactionconnections)**. Questi record vengono usati dal processo periodico **Importa dalla tabella di gestione temporanea** durante la creazione di righe del giornale di registrazione di integrazione di Project Operations e righe della proposta fattura di progetto.

La registrazione di un giornale di registrazione di integrazione di Project Operations e di una proposta di fattura di progetto attiva un aggiornamento nei rispettivi record nella tabella di gestione temporanea **ProjCDSActualsImport**. Il sistema acquisisce e registra i seguenti attributi contabili per le transazioni effettive:

- Importo in valuta contabile
- Tasso di cambio
- Numero del giustificativo
- Importo IVA

La mappa della tabella **Valori effettivi di integrazione di Project Operations** aggiorna i rispettivi record effettivi in Dataverse con queste informazioni.
