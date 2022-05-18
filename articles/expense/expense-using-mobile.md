---
title: App spese per dispositivi mobili
description: In questo argomento vengono fornite informazioni sull'area di lavoro per dispositivi Gestione delle spese.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 14bd76df5f058d2af9f77990471a0a173fe8c15d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588925"
---
# <a name="mobile-expense-app"></a>App spese per dispositivi mobili

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

In questo argomento vengono fornite informazioni sull'area di lavoro per dispositivi **Gestione delle spese**. Questa area di lavoro consente agli utenti di acquisire e caricare una ricevuta, in modo da poterla allegare a una nota spese in un secondo momento. Gli utenti possono anche creare rapidamente una riga di spesa utilizzando una ricevuta allegata e creare e gestire le proprie note spese. Inoltre, gli approvatori possono utilizzare l'area di lavoro per dispositivi mobili **Gestione delle spese** per visualizzare le note spese loro assegnate e approvarle o rifiutarle.

Quest'area di lavoro per dispositivi mobili deve essere utilizzata con l'app dispositivi mobili Dynamics 365.

Molte organizzazioni richiedono che una copia della ricevuta sia allegata a una nota spese di viaggio o di lavoro che un dipendente presenta per il rimborso. L'area di lavoro per dispositivi mobili **Gestione delle spese** consente agli utenti di creare rapidamente nuove righe di spesa sul dispositivo mobile di loro scelta utilizzando la foto di una ricevuta allegata. In alternativa, gli utenti possono acquisire la foto di una ricevuta e allegarla successivamente a una nota spese. I dipendenti possono anche creare e gestire le proprie note spese, quindi inviarle per l'approvazione e il rimborso utilizzando il proprio dispositivo mobile.

In particolare, l'area di lavoro per dispositivi mobili **Gestione delle spese** consente agli utenti di eseguire queste attività:

- Acquisire la foto di una ricevuta. Caricare la foto della ricevuta e allegarla a una nota spese in un secondo momento.
- Caricare un file come ricevuta acquisita. È quindi possibile allegare il file a una nota spese in un secondo momento.
- Creare una nuova riga di spesa utilizzando una ricevuta allegata. È quindi possibile aggiungere la voce a una nota spese in un secondo momento e inviarla per l'approvazione e il rimborso.

Puoi utilizzare anche le funzionalità per:

- Creare una nuova nota spesa.
- Allegare transazioni con carta di credito e altre spese precedentemente create a una nota spese.
- Creare nuove spese per una nota spese.
- Allegare una ricevuta a qualsiasi spesa per una nota spese, scattando una foto della ricevuta o caricando un file come ricevuta acquisita.
- A seconda dei criteri di spesa dell'azienda, aggiungere l'elenco degli ospiti a una spesa.
- A seconda dei criteri di spesa dell'azienda, dettagliare le spese.
- Inviare una nota spese per approvazione e rimborso.
- Approvare o rifiutare le note spese per le quali sei un approvatore assegnato.

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Prerequisiti per l'utilizzo di Dynamics 365 Finance

Se Finance è stato distribuito per la tua organizzazione, l'amministratore di sistema deve pubblicare l'area di lavoro per dispositivi mobili **Gestione delle spese**. 

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Scaricare e installare l'app per dispositivi mobili Dynamics 365 Unified Ops
Scarica e installa l'app per dispositivi mobili Dynamics 365 Unified Ops:

