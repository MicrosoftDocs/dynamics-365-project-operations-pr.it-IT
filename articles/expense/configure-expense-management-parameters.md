---
title: Configurare i parametri di gestione delle spese
description: In questo articolo vengono descritti i parametri che controllano il comportamento generale nella gestione delle spese.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 6432e119f38071b028c013561bab99820778a11d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931473"
---
# <a name="configure-expense-management-parameters"></a>Configurare i parametri di gestione delle spese

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

In questo articolo vengono descritti i parametri che controllano il comportamento generale nella gestione delle spese.

## <a name="general"></a>Generali

| Campo                                                    | Descrizione |
|----------------------------------------------------------|-------------|
| Tariffa standard chilometraggio                                 | Immetti la percentuale di rimborso per le spese di indennità di trasferta. Questa percentuale viene moltiplicata per i chilometri immessi per la spesa per calcolare l'importo rimborsato per la spesa di viaggio. |
| Convalida fine della spesa                                 | Attiva questa opzione per limitare gli utenti a un set di valori esistente configurato nel campo **Scopo della nota spese** quando creano note spese. |
| Spese personali pagate da                                | Seleziona chi è responsabile del pagamento degli importi delle transazioni con carta di credito classificati come personali. |
| Visualizza intera nota spese in drill-back               | Seleziona questa opzione per visualizzare tutte le spese per una nota spese quando i dettagli del documento originale vengono visualizzati per un giustificativo specifico generato quando è stata registrata la nota spese. |
| La preautorizzazione del viaggio è obbligatoria                 | Seleziona questa opzione per richiedere che una richiesta di viaggio venga inviata e approvata prima che un dipendente possa inviare una nota spese. |
| Consenti modifica delle distribuzioni prima della registrazione            | Seleziona se le distribuzioni di una nota spese possono essere modificate prima della registrazione. |
| Valuta criteri di gestione spese                     | Seleziona quando vengono valutate le spese per determinare se i criteri di gestione spese sono stati violati. Le spese possono essere valutate per le violazioni quando la voce di spesa viene inserita e salvata o quando la spesa viene inviata per l'approvazione. Le regole dei criteri per le entrate richieste verranno valutate quando viene salvata la riga di spesa. |
| Consenti righe spese interaziendali                         | Seleziona se le spese per altre persone giuridiche possono essere inserite in una nota spese. |
| Consenti la modifica del tasso di cambio per le spese con carta di credito | Seleziona questa opzione per consentire all'utente di modificare il tasso di cambio per le spese della carta di credito importata. |
| Campi della gerarchia multilivello da visualizzare                  | Seleziona i campi del responsabile approvazione da visualizzare quando il tipo di assegnazione del flusso di lavoro è impostato su una gerarchia e la seleziona **Gerarchia** è impostata per utilizzare la gerarchia di approvazione e l'approvazione a più livelli di spesa. Quando la gerarchia di approvazione multilivello viene utilizzata per un flusso di lavoro, i campi selezionati verranno visualizzati nella nota spese e potranno essere modificati. |
| Immettere il numero di carta di credito del dipendente                        | Seleziona se è possibile inserire e salvare un numero di 15 o 16 caratteri nel campo **ID carta** sulla pagina **Carte di credito** per un dipendente. |
| Convalida fine della richiesta di viaggio                      | Attiva questa opzione per limitare gli utenti a un set di valori esistente configurato nel campo **Scopo della nota spese** quando creano le richieste di viaggio. |

## <a name="financial"></a>Commercio all'ingrosso, al dettaglio, riparazioni

| Campo                                                                                    | Descrizione |
|------------------------------------------------------------------------------------------|-------------|
| Nome giornale di registrazione contabile                                                                | Seleziona il nome del giornale di registrazione contabile in cui vengono registrate le note spese approvate. |
| Attiva recupero imposte da spese                                                        | Seleziona questa opzione per abilitare il recupero delle imposte sulle spese per le spese ammissibili. Questa opzione non può essere selezionata se sono abilitate le norme sull'imposta sulle vendite e sull'imposta sull'utilizzo degli Stati Uniti. |
| Registra anticipo contanti immediatamente                                                           | Seleziona questa opzione per registrare un anticipo in contanti approvato al termine del processo di pagamento e trasferimento. Se questa opzione non è selezionata, il processo di pagamento e trasferimento genera un giornale di registrazione generale non registrato. |
| Correggi data di registrazione durante la registrazione                                                   | Seleziona questa opzione per aggiornare la data contabile quando vengono registrate le spese, se il periodo corrente è in attesa o chiuso. La data contabile sarà fissata al successivo periodo aperto. |
| Consenti raggruppamento di transazioni in base al conto di contropartita specificato nel metodo di pagamento       | Seleziona questa opzione per riepilogare le transazioni di spesa per una nota spese, in base al conto di contropartita specificato nel metodo di pagamento per le spese. |
| Tasse incluse                                                                             | Seleziona questa opzione per includere l'IVA nell'importo della spesa per impostazione predefinita. |
| Rilascia impegni di spesa alla chiusura delle richieste di viaggio                                      | Seleziona questa opzione per sbloccare i fondi impegnati quando una richiesta di viaggio approvata viene chiusa. |
| Consenti inoltro richiesta di viaggio in caso di sovraccarico di budget per registro di budget e budget di progetto | Seleziona questa opzione per consentire ai dipendenti di inviare le richieste di viaggio per l'approvazione, anche se superano il budget consentito impostato nel registro del budget o il budget consentito per un progetto. |
| Consenti inoltro nota spese in caso di sovraccarico di budget per registro di budget e budget di progetto     | Seleziona questa opzione per consentire ai dipendenti di inviare le note spese per l'approvazione, anche se superano il budget consentito impostato nel registro del budget o il budget consentito per un progetto. |
| Consenti approvazione nota spese in caso di sovraccarico di budget solo per registro di budget                 | Seleziona questa opzione per consentire ai responsabili dell'approvazione di approvare le note spese che superano il budget consentito impostato nel registro del budget. |

