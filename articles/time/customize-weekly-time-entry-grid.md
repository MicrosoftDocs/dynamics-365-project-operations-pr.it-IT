---
title: Estensione degli inserimenti ore
description: In questo articolo vengono fornite informazioni su come gli sviluppatori possono estendere il controllo dell'inserimento ore.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914775"
---
# <a name="extending-time-entries"></a>Estensione degli inserimenti ore

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations include un controllo personalizzato di inserimento ore estendibile. Questo controllo include le seguenti funzionalità:

- Immissione delle ore in orizzontale su una settimana
- Totali per giorno, riga o settimana
- Copia di righe o settimane
- Inserimento ore tramite HH: mm o HH.hh (converte automaticamente in HH.hh)
- Importazione da assegnazioni, prenotazioni o appuntamenti

Gli inserimenti ore possono essere estesi in due aree:
- [Aggiungere inserimenti ore personalizzati per uso personale](#add)
- [Personalizzare il controllo Inserimento ore settimanale](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Aggiungere inserimenti ore personalizzati per uso personale

Gli inserimenti ore sono un'entità di base utilizzata in più scenari. Nel primo ciclo di aprile 2020, è stata introdotta la soluzione di base TESA. TESA fornisce un'entità **Impostazioni** e un nuovo ruolo di sicurezza **Utente inserimento ore**. Sono anche stati introdotti i nuovi campi, **msdyn_start** e **msdyn_end** che hanno una relazione diretta con **msdyn_duration**. La nuova entità, il nuovo ruolo di sicurezza e i nuovi campi consentono un approccio più unificato al tempo su più prodotti.


### <a name="time-source-entity"></a>Entità origine ora
| Campo | Descrizione | 
|-------|------------|
| Nome  | Il nome della voce Origine ora utilizzata come valore di selezione durante la creazione degli inserimenti ore. |
| Origine ora predefinita [Origine ora: isdefault] | Per impostazione predefinita, è possibile contrassegnare una sola origine dell'ora predefinita. Ciò consente alle voci di selezionare come impostazione predefinita un'origine ora se non è specificata. |
|Tipo di origine ora [Origine ora: tipo di origine] | Il tipo di origine è un'opzione (Tipo di origine inserimento ore) che consente l'associazione dell'origine ora a un'app. Microsoft riserva valori maggiori di 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Inserimenti ore e Entità origine ora
Ogni inserimento ore è associato a un record origine ora. Questo record determina quali applicazioni devono elaborare l'inserimento ore e come.

Gli inserimenti ore sono sempre un blocco di tempo contiguo con l'inizio, la fine e la durata collegati.

La logica aggiornerà automaticamente il record di inserimenti ore nelle seguenti situazioni:

- Se vengono forniti due dei tre campi seguenti, il terzo viene calcolato automaticamente: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- I campi **msdyn_start** e **msdyn_end** sono sensibili al fuso orario.
- Gli inserimenti ore creati solo con **msdyn_date** e **msdyn_duration** specificati inizieranno a mezzanotte. I campi **msdyn_start** e **msdyn_end** vengono aggiornati di conseguenza.

#### <a name="time-entry-types"></a>Tipo di inserimento ore

I record di inserimento ore hanno un tipo associato che definisce il comportamento nel flusso di invio per l'applicazione associata.

|Etichetta | valore|
|-----|-----|
|In pausa   |192,355,000|
|Viaggi | 192,355,001|
|Straordinario   | 192,354,320|
|Lavoro   | 192,350,000|
|Assenza    | 192,350,001|
|Vacanza   | 192,350,002|


## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Personalizzare il controllo Inserimento ore settimanale
Gli sviluppatori possono aggiungere ulteriori campi e ricerche ad altre entità e implementare regole di business personalizzate per supportare i loro scenari di business.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Aggiungere campi personalizzati con campi di ricerca ad altre entità
Per aggiungere un campo personalizzato alla griglia di inserimento ore settimanale, devi completare tre passaggi principali:

1. Aggiungi il campo personalizzato alla finestra di dialogo **Creazione rapida**.
2. Configurare la griglia per visualizzare il campo personalizzato.
3. Aggiungi il campo personalizzato alla pagina **Modifica riga** o **Modifica inserimento ore**, a seconda dei casi.

Assicurati che il nuovo campo comporti le convalide necessarie nella pagina **Modifica riga** o **Modifica inserimento ore**. Come parte di questa attività, blocca il campo in base allo stato dell'inserimento ore.

Quando aggiungi un campo personalizzato alla griglia **Inserimento ore** e quindi crei gli inserimenti ore direttamente nella griglia, il campo personalizzato per tali inserimenti viene impostato automaticamente in modo che corrisponda alla riga. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Aggiungere il campo personalizzato alla finestra di dialogo Creazione rapida
Aggiungi il campo personalizzato alla finestra di dialogo **Creazione rapida: Crea inserimento ore** Gli utenti possono quindi immettere un valore quando aggiungono inserimenti ore selezionando **Nuovo**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurare la griglia per visualizzare il campo personalizzato
Esistono due modi di aggiungere un campo personalizzato alla griglia **inserimento ore settimanale**.

- Personalizza la visualizzazione **Inserimenti ore personali settimanali** e aggiungi il campo alla stessa. Puoi specificare la posizione e le dimensioni del campo personalizzato nella griglia modificando le proprietà nella vista.
- Crea una nuova vista di inserimenti ore personalizzata e impostala come vista predefinita. Questa vista contiene i campi **Descrizione** e **Commenti esterne**, nonché le colonne che desideri includere nella griglia. Puoi specificare la posizione, le dimensioni e l'ordine predefinito della griglia modificando le proprietà nella vista. Successivamente, configura il controllo personalizzato per questa vista di modo che sia un controllo **Griglia inserimento ore**. Aggiungi il controllo alla vista e selezionalo per **Web**, **Telefono**, e **Tablet**. Quindi, configura i parametri per la griglia **inserimento ore settimanale**. Imposta il campo **Data di inizio** su **msdyn\_date**, imposta il campo **Durata** su **msdyn\_duration**, e imposta il campo **Stato** su **msdyn\_entrystatus**. Il campo **Elenco stato di sola lettura** è impostato su **192350002 (Approvato)**, **192350003 (Inviato)**, o **192350004 (Richiamata richiesta)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Aggiungere il campo personalizzato alla pagina di modifica appropriata
Le pagine utilizzate per modificare un inserimento ore o una riga di inserimento ore si trovano in **Moduli**. Il pulsante **Modifica inserimento** nella griglia apre la pagina **Modifica inserimento** e il pulsante **Modifica riga** apre la pagina **Modifica riga**. Puoi modificare queste pagine in modo che includano i campi personalizzati.

Entrambe le opzioni rimuovono alcune opzioni di filtro predefinite nelle entità **Progetto** e **Attività di progetto** di modo che tutte le viste di ricerca per le entità siano visibili. Per impostazione predefinita, solo le viste di ricerca pertinenti sono visibili.

Devi determinare la pagina appropriata per il campo personalizzato. Molto probabilmente, se hai aggiunto il campo alla griglia, deve essere integrato nella pagina **Modifica riga** utilizzato per i campi applicati all'intera riga di inserimenti ore. Se il campo personalizzato ha un valore univoco nella riga ogni giorno (ad esempio, se è un campo personalizzato per l'ora di fine), deve andare nella pagina **Modifica inserimento ore**.

Per aggiungere il campo personalizzato a una pagina, trascina un elemento **Campo** nella posizione appropriata sulla pagina e quindi imposta le relative proprietà.

### <a name="add-new-option-set-values"></a>Aggiungere nuovi valori di set di opzioni
Per aggiungere valori di set di opzioni a un campo predefinito, attieniti alla seguente procedura.

1. Apri la pagina di modifica per il campo, quindi in **Tipo**, seleziona **Modifica** accanto al set di opzioni.
2. Aggiungi una nuova opzione che ha un'etichetta e un colore personalizzati. Se intendi aggiungere un nuovo stato di inserimento ore, il campo predefinito è denominato **Stato inserimento**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designare un nuovo stato di inserimento ore come di sola lettura
Per designare un nuovo stato di inserimento ore come di sola lettura, aggiungi un nuovo valore di inserimento ore alla proprietà **Elenco stato di sola lettura**. Assicurati di aggiungere il numero, non l'etichetta. La parte modificabile della griglia di inserimento ore viene ora bloccata per le righe che hanno un nuovo stato. Per impostare la proprietà **Elenco stato di sola lettura** in modo diverso per una vista **Inserimento ore** diversa, aggiungi la griglia **Inserimento ore** in una sezione **Controlli personalizzati** e configura i parametri in modo appropriato.

Successivamente, aggiungi regole di business per bloccare tutti i campi nelle pagine **Modifica riga** e **Modifica inserimento ore**. Per accedere alle regole di business per queste pagine, apri l'editor di moduli per ogni pagina e quindi seleziona **Regole di business**. Puoi aggiungere il nuovo stato alla condizione nelle regole di business esistenti, oppure aggiungere una nuova regola di business per il nuovo stato.

### <a name="add-custom-validation-rules"></a>Aggiungere regole di convalida personalizzate
È possibile aggiungere due tipi di regole di convalida per l'esperienza griglia **Inserimento ore settimanale**:

- Regole aziendali lato client che funzionano sulle pagine
- Convalide dei plug-in lato server che si applicano a tutti gli aggiornamenti di inserimento ore

#### <a name="client-side-business-rules"></a>Regole aziendali lato client
Utilizza le regole di business per bloccare e sbloccare campi, immettere valori predefiniti nei campi e definire convalide che richiedono informazioni solo del record di inserimento ore corrente. Per accedere alle regole di business per una pagina, apri l'editor di moduli e quindi seleziona **Regole di business**. Puoi quindi modificare le regole di business esistenti o aggiungere una nuova regola di business.

#### <a name="server-side-plug-in-validations"></a>Convalide dei plug-in lato server
Dovresti utilizzare convalide di plug-in per qualsiasi convalida che richiede più contesto di quello disponibile in un singolo record di inserimento ore. Devi usarli per qualsiasi convalida che desideri eseguire su aggiornamenti inline nella griglia. Per completare le convalide, crea un plug-in personalizzato nell'entità **Inserimento ore**.

### <a name="limits"></a>Limiti
Attualmente, la griglia **Inserimento ore** ha un limite di dimensione di 500 righe. Se sono presenti più di 500 righe, le righe in eccesso non verranno visualizzate. Non c'è modo di aumentare questo limite di dimensioni.

### <a name="copying-time-entries"></a>Copia di inserimenti ore
Usa la vista **Copia colonne inserimenti ore** per definire l'elenco dei campi da copiare durante l'inserimento ore. I campi **Data** e **Durata** sono obbligatori e non devono essere rimossi dalla visualizzazione.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
