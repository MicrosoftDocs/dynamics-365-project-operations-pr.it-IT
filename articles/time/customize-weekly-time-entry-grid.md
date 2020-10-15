---
title: Estensione degli inserimenti ore
description: Questo argomento fornisce informazioni su come gli sviluppatori sono in grado di estendere il controllo degli inserimenti ore.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930885"
---
# <a name="extending-time-entries"></a>Estensione degli inserimenti ore

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations include un controllo personalizzato di inserimenti ore estendibile. Questo controllo include le seguenti funzionalità:

- Immissione delle ore in orizzontale su una settimana
- Totali per giorno, riga o settimana
- Copia di righe o settimane
- Inserimento ore tramite HH: mm o HH.hh (converte automaticamente in HH.hh)
- Importazione da assegnazioni, prenotazioni o appuntamenti

Gli inserimenti ore possono essere estesi in due aree:
- [Aggiungere inserimenti ore personalizzati per uso personale](#add)
- [Personalizzare il controllo Inserimento ore settimanale](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Aggiungere inserimenti ore personalizzati per uso personale.

Gli inserimenti ore sono un'entità principale progettata per essere utilizzata in più scenari. Nel primo ciclo di rilascio di aprile 2020 è stata introdotta la soluzione principale TESA, che fornisce un'entità **Impostazioni** e un nuovo ruolo di sicurezza **Utente inserimento ore**. Sono anche stati introdotti i nuovi campi, **msdyn_start** e **msdyn_end** che hanno una relazione diretta con **msdyn_duration**. La nuova entità, il nuovo ruolo di sicurezza e i nuovi campi consentono un approccio più unificato al tempo su più prodotti.


### <a name="time-source-entity"></a>Entità origine ora
| Campo | Descrizione | 
|-------|------------|
| Nome  | Il nome della voce Origine ora utilizzata come valore di selezione durante la creazione della voce di ora. |
| Origine ora predefinita [Origine ora: isdefault] | Per impostazione predefinita, è possibile contrassegnare una sola origine dell'ora nell'origine dell'ora predefinita. Questa funzionalità consente alle voci di selezionare come impostazione predefinita un'origine ora se non è specificata. |
|Tipo di origine ora [Origine ora: tipo di origine] | Il tipo di origine è un'opzione (Tipo di origine inserimento ore) che consente l'associazione dell'origine ora a un'app. Valori aggiuntivi verranno aggiunti a questo set di opzioni man mano che vengono aggiunte ulteriori applicazioni. Tieni presente che Microsoft riserva valori maggiori di 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Inserimenti ore e Entità origine ora
Ogni inserimento ore è associato a un record origine ora. Questo record determina come e quali applicazioni devono elaborare l'inserimento ore.

Gli inserimenti ore sono sempre un blocco di tempo contiguo con l'inizio, la fine e la durata collegati.

La logica aggiornerà automaticamente il record di inserimenti ore nelle seguenti situazioni:

- Se vengono forniti due dei tre campi seguenti, il terzo viene calcolato automaticamente 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- I campi **msdyn_start** e **msdyn_end** riconoscono il fuso orario.
- Gli inserimenti ore creati solo con **msdyn_date** e **msdyn_duration** specificati inizieranno a mezzanotte e **msdyn_start** e **msdyn_end** verranno aggiornati di conseguenza.

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

- Aggiungere il campo personalizzato alla finestra di dialogo di creazione rapida.
- Configurare la griglia per visualizzare il campo personalizzato.
- Aggiungi il campo personalizzato al flusso di attività di modifica delle righe o al flusso di attività di modifica di celle.

Devi inoltre assicurarti che il nuovo campo comporti le convalide necessarie nel flusso di attività di modifica di celle o righe. Come parte di questo passaggio, devi bloccare il campo in base allo stato dell'inserimento ore.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Aggiungere il campo personalizzato alla finestra di dialogo di creazione rapida
Devi aggiungere il campo personalizzato alla finestra di dialogo di creazione rapida **Crea inserimento ore**. Gli utenti possono quindi immettere un valore quando aggiungono inserimenti ore selezionando **Nuovo**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurare la griglia per visualizzare il campo personalizzato
Esistono due modi di aggiungere un campo personalizzato alla griglia di inserimento ore settimanale:

  - Personalizzare una visualizzazione e aggiungere un campo personalizzato
  - Creare un nuovo inserimento ore personalizzato predefinito 


**Personalizzare una visualizzazione e aggiungere un campo personalizzato**

Puoi personalizzare la visualizzazione **Inserimenti ore personali settimanali** e aggiungere il campo alla stessa. Puoi scegliere la posizione e le dimensioni del campo personalizzato nella griglia modificando tali proprietà nella vista.

**Creare un nuovo inserimento ore personalizzato predefinito** 

Questa vista contiene i campi **Descrizione** e **Commenti esterne**, nonché le colonne che desideri avere nella griglia. 

1. Scegli la posizione, le dimensioni e l'ordine predefinito della griglia modificando tali proprietà nella vista. 
2. Configura il controllo personalizzato per questa vista di modo che sia un controllo **Griglia inserimento ore**. 
3. Aggiungi questo controllo alla vista e selezionalo per Web, telefono e tablet. 
4. Configura i parametri per la griglia di inserimento ore settimanale. Imposta il campo **Data di inizio** su **msdyn_date**, imposta il campo **Durata** su **msdyn_duration** e imposta il campo **Stato** su **msdyn_entrystatus**. 
5. Per la vista predefinita, il campo **Elenco stato di sola lettura** è impostato su **192350002,192350003,192350004**, il campo **Flusso di attività modifica riga** è impostato su **msdyn_timeentryrowedit** e il campo **Flusso di attività modifica cella** è impostato su **msdyn_timeentryedit**. 
6. Puoi personalizzare questi campi per aggiungere o rimuovere lo stato di sola lettura o per utilizzare una differente esperienza basata su attività (TBX) per la modifica di celle o righe. Questi campi devono essere limitati a un valore statico.


> [!NOTE] 
> Entrambe le opzioni rimuoveranno alcune opzioni di filtro predefinite nelle entità **Progetto** e **Attività di progetto** di modo che tutte le viste di ricerca per le entità siano visibili. Per impostazione predefinita, solo le viste di ricerca pertinenti sono visibili.
Devi determinare il flusso di attività appropriato per il campo personalizzato. Molto probabilmente, se hai aggiunto il campo alla griglia, deve essere integrato nel flusso di attività di modifica di righe utilizzato per i campi applicati all'intera riga di inserimenti ore. Se il campo personalizzato ha un valore univoco ogni giorno, ad esempio un campo personalizzato per **Ora di fine**, deve essere integrato nel flusso di attività di modifica di celle.

Per aggiungere il campo personalizzato a un flusso di attività, trascina un elemento **Campo** nella posizione appropriata sulla pagina e quindi imposta le proprietà del campo. Imposta la proprietà **Origine** su **Inserimento ore** e imposta la proprietà **Campo dati** sul campo personalizzato. La proprietà **Campo** specifica il nome visualizzato nella pagina TBX. Seleziona **Applica** per salvare le modifiche nel campo, quindi seleziona **Aggiorna** per salvare le modifiche alla pagina.

Per utilizzare una nuova pagina TBX personalizzata, crea un nuovo processo. Imposta la categoria su **Processo aziendale**, imposta l'entità su **Inserimento ore** e imposta il tipo di processo aziendale su **Esegui processo come flusso di attività**. In **Proprietà**, la proprietà **Nome pagina** deve essere impostata sul nome visualizzato per la pagina. Aggiungi tutti i campi pertinenti alla pagina TBX. Salva e attiva il processo, quindi aggiorna la proprietà di controllo personalizzata per il flusso di attività pertinente al valore **Nome** del processo.

### <a name="add-new-option-set-values"></a>Aggiungere nuovi valori di set di opzioni
Per aggiungere valori di set di opzioni a un campo predefinito, apri la pagina di modifica per il campo, quindi in **Tipo**, seleziona **Modifica** accanto al set di opzioni. Successivamente, aggiungi una nuova opzione che ha un'etichetta e un colore personalizzati. Se intendi aggiungere un nuovo stato di inserimento ore, il campo predefinito è denominato **Stato inserimento**, non **Stato**

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designare un nuovo stato di inserimento ore come di sola lettura
Per designare un nuovo stato di inserimento ore come di sola lettura, aggiungi un nuovo valore di inserimento ore alla proprietà **Elenco stato di sola lettura**. La parte modificabile della griglia di inserimento ore viene bloccata per le righe che hanno un nuovo stato.
Successivamente, aggiungi regole di business per bloccare tutti i campi nelle pagine TBX **Modifica riga inserimento ore** e **Modifica inserimento ore**. Puoi accedere alle regole di business per queste pagine aprendo l'editor di processi aziendali della pagina e quindi selezionando **Regole di business**. Puoi aggiungere il nuovo stato alla condizione nelle regole di business esistenti, oppure aggiungere una nuova regola di business per il nuovo stato.

### <a name="add-custom-validation-rules"></a>Aggiungere regole di convalida personalizzate
Esistono due tipi di regole di convalida che è possibile aggiungere per l'esperienza della griglia di inserimento ore settimanale:

- Regole di business lato client che funzionano nelle finestre di dialogo di creazione rapida e nelle pagine TBX.
- Convalide dei plug-in lato server che si applicano a tutti gli aggiornamenti di inserimento ore.

#### <a name="business-rules"></a>Regole di business
Utilizza le regole di business per bloccare e sbloccare campi, immettere valori predefiniti nei campi e definire convalide che richiedono informazioni solo del record di inserimento ore corrente. Puoi accedere alle regole di business per una pagina TBX aprendo l'editor del flusso di processi aziendali della pagina e quindi selezionando **Regole di business**. Puoi quindi modificare le regole di business esistenti o aggiungere una nuova regola di business. Per convalide ancora più personalizzate, puoi utilizzare una regola di business per eseguire JavaScript.

#### <a name="plug-in-validations"></a>Convalide di plug-in
Dovresti utilizzare convalide di plug-in per qualsiasi convalida che richiede più contesto di quello disponibile in un singolo record di inserimento ore oppure per qualsiasi convalida che desideri eseguire su aggiornamenti in linea nella griglia. Per completare la convalida, crea un plug-in personalizzato nell'entità **Inserimento ore**.
