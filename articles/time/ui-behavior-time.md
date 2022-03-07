---
title: Comportamento dell'interfaccia utente per l'inserimento ore
description: In questo argomento vengono fornite informazioni sul comportamento dell'interfaccia utente per l'inserimento ore.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ef99f220e9ff207a7620a900aa0630e2803f4f7261eccfbf73ed79717648bf92
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999456"
---
# <a name="time-entry-ui-behavior"></a>Comportamento dell'interfaccia utente per l'inserimento ore

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


La griglia **Inserimento ore settimanale** è un controllo personalizzato con due sezioni principali, **Dimensioni** e **Durata**.

## <a name="keyboard-shortcuts"></a>Scelte rapide da tastiera
| Azione        | Collegamento                  |
|------------   |------------------------   |
| Nuovo elemento           | ALT + MAIUSC + N           |
| Copia riga      | ALT + MAIUSC + C           |
| Modifica inserimento    | ALT + MAIUSC + E           |
| Modifica riga      | ALT + MAIUSC + CTROL + E    |
| Apri inserimento    | ALT + MAIUSC + O           |
| Invio        | ALT + MAIUSC + S           |
| Richiamo        | ALT + MAIUSC + R           |
| CANC        | ALT + MAIUSC + D           |
| Copia settimana     | ALT + MAIUSC + W           |

## <a name="dimensions"></a>Dimensioni
La sezione **Dimensioni** visualizza le dimensioni per le quali è possibile inserire le ore. Le seguenti dimensioni sono supportate per impostazione predefinita:

  - Project
  - Attività di progetto
  - Ruolo
  - Tipo
  - Stato inserimento

La sezione **Dimensioni** non consente la modifica in linea. Questa sezione è supportata da una vista che consente l'aggiunta di campi personalizzati alla griglia di inserimento ore settimanale.

## <a name="duration"></a>Durata
La sezione Durata visualizza i giorni della settimana come intestazioni di colonna. Questa sezione consente la modifica in linea. Dopo la creazione di una riga di inserimento ore con le dimensioni appropriate, gli utenti possono immettere rapidamente la quantità di tempo dedicata a queste dimensioni.

## <a name="create-a-new-time-entry"></a>Creare un nuovo inserimento ore

1. Nella griglia di inserimento ore seleziona **Nuovo**. 
2. Nella finestra di dialogo **Creazione rapida inserimento ore**, seleziona la data di inserimento ore.
3. Immetti i dati per le dimensioni **Progetto**, **Attività di progetto**, **Ruolo** e **Durata**. Queste informazioni dovrebbero essere aggiunte in minuti, ore o giorni digitando **h**, **m** o **g** insieme al numero. 
4. Immetti una descrizione per l'inserimento ed eventuali commenti condivisibili all'esterno relativi all'inserimento ore. 

Quando salvi l'inserimento, i valori immessi vengono visualizzati nella sezione **Dimensioni**. Le informazioni immesse nel campo **Durata** sono visualizzate con la data di creazione dell'inserimento ore.

I campi di ricerca sono supportati da viste di sistema. Ad esempio, dopo che un utente immette un progetto, per impostazione predefinita il campo **Attività di progetto** viene impostato sulla vista **Copia**. Per creare inserimenti ore per le attività non assegnate a un utente, seleziona **Cambia vista** nella finestra di dialogo di ricerca e quindi seleziona la vista **Tutte le attività di progetto attive**.

## <a name="edit-a-time-entry"></a>Modificare un inserimento ore 
I dettagli di alcuni campi nella pagina dell'inserimento ore, ad esempio **Descrizione** e **Commenti esterni**, non sono visualizzati nella griglia di inserimento ore settimanale. Viene invece visualizzato un piccolo indicatore triangolare nelle celle **Durata** che hanno questi dettagli aggiuntivi. 

1. Per modificare un inserimento ore, seleziona la cella da aggiornare nell'inserimento ore.
2. Seleziona **Modifica dettagli** per aggiornare i dati nel riquadro **Modulo principale inserimento ore**. 

