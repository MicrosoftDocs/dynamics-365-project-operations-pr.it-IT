---
title: Concetti di stima finanziaria
description: Questo argomento fornisce informazioni sulle stime finanziarie di progetti in Project Operations.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a251be995abddba04cee689714d0a8f4e9d9e7d7
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701741"
---
# <a name="financial-estimation-concepts"></a>Concetti di stima finanziaria

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

In Dynamics 365 Project Operations, puoi stimare finanziariamente i progetti in due fasi: 
1. Durante la fase di prevendita prima dell'acquisizione della transazione. 
2. Durante la fase di esecuzione dopo la creazione del contratto di progetto. 

Puoi creare una stima finanziaria per il lavoro basato su progetto utilizzando una delle seguenti 3 pagine:
- La pagina **Riga di offerta**, utilizzando i dettagli della riga di offerta.  
- La pagina **Voce di contratto di progetto**, utilizzando i dettagli della voce di contratto. 
- La pagina **Progetto**, utilizzando le pagine delle schede **Attività** o **Stime di spesa**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Usare un'offerta di progetto per creare una stima
In un'offerta basata su progetto, puoi utilizzare l'entità **Dettagli riga di offerta** per stimare il lavoro necessario per completare un progetto. Puoi quindi condividere quella stima con il cliente.

Le righe di offerta basate su progetto possono avere da zero a molti dettagli di riga di offerta. I dettagli di riga di offerta sono utilizzati per stimare tempo, spese o commissioni. Microsoft Dynamics 365 Project Operations non consente l'utilizzo di stime materiale per i dettagli di riga di offerta. Queste sono denominate classi di transazioni. Gli importi stimati delle imposte possono anche essere immessi in una classe di transazioni.

Oltre alle classi di transazioni, i dettagli di riga di offerta hanno un tipo di transazione. Sono supportati due tipi di transazione per i dettagli di riga di offerta: **Costo** e **Contratto di progetto**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Usare un contratto di progetto per creare una stima

Se hai utilizzato un'offerta alla creazione di un contratto basato su progetto, la stima generata per ogni riga di offerta viene copiata nel contratto di progetto. La struttura di un contratto di progetto è uguale a quella dell'offerta di progetto con righe, dettagli di riga e pianificazioni fatturazione.

Le stime possono essere eseguite direttamente in un contratto di progetto nonché in un'offerta di progetto. Per un'offerta di progetto, la stima viene eseguita utilizzando voci di contratto e dettagli di voce di contratto. I dettagli di voce di contratto possono anche essere generati da un piano di progetto creato utilizzando l'approccio con stima bottom-up.

I dettagli di voce di contratto possono essere utilizzati per stimare tempo, spese o imposte. Gli importi stimati delle imposte possono anche essere immessi nel dettaglio di una voce di contratto.

Le stime materiale non sono consentite per i dettagli di voce di contratto.

## <a name="use-a-project-to-create-an-estimate"></a>Usare un progetto per creare una stima 

Puoi stimare tempo e spese nei progetti. Project Operations non supporta stime di materiali o commissioni sui progetti.

Le stime di tempo vengono generate quando si crea un'attività e si identificano gli attributi di una risorsa generica necessaria per eseguire l'attività. Le stime di tempo vengono generate a partire dalle attività di pianificazione. Le stime di tempo non vengono create se crei membri del team generici al di fuori del contesto della pianificazione.

Le stime di spesa vengono immesse nella griglia della pagina **Stime di spesa**.

La creazione di una stima per un progetto è una procedura consigliata poiché è possibile creare stime dettagliate bottom-up per manodopera o tempo e spese in ciascuna attività nel piano di progetto. Puoi quindi utilizzare questa stima dettagliata per creare stime per ogni riga di offerta e creare un'offerta più credibile per il cliente. Quando importi o crei una stima dettagliata nella riga di offerta utilizzando il piano di progetto, Project Operations importa i valori delle vendite e i valori di costo di queste stime. Dopo l'importazione, è possibile visualizzare le metriche relative a redditività, margini e fattibilità nell'offerta di progetto.

## <a name="understanding-estimates"></a>Informazioni sulle stime

Utilizzare la tabella seguente come guida per comprendere la logica di business nella fase di stima.

