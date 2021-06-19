---
title: Aggiornare Project Operations nel tuo ambiente Finance
description: Questo argomento fornisce informazioni su come aggiornare Project Operations nell'ambiente Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011061"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Aggiornare Project Operations nel tuo ambiente Finance

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_


Questo argomento fornisce informazioni su come aggiornare Dynamics 365 Project Operations nell'ambiente Dynamics 365 Finance. Sono disponibili tre procedure richieste per aggiornare Project Operations all'aggiornamento 5 (UR5):

- [Importare il pacchetto nel progetto di anteprima](#import)
- [Applicare l'aggiornamento](#apply)
- [Aggiornare l'ambiente Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importare il pacchetto nel progetto LCS

1. Accedi a [Lifecycle Services (LCS)](https://lcs.dynamics.com/) come proprietario del progetto o responsabile dell'ambiente.
2. Nell'elenco dei progetti seleziona il progetto LCS.
3. Nella pagina **Progetto** nel gruppo **Ambienti** apri l'ambiente che desideri aggiornare.
4. Verifica che l'ambiente sia in esecuzione. Se non è avviato, avvia l'ambiente.
5. Nella sezione **Nuova versione** sotto **Aggiornamenti disponibili**, seleziona **Visualizza aggiornamento** per 10.0.15.

![Pulsante Visualizza aggiornamento](media/view-update.png)

6. Nella pagina **Aggiornamenti binari** seleziona **Salva pacchetto**.
7. Nella pagina **Esamina e salva aggiornamenti** seleziona **Salva pacchetto**.
8. Nel riquadro **Salva pacchetto nella raccolta cespiti** che si apre, immetti il nome del pacchetto e quindi seleziona **Salva pacchetto**.
9. Quando LCS ha terminato di salvare il pacchetto, il pulsate **Fatto** è abilitato. Seleziona **Fatto**. LCS verificherà il pacchetto. La verifica può richiedere alcuni minuti o fino a un'ora.


## <a name="apply-the-package-update"></a><a name="apply"></a>Applicare l'aggiornamento del pacchetto

1. In LCS, sulla pagina **Dettagli ambiente** seleziona **Gestisci** > **Applica aggiornamenti**.
2. Dall'elenco, seleziona il pacchetto che hai salvato in precedenza, quindi seleziona **Applica**.
3. Seleziona **Sì** per confermare che desideri distribuire il pacchetto.

![Finestra di dialogo Conferma distribuzione del pacchetto](media/confirm-package-deployment.png)

4. Seleziona **Sì** per confermare che desideri aggiornare l'applicazione.

![Finestra di dialogo Conferma aggiornamento dell'applicazione](media/confirm-application-update.png)

La distribuzione e l'aggiornamento dell'applicazione verranno avviati. 

Sulla pagina **Dettagli ambiente** nell'angolo in alto a destra, lo stato dell'ambiente verrà aggiornato su **Manutenzione**. In circa due ore l'aggiornamento sarà completo. Le informazioni sulla versione dell'applicazione verranno aggiornate su **Microsoft Dynamics 365 for Finance and Operations 10.0.15** e lo stato dell'ambiente verrà aggiornato su **Distribuito**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Aggiornare l'ambiente Dataverse

1. Accedi all'[interfaccia di amministrazione di Power Platform](https://admin.powerplatform.com/).
2. Nell'elenco, trova e apri l'ambiente che hai utilizzato per installare Project Operations.
3. Sulla pagina **Ambienti** seleziona **Risorsa** > **App Dynamics 365**.
4. Nell'elenco, individua **Microsoft Dynamics 365 Project Operations** e nella colonna **Stato** seleziona **Aggiornamento disponibile**.
5. Seleziona la casella di controllo **Accetto le condizioni d'uso**, quindi seleziona **Aggiorna**. L'ultima versione della soluzione verrà installata.

Al termine dell'installazione, avrai la versione 4.5.0.134 installata.

## <a name="configure-new-features"></a>Configurare le nuove funzionalità

### <a name="enable-dual-write-mapping"></a>Abilitare il mapping doppia scrittura

Dopo aver completato l'aggiornamento degli ambienti Finance e Dataverse puoi abilitare i mapping a doppia scrittura richiesti. Completa le seguenti procedure per abilitare i mapping a doppia scrittura.

- [Aggiornare le impostazioni di sicurezza nell'ambiente Customer Engagement](#security)
- [Aggiornare le entità di dati](#refresh)
- [Aggiornare ed eseguire i mapping a doppia scrittura](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Aggiornare le impostazioni di sicurezza nell'ambiente Dataverse

I seguenti aggiornamenti ai privilegi di sicurezza per le entità sono richiesti come parte dell'aggiornamento a UR5.

1. Nell'ambiente Dataverse vai a **Impostazioni** e nel gruppo **Sistema** seleziona **Sicurezza**.

![Impostazioni dell'ambiente Dataverse](media/Picture21.png)

2. Seleziona **Ruoli di sicurezza**.
3. Seleziona **utente app a doppia scrittura** e seleziona la scheda **Entità personalizzate**. 
4. Verifica che il ruolo abbia le autorizzazioni **Lettura** e **Aggiungi a** per:

      - **Tipo di tasso di cambio valuta**
      - **Piano dei conti** 
      - **Calendario fiscale** 
      - **Libro mastro**

5. Dopo aver aggiornato ruolo di sicurezza, vai a **Impostazioni** > **Sicurezza** > **Team**. Verifica che il ruolo **utente app a doppia scrittura** sia stato applicato al team. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Aggiornare le entità di dati dall'aggiornamento

1. Nel tuo ambiente Finance, apri l'area di lavoro **Gestione dati**, quindi apri la pagina **Parametri framework**.
2. Sulla scheda **Impostazioni entità** seleziona **Aggiorna elenco entità**.
3. Seleziona **Chiudi** per confermare l'aggiornamento dell'entità.

 > [!NOTE]
 > Questo processo richiederà circa 20 minuti per il completamento. Riceverai una notifica quando l'aggiornamento è completo.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Aggiornare i mapping doppia scrittura

1. Nell'area di lavoro **Gestione dati** seleziona **Doppia scrittura**.
2. Seleziona **Applicare soluzioni**, seleziona entrambe le soluzioni nell'elenco, quindi seleziona **Applica**.
3. Sulla pagina **Doppia scrittura** seleziona le seguenti mappe tabella, quindi seleziona **Arresta**.

    - **Valori effettivi dell'integrazione di Project Operations (msdyn_actuals)**
    - **Categorie di spesa del progetto di integrazione di Project Operations (msdyn_expensecategories)**
    - **Entità di esportazione delle spese di progetto effettive di integrazione di Project Operations (msdyn_expenses)**

4. Sulla pagina **Versione del mapping di tabella**, applica una nuova versione della mappa a ciascuna delle tre entità.
5. Sulla pagina **Doppia scrittura** seleziona Esegui per riavviare i mapping.
6. Dall'elenco dei mapping, seleziona il mapping **Libro mastro (msdyn_ledgers)** con tutti i prerequisiti e seleziona la casella di controllo **Sincronizzazione iniziale**. 
7. Nel campo **Master per la sincronizzazione iniziale** seleziona **App Finance and Operations** e poi seleziona **Esegui**.
 
 ![Sincronizzazione dei mapping del libro mastro](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]