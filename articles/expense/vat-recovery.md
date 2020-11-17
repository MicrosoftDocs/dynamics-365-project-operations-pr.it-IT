---
title: Recupero dell'IVA in Gestione spese
description: Questo argomento spiega come ricevere rimborsi su transazioni idonee per l'imposta sul valore aggiunto (IVA).
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: c52d5ccef681ef9d9ff767c99af6f2fd0fd6da52
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126128"
---
# <a name="vat-recovery-in-expense-management"></a>Recupero dell'IVA in Gestione spese

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Per ricevere rimborsi su transazioni idonee per l'imposta sul valore aggiunto (IVA), un'azienda o un'organizzazione deve identificare, raccogliere, verificare e inviare informazioni accurate. Questo processo include più attività e, a seconda delle dimensioni dell'azienda, può includere diversi dipendenti o ruoli.

Per recuperare l'IVA nel modulo **Gestione spese**, devono essere soddisfatti i seguenti prerequisiti:

- Devono essere creati i codici imposta per i paesi/aree geografiche che sono assegnati a categorie di spesa.
- È necessario creare una fascia IVA per ogni codice imposta.
- È necessario creare un codice IVA articoli per ogni fascia IVA.

Dopo aver completato i prerequisiti, è necessario completare i seguenti passaggi per richiedere i rimborsi per le transazioni IVA.

1. In una nota spese, inserisci le informazioni fiscali sulle transazioni con carta di credito per individuare i rimborsi IVA idonei.
2. Verifica che tutte le informazioni fiscali siano complete, quindi registra la nota spese.
3. Elabora le spese idonee per il recupero dell'IVA internazionale.
4. Invia i dati di recupero dell'IVA al fornitore di terze parti per presentare le dichiarazioni per il recupero internazionale.
5. Elabora le spese per il recupero dell'IVA nazionale.

Le sezioni seguenti forniscono esempi che mostrano come i dipendenti di Contoso completano ogni passaggio.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Immettere le informazioni fiscali sulle transazioni con carta di credito per individuare i rimborsi IVA idonei

Nancy, una rappresentante di vendita di Contoso con sede negli Stati Uniti, è tornata di recente da un viaggio di lavoro nel Regno Unito. Durante il viaggio, Nancy ha sostenuto alcune spese di vitto con una carta di credito personale. Nancy deve ora creare una nota spese per riconciliare le spese.

Quando Nancy inserisce le informazioni nella nota spese, seleziona **Regno Unito** nel campo **Paese/area geografica** nella pagina **Modifica nota spese**. L'elenco delle fasce IVA viene quindi filtrato in modo da mostrare solo i gruppi che si applicano al Regno Unito. Nancy seleziona la fascia IVA **Regno Unito 001** e quindi seleziona la fascia IVA articoli **Vitto**. Successivamente, Nancy aggiunge una nuova transazione per l'alloggio. Poiché esiste solo una fascia IVA e una fascia IVA articoli per l'alloggio nel Regno Unito, queste informazioni vengono inserite automaticamente nella nota spese di Nancy.

In base ai criteri di Contoso, tutte le spese devono avere una ricevuta corrispondente. Pertanto, quando Nancy salva la nota spese, riceve un messaggio che indica che deve allegare una ricevuta per ogni transazione che ha elencato nella sua nota spese. Nancy verifica di aver allegato un'immagine digitale di ciascuna ricevuta di transazione alla sua nota spese e quindi invia la nota spese per l'approvazione. Quindi invia le ricevute cartacee al team di elaborazione di back office. Questo team invierà i dati di recupero IVA al fornitore di terze parti che presenta le dichiarazioni per il recupero IVA internazionale per Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Verificare le informazioni fiscali e registrare una nota spese

Prima che April, il coordinatore della contabilità fornitori di Contoso, possa registrare una nota spese, deve inserire tutte le informazioni fiscali mancanti. Apre la pagina **Dettagli nota spese** e vede la nota spese approvata di Nancy. April quindi apre la nota spese per visualizzare i dettagli delle transazioni. Vede che Nancy non ha inserito una fascia IVA articoli per una delle transazioni. Poiché queste informazioni non sono state fornite, April non può registrare la nota spese. Pertanto, controlla la pagina **Configurazioni imposte** in Gestione spese e trova la fascia IVA articoli appropriata per il paese/area geografica e il tipo di transazione. April può ora registrare la nota spese nella contabilità generale.

Quando April registra la nota spese, viene creato un elemento di lavoro recuperabile IVA. Questo elemento di lavoro viene assegnato a un membro del team di elaborazione di back office. April riceve un messaggio di conferma che la registrazione è andata a buon fine. Questo messaggio elenca anche il numero di transazioni IVA identificate per il recupero.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Elaborare le spese idonee per il recupero dell'IVA internazionale

Arnie, un membro del team di elaborazione di back-office di Contoso, è responsabile di verificare che tutte le informazioni obbligatorie per il recupero dell'IVA siano incluse nelle note spese. Apre la pagina **Recupero imposte su spese** e seleziona la nota spese inviata da Nancy. Arnie verifica quindi che tutte le ricevute obbligatorie siano allegate e che siano stati inseriti la fascia IVA e i codici IVA articoli corretti.

Quando Arnie riceve le ricevute cartacee da Nancy, le confronta con le ricevute digitali e quindi modifica lo stato della nota spese in **Pronte per il recupero**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Inviare i dati di recupero dell'IVA al fornitore di terze parti

Quando Arnie è pronto per inviare i dati della nota spese al fornitore di terze parti che presenterà le dichiarazioni per il recupero IVA, apre la pagina **Recupero imposte su spese**. Filtra la pagina in modo che mostri solo le note spese contrassegnate come **Pronte per il recupero**. Arnie quindi seleziona **File** &gt; **Esporta in Excel**. Le informazioni sull'IVA delle note spese vengono esportate in un foglio di lavoro di Microsoft Excel. Arnie invia questo foglio di lavoro al fornitore di terze parti e include un messaggio per informare che le ricevute cartacee sono state inviate tramite corriere.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Elaborare le spese per il recupero dell'IVA nazionale

Arnie deve verificare che le transazioni della nota spese siano idonee per il recupero dell'IVA e che le ricevute digitali siano allegate alle note spese. Per iniziare a elaborare le spese idonee per il recupero nazionale, Arnie apre la pagina **Recupero imposte su spese** e seleziona la nota spese che richiede la verifica. Verifica che le ricevute siano intestate all'azienda anziché al dipendente. (Per il recupero dell'IVA le ricevute devono essere intestate all'azienda.) Arnie verifica quindi che siano stati inseriti la fascia IVA e i codici IVA articoli corretti.

Quando Arnie riceve le ricevute cartacee, cambia lo stato della nota spese in **Pronte per il recupero**. Può quindi presentare la dichiarazione all'autorità fiscale appropriata. In questo caso, l'autorità fiscale appropriata negli Stati Uniti è l'Internal Revenue Service (IRS).