- [Per telefoni Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Per iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Accedere all'app per dispositivi mobili
1. Avvia l'app sul dispositivo mobile.
2. Immetti l'URL di Dynamics 365.
4. La prima volta che accedi, ti vengono richiesti il nome utente e la password. Immetti le tue credenziali.
5. Dopo aver effettuato l'accesso, vengono visualizzate le aree di lavoro disponibili per la tua azienda. Se l'amministratore di sistema pubblica una nuova area di lavoro in un secondo momento, dovrai aggiornare l'elenco delle aree di lavoro per dispositivi mobili.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Acquisisci una ricevuta utilizzando l'area di lavoro per dispositivi mobili Gestione delle spese

1. Sul tuo dispositivo mobile, apri l'area di lavoro **Gestione delle spese**.
2. Seleziona **Acquisisci ricevuta**.
3. Seleziona **Scatta foto** o **Scegli immagine**.
4. Segui uno di questi passaggi:

    - Se hai selezionato **Scatta foto**, segui questi passaggi:

        1. Viene aperta la fotocamera del tuo dispositivo mobile, in modo da poter scattare una foto della ricevuta. 
        2. Quando hai finito di scattare la foto, seleziona **OK** per accettare la foto.
        3. Facoltativo: inserisci un nome per la foto e inserisci eventuali note.

    - Se hai selezionato **Scegli immagine**, segui questi passaggi:

        1. Seleziona un'immagine dall'elenco.
        2. Facoltativo: inserisci un nome per l'immagine e inserisci eventuali note.

5. Seleziona **Fatto**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Immettere rapidamente le spese utilizzando l'area di lavoro per dispositivi mobili Gestione delle spese

1. Sul tuo dispositivo mobile, apri l'area di lavoro **Gestione delle spese**.
2. Seleziona **Immissione rapida spese**.
3. Seleziona la categoria di spesa. Viene visualizzato l'elenco delle categorie di spesa caricate nella tua app per l'utilizzo offline. Per impostazione predefinita, vengono caricati 50 elementi, ma uno sviluppatore può modificare questo numero. Per altre informazioni, gli sviluppatori possono fare riferimento a [Piattaforma per dispositivi mobili](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se la tua categoria non è nell'elenco, seleziona **Cerca** per eseguire una ricerca online. Cerca per categoria di spesa o passa alla ricerca per tipo di spesa.
4. Immetti la data di transazione della spesa.
5. Facoltativo: inserisci il commerciante per la spesa.
6. Immetti l'importo della spesa.
7. Seleziona la valuta della spesa. Viene visualizzato l'elenco dei codici valuta caricati nella tua app per l'utilizzo offline. Per impostazione predefinita, vengono caricate 400 valute, ma uno sviluppatore può modificare questo numero. Per altre informazioni, gli sviluppatori possono fare riferimento a [Piattaforma per dispositivi mobili](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se la tua valuta non è nell'elenco, seleziona **Cerca** per eseguire una ricerca online. Cerca per valuta o passa alla ricerca per nome.
8. Seleziona **Scatta foto** o **Scegli immagine**.
9. Segui uno di questi passaggi:

    - Se hai selezionato **Scatta foto**, viene aperta la fotocamera del tuo dispositivo mobile, in modo da poter scattare una foto della ricevuta. Quando hai finito di scattare la foto, seleziona **OK** per accettare la foto.
    - Se hai selezionato **Scegli immagine**, seleziona un'immagine dall'elenco.

10. Seleziona **Fatto**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Approvare una nota spese tramite l'area di lavoro per dispositivi mobili Gestione spese

1. Sul tuo dispositivo mobile, apri l'area di lavoro **Gestione delle spese**.
2. **Approvazione delle spese** mostra il numero di note spese che ti sono state assegnate per l'approvazione. Il numero viene aggiornato circa ogni 30 minuti. Seleziona **Approvazione delle spese**.

    Viene visualizzato l'elenco delle note spese che ti sono state assegnate per l'approvazione.

3. Seleziona una nota spese per visualizzarne i dettagli di spesa.
4. Seleziona una spesa per visualizzarne i dettagli. Le informazioni visualizzate per una spesa includono eventuali dettagli su ricevuta, ospite e articolo.
5. Torna alla pagina **Nota spese** e seleziona per approvare o rifiutare la nota spese.
6. Immetti eventuali commenti per l'azione di approvazione.
7. Seleziona **Fatto**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Creare una nuova nota spese e inviarla per l'approvazione usando l'area di lavoro per dispositivi mobili Gestione spese

1. Sul tuo dispositivo mobile, apri l'area di lavoro **Gestione delle spese**.
2. Seleziona **Voce di spesa**.
3. Seleziona **Nuovo report** oppure seleziona una nota spese esistente nell'elenco.
4. Per le nuove note spese, immetti lo scopo e le eventuali informazioni aggiuntive disponibili. Queste informazioni variano a seconda del modo in cui la gestione delle spese è configurata per la tua azienda.
5. Seleziona **Fatto**.
6. Per aggiungere le spese esistenti, come le transazioni con carta di credito, alla nota spese, seleziona **Allega**.
7. Seleziona nell'elenco una o più spese.
8. Seleziona **Fatto**.
9. Per aggiungere una nuova spesa alla nota spese, seleziona **Nuova spesa**.
10. Seleziona la categoria per la spesa. Viene visualizzato l'elenco delle categorie di spesa caricate nella tua app per l'utilizzo offline. Per impostazione predefinita, vengono caricati 50 elementi, ma uno sviluppatore può modificare questo numero. Per altre informazioni, gli sviluppatori possono fare riferimento a [Piattaforma per dispositivi mobili](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se la tua categoria non è nell'elenco, seleziona **Cerca** per eseguire una ricerca online. Cerca per categoria di spesa o passa alla ricerca per tipo di spesa.
11. Facoltativo: inserisci il commerciante per la spesa.
12. Immetti la data di transazione della spesa.
13. Immetti l'importo della spesa.
14. Seleziona la valuta della spesa. Viene visualizzato l'elenco dei codici valuta caricati nella tua app per l'utilizzo offline. Per impostazione predefinita, vengono caricate 400 valute, ma uno sviluppatore può modificare questo numero. Per altre informazioni, gli sviluppatori possono fare riferimento a [Piattaforma per dispositivi mobili](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se la tua valuta non è nell'elenco, seleziona **Cerca** per eseguire una ricerca online. Cerca per valuta o passa alla ricerca per nome.
15. Seleziona **Fatto**.
16. Per aggiungere ulteriori dettagli alla spesa, seleziona **Aggiungi altri dettagli**. I campi disponibili dipendono dalla configurazione della gestione delle spese per la tua azienda.
17. Se i criteri aziendale richiedono una ricevuta per la spesa, seleziona **Ricevute** e quindi segui questi passaggi:

    1. Seleziona **Acquisisci ricevuta** o **Allega ricevuta**.
    2. Segui uno di questi passaggi:

        - Se hai selezionato **Acquisisci ricevuta**, segui questi passaggi:

            1. Seleziona **Scatta foto** o **Scegli immagine**.
            2. Segui uno di questi passaggi:

                - Se hai selezionato **Scatta foto**, segui questi passaggi:

                    1. Viene aperta la fotocamera del tuo dispositivo mobile, in modo da poter scattare una foto della ricevuta. Quando hai finito di scattare la foto, seleziona **OK** per accettare la foto.
                    2. Facoltativo: inserisci un nome per la foto e inserisci eventuali note.

                - Se hai selezionato **Scegli immagine**, segui questi passaggi:

                    1. Seleziona un'immagine dall'elenco.
                    2. Facoltativo: inserisci un nome per l'immagine e inserisci eventuali note.

            3. Seleziona **Fatto**.

        - Se hai selezionato **Allega ricevuta**, segui questi passaggi:

            1. Nell'elenco seleziona una o più immagini.
            2. Seleziona **Fatto**.

    3. Seleziona il pulsante **Indietro** per tornare ai dettagli della spesa.

18. Se i criteri aziendale richiedono gli ospiti per la spesa, seleziona **Guest** e quindi segui questi passaggi:

    1. Seleziona **Guest**, **Guest precedenti** o **Colleghi**.
    2. Segui uno di questi passaggi:

        - Se hai selezionato **Guest**, segui questi passaggi:

            1. Immettere il nome del guest.
            2. Facoltativo: inserisci l'organizzazione e/o il paese del guest.
            3. Facoltativo: immetti la posizione del guest.
            4. Seleziona **Fatto**.

        - Se hai selezionato **Guest precedenti**, segui questi passaggi:

            1. Seleziona uno o più guest precedenti nell'elenco. Viene visualizzato un elenco dei guest precedenti che hai aggiunto alle note spese precedenti caricate nella tua app per l'utilizzo offline. Per impostazione predefinita, vengono caricati 50 elementi, ma uno sviluppatore può modificare questo numero. Per altre informazioni, gli sviluppatori possono fare riferimento a [Piattaforma per dispositivi mobili](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se il guest precedente non è nell'elenco, seleziona **Cerca** per eseguire una ricerca online. Cerca per nome o passa alla ricerca per organizzazione, paese o posizione.
            2. Seleziona **Fatto**.

        - Se hai selezionato **Collaboratori**, segui questi passaggi:

            1. Seleziona uno o più collaboratori nell'elenco. Viene visualizzato l'elenco dei collaboratori caricati nella tua app per l'utilizzo offline. Per impostazione predefinita, vengono caricati 50 elementi, ma uno sviluppatore può modificare questo numero. Per altre informazioni, gli sviluppatori possono fare riferimento a [Piattaforma per dispositivi mobili](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se il collaboratore non è nell'elenco, seleziona **Cerca** per eseguire una ricerca online. Cerca per nome o passa alla ricerca per società o posizione.
            2. Seleziona **Fatto**.

    3. Seleziona il pulsante **Indietro** per tornare ai dettagli della spesa.

19. Se i criteri aziendale richiedono che la spesa sia dettagliata, seleziona **Dettaglia** e quindi segui questi passaggi:

    1. Seleziona la prima data da dettagliare.
    2. Seleziona **Aggiungi dettaglio**.
    3. Seleziona la sottocategoria per il dettaglio spesa. Viene visualizzato l'elenco delle sottocategorie di spesa caricate nella tua app per l'utilizzo offline. Per impostazione predefinita, vengono caricati 50 elementi, ma uno sviluppatore può modificare questo numero. Per altre informazioni, gli sviluppatori possono fare riferimento a [Piattaforma per dispositivi mobili](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se la tua sottocategoria non è nell'elenco, seleziona **Cerca** per eseguire una ricerca online. Cerca per nome della sottocategoria di spesa.
    4. Immetti l'importo della transazione per il dettaglio.
    5. Modifica la data della transazione, se necessario.
    6. Seleziona **Fatto**.
    7. Ripeti i passaggi precedenti fino a quando non hai terminato di aggiungere tutti i dettagli per la data selezionata.
    8. Per altri giorni, puoi selezionare **Copia al giorno successivo** per copiare i dettagli al giorno successivo. In alternativa, puoi selezionare la data da dettagliare e quindi aggiungere i dettagli come hai fatto per la prima data.
    9. Dopo aver finito di dettagliare la spesa, seleziona il pulsante **Indietro** per tornare ai dettagli della spesa.

20. Seleziona il pulsante **Indietro** per tornare alla pagina **Nota spese**.
21. Ripeti i passaggi precedenti finché non hai finito di aggiungere tutte le spese.
22. Seleziona **Invia**.
23. Immetti eventuali commenti per il responsabile dell'approvazione.
24. Seleziona **Fatto**.

## <a name="frequently-asked-questions"></a>Domande frequenti

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>Perché l'app per dispositivi mobili Gestione spese non è inclusa nel metodo di pagamento per impostazione predefinita?

Le organizzazioni possono personalizzare l'impostazione **Metodo di pagamento predefinito** per ogni categoria di spesa così come è stata creata. Quando imposti i metodi di pagamento, puoi inoltre configurare il campo **Metodo di pagamento predefinito** su **Solo importazione**.

Quando **Solo importazione** è abilitato per un metodo di pagamento, quest'ultimo non è immesso per impostazione predefinita: sarà vuoto nelle categorie di spesa in cui è impostato questo metodo di pagamento. Questo comportamento è coerente sia nell'ambito dell'esperienza Web sia in quella su dispositivi mobili.
    
Quando **Solo importazione** non è abilitato per un metodo di pagamento, il valore impostato viene immesso per impostazione predefinita per le categorie di spesa in cui è impostato questo metodo di pagamento. Esiste tuttavia un problema noto che impedisce l'immissione del valore predefinito nell'app per dispositivi mobili Gestione spese. Per risolvere il problema, seleziona manualmente un metodo di pagamento prima di salvare la nota spese. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>Perché non posso aggiungere o modificare le dimensioni finanziarie nell'app per dispositivi mobili Gestione spese?

L'immissione di dimensioni e distribuzioni non è supportata. Per aggirare questa limitazione, puoi fare in modo che questi campi siano configurati per impostazione predefinita nell'app per dispositivi mobili, configurando le dimensioni finanziarie predefinite per progetto o dipendente.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>Perché a volte vedo un errore di sincronizzazione nell'app per dispositivi mobili Gestione spese?

Se le righe spese non soddisfano i requisiti dei criteri e l'utente invia la nota spese senza risolvere l'avviso relativo ai criteri, i dati dei dispositivi mobili non vengono sincronizzati con il server e si verifica un errore di sincronizzazione. Tutte le note spese inviate dopo che si è verificato un errore di sincronizzazione rimarranno in uno stato di errore e causeranno altri errori di sincronizzazione. L'unico modo per risolvere questa situazione consiste nell'eliminare manualmente le notifiche di sincronizzazione. Questo problema è stato risolto interrompendo l'invio delle note spese qualora gli avvisi relativi ai criteri non sono stati risolti, così da evitare errori di sincronizzazione.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>Perché la convalida del progetto e della categoria non viene riflessa correttamente nell'app per dispositivi mobili Gestione spese?

Questo convalida non è attualmente supportata. Tuttavia, il supporto potrebbe essere aggiunto in futuro. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Quali tipi di documento sono supportati nell'app per dispositivi mobili Gestione spese?

L'app per dispositivi mobili Gestione spese supporta solo le immagini. Attualmente non supporta file PDF o altri documenti.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
