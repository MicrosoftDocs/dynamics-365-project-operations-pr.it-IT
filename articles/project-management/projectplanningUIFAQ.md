---
title: Risolvere i problemi relativi alla griglia delle attività
description: Questo argomento fornisce le informazioni sulla risoluzione dei problemi necessaria quando si utilizza la griglia delle attività.
author: ruhercul
ms.date: 09/22/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 67136229d84a09886fffe9677b10f671aea3c393
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547204"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Risolvere i problemi relativi alla griglia delle attività 


_**Si applica a:** Project Operations per scenari basati su articoli non stoccati/risorse e Distribuzione semplice: dalla transazione alla fatturazione proforma, Project for the Web_

La griglia delle attività sfruttata da Dynamics 365 Project Operations è un iframe ospitato all'interno di Microsoft Dataverse. A seguito di tale utilizzo, devono essere soddisfatti requisiti specifici per garantire il corretto funzionamento dell'autenticazione e dell'autorizzazione. Questo argomento delinea i problemi comuni che possono influire sulla capacità di eseguire il rendering della griglia o gestire le attività nella struttura di suddivisione del lavoro (WBS).

I problemi comuni includono:

- La scheda **Attività** nella griglia delle attività è vuota.
- Quando si apre il progetto, il progetto non viene caricato e l'interfaccia utente (UI) è bloccata sulla casella di selezione.
- Amministrazione dei privilegi per **Project for the Web**.
- Le modifiche non vengono salvate quando crei, aggiorni o elimini un'attività.

## <a name="issue-the-task-tab-is-empty"></a>Problema: la scheda Attività è vuota

### <a name="mitigation-1-enable-cookies"></a>Mitigazione 1: abilitare i cookie

Project Operations richiede che i cookie di terze parti siano abilitati per rendere la struttura di suddivisione del lavoro. Quando i cookie di terze parti non sono abilitati, invece di visualizzare le attività, vedrai una pagina vuota quando selezioni la scheda **Attività** nella pagina **Progetto**.

Per Microsoft Edge o Google Chrome, le seguenti procedure delineano come aggiornare le impostazioni del browser per abilitare i cookie di terze parti.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Apri il browser Edge.
2. Nell'angolo superiore destro seleziona i **puntini di sospensione** (...) e quindi **Impostazioni**.
3. Sotto **Cookie e autorizzazioni del sito** seleziona **Cookie e dati dei siti**.
4. Disattiva **Blocca cookie di terze parti**.
5. Aggiorna il browser. 

#### <a name="google-chrome"></a>Google Chrome

1. Aprire il browser Chrome.
2. Nell'angolo superiore destro, seleziona i tre puntini verticali e quindi seleziona **Impostazioni**.
3. Sotto **Privacy e sicurezza** seleziona **Cookie e altri dati dei siti**.
4. Seleziona **Consenti tutti i cookie**.
5. Aggiorna il browser. 

> [!NOTE]
> Se blocchi i cookie di terze parti, tutti i cookie e i dati di altri siti verranno bloccati, anche se il sito è consentito nell'elenco delle eccezioni.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Mitigazione 2: verificare che l'endpoint PEX sia stato configurato correttamente

Project Operations richiede che un parametro di progetto faccia riferimento all'endpoint PEX. Questo endpoint è necessario per comunicare con il servizio utilizzato per eseguire il rendering della struttura di suddivisione del lavoro. Se il parametro non è abilitato, riceverai l'errore "Il parametro del progetto non è valido". Per aggiornare l'endpoint PEX, completare i seguenti passaggi.

1. Aggiungi il campo **Endpoint PEX** alla pagina **Parametri di progetto**.
2. Identifica il tipo di prodotto che stai utilizzando.. Questo valore viene utilizzato quando è impostato l'endpoint PEX. Al momento del recupero, il tipo di prodotto è già definito nell'endpoint PEX. Mantieni quel valore.
3. Aggiorna il campo con il seguente valore: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. La tabella seguente fornisce il parametro del tipo da utilizzare in base al tipo di prodotto.

      | **Tipo di prodotto**                     | **Parametro del tipo** |
      |--------------------------------------|--------------------|
      | Project for the Web sull'organizzazione predefinita   | tipo=0             |
      | Project for the Web sull'organizzazione con nome CDS | tipo=1             |
      | Project Operations                   | tipo=2             |

4. Rimuovi il campo dalla pagina **Parametri di progetto**.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problema: il progetto non si carica e l'interfaccia utente è bloccata sulla casella di selezione