| Scenario                                                                                                                                                                                                                                                                                                                                          | Record dell'entità                                                                                                                                                                                                       | Tipo di transazione | Classe di transazione | Informazioni aggiuntive                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Se devi stimare il valore di vendita del tempo per un'offerta                                                                                                                                                                                                                                                                                    | Viene creato il record Dettagli riga di offerta                                                                                                                                                                               | Contratto di progetto | Time        | Il campo Origine transazione nella riga dei dettagli di riga sul lato vendite fa riferimento ai dettagli di riga di offerta sul lato costi |
|                                                                                                                                                                                                                                                                                     | Un secondo record Dettagli riga di offerta viene creato dal sistema per memorizzare i valori di costo corrispondenti. Tutti i campi di tipo non money vengono copiati dai dettagli riga di offerta di vendita nei dettagli riga di offerta di costo.                                                                                                                                                                               | Costo | Time        | Il campo Origine transazione nel dettaglio della riga di offerta sul lato vendite fa riferimento ai dettagli di riga di offerta sul lato costi |
| Se devi stimare il valore di vendita del tempo per un contratto                                                                                                                                                                                                                                                                                 | Viene creato il record Dettagli di voce di contratto di progetto                                                                                                                                                                    | Contratto di progetto | Time        | Il campo Origine transazione nei dettagli di voce di contratto sul lato vendite fa riferimento ai dettagli di voce di contratto sul lato costi      |
|                                                                                                                                                                                                                                                                                  | Un secondo record Dettagli voce di contratto viene creato dal sistema per memorizzare i valori di costo corrispondenti. Tutti i campi di tipo non money vengono copiati dai dettagli voce di contratto lato vendita nei dettagli voce di contratto lato costo.                                                                                                                                                                    | Costo | Time        | Il campo Origine transazione nei dettagli di voce di contratto sul lato vendite fa riferimento ai dettagli di voce di contratto sul lato costi      |
| Quando l'utente descrive una risorsa per un'attività di progetto                                                                                                                                                                                                                                                                                            | Un record di riga di stima per visualizzare il valore di vendita dell'attività viene creato quando un'attività viene creata con tutte le dimensioni di determinazione dei prezzi necessarie. Il ruolo e le unità organizzative sono le dimensioni di determinazione dei prezzi | Contratto di progetto | Ore        |                                                                                   |
|     | Il record di riga di stima per visualizzare il valore di costo dell'attività viene creato quando un'attività viene creata con tutte le dimensioni di determinazione dei prezzi necessarie. Tutti i campi di tipo non money vengono copiati dal sistema dalla riga di stima di vendita nella riga di stima di costo. Il ruolo e l'unità organizzativa sono le dimensioni di determinazione dei prezzi per i tassi di costo e di fatturazione.                                                                                                                                                                                                                | Costo             | Ore           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalizzare le entità Dettagli riga di offerta e Dettagli voce di contratto

Se hai aggiunto un campo personalizzato per il dettaglio di riga di offerta e vuoi che il sistema immetta il valore del campo come valore predefinito nella riga dei costi correlata che crea, utilizza gli strumenti di registrazione del plug-in **PreOperationContractLineDetailUpdate** e **PreOperationQuoteLineDetailUpdate**. Questi plug-in devono essere registrati dopo la modifica del dettaglio di riga di offerta o del dettaglio di voce di contratto. Segui i passaggi seguenti per completare il processo:

1. Apri PluginRegistrationTool e connettiti all'istanza online.
2. Seleziona **Cerca** e cerca il plug-in da aggiornare.
3. Seleziona il plug-in e quindi, nella pagina principale, fai clic su **Seleziona**.
4. Seleziona il passaggio del plug-in da aggiornare, fai clic con il pulsante destro del mouse e quindi scegli **Aggiorna**.
5. Nella finestra di dialogo **Aggiorna passaggio esistente**, nel campo **Attributi filtro**, seleziona il pulsante con i puntini di sospensione (**...**):
6. Nella finestra di dialogo **Seleziona attributi**, seleziona le caselle di controllo relative agli attributi personalizzati.
7. Seleziona **OK** per chiudere la finestra di dialogo e quindi seleziona **Aggiorna passaggio**.
8. Ripeti i passaggi da 1 a 7 per il secondo plug-in.
9. Chiudi **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
