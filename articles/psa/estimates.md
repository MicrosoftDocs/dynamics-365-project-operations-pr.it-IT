---
title: Stime
description: In questo argomento vengono fornite informazioni sulle stime in Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fcb3c85af092667cc5a473ab4674c3be47e33327
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007596"
---
# <a name="estimates"></a>Stime

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In un'offerta basata su progetto, puoi utilizzare l'entità Dettagli riga di offerta per stimare il lavoro necessario per completare un progetto. Puoi quindi condividere quella stima con il cliente.

Le righe di offerta basate su progetto non devono avere dettagli di riga di offerta. In alternativa, possono avere molti dettagli di riga di offerta. I dettagli di riga di offerta sono utilizzati per stimare tempo, spese o commissioni. PSA non consente l'utilizzo di stime materiale per i dettagli di riga di offerta. Queste sono denominate classi di transazioni. Gli importi stimati delle imposte possono anche essere immessi in una classe di transazioni.

Oltre alle classi di transazioni, i dettagli di riga di offerta hanno un tipo di transazione. PSA supporta due tipi di transazioni per i dettagli di riga di offerta: **Costo** e **Contratto di progetto**.

## <a name="estimate-by-using-a-contract"></a>Stima utilizzando un contratto

Se hai utilizzato un'offerta PSA alla creazione di un contratto basato su progetto, la stima generata per ogni riga di offerta viene copiata nel contratto di progetto. La struttura di un contratto di progetto è uguale a quella dell'offerta di progetto con righe, dettagli di riga e pianificazioni fatturazione.

Le stime possono essere eseguite direttamente in un contratto di progetto nonché in un'offerta di progetto. Per un'offerta di progetto, la stima viene eseguita utilizzando voci di contratto e dettagli di voce di contratto. I dettagli di voce di contratto possono anche essere generati da un piano di progetto creato utilizzando l'approccio con stima bottom-up.

I dettagli di voce di contratto possono essere utilizzati per stimare tempo, spese o imposte. Gli importi stimati delle imposte possono anche essere immessi in un dettaglio di voce di contratto.

PSA non consente l'utilizzo di stime materiale per i dettagli di voce di contratto.

I processi supportati in un contratto di progetto sono la creazione e la conferma di fatture. La creazione di fatture crea una bozza di una fattura basata su progetto che include tutti i valori effettivi di vendita non fatturati fino alla data corrente.

La conferma rende il contratto di sola lettura e ne modifica lo stato da **Bozza** a **Confermato**. Se esegui tale azione, non puoi annullarla. Poiché questa azione è definitiva, è consigliabile mantenere il contratto nello stato **Bozza**.

Le sole differenze tra le bozze di contratto e i contratti confermati sono lo stato e il fatto che le bozze di contratto, a differenza dei contratti confermati, possono essere modificate. La creazione di fatture e la tracciatura di dati effettivi possono essere effettuate nelle bozze di contratto e nei contratti confermati.

PSA non supporta ordini di modifica in contratti o progetti.

## <a name="estimating-projects"></a>Stima dei progetti

Puoi stimare tempo e spese nei progetti. PSA non consente le stime di materiali o imposte nei progetti.

Le stime di tempo vengono generate quando si crea un'attività e si identificano gli attributi di una risorsa generica necessaria per eseguire l'attività. Le stime di tempo vengono generate a partire dalle attività di pianificazione. Le stime di tempo non vengono create se crei membri del team generici al di fuori del contesto della pianificazione.

Le stime di spesa vengono immesse nella griglia della pagina **Stime**.

## <a name="understanding-estimation"></a>Informazioni sulle stime

Utilizza la tabella seguente come guida per comprendere la logica di business nella fase di stima.