Ai fini dell'autenticazione, i popup devono essere abilitati per il caricamento della griglia delle attività. Se i popup non sono abilitati, lo schermo sarà bloccato sulla casella di selezione per il caricamento. Il grafico seguente mostra l'URL con un'etichetta popup bloccata nella barra degli indirizzi che fa sì che la casella di selezione si blocchi durante il tentativo di caricamento della pagina. 

   ![Casella di selezione bloccata e blocco popup.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Mitigazione 1: abilitare i popup

Quando il tuo progetto è bloccato sulla casella di selezione, è possibile che i popup non siano abilitati.

#### <a name="microsoft-edge"></a>Microsoft Edge

Esistono due modi per abilitare i popup nel browser Edge.

1. Nel browser Edge, seleziona la notifica nell'angolo in alto a destra del browser.
2. Seleziona **Consenti sempre popup e reindirizzamenti** dallo specifico ambiente Dataverse.
 
     ![Finestra popup bloccata.](media/enablepopups.png)

In alternativa, puoi completare uno dei passaggi seguenti.

1. Apri il browser Edge.
2. Nell'angolo in alto a destra, seleziona i **puntini di sospensione** (...), quindi seleziona **Impostazioni** > **Autorizzazioni sito** > **Popup e reindirizzamenti**.
3. Disattiva **Pop-up e reindirizzamenti** per bloccare i popup o attivali per consentire i popup sul tuo dispositivo.
4. Dopo aver abilitato i popup, aggiorna il browser. 

#### <a name="google-chrome"></a>Google Chrome
1. Aprire il browser Chrome.
2. Vai a una pagina in cui i popup sono bloccati.
3. Nella barra degli indirizzi, seleziona **Popup bloccato**.
4. Seleziona il collegamento per il popup che desideri visualizzare.
5. Dopo aver abilitato i popup, aggiorna il browser. 

> [!NOTE]
> Per vedere sempre i popup per il sito, seleziona **Consenti sempre popup e reindirizzamenti da [sito]** e seleziona **Fatto**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problema 3: amministrazione dei privilegi per Project for the Web

Project Operations si basa su un servizio di pianificazione esterno. Il servizio richiede che un utente abbia diversi ruoli assegnati che gli consentano di leggere e scrivere su entità relative alla WBS. Queste entità includono attività di progetto, assegnazioni di risorse e dipendenze tra attività. Se un utente non è in grado di eseguire il rendering della WBS quando accede alla scheda **Attività**, probabilmente è perché **Progetto** per **Project Operations** non è stato abilitato. Un utente potrebbe ricevere un errore relativo al ruolo di sicurezza o un errore relativo a un rifiuto di accesso.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Mitigazione 1: convalidare l'utente dell'applicazione e dei ruoli di sicurezza dell'utente finale

1. Vai a **Impostazione** > **Sicurezza** > **Utenti** > **Utenti dell'applicazione**.  

   ![Lettore dell'applicazione.](media/applicationuser.jpg)
   
2. Fare doppio clic sul record utente dell'applicazione per verificare:

     - L'utente ha accesso al progetto: Puoi farlo verificando che l'utente abbia il ruolo di sicurezza **Responsabile di progetto**.
     - L'utente dell'applicazione Microsoft Project esiste ed è configurato correttamente.
 
3. Se questo utente non esiste, crea un nuovo record utente. 
4. Seleziona **Nuovi utenti**, modifica il modulo di inserimento in **Utente dell'applicazione**, quindi aggiungi l'**ID applicazione**.

   ![Dettagli utente dell'applicazione.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problema 4: le modifiche non vengono salvate quando crei, aggiorni o elimini un'attività

Quando effettui uno o più aggiornamenti alla WBS, le modifiche falliscono e non vengono salvate. Si verifica un errore nella griglia di pianificazione con un messaggio che dice "Impossibile salvare le modifiche recenti apportate".

### <a name="mitigation-1-validate-the-license-assignment"></a>Mitigazione 1: convalidare l'assegnazione della licenza

1. Verifica che all'utente sia stata assegnata la licenza corretta e che il servizio sia abilitato nei dettagli dei piani di servizio della licenza.  
2. Verifica che l'utente possa aprire **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Mitigazione 2: configurazione della convalida dell'utente dell'applicazione di Project
1. Verifica che l'utente dell'applicazione di progetto sia stato creato.
2. Applica i seguenti ruoli di sicurezza all'utente:
  
  - Utente Dataverse o utente di base
  - Sistema Project Operations
  - Sistema progetto
  - Sistemi in doppia scrittura di Project Operations. Questo ruolo è richiesto per lo scenario basato su risorse/non stoccate di Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
