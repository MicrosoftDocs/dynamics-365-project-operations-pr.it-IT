---
title: Integrazione di gestione spese
description: Questo argomento fornisce informazioni sull'integrazione delle note spese in Project Operations usando la doppia scrittura.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b41be519dbfa89668712bc28ccb1888cd08c38a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585797"
---
# <a name="expense-management-integration"></a>Integrazione di gestione spese

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento fornisce informazioni sull'integrazione delle note spese nella [distribuzione completa delle spese](../expense/expense-overview.md) di Project Operations usando la doppia scrittura.

## <a name="expense-categories"></a>Categorie di spesa

In una distribuzione di spesa completa, le categorie di spesa vengono create e gestite nelle app per la finanza e le operazioni. Per creare una nuova categoria di spesa, completa i seguenti passaggi:

1. In Microsoft Dataverse, crea una categoria **Transazione**. L'integrazione a doppia scrittura sincronizzerà questa categoria di transazione con le app per la finanza e le operazioni. Per ulteriori informazioni, vedi [Configurare le categorie di progetto](/dynamics365/project-operations/project-accounting/configure-project-categories) e [Installazione di Project Operations e integrazione dei dati di configurazione](resource-dual-write-setup-integration.md). Come risultato di questa integrazione, il sistema crea quattro record di categoria condivisi nelle app per la finanza e le operazioni.
2. In Finance, vai in **Gestione spese** > **Configura** > **Categorie condivise** e seleziona una categoria condivisa con una classe di transazione **Spese**. Imposta il parametro **Può essere utilizzato in Spese** su **Vero** e definisci il tipo di spesa da utilizzare.
3. Utilizzando questo record di categoria condivisa, crea una nuova categoria di spesa andando in **Gestione spese** > **Configura** > **Categorie di spesa** e selezionando **Nuovo**. Quando il record viene salvato, la doppia scrittura utilizza la mappa della tabella **Entità di esportazione categorie di spesa di progetto integrazione di Project Operations (msdyn\_expensecategories)** per sincronizzare questo record in Dataverse.

  ![Integrazione di categorie di spesa.](./media/DW6ExpenseCategories.png)

Le categorie di spesa nelle app per la finanza e le operazioni sono specifiche dell'azienda o della persona giuridica. Esistono record corrispondenti specifici della persona giuridica separati in Dataverse. Quando un responsabile di progetto stima le spese, non può selezionare le categorie di spesa create per un progetto di proprietà di una società diversa da quella a cui appartiene il progetto su cui stanno lavorando. 

## <a name="expense-reports"></a>Note spese

Le note spese vengono create e approvate nelle app per la finanza e le operazioni. Per ulteriori informazioni, vedi [Creare ed elaborare le note spese in Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Dopo che la nota spese è stata approvata dal responsabile di progetto, viene registrata nella contabilità generale. In Project Operations, le righe delle note spese relative al progetto vengono registrate utilizzando regole di registrazione speciali:

  - Il costo relativo al progetto (inclusa l'imposta non recuperabile) non viene registrato immediatamente nel conto dei costi di progetto della contabilità generale, ma viene invece registrato nel conto di integrazione delle spese. Questo conto è configurato in **Gestione progetti e contabilità** > **Configura** > **Parametri di gestione progetti e contabilità** , **Project Operations in Dynamics 365 Customer Engagement**.
  - La doppia scrittura si sincronizza con Dataverse utilizzando la mappa della tabella **Entità di esportazione delle spese di progetto di integrazione di Project Operations (msdyn\_expenses)** .
  - Registro secondario delle imposte, registro secondario del fornitore e altre registrazioni finanziarie vengono registrati come applicabili quando viene registrata la nota spese.

  ![Integrazione di note spese.](./media/DW6ExpenseReports.png)

Quando un record viene scritto nell'entità **Spese** in Dataverse, il sistema attiva il processo di approvazione automatizzato del record. Se necessario, lo stato del processo di approvazione automatizzato può essere rivisto in Dataverse andando in **Impostazioni avanzate** > **Sistema** > **Processi di sistema**. Dopo che l'approvazione è stata completata, vengono creati i record della classe di transazione materiale nell'entità **Valori effettivi**.

I valori effettivi relativi alle spese vengono quindi elaborati utilizzando la mappa della tabella a doppia scrittura **Valori effettivi dell'integrazione di Project Operations (msdyn\_actuals)**. Per ulteriori informazioni, vedi [Stime e valori effettivi di progetto](resource-dual-write-estimates-actuals.md).

Il processo periodico, **Importa da gestione temporanea** crea righe di giornale di registrazione di integrazione Project Operations correlate alla nota spesa. L'impostazione predefinita del conto di contropartita è il conto di integrazione della spesa. La registrazione del giornale di registrazione di integrazione cancella il saldo del conto per la transazione di spesa e sposta l'importo della spesa nel conto dei costi di progetto. Il sistema inoltre crea le transazioni di contabilità secondaria del progetto per la fatturazione a valle e per il riconoscimento dei ricavi.