| Scenario                                                                                                                                                                                                                                                                                                                                          | Record dell'entità                                                                                                                                                                                                       | Tipo di transazione | Classe di transazione | Informazioni aggiuntive                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Se devi stimare il valore di vendita del tempo per un'offerta                                                                                                                                                                                                                                                                                    | Viene creato il record Dettagli riga di offerta                                                                                                                                                                               | Contratto di progetto | Time        | Il campo Origine transazione nella riga dei dettagli di riga sul lato vendite fa riferimento ai dettagli di riga di offerta sul lato costi |
|                                                                                                                                                                                                                                                                                     | Un secondo record Dettagli riga di offerta viene creato dal sistema per memorizzare i valori di costo corrispondenti. Tutti i campi di tipo non money vengono copiati dai dettagli riga di offerta di vendita nei dettagli riga di offerta di costo.                                                                                                                                                                               | Costo | Time        | Il campo Origine transazione nel dettaglio della riga di offerta sul lato vendite fa riferimento ai dettagli di riga di offerta sul lato costi |
| Se devi stimare il valore di vendita del tempo per un contratto                                                                                                                                                                                                                                                                                 | Viene creato il record Dettagli di voce di contratto di progetto                                                                                                                                                                    | Contratto di progetto | Time        | Il campo Origine transazione nei dettagli di voce di contratto sul lato vendite fa riferimento ai dettagli di voce di contratto sul lato costi      |
|                                                                                                                                                                                                                                                                                  | Un secondo record Dettagli voce di contratto viene creato dal sistema per memorizzare i valori di costo corrispondenti. Tutti i campi di tipo non money vengono copiati dai dettagli voce di contratto lato vendita nei dettagli voce di contratto lato costo.                                                                                                                                                                    | Costo | Time        | Il campo Origine transazione nei dettagli di voce di contratto sul lato vendite fa riferimento ai dettagli di voce di contratto sul lato costi      |
| Quando l'utente descrive una risorsa per un'attività di progetto                                                                                                                                                                                                                                                                                            | Un record di riga di stima per visualizzare il valore di vendita dell'attività viene creato quando un'attività viene creata con tutte le dimensioni di determinazione dei prezzi necessarie. Il ruolo e le unità organizzative sono le dimensioni di determinazione dei prezzi di OOB Project Service | Contratto di progetto | Time        |                                                                                   |
|     | Il record di riga di stima per visualizzare il valore di costo dell'attività viene creato quando un'attività viene creata con tutte le dimensioni di determinazione dei prezzi necessarie. Tutti i campi di tipo non money vengono copiati dal sistema dalla riga di stima di vendita nella riga di stima di costo. Il ruolo e l'unità organizzativa sono le dimensioni di determinazione dei prezzi di OOB PSA per i tassi di costo e di fatturazione.                                                                                                                                                                                                                | Costo             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalizzare le entità Dettagli riga di offerta e Dettagli voce di contratto

Se hai aggiunto un campo personalizzato per i dettagli di riga di offerta e vuoi che il sistema immetta il valore del campo come valore predefinito nella riga dei costi correlata che crea, utilizza gli strumenti di registrazione del plug-in PreOperationContractLineDetailUpdate and PreOperationQuoteLineDetailUpdate . Questi plug-in devono essere registrati dopo la modifica del dettaglio di riga di offerta o del dettaglio di voce di contratto. Segui i passaggi seguenti per completare il processo:

1. Apri PluginRegistrationTool e connettiti all'istanza online.
2. Seleziona **Cerca** e cerca il plug-in da aggiornare.

    ![Finestra di dialogo Albero ricerca](media/basic-guide-19.png)

3. Seleziona il plug-in e quindi, nella pagina principale, seleziona **Seleziona**.
4. Seleziona il passaggio del plug-in da aggiornare, fai clic con il pulsante destro del mouse e quindi scegli **Aggiorna**.

    ![Selezionare un passaggio nel plug-in](media/basic-guide-20.png)

5. Nella finestra di dialogo **Aggiorna passaggio esistente**, nel campo **Attributi filtro**, seleziona il pulsante con i puntini di sospensione (**...**):
 
    ![Finestra di dialogo Aggiorna passaggio esistente](media/basic-guide-21.png)

6. Nella finestra di dialogo **Seleziona attributi**, seleziona le caselle di controllo relative agli attributi personalizzati.

    ![Finestra di dialogo Seleziona attributi](media/basic-guide-22.png)

7. Seleziona **OK** per chiudere la finestra di dialogo e quindi seleziona **Aggiorna passaggio**.
 
    ![Pulsante Aggiorna passaggio](media/basic-guide-23.png)

8. Ripeti i passaggi da 1 a 7 per il secondo plug-in.
9. Chiudi PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]