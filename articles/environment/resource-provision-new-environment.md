---
title: Effettuare il provisioning di un nuovo ambiente
description: Questo argomento fornisce informazioni su come effettuare il provisioning di un nuovo ambiente Project Operations.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a00426678d23000dc19386792d346318eab74ed9
ms.sourcegitcommit: d3f66dfb5978c5c6b7fd51363c7f9278737c49c1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2021
ms.locfileid: "7928666"
---
# <a name="provision-a-new-environment"></a>Effettuare il provisioning di un nuovo ambiente

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Questo argomento fornisce informazioni su come eseguire il provisioning di un nuovo ambiente Dynamics 365 Project Operations per scenari basati risorse/materiali non stoccati.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Abilitare il provisioning automatizzato di Project Operations in un progetto LCS

Utilizza i passaggi seguenti per abilitare il flusso di provisioning automatizzato di Project Operations per il progetto LCS.

1. Vai a [LCS](https://lcs.dynamics.com/v2) e seleziona il riquadro **Gestione funzionalità di anteprima**.
2. Nell'elenco **Funzionalità di anteprima** seleziona **Funzionalità Project Operations**, quindi seleziona **Funzionalità di anteprima abilitata** per abilitare Project Operations.

   > [!NOTE]
   > Questo passaggio viene eseguito solo una volta per progetto LCS.

## <a name="provision-a-project-operations-environment"></a>Effettuare il provisioning di un ambiente Project Operations

1. Apri una nuova distribuzione di [ambiente demo](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [ambiente di produzione/sandbox](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) di Dynamics 365 Finance. 
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

     ![Impostazioni di distribuzione.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Seleziona **Accetto** per accettare le condizioni d'uso e quindi seleziona **Fatto** per tornare alle impostazioni di distribuzione.
    >
    >![Consenso distribuzione.](./media/2DeploymentConsent.png)

7. Facoltativo: applica i dati demo all'ambiente. Vai a **Impostazioni avanzate** seleziona **Personalizza configurazione database SQL** e imposta **Specificare un set di dati per il database dell'applicazione** su **Demo**.
8. Completa i restanti campi obbligatori nella procedura guidata e conferma la distribuzione. Il tempo per il provisioning dell'ambiente varia in base al tipo di ambiente. Il provisioning potrebbe richiedere fino a sei ore.

   Dopo il completamento della distribuzione, l'ambiente verrà visualizzato come **Distribuito**.

9. Per confermare che l'ambiente è stato distribuito correttamente, seleziona **Accesso** e accedi all'ambiente per confermare.

    ![Dettagli ambiente.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Applicare gli aggiornamenti all'ambiente Finance

Project Operations richiede un ambiente Finance con la versione dell'applicazione **10.0.13 (10.0.569.20009)** o superiore.

Potrebbe essere necessario applicare aggiornamenti di qualità all'ambiente Finance per ricevere questa versione.

1. In LCS, nella pagina **Dettagli ambiente**, nella sezione **Aggiornamenti disponibili**, seleziona **Visualizza aggiornamento**.

    ![Visualizzare gli aggiornamenti.](./media/5ViewUpdates.png)

2. Nella pagina **Aggiornamenti binari**, seleziona **Salva pacchetto**.

    ![Salvare il pacchetto.](./media/6SavePackage.png)

3. Fai clic su **Seleziona tutto** e quindi seleziona **Salva pacchetto**.

    ![Verificare e salvare gli aggiornamenti.](./media/7ReviewAndSaveUpdates.png)

4. Immetti un nome e una descrizione del pacchetto, quindi seleziona **Salva**. A seconda della connessione Internet, questo processo potrebbe richiedere del tempo.

    ![Caricare il pacchetto nella raccolta di risorse.](./media/8UploadPackageToAssetsLibrary.png)

5. Dopo aver salvato il pacchetto, seleziona **Fatto** e salva questo pacchetto nella raccolta di risorse nel progetto LCS.

   Il salvataggio e la convalida del pacchetto potrebbero richiedere circa 15 minuti.

6. Per applicare l'aggiornamento, passa alla pagina **Dettagli ambiente** in LCS e seleziona **Gestisci** > **Applica aggiornamenti**.

    ![Gestire gli ambienti.](./media/9MaintainEnvironment.png)

7. Nell'elenco degli aggiornamenti seleziona il pacchetto che hai creato e seleziona **Applica**.

    ![Applicare gli aggiornamenti.](./media/10ApplyUpdates.png)

   La manutenzione dell'ambiente richiederà del tempo. Al termine, l'ambiente tornerà a uno stato distribuito.

    ![Ambiente distribuito.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Stabilire una connessione a Doppia scrittura 

1. Nel progetto LCS, vai alla pagina **Dettagli ambiente**.
2. In **Informazioni sull'ambiente Common Data Service**, seleziona **Collega a CDS per app**.
3. Dopo aver completato il collegamento, seleziona di nuovo **Collega a CDS per app**. Verrai reindirizzato a Doppia scrittura in Finance.

    ![Collegamento a CDS.](./media/12LinktoCDS.png)

4. Seleziona **Applica soluzione** per accedere alle entità che verranno mappate nell'integrazione.

    ![Applicare soluzioni.](./media/13ApplySolutions.png)

5. Seleziona entrambe le soluzioni, **Dynamics 365 Finance and Operations Dual Write Entity Map** e **Dynamics 365 Project Operations Dual Write Entity Maps** e quindi seleziona **Applica**.

    ![Confermare le soluzioni.](./media/14ConfirmSolutions.png)

    Dopo aver applicato le soluzioni, le entità doppia scrittura vengono applicate all'ambiente.

    ![Applicazione delle soluzioni.](./media/15ApplyingSolutions.png)

    Dopo l'applicazione delle entità, tutti i mapping disponibili vengono elencati nell'ambiente.

    ![Mapping doppia scrittura.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Aggiornare le entità di dati dopo l'aggiornamento

1. In Finance, vai all'area di lavoro **Gestione dati**.

    ![Area di lavoro Gestione dati.](./media/16DataManagement.png)

2. Seleziona il riquadro **Parametri framework**.

    ![Parametri framework.](./media/17FrameworkParameters.png)

3. Nella pagina **Impostazioni entità**, seleziona **Aggiorna elenco di entità**.

    ![Aggiornare l'elenco di entità.](./media/18RefreshEntityList.png)

L'aggiornamento richiederà circa 20 minuti. Riceverai un avviso quando sarà completo.

  ![Conferma dell'aggiornamento.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Aggiornare le impostazioni di sicurezza su Project Operations su Dataverse

1. Vai Project Operations nell'ambiente Dataverse. 
2. Passa a **Impostazioni** > **Sicurezza** > **Ruoli di sicurezza**. 
3. Nella pagina **Ruoli di sicurezza** nell'elenco dei ruoli, seleziona **utente app a doppia scrittura** e seleziona la scheda **Entità personalizzate**.  
4. Verificare che il ruolo abbia le autorizzazioni **Leggi** e **Aggiungi a** per le seguenti entità:
      
      - **Tipo di tasso di cambio valuta**
      - **Piano dei conti**
      - **Calendario fiscale**
      - **Libro mastro**
      - **Azienda**
      - **Spesa**

5. Dopo aver aggiornato ruolo di sicurezza, vai a **Impostazioni** > **Sicurezza** > **Team** e seleziona il team predefinito nella visualizzazione team **Proprietario azienda locale**.
6. Seleziona **Gestisci ruoli** e verifica che il privilegio di sicurezza **utente app a doppia scrittura** sia applicato a questo team.

## <a name="run-project-operations-dual-write-maps"></a>Eseguire il mapping doppia scrittura di Project Operations

1. Nel progetto LCS, vai alla pagina **Dettagli ambiente**.
2. In **Informazioni sull'ambiente Common Data Service**, seleziona **Collega a CDS per app**. Dopo aver selezionato il collegamento, verrai reindirizzato all'elenco delle entità nei mapping.
3. Avvia le mappe. Per ulteriori informazioni, vedi [Versioni della mappa a doppia scrittura di Project Operations](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Conferma che tutti i mapping relativi al progetto siano in stato di esecuzione.

    ![Tutti i mapping in esecuzione.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Applicare i dati di configurazione in CDS per Project Operations (facoltativo)

Se hai applicato i dati demo all'ambiente Finance, vedi [Impostare e applicare i dati di configurazione in Common Data Service per Project Operations](resource-apply-pro-setup-config-data.md) per applicare i dati demo all'ambiente CDS.


Il provisioning e la configurazione dell'ambiente Project Operations sono stati ora completati. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
