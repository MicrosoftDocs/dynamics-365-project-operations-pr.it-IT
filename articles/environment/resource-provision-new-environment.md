---
title: Effettuare il provisioning di un nuovo ambiente
description: Questo argomento fornisce informazioni su come effettuare il provisioning di un nuovo ambiente Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949367"
---
# <a name="provision-a-new-environment"></a>Effettuare il provisioning di un nuovo ambiente

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento fornisce informazioni su come effettuare il provisioning di un nuovo ambiente Dynamics 365 Project Operations per scenari basati su risorse/non stoccate.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Abilitare il provisioning automatizzato di Project Operations in un progetto LCS

Utilizza i passaggi seguenti per abilitare il flusso di provisioning automatizzato di Project Operations per il progetto LCS.

1. Vai a [LCS](https://lcs.dynamics.com/v2) e seleziona il riquadro **Gestione funzionalità di anteprima**.
2. Nell'elenco **Funzionalità di anteprima** seleziona **Project Operations**, quindi seleziona **Funzionalità di anteprima abilitata** per abilitare Project Operations.

> [!NOTE]
> Questo passaggio viene eseguito solo una volta per progetto LCS.

## <a name="provision-a-project-operations-environment"></a>Effettuare il provisioning di un ambiente Project Operations

1. Apri una nuova distribuzione di [ambiente demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [ambiente di produzione/sandbox](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) di Dynamics 365 Finance. 
2. Segui la procedura guidata **Provisioning ambiente**. 

> [!IMPORTANT]
> Assicurati che la versione dell'applicazione selezionata sia 10.0.13 o successiva.

3. Per effettuare il provisioning di Project Operations, in **Impostazioni avanzate** seleziona **Common Data Service**. 
4. Abilita l'**Impostazione Common Data Service** selezionando **Sì** e quindi inserisci le informazioni nei campi obbligatori:

  - Nome
  - Area geografica
  - Linguaggio
  - Valuta
 
5. Nel campo **Modello Common Data Service**, seleziona **Project Operations** 

6. Seleziona il tipo di ambiente per la distribuzione. Una versione di valutazione basata su abbonamento ti consentirà di distribuire un ambiente CDS per 30 giorni. 

![Impostazioni di distribuzione](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Seleziona **Accetto** per accettare le condizioni d'uso e quindi seleziona **Fatto** per tornare alle impostazioni di distribuzione.

![Consenso distribuzione](./media/2DeploymentConsent.png)

7. Completa i restanti campi obbligatori nella procedura guidata e conferma la distribuzione. Il tempo di provisioning dell'ambiente varia in base al tipo di ambiente. Il provisioning potrebbe richiedere fino a sei ore.

  Dopo il completamento della distribuzione, l'ambiente verrà visualizzato come **Distribuito**.

8. Per confermare che l'ambiente è stato distribuito correttamente, seleziona **Accedi** e accedi all'ambiente per confermare.

![Dettagli degli ambienti ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Applicare i dati dimostrativi di Project Operations Finance (passaggio facoltativo)

Applica i dati dimostrativi di Project Operations Finance all'ambiente ospitato su cloud versione del servizio 10.0.13 come descritto in [questo articolo](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Applicare gli aggiornamenti all'ambiente Finance

Project Operations richiede un ambiente Finance con la versione dell'applicazione **10.0.13 (10.0.569.20009)** o superiore.

Potrebbe essere necessario applicare aggiornamenti di qualità all'ambiente Finance per ricevere questa versione.

1. In LCS, nella pagina **Dettagli ambiente**, nella sezione **Aggiornamenti disponibili**, seleziona **Visualizza aggiornamento**.

![Visualizzare gli aggiornamenti](./media/5ViewUpdates.png)

2. Nella pagina **Aggiornamenti binari**, seleziona **Salva pacchetto**.

![Salvare il pacchetto](./media/6SavePackage.png)

3. Fai clic su **Seleziona tutto** e quindi seleziona **Salva pacchetto**.

![Verificare e salvare gli aggiornamenti](./media/7ReviewAndSaveUpdates.png)

4. Immetti un nome e una descrizione del pacchetto, quindi seleziona **Salva**. A seconda della connessione Internet, questo processo potrebbe richiedere del tempo.

![Caricare il pacchetto nella raccolta di risorse](./media/8UploadPackageToAssetsLibrary.png)

5. Dopo aver salvato il pacchetto, seleziona **Fatto** e salva questo pacchetto nella raccolta di risorse nel progetto LCS.

Il salvataggio e la convalida del pacchetto potrebbero richiedere circa 15 minuti.

6. Per applicare l'aggiornamento, passa alla pagina **Dettagli ambiente** in LCS e seleziona **Gestisci** > **Applica aggiornamenti**.

![Gestire gli ambienti](./media/9MaintainEnvironment.png)

7. Nell'elenco degli aggiornamenti seleziona il pacchetto che hai creato e seleziona **Applica**.

![Applicare gli aggiornamenti](./media/10ApplyUpdates.png)

La manutenzione dell'ambiente richiederà del tempo. Al termine, l'ambiente tornerà a uno stato distribuito.

![Ambiente distribuito](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Stabilire una connessione a Doppia scrittura 

1. Nel progetto LCS, vai alla pagina **Dettagli ambiente**.
2. In **Informazioni sull'ambiente Common Data Service**, seleziona **Collega a CDS per app**.
3. Dopo aver completato il collegamento, seleziona di nuovo **Collega a CDS per app**. Verrai reindirizzato a Doppia scrittura in Finance.

![Collegamento a CDS](./media/12LinktoCDS.png)

4. Seleziona **Applica soluzione** per accedere alle entità che verranno mappate nell'integrazione.

![Applica soluzioni](./media/13ApplySolutions.png)

5. Seleziona entrambe le soluzioni, **Mapping entità doppia scrittura Dynamics 365 Finance and Operations** e **Mapping entità doppia scrittura Dynamics 365 Project Operations**, quindi seleziona **Applica**.

![Confermare le soluzioni](./media/14ConfirmSolutions.png)

Dopo aver applicato le soluzioni, le entità doppia scrittura vengono applicate all'ambiente.

![Applicazione delle soluzioni](./media/15ApplyingSolutions.png)

Dopo l'applicazione delle entità, tutti i mapping disponibili vengono elencati nell'ambiente.

![Mapping doppia scrittura](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Aggiornare le entità di dati dopo l'aggiornamento

1. In Finance, vai all'area di lavoro **Gestione dati**.

![Area di lavoro Gestione dati](./media/16DataManagement.png)

2. Seleziona il riquadro **Parametri framework**.

![Parametri framework](./media/17FrameworkParameters.png)

3. Nella pagina **Impostazioni entità**, seleziona **Aggiorna elenco di entità**.

![Aggiornare l'elenco di entità](./media/18RefreshEntityList.png)

L'aggiornamento richiederà circa 20 minuti. Riceverai un avviso quando sarà completo.

![Conferma dell'aggiornamento](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Eseguire il mapping doppia scrittura di Project Operations

1. Nel progetto LCS, vai alla pagina **Dettagli ambiente**.
2. In **Informazioni sull'ambiente Common Data Service**, seleziona **Collega a CDS per app**. Dopo aver selezionato il collegamento, verrai reindirizzato all'elenco delle entità nei mapping.
3. Avvia il mapping come descritto nella tabella seguente. Assicurati di seguire la sequenza elencata.

| **Mapping entità** | **Aggiorna entità** | **Sincronizzazione iniziale** | **Master per la sincronizzazione iniziale** | **Esegui prerequisiti** | **Sincronizzazione iniziale prerequisiti** |
| --- | --- | --- | --- | --- | --- |
| **Ruoli delle risorse di progetto per tutte le aziende (bookableresourcecategories)** | No | Sì | Common Data Service | No | N/A |
| **Persone giuridiche (cdm\_companies)** | No | Sì | App Finance and Operations | No | N/A |
| **Valori effettivi dell'integrazione di Project Operations (msdyn\_actuals)** | No | No | N/A | Sì | No |
| **Voci del contratto di progetto (salesorderdetails)** | No | No | N/A | No | No |
| **Entità di integrazione per le relazioni di transazione del progetto (msdyn\_transactionconnections)** | No | No | N/A | No | N/A |
| **Passaggi fondamentali della voce di contratto dell'integrazione di Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | N/A | No | N/A |
| **Entità di integrazione di Project Operations per le stime di spesa (msdyn\_estimateslines)** | No | No | N/A | No | N/A |
| **Entità di integrazione di Project Operations per le stime delle ore (msdyn\_resourceassignments)** | No | No | N/A | No | N/A |
| **Entità di esportazione delle spese di progetto di integrazione di Project Operations (msdyn\_expenses)** | Sì | No | N/A | No | N/A |
| **Entità di integrazione di Project Operations per le stime delle ore (msdyn\_resourceassignments)** | Sì | No | N/A | No | N/A |

4. Per aggiornare l'entità, seleziona il nome del mapping, quindi seleziona **Aggiorna entità**. 
5. Procedi con l'esecuzione del mapping al termine dell'aggiornamento.

![Aggiornare il mapping](./media/20RefreshMapping.png)

Prima di abilitare il mapping successivo, verificare che il mapping nella tabella sia in uno stato **In esecuzione**. L'esecuzione di mapping con un numero maggiore di prerequisiti potrebbe richiedere del tempo.

Per eseguire un mapping con prerequisiti, abilita l'interruttore **Mostra mapping entità correlate**. Se la tabella indica che **Sincronizzazione iniziale prerequisiti** è **No**, verifica che il contrassegno **Sincronizzazione iniziale** sia **Disattivato** in tutti i mapping di prerequisiti prima di eseguirlo.

![Eseguire il mapping](./media/21RunMap.png)

6. Conferma che tutti i mapping relativi al progetto siano in stato di esecuzione.

![Tutti i mapping in esecuzione](./media/22AllMapsRunning.png)

Il provisioning e la configurazione dell'ambiente Project Operations sono stati ora completati.
