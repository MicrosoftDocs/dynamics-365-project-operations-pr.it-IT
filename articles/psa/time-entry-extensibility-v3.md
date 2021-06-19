---
title: Personalizzare un inserimento ore settimanale
description: In questo argomento vengono fornite informazioni su come implementare regole di business personalizzate che supportano le pratiche dell'organizzazione.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
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
ms.openlocfilehash: c117e06e7a5c57c7f9b70d1380f450c0ea97cd12
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013041"
---
# <a name="customize-weekly-time-entry"></a>Personalizzare l'inserimento ore settimanale 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In Microsoft Dynamics 365 Project Service Automation versione 3.3, Microsoft ha introdotto una griglia moderna che consente alle risorse di progetto di immettere rapidamente il tempo fino a una settimana alla volta. La nuova griglia di inserimento ore settimanale può visualizzare i totali degli inserimenti per data, riga o settimana. Le risorse possono eseguire copie degli inserimenti ore settimanali nonché effettuare una copia in blocco delle settimane precedenti. Gli addetti alla personalizzazione del sistema possono personalizzare la vista aggiungendo campi, campi di ricerca ad altre entità e implementare regole di business personalizzate per supportare le pratiche dell'organizzazione.

L'inserimento ore e la nuova griglia di inserimento ore settimanale sono accessibili tramite la mappa del sito. L'esperienza di inserimento ore personalizzata non estendibile delle versioni precedenti di PSA è stata sostituita dalla griglia di inserimento ore settimanale estendibile nonché da un'esperienza alternativa nella griglia e nel calendario di sola lettura. A seguito di questa modifica, gli utenti possono immettere il tempo in quantità settimanali.

## <a name="page-layout"></a>Layout della pagina
La nuova griglia di inserimento ore settimanale è un controllo personalizzato con una barra degli strumenti e due sezioni principali, **Dimensioni** e **Durata**. La barra degli strumenti include un pulsante applicabile solo a questo controllo personalizzato per la griglia di inserimento ore. I pulsanti nel riquadro azioni nella parte superiore della pagina si applicano invece a tre tipi di controlli supportati per l'inserimento ore: il controllo di inserimento ore settimanale, il controllo di sola lettura e il controllo del calendario.

### <a name="dimensions"></a>Dimensioni
La sezione **Dimensioni** visualizza, come le intestazioni delle colonne, tutte le dimensioni per le quali è possibile inserire le ore. Le seguenti dimensioni sono supportate per impostazione predefinita:

- Progetto
- Attività di progetto
- Ruolo
- Tipo
- Stato inserimento

La sezione **Dimensioni** non consente la modifica in linea. Questa sezione è supportata da una vista che consente l'aggiunta di campi personalizzati alla griglia di inserimento ore settimanale. Per informazioni su come aggiungere campi personalizzati, vedi la sezione "Estendibilità" più avanti in questo argomento.

### <a name="duration"></a>Durata
La sezione Durata visualizza i giorni della settimana come intestazioni di colonna. Questa sezione consente la modifica in linea. Dopo la creazione di una riga di inserimento ore con le dimensioni appropriate, gli utenti possono immettere rapidamente, in linea, la quantità di tempo dedicata a queste dimensioni.

## <a name="create-a-new-time-entry"></a>Creare un nuovo inserimento ore
Per creare un nuovo inserimento ore nella griglia di inserimento ore, seleziona **Nuovo**. Nella finestra di dialogo **Creazione rapida inserimento ore**. Nella finestra di dialogo, gli utenti possono selezionare la data dell'inserimento ore e quindi immettere dati per le dimensioni **Progetto**, **Attività di progetto**, **Ruolo** e **Durata** in minuti, ore, giorni digitando **h**, **m** o **d** insieme al numero. Gli utenti possono anche immettere una descrizione e commenti condivisibili per l'inserimento ore. Quando gli utenti salvano le modifiche, i valori che hanno immesso per le dimensioni sono visualizzati nella sezione **Dimensioni**. Le informazioni sulla durata immesse nel campo **Durata** sono visualizzate con la data di creazione dell'inserimento ore.

I campi di ricerca sono supportati da viste di sistema. Ad esempio, dopo che un utente immette un progetto, per impostazione predefinita il campo **Attività di progetto** viene impostato sulla vista **Copia**. Per creare inserimenti ore per le attività non assegnate a un utente, seleziona **Cambia vista** nella finestra di dialogo di ricerca e quindi seleziona la vista **Tutte le attività di progetto attive**.

