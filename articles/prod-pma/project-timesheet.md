---
title: Applicazione per dispositivi mobili Foglio presenze progetto
description: Questo argomento fornisce informazioni sull'appplicazione per dispositivi mobili Microsoft Dynamics 365 Project Timesheet. L'app per dispositivi mobili Foglio presenze progetto consente agli utenti di inviare e approvare i fogli presenza per i progetti sul proprio dispositivo mobile.
author: abruer
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: df6d286b6d5716fb0ea908ed71c2257b4db21ecfd35148fea65dfd96e058ac9a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997206"
---
# <a name="project-timesheet-mobile-application"></a>Applicazione per dispositivi mobili Foglio presenze progetto

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Panoramica

L'app per dispositivi mobili Microsoft Dynamics 365 Project Timesheet consente agli utenti di inviare e approvare i fogli presenza per i progetti sul proprio dispositivo mobile (iPhone o Android). Questa app per dispositivi mobili presenta la funzionalità del foglio presenze che risiede nell'area Gestione progetti e contabilità di Dynamics 365 Finance, migliorando la produttività e l'efficienza degli utenti, oltre a consentire l'immissione e l'approvazione tempestive dei fogli presenze del progetto.

## <a name="download-and-install-the-mobile-app"></a>Scaricare e installare l'app per dispositivi mobili

Scarica e installa l'app per dispositivi mobili Microsoft Dynamics 365 Project Timesheet per Android o iPhone dallo store mobile per il tuo dispositivo.

## <a name="enable-the-app"></a>Abilitare l'app 

In Finance, l'app per dispositivi mobili Foglio presenze progetto deve essere abilitata. Per abilitare la funzionalità, vai a **Parametri Gestione progetti e contabilità \> Foglio presenze** e seleziona il parametro **Abilita Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Accedere all'app

1.  Avvia l'app sul dispositivo mobile.

2.  Immetti l'URL di Finance.

3.  La prima volta che accedi, ti vengono richiesti il nome utente e la password. Immetti le tue credenziali.

4.  Verrai connesso alla tua azienda predefinita.

## <a name="submit-a-project-timesheet"></a>Inviare un foglio presenze del progetto

Puoi creare e inviare un foglio presenze del progetto nell'app. Puoi basare un nuovo foglio presenze sulle informazioni di un foglio presenze precedente, le righe salvate o assegnazioni di progetti. Se sei designato come delegato, puoi anche immettere un foglio presenze per un altro ruolo di lavoro. Per creare un foglio presenze come delegato, seleziona il pulsante **Menu** e seleziona un nome di risorsa.

La pagina del foglio presenze creerà un nuovo foglio presenze per il periodo del foglio presenze, in base alla data corrente. Verrà visualizzata la settimana lavorativa. Se il periodo del foglio presenze copre più settimane, puoi selezionare un'altra settimana lavorativa dalle schede della settimana lavorativa.
Se esiste un foglio presenze per la data corrente, verrà visualizzato. Se devi creare un nuovo foglio presenze in un periodo di foglio presenze diverso, seleziona il pulsante **Menu** e quindi seleziona **Nuovo foglio presenze**.

Puoi inserire le informazioni sul progetto facendo clic sull'azione **Aggiungi tempo** o l'azione **Copia tempo da**. L'azione **Copia tempo da** copierà le informazioni sulla riga del progetto, ma non le ore. Il menu **Copia tempo da** include le seguenti opzioni:

- **Copia da foglio presenze esistente**: copia le righe del foglio presenze da un foglio presenze esistente.

- **Copia dai preferiti**: crea nuove righe del foglio presenze utilizzando le impostazioni del foglio presenze selezionate come preferiti.

- **Copia da assegnazione**: crea nuove righe del foglio presenze dai progetti assegnati.

Le informazioni sul progetto visualizzate dipendono dai parametri mobili definiti nella pagina **Parametri Gestione progetti e contabilità**.

Nel campo **Persona giuridica** seleziona la persona giuridica per la quale è stato eseguito il lavoro di progetto. Il campo **Persona giuridica** è disponibile solo se il supporto del foglio presenze interaziendale è stato abilitato per la persona giuridica.

Seleziona il cliente associato al progetto per il foglio presenze. Per la versione iniziale su Android, l'immissione per cliente non è supportata, poiché è necessario prima selezionare il progetto. Se hai selezionato prima il progetto, il campo **Cliente** viene compilato automaticamente.

Nel campo **Progetto**, seleziona il progetto per il quale stai immettendo l'ora. Il campo **Cliente** viene compilato automaticamente.

Le ricerche di clienti e progetti consentono la ricerca tra clienti e progetti.

Seleziona le informazioni nei campi **Categoria**, **Impegno**, **Proprietà riga**, **Gruppo IVA** e **Gruppo IVA articolo** in base alle esigenze. Questi campi possono essere sovrascritti.

Il campo **Proprietà riga** verrà impostato su un valore predefinito, in base ai paramteri di gestione del progetto e contabili. Quando i parametri progetto/categoria e categoria/risorsa sono abilitati, il valore **Proprietà riga** verrà impostato sul valore predefinito definito per questa convalida. Quando i parametri progetto/categoria e categoria/risorsa non sono abilitati, il valore **Proprietà riga** sarà predefinito in base al campi **Abilita proprietà riga predefinite** nella pagina **Parametri Gestione progetti e contabilità**. Il valore **Proprietà riga** può essere sovrascritto.

Seleziona un giorno per aggiungere tempo. Immetti il numero di ore lavorate ogni giorno.

Per aggiungere commenti sulle ore immesse, fai clic su **Aggiungi commenti**, quindi inserisci i commenti per un gruppo di destinatari interno, gruppo di destinatari del cliente o entrambi.
I commenti interni possono essere visualizzati dai project manager. I commenti dei clienti sono inclusi nelle fatture.

Per salvare la riga come preferita, seleziona la casella di controllo e quindi fai clic su **Salva come preferito**.

La dimensione finanziaria e il supporto per gli allegati non sono forniti nell'applicazione per dispositivi mobili.

Continua ad aggiungere righe di progetto secondo necessità per completare il foglio presenze.

Fai clic su **Invia** per inviare il foglio presenze al flusso di lavoro di approvazione.

## <a name="review-timesheets"></a>Rivedere i fogli presenze

Nel menu è disponibile un elenco dei fogli presenze che devono essere rivisti. Questa opzione è disponibile solo se sei stato designato come approvatore del flusso di lavoro. Sono supportate sia l'intestazione che l'approvazione della riga. L'approvazione a livello di riga offre la possibilità di contrassegnare una o più righe per l'approvazione. Dopo aver esaminato le informazioni sulla scheda attività, fai clic su **Approva**, **Delega** o **Restituisci** per continuare il flusso di lavoro.


[!INCLUDE[footer-include](../includes/footer-banner.md)]