## <a name="copy-a-time-entry-row"></a>Copiare una riga di inserimento ore
Dopo la creazione della riga, puoi selezionare **Copia riga** per copiare l'intera riga in una nuova riga. Quando una riga viene copiata in questo modo, vengono copiate anche dimensioni e durate. Puoi inoltre selezionare **Modifica riga** per aggiornare le durate e i valori delle dimensioni nella sezione **Durata**.

## <a name="open-a-time-entry-behavior"></a>Comportamento dell'apertura di un inserimento ore
Per supportare un inserimento ottimale e rapido nei campi più importanti, la griglia di inserimento ore settimanale visualizza un sottoinsieme delle dimensioni e delle durate selezionate. Per visualizzare tutti i dettagli di un singolo inserimento ore, sotto **Modifica inserimento**, seleziona **Apri**.

## <a name="submit-a-time-entry"></a>Inviare un inserimento ore
Puoi inviare un singolo inserimento ore o un gruppo di inserimenti ore selezionando un blocco di celle o un'intera riga di inserimento ore e quindi selezionando **Invia**. Gli inserimenti ore inviati sono visualizzati come inserimenti in attesa di approvazione nella pagina **Approvazione** dei responsabili approvazione. Dopo che gli inserimenti ore sono stati inviati, non possono essere modificati.

## <a name="recall-a-time-entry"></a>Richiamare un inserimento ore
Puoi richiamare inserimenti ore inviati. Puoi richiamare un singolo inserimento ore, un blocco di inserimenti ore o un'intera riga di inserimenti ore. È possibile modificare gli inserimenti ore richiamati.

## <a name="time-entry-status"></a>Stato dell'inserimento ore

- **Bozza**: ai nuovi inserimenti ore viene automaticamente assegnato lo stato **Bozza**. Solo gli inserimenti ore il cui stato è **Bozza** possono essere eliminati.
- **Inviato**: quando un inserimento ore viene inviato, lo stato diventa **Inviato**. 
- **Approvato**: quando un inserimento ore inviato viene approvato, lo stato diventa **Approvato**. 
- **Restituito**: se un inserimento ore viene rifiutato, lo stato diventa **Restituito** e l'inserimento diventa disponibile per la correzione e un nuovo invio. 

## <a name="view-rejection-comments"></a>Visualizzare i commenti sul rifiuto
Quando un inserimento ore viene rifiutato da un responsabile approvazione, quest'ultimo può aggiungere dei commenti per consentire alla risorsa di comprendere il motivo del rifiuto. Per visualizzare i commenti sul rifiuto per un inserimento ore, seleziona **Apri inserimento**. I commenti sul rifiuto saranno visualizzati nella sequenza temporale. L'utente può rispondere ai commenti sul rifiuto prima di inviare nuovamente l'inserimento.

## <a name="copy-week"></a>Copia settimana
Dopo che sono stati creati alcuni inserimenti ore, gli utenti possono creare più inserimenti ore contemporaneamente.

1. Nel modulo **Inserimenti ore**, seleziona **Copia settimana** per creare in blocco altri inserimenti ore. 
2. Nella finestra di dialogo **Copia**, nella sezione **Dal periodo**, utilizza i campi **Data di inizio** e **Data di fine** per definire l'intervallo di date da cui copiare gli inserimenti ore. 
3. Nella sezione **Al periodo**, nel campo **Data di inizio**, specifica la data a partire dalla quale creare gli inserimenti ore. 
4. Seleziona **Copia**. Per la data specificata in **Al periodo**, viene creata una copia degli inserimenti ore per il giorno della settimana corrispondente in **Dal periodo**. Ad esempio, l'inserimento ore di lunedì dell'ultima settimana viene copiato nel lunedì della settimana specificata come **Al periodo**.

## <a name="import"></a>Importazione
Lo stesso processo di base viene utilizzato per eseguire importazioni di prenotazioni, assegnazioni e scambi. Puoi specificare l'intervallo di date da cui sono importate le prenotazioni e quindi selezionare in modo esplicito le prenotazioni che devono essere copiate negli inserimenti ore in bozza. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