## <a name="edit-a-time-entry"></a>Modificare un inserimento ore
I dettagli di alcuni campi nella pagina dell'inserimento ore, ad esempio **Descrizione** e **Commenti esterni**, non sono visualizzati nella griglia di inserimento ore settimanale. Viene invece visualizzato un piccolo indicatore triangolare nelle celle della durata che hanno questi dettagli aggiuntivi. Seleziona la cella e quindi seleziona **Modifica dettagli** per visualizzare i dati nel riquadro **Modifica rapida**. Per modificare o aggiornare i dettagli di uno specifico inserimento ore che non fa parte della griglia di inserimento ore settimanali, gli utenti devono aprire il riquadro **Modifica rapida**.

## <a name="copy-a-time-entry-row"></a>Copiare una riga di inserimento ore
Dopo la creazione della prima riga di inserimento ore, gli utenti possono selezionare **Copia riga** per copiare l'intera riga in una nuova riga. Quando una riga viene copiata in questo modo, vengono copiate anche dimensioni e durate. Gli utenti possono inoltre selezionare **Modifica riga** per aggiornare in linea le durate e i valori delle dimensioni nella sezione **Durata**.

## <a name="open-a-time-entry"></a>Aprire un inserimento ore
Per supportare un inserimento ottimale e rapido nei campi più importanti, la griglia di inserimento ore settimanale visualizza un sottoinsieme delle dimensioni e delle durate selezionate. Per visualizzare tutti i dettagli di un singolo inserimento ore, sotto **Modifica inserimento**, seleziona **Apri**.

## <a name="submit-a-time-entry"></a>Inviare un inserimento ore
Gli utenti possono inviare un singolo inserimento ore o un gruppo di inserimenti ore selezionando un blocco di celle o un'intera riga di inserimento ore e quindi selezionando **Invia**. Gli inserimenti ore inviati sono visualizzati come inserimenti in attesa di approvazione nella pagina **Approvazione** dei responsabili approvazione. Dopo che gli inserimenti ore sono stati inviati, non possono essere modificati.

## <a name="recall-a-time-entry"></a>Richiamare un inserimento ore
Puoi richiamare inserimenti ore inviati. Puoi richiamare un singolo inserimento ore, un blocco di inserimenti ore o un'intera riga di inserimenti ore. Gli inserimenti ore richiamati sono disponibili per la modifica da parte delle risorse.

## <a name="time-entry-status"></a>Stato dell'inserimento ore
Ai nuovi inserimenti ore viene automaticamente assegnato lo stato **Bozza**. Quando un inserimento ore viene inviato, lo stato diventa **Inviato**. Quando un inserimento ore inviato viene approvato, lo stato diventa **Approvato**. Se un inserimento ore viene rifiutato, lo stato diventa **Restituito** e l'inserimento diventa disponibile per la correzione e un nuovo invio. Solo gli inserimenti ore il cui stato è **Bozza** possono essere eliminati.

## <a name="view-rejection-comments"></a>Visualizzare i commenti sul rifiuto
Quando un inserimento ore viene rifiutato da un responsabile approvazione, quest'ultimo aggiunge commenti sul rifiuto per consentire alla risorsa di comprendere il motivo del rifiuto. Per visualizzare i commenti sul rifiuto per un inserimento ore, seleziona **Apri inserimento**. I commenti sul rifiuto saranno visualizzati nella sequenza temporale. Nella sequenza temporale, la risorsa può rispondere ai commenti sul rifiuto prima di inviare di nuovo l'inserimento.

## <a name="copy-week"></a>Copiare una settimana
Dopo la creazione di alcuni inserimenti ore, gli utenti possono selezionare **Copia settimana** per creare ulteriori inserimenti ore in blocco. Viene visualizzata la finestra di dialogo **Copia**. Nella sezione **Da periodo**, utilizza i campi **Data di fine** e **Data di inizio** per definire un intervallo di date dal quale copiare gli inserimenti ore. Nella sezione **Al periodo**, nel campo **Data di inizio**, specifica la data a partire dalla quale creare gli inserimenti ore. Quindi seleziona **Copia**. Per la data specificata nel periodo "a", viene creata una copia di sistema degli inserimenti ore per giorno della settimana corrispondente nel periodo "da". Ad esempio, l'inserimento ore di lunedì dell'ultima settimana viene copiato nel lunedì della settimana specificata come periodo "a".

