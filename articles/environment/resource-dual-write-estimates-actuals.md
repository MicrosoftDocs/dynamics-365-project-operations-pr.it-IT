---
title: Integrazione di stime e valori effettivi di progetto
description: Questo argomento fornisce informazioni sull'integrazione a doppia scrittura di Project Operations per le stime e i valori effettivi di progetto.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006296"
---
# <a name="project-estimates-and-actuals-integration"></a>Integrazione di stime e valori effettivi di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento fornisce informazioni sull'integrazione a doppia scrittura di Project Operations per le stime e i valori effettivi di progetto.

## <a name="project-estimates"></a>Stime di progetto

La manodopera del progetto, le spese e le stime dei materiali vengono create e mantenute in Microsoft Dataverse e sincronizzate con le app Finance and Operations per scopi contabili. Le operazioni di creazione, aggiornamento ed eliminazione non sono supportate tramite le app Finance and Operations.

La creazione di stime richiede una configurazione contabile valida per il progetto. I progetti associati alle righe di contratto devono avere un profilo di costi e ricavi del progetto valido definito nelle regole del profilo dei ricavi e dei costi del progetto. Per ulteriori informazioni, vedi [Configurare la contabilità per i progetti fatturabili](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Stime di manodopera

Le stime di manodopera vengono create dal responsabile di progetto o dal responsabile delle risorse che assegna una risorsa generica o denominata all'attività del progetto. I record di assegnazione delle risorse possono essere esaminati nella scheda **Assegnazioni risorse** della pagina **Dettagli progetto** in Dataverse. I record di assegnazione delle risorse in Dataverse creano record di previsioni orarie nelle app Finance and Operations utilizzando **Entità di integrazione di Project Operations per le stime delle ore (msdyn\_resourceassignments)**.

   ![Integrazione di stime di manodopera.](./Media/DW4LaborEstimates.png)

La doppia scrittura sincronizza i record di assegnazione delle risorse alla tabella di gestione temporanea (**ProjCDSEstimateHoursImport**), quindi utilizza la logica aziendale per creare e aggiornare i record delle previsioni orarie (**ProjForecastEmpl**).

Il contabile del progetto esamina i record delle ore di previsione creati nelle app Finance and Operations andando in **Gestione progetti e contabilità** > **Tutti i progetti** > **Piano** > **Previsioni orarie**.

## <a name="expense-estimates"></a>Stime di spesa

Le stime di spesa vengono create dal responsabile di progetto nella scheda **Stime di spesa** della pagina **Dettagli progetto** in Dataverse. I record delle stime di spesa vengono archiviati nell'entità **Riga di stima** in Dataverse. Questi record di stima hanno la classe di transazione **Spese** e vengono sincronizzati con i record delle previsioni di spesa nelle app Finance and Operations utilizzando **Entità di integrazione di Project Operations per le stime di spesa (msdyn\_estimatelines)**.

   ![Integrazione di stime di spesa.](./Media/DW4ExpenseEstimates.png)

La doppia scrittura sincronizza i record di stima di spesa alla tabella di gestione temporanea **ProjCDSEstimateExpenseImport**, quindi utilizza la logica aziendale per creare e aggiornare i record delle previsioni di spesa (**ProjForecastCost**). Le righe di stima memorizzano la stima delle vendite e i record della stima dei costi separatamente. La logica aziendale nelle app Finance and Operations popola un singolo record di previsione di spesa utilizzando questo dettaglio nella tabella di gestione temporanea.

Il contabile del progetto può esaminare i record di previsione di spesa creati nelle app Finance and Operations andando in **Gestione progetti e contabilità** > **Tutti i progetti** > **Piano** > **Previsioni di spesa**.

## <a name="material-estimates"></a>Stime di materiale

Le stime di materiale vengono create dal responsabile di progetto nella scheda **Stime di materiale** della pagina **Dettagli progetto** in Dataverse. I record delle stime di materiale vengono archiviati nell'entità **Riga di stima** in Dataverse. Questi record di stima hanno la classe di transazione **materiale** e vengono sincronizzati con i record delle previsioni di articolo nelle app Finance and Operations utilizzando **Tabella di integrazione di Project Operations per le stime di materiale (msdyn\_estimatelines)**.

   ![Integrazione di stime di materiale.](./Media/DW4MaterialEstimates.png)

La doppia scrittura sincronizza i record di stima di materiale alla tabella di gestione temporanea **ProjForecastSalesImpor**, quindi utilizza la logica aziendale per creare e aggiornare i record delle previsioni di articolo (**ForecastSales**). Le righe di stima memorizzano la stima delle vendite e i record della stima dei costi separatamente. La logica aziendale nelle app Finance and Operations popola un singolo record di previsione di articolo utilizzando questo dettaglio nella tabella di gestione temporanea.

Il contabile del progetto può esaminare i record di previsione di articolo creati nelle app Finance and Operations andando in **Gestione progetti e contabilità** > **Tutti i progetti** > **Piano** > **Previsioni di articolo**.

## <a name="project-actuals"></a>Valori effettivi di progetto

I valori effettivi di progetto vengono creati in Dataverse, in base a tempo, spesa, materiale e attività di fatturazione. Tutti gli attributi operativi di queste transazioni, tra cui quantità, prezzo di costo, prezzo di vendita e progetto, vengono acquisiti in questa entità Dataverse. Per ulteriori informazioni, vedi [Valori effettivi](../actuals/actuals-overview.md). I record di valori effettivi vengono sincronizzati con le app Finance and Operations utilizzando la mappa della tabella a doppia scrittura **Valori effettivi dell'integrazione di Project Operations (msdyn\_actuals)** per la contabilità a valle.

   ![Integrazione di valori effettivi.](./Media/DW4Actuals.png)

La mappa della tabella **Valori effettivi di integrazione di Project Operations** sincronizza tutti i record dall'entità **Valori effettivi** in Dataverse, con l'attributo **Ignora sincronizzazione (solo per uso interno)** impostato su **Falso**. Questo valore dell'attributo è impostato in Dataverse automaticamente quando viene creato il record. Esempi in cui questo attributo è impostato su **Vero** sono:

  - Valori effettivi dei costi di progetto per le transazioni interaziendali. Per ulteriori informazioni, vedi [Creare transazioni interaziendali](../project-accounting/create-intercompany-transactions.md). Questi record vengono ignorati perché il sistema ricrea il costo effettivo del progetto nelle app Finance and Operations quando viene registrata la fattura fornitore interaziendale.
  - Record di vendita non fatturati negativi creati quando la fattura proforma viene confermata. Questi record vengono ignorati perché la contabilità secondaria del progetto nelle app Finance and Operations non annullano il record delle vendite non fatturate al momento della fatturazione ma cambiano lo stato in completamente fatturato.

La mappa della tabella a doppia scrittura sincronizza i record effettivi con la tabella di gestione temporanea **ProjCDSActualsImport**. Questi record vengono elaborati dal processo periodico **Importa dalla tabella di gestione temporanea** durante la creazione di righe del giornale di registrazione di integrazione di Project Operations e righe della proposta fattura di progetto. Per ulteriori informazioni, vedi [Giornale di registrazione integrazione in Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse acquisisce anche i collegamenti tra le transazioni effettive del progetto nell'entità **Connessione di transazione**. Per ulteriori informazioni, vedi [Collegare i valori effettivi ai record originali](../actuals/linkingactuals.md). Vengono sincronizzati anche i collegamenti tra le transazioni effettive nelle app Finance and Operations che utilizzano la mappa della tabella a doppia scrittura **Entità di integrazione per le relazioni di transazione del progetto (msdyn\_transactionconnections)**. Questi record vengono usati dal processo periodico **Importa dalla tabella di gestione temporanea** durante la creazione di righe del giornale di registrazione di integrazione di Project Operations e righe della proposta fattura di progetto.

La registrazione di un giornale di registrazione di integrazione di Project Operations e di una proposta di fattura di progetto attiva un aggiornamento nei rispettivi record nella tabella di gestione temporanea **ProjCDSActualsImport**. Il sistema acquisisce e registra i seguenti attributi contabili per le transazioni effettive:

- Importo in valuta contabile
- Tasso di cambio
- Numero del giustificativo
- Importo IVA

La mappa della tabella **Valori effettivi di integrazione di Project Operations** aggiorna i rispettivi record effettivi in Dataverse con queste informazioni.
