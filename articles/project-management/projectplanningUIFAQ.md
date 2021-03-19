---
title: Risolvere i problemi relativi alla griglia delle attività
description: Questo argomento fornisce le informazioni sulla risoluzione dei problemi necessaria quando si utilizza la griglia delle attività.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286568"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Risolvere i problemi relativi alla griglia delle attività 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questa argomento descrive come risolvere i problemi che potresti riscontrare mentre utilizzi la gestione dei costi.

## <a name="enable-cookies"></a>Abilitare i cookie

Project Operations richiede che i cookie di terze parti siano abilitati per eseguire il rendering della struttura di suddivisione del lavoro. Quando i cookie di terze parti non sono abilitati, invece di visualizzare le attività, vedrai una pagina vuota quando selezioni la scheda **Attività** nella pagina **Progetto**.

![Scheda vuota quando i cookie di terze parti non sono abilitati](media/blankschedule.png)


### <a name="workaround"></a>Soluzione alternativa
Per Microsoft Edge o Google Chrome, le seguenti procedure delineano come aggiornare le impostazioni del browser per abilitare i cookie di terze parti.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Apri il browser Edge.
2. Nell'angolo superiore destro seleziona i **puntini di sospensione** (...) e quindi **Impostazioni**.
3. Sotto **Cookie e autorizzazioni del sito** seleziona **Cookie e dati dei siti**.
4. Disattiva **Blocca cookie di terze parti**.

#### <a name="google-chrome"></a>Google Chrome

1. Aprire il browser Chrome.
2. Nell'angolo superiore destro, seleziona i tre puntini verticali e quindi seleziona **Impostazioni**.
3. Sotto **Privacy e sicurezza** seleziona **Cookie e altri dati dei siti**.
4. Seleziona **Consenti tutti i cookie**.

> [!IMPORTANT]
> Se blocchi i cookie di terze parti, tutti i cookie e i dati di altri siti verranno bloccati, anche se il sito è consentito nell'elenco delle eccezioni.

## <a name="pex-endpoint"></a>Endpoint PEX

Project Operations richiede che un parametro di progetto faccia riferimento all'endpoint PEX. Questo endpoint è necessario per comunicare con il servizio utilizzato per il rendering della struttura di suddivisione del lavoro. Se il parametro non è abilitato, riceverai l'errore "Il parametro del progetto non è valido". 

### <a name="workaround"></a>Soluzione alternativa
 ![Campo Endpoint PEX nel parametro di progetto](media/projectparameter.png)

1. Aggiungi il campo **Endpoint PEX** alla pagina **Parametri di progetto**.
2. Aggiorna il campo con il seguente valore: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Rimuovi il campo dalla pagina **Parametri di progetto**.

## <a name="privileges-for-project-for-the-web"></a>Privilegi per progetto per il Web

Project Operations si basa su un servizio di pianificazione esterno. Il servizio richiede che un utente abbia diversi ruoli assegnati per leggere e scrivere nelle entità correlate alla struttura di suddivisione del lavoro. Queste entità includono attività di progetto, assegnazioni di risorse e dipendenze tra attività. Se un utente non può eseguire il rendering della struttura di suddivisione del lavoro quando accede alla scheda **Attività** probabilmente è perché Progetto per Project Operations non è stato abilitato. Un utente potrebbe ricevere un errore relativo al ruolo di sicurezza o un errore relativo a un rifiuto di accesso.


## <a name="workaround"></a>Soluzione alternativa

1. Vai a **Impostazioni > Sicurezza > Utenti > Utenti dell'applicazione**.  

   ![Lettore dell'applicazione](media/applicationuser.jpg)
   
2. Fai doppio clic sul record dell'utente dell'applicazione per verificare quanto segue:

 - L'utente ha accesso al progetto: Questa verifica viene in genere eseguita assicurando che l'utente abbia il ruolo di sicurezza **Responsabile di progetto**.
 - L'utente dell'applicazione Microsoft Project esiste ed è configurato correttamente.
 
3. Se l'utente non esiste, puoi crearne un nuovo record utente. Seleziona **Nuovi utenti**. Modifica il modulo di immissione su **Utente dell'applicazione**, quindi aggiungi l'**ID applicazione**.

   ![Dettagli utente dell'applicazione](media/applicationuserdetails.jpg)

4. Verifica che all'utente sia stata assegnata la licenza corretta e che il servizio sia abilitato nei dettagli dei piani di servizio della licenza.
5. Verifica che l'utente possa aprire project.microsoft.com.
6. Verifica tramite i parametri di progetto che il sistema stia puntando all'endpoint di progetto corretto.
7. Verifica che l'utente dell'applicazione di progetto sia stato creato.
8. Applica i seguenti ruoli di sicurezza all'utente:

  - Utente di Dataverse
  - Sistema Project Operations
  - Sistema di progetto

## <a name="error-when-updating-the-work-breakdown-structure"></a>Errore durante l'aggiornamento della struttura di suddivisione del lavoro

Quando vengono apportati uno o più aggiornamenti alla struttura di suddivisione del lavoro, le modifiche non riescono e non vengono salvate. Si verifica un errore nella griglia di pianificazione indicante che "Impossibile salvare la modifica recente apportata".

### <a name="workaround"></a>Soluzione alternativa

1. Verifica che all'utente sia stata assegnata la licenza corretta e che il servizio sia abilitato nei dettagli dei piani di servizio della licenza.
2. Verifica che l'utente possa aprire project.microsoft.com.
3. Verifica che il sistema stia puntando all'endpoint di progetto corretto.
4. Verifica che l'utente dell'applicazione di progetto sia stato creato.
5. Applica i seguenti ruoli di sicurezza all'utente:
  
  - Utente Dataverse o utente di base
  - Sistema Project Operations
  - Sistema di progetto
  - Sistema di doppia scrittura di Project Operations (questo ruolo è richiesto se distribuisci lo scenario basato su risorse/materiali non stoccati di operazioni di progetto).


[!INCLUDE[footer-include](../includes/footer-banner.md)]