## <a name="import"></a>Importazione
Lo stesso processo di base viene utilizzato per eseguire importazioni di prenotazioni, assegnazioni e scambi. Gli utenti possono specificare l'intervallo di date da cui vengono importate le prenotazioni. Devono quindi selezionare in modo esplicito le prenotazioni che devono essere copiate nelle bozze degli inserimenti ore. Nella versione precedente, gli inserimenti ore suggeriti erano visualizzati nella griglia e nel calendario e andavano persi all'aggiornamento della sessione.

## <a name="extensibility"></a>Estendibilità 
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Aggiungere campi personalizzati che hanno campi di ricerca ad altre entità
Per aggiungere un campo personalizzato alla griglia di inserimento ore settimanale, devi completare tre passaggi principali:

1.  Aggiungere il campo personalizzato alla finestra di dialogo di creazione rapida.
2.  Configurare la griglia per visualizzare il campo personalizzato.
3.  Aggiungere il campo personalizzato al flusso di attività di modifica delle righe o al flusso di attività di modifica di celle, come appropriato.

Devi inoltre assicurarti che il nuovo campo comporti le convalide necessarie nel flusso di attività di modifica di celle o righe. Come parte di questo passaggio, devi bloccare il campo in base allo stato dell'inserimento ore.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Aggiungere il campo personalizzato alla finestra di dialogo di creazione rapida
Devi aggiungere il campo personalizzato alla finestra di dialogo di creazione rapida Crea inserimento ore di modo che gli utenti possano immettere un valore per lo stesso quando aggiungono Inserimenti ore tramite il pulsante **Nuovo**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurare la griglia per visualizzare il campo personalizzato
Esistono due modi di aggiungere un campo personalizzato alla griglia di inserimento ore settimanale. La prima opzione è personalizzare la vista **Inserimenti ore personali settimanali** e aggiungere il campo alla stessa. Puoi scegliere la posizione e le dimensioni del campo personalizzato nella griglia modificando tali proprietà nella vista.

La seconda opzione è creare una nuova vista di inserimenti ore personalizzata e impostarla come vista predefinita. Questa vista contiene i campi **Descrizione** e **Commenti esterne**, nonché le colonne che desideri avere nella griglia. Puoi scegliere la posizione, le dimensioni e l'ordine predefinito della griglia modificando tali proprietà nella vista. Successivamente, configura il controllo personalizzato per questa vista di modo che sia un controllo **Griglia inserimento ore**. Aggiungi questo controllo alla vista e selezionalo per Web, telefono e tablet. Quindi, configura i parametri per la griglia di inserimento ore settimanale. Imposta il campo **Data di inizio** su **msdyn_date**, imposta il campo **Durata** su **msdyn_duration** e imposta il campo **Stato** su **msdyn_entrystatus**. Per la vista predefinita, il campo **Elenco stato di sola lettura** è impostato su **192350002,192350003,192350004**, il campo **Flusso di attività modifica riga** è impostato su **msdyn_timeentryrowedit** e il campo **Flusso di attività modifica cella** è impostato su **msdyn_timeentryedit**. Puoi personalizzare questi campi per aggiungere o rimuovere lo stato di sola lettura o per utilizzare una differente esperienza basata su attività (TBX) per la modifica di celle o righe. Questi campi devono essere limitati a un valore statico.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Aggiungere il campo personalizzato al flusso di attività di modifica appropriato
Le pagine TBX utilizzate per la modifica si trovano in **Processi**. Le pagine predefinite sono **Project Service - Modifica riga inserimento ore** e **Project Service - Modifica inserimento ore**. Puoi modificare queste pagine predefinite o creare nuove pagine TBX personalizzate.

> [!NOTE] 
> Entrambe le opzioni rimuoveranno alcune opzioni di filtro predefinite nelle entità **Progetto** e **Attività di progetto** di modo che tutte le viste di ricerca per le entità siano visibili. Per impostazione predefinita, solo le viste di ricerca pertinenti sono visibili.

Devi determinare il flusso di attività appropriato per il campo personalizzato. Molto probabilmente, se hai aggiunto il campo alla griglia, deve essere integrato nel flusso di attività di modifica di righe utilizzato per i campi applicati all'intera riga di inserimenti ore. Se il campo personalizzato ha un valore univoco ogni giorno, ad esempio un campo personalizzato per **Ora di fine**, deve essere integrato nel flusso di attività di modifica di celle.