## <a name="per-diem"></a>Diaria

| Campo                                 | Descrizione |
|---------------------------------------|-------------|
| Minimo ore per trasferta giornaliera            | Immetti il numero minimo predefinito di ore che un dipendente deve lavorare in un giorno per avere diritto a ricevere una diaria per le spese di viaggio. Questo valore viene utilizzato come valore predefinito solo per il campo **Minimo ore** per livelli di tariffa giornaliera. |
| Percentuale vitto                          | Immetti la percentuale predefinita della diaria per il vitto che viene utilizzata il primo e l'ultimo giorno della spesa relativa al viaggio quando il campo **Calcola riduzione per vitto per** è impostato su **Tipo di pasto al giorno** o **Numero di pasti al giorno**. La giornata lavorativa del primo e dell'ultimo giorno potrebbe essere più breve di una giornata lavorativa standard. Pertanto, l'importo della diaria in quei giorni potrebbe differire dall'importo standard. Se la percentuale è impostata su **0** (zero), le detrazioni per il primo e l'ultimo giorno saranno 0,00. |
| Percentuale hotel                         | Immetti la percentuale predefinita della diaria per gli hotel utilizzata il primo e l'ultimo giorno della spesa relativa al viaggio. La giornata lavorativa del primo e dell'ultimo giorno potrebbe essere più breve di una giornata lavorativa standard. Pertanto, l'importo della diaria in quei giorni potrebbe differire dall'importo standard. Se la percentuale è impostata su **0** (zero), le detrazioni per il primo e l'ultimo giorno saranno 0,00. |
| Altra percentuale                         | Immetti la percentuale predefinita della diaria per le spese varie utilizzata il primo e l'ultimo giorno della spesa relativa al viaggio. La giornata lavorativa del primo e dell'ultimo giorno potrebbe essere più breve di una giornata lavorativa standard. Pertanto, l'importo della diaria in quei giorni potrebbe differire dall'importo standard. Se la percentuale è impostata su **0** (zero), le detrazioni per il primo e l'ultimo giorno saranno 0,00. |
| Percentuale di riduzione per colazione | Inserisci l'importo di cui è ridotta la diaria per la colazione. Ad esempio, se un dipendente riceve una colazione gratuita, potresti voler ridurre l'importo della diaria del 10%. |
| Percentuale di riduzione per pranzo     | Inserisci l'importo di cui è ridotta la diaria per il pranzo. Ad esempio, se un dipendente riceve un pranzo gratuito, potresti voler ridurre l'importo della diaria del 15%. |
| Percentuale di riduzione per cena    | Inserisci l'importo di cui è ridotta la diaria per la cena. Ad esempio, se un dipendente riceve una cena gratuita, potresti voler ridurre l'importo della diaria del 25%. |
| Calcola riduzione per vitto per           | Specifica in che modo il sistema dovrebbe calcolare la riduzione del vitto giornaliero, selezionando se la riduzione è basata sul tipo di pasto per viaggio o al giorno, o se è basata sul numero di pasti consentiti al giorno. |
| Arrotondamento trasferta giornaliera                     | Seleziona il tipo di arrotondamento utilizzato per le spese giornaliere. Se selezioni l'arrotondamento normale, qualsiasi spesa giornaliera con un importo di 0,50 viene arrotondata a 1,00 e qualsiasi spesa giornaliera con un importo inferiore a 0,50 viene arrotondata per difetto a 0,00. |
| Base per il calcolo della trasferta giornaliera          | Seleziona se l'importo giornaliero è basato su un giorno di calendario o su un periodo di 24 ore. |

## <a name="fax-cover-pages"></a>Copertine fax

| Campo                          | Descrizione |
|--------------------------------|-------------|
| Istruzioni                   | Immetti le istruzioni che i dipendenti devono seguire quando creano un frontespizio per un fax utilizzato per inviare ricevute correlate a una nota spese. Per inserire un testo specifico per la lingua che verrà mostrato, in base alla lingua dell'utente, seleziona **Traduzioni**. |
| ID utente (informazioni sul codice a barre) | Seleziona questa opzione per memorizzare l'identificatore univoco di un dipendente nel codice a barre utilizzato sulla copertina del fax. |
| Codice a barre                       | Selezionare il codice a barre utilizzato sulla copertina del fax. I codici a barre 39 e 128 sono supportati in Gestione spese. |

## <a name="anti-corruption"></a>Anticorruzione

| Campo                                 | Descrizione |
|---------------------------------------|-------------|
| Visualizza attestazione anticorruzione   | Seleziona questa opzione per mostrare il testo anticorruzione quando viene creata una nota spese. È quindi possibile abilitare categorie di spesa specifiche che richiederanno la selezione dell'attestazione anticorruzione nella nota spese. Ad esempio, una categoria di regali correlata a una spesa di un funzionario governativo potrebbe richiedere al dipendente di confermare che la spesa soddisfa i criteri aziendali correlati ai funzionari pubblici. |
| Messaggio anticorruzione per autore dell'invio | Immetti il testo che deve essere mostrato a un dipendente che sta creando una nota spese. Per inserire un testo specifico per la lingua che verrà mostrato, in base alla lingua dell'utente, seleziona **Traduzioni**. |
| Messaggio anticorruzione per approvatore  | Immetti il testo che deve essere mostrato a un approvatore quando viene creata una nota spese. Per inserire un testo specifico per la lingua che verrà mostrato, in base alla lingua dell'utente, seleziona **Traduzioni**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]