Per aggiungere il campo personalizzato a un flusso di attività, trascina un elemento **Campo** nella posizione appropriata sulla pagina e quindi imposta le relative proprietà. Imposta la proprietà **Origine** su **Inserimento ore** e imposta la proprietà **Campo dati** sul campo personalizzato. La proprietà **Campo** specifica il nome visualizzato nella pagina TBX. Seleziona **Applica** per salvare le modifiche a questo campo. Seleziona quindi **Aggiorna** per salvare le modifiche alla pagina.

Per utilizzare una nuova pagina TBX personalizzata, crea un nuovo processo. Imposta la categoria su **Processo aziendale**, imposta l'entità su **Inserimento ore** e imposta il tipo di processo aziendale su **Esegui processo come flusso di attività**. In **Proprietà**, la proprietà **Nome pagina** deve essere impostata sul nome visualizzato per la pagina. Aggiungi tutti i campi pertinenti alla pagina TBX. Salva e attiva il processo, quindi aggiorna la proprietà di controllo personalizzata per il flusso di attività pertinente al valore **Nome** del processo.

### <a name="add-new-option-set-values"></a>Aggiungere nuovi valori di set di opzioni
Per aggiungere valori di set di opzioni a un campo predefinito, apri la pagina di modifica per il campo, quindi in **Tipo**, seleziona **Modifica** accanto al set di opzioni. Successivamente, aggiungi una nuova opzione che ha un'etichetta e un colore personalizzati. Se intendi aggiungere un nuovo stato di inserimento ore, il campo predefinito è denominato **Stato inserimento**, non **Stato**

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designare un nuovo stato di inserimento ore come di sola lettura
Per designare un nuovo stato di inserimento ore come di sola lettura, aggiungi un nuovo valore di inserimento ore (il numero, non l'etichetta) alla proprietà. **Elenco stato di sola lettura**. La parte modificabile della griglia di inserimento ore viene bloccata per le righe che hanno un nuovo stato.
Successivamente, aggiungi regole di business per bloccare tutti i campi nelle pagine TBX **Modifica riga inserimento ore** e **Modifica inserimento ore**. Puoi accedere alle regole di business per queste pagine aprendo l'editor di processi aziendali della pagina e quindi selezionando **Regole di business**. Puoi aggiungere il nuovo stato alla condizione nelle regole di business esistenti, oppure aggiungere una nuova regola di business per il nuovo stato.

### <a name="add-custom-validation-rules"></a>Aggiungere regole di convalida personalizzate
Esistono due tipi di regole di convalida che puoi aggiungere per l'esperienza relativa alla griglia di inserimento ore settimanale: •   Le regole di business sul lato client utilizzate nelle finestre di dialogo di creazione rapida e nelle pagine TBX •   Le convalide di plug-in sul lato server applicabili a tutti gli aggiornamenti dell'inserimento ore

#### <a name="business-rules"></a>Regole di business.
Utilizza le regole di business per bloccare e sbloccare campi, immettere valori predefiniti nei campi e definire convalide che richiedono informazioni solo del record di inserimento ore corrente. Puoi accedere alle regole di business per una pagina TBX aprendo l'editor del flusso di processi aziendali della pagina e quindi selezionando **Regole di business**. Puoi quindi modificare le regole di business esistenti o aggiungere una nuova regola di business. Per convalide ancora più personalizzate, puoi utilizzare una regola di business per eseguire JavaScript.

#### <a name="plug-in-validations"></a>Convalide di plug-in
Dovresti utilizzare convalide di plug-in per qualsiasi convalida che richiede più contesto di quello disponibile in un singolo record di inserimento ore oppure per qualsiasi convalida che desideri eseguire su aggiornamenti in linea nella griglia. Per completare la convalida, crea un plug-in personalizzato nell'entità **Inserimento ore**.

> [!IMPORTANT] 
> Attualmente, un problema noto nelle pagine TBX impedisce agli utenti di correggere le informazioni e di selezionare di nuovo Fatto quando l'aggiornamento di una convalida di plug-in non riesce. Come soluzione alternativa, imposta convalide di regole di business per evitare questa situazione il più possibile.


[!INCLUDE[footer-include](../includes/footer-banner.md)]