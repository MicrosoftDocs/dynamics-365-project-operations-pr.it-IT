---
title: Righe dell'offerta basate sul progetto (Pro)
description: Questo argomento fornisce informazioni sull'utilizzo delle righe dell'offerta basate sul progetto per il lavoro del progetto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908277"
---
# <a name="project-based-quote-lines-pro"></a>Righe dell'offerta basate sul progetto (Pro)

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le righe dell'offerta basate sul progetto sono progettate per aiutare a stimare il lavoro del progetto per un impegno. La struttura di una riga dell'offerta basata sul progetto è estesa per le stime di progetto con i seguenti concetti:

- Metodo di fatturazione
- Mapping di progetti e attività
- Classi di transazione incluse
- Limite da non superare
- Impostazione dell'esigibilità
- Stima utilizzando i dettagli della riga dell'offerta
- Clienti riga di offerta

La tabella seguente fornisce informazioni sui campi nella scheda **Generale** della riga dell'offerta basata sul progetto. Questi campi aiutano a creare le basi per una stima dettagliata e completa del lavoro del progetto.

| **Campo** | **Pertinenza, scopo e indicazioni** | **Impatto downstream** |
| --- | --- | --- |
| Nome | Il nome della riga dell'offerta che dovrebbe aiutarti a identificare il componente discreto dell'offerta che viene stimata. | Copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Metodo di fatturazione | In un'offerta creata da un'opportunità, questo valore viene copiato dal campo corrispondente nella riga dell'opportunità. Questo campo include i due principali modelli di contratto supportati da Dynamics 365 Project Operations:</br>- Prezzo fisso</br>- Tempistica e materiali.| Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Project | Utilizza questo campo facoltativo per identificare il progetto che verrà utilizzato per fornire il lavoro su questo impegno. Quando un progetto viene mappato a una riga dell'offerta, viene semplificata l'impostazione delle attività addebitabili e anche l'inserimento di una stima basata sul progetto nella riga dell'offerta come dettagli della riga dell'offerta. Quando un progetto non è mappato a una riga dell'offerta basata sul progetto, la stima deve essere creata manualmente creando ogni dettaglio della riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.|
| Attività incluse | Indica se questa riga dell'offerta viene utilizzata per tutte o alcune delle attività di progetto per il progetto selezionato. Di seguito sono riportati i valori possibili di questo campo:</br>- Tutte le attività di progetto</br>- Solo le attività di progetto selezionate</br>Un valore vuoto in questo campo equivale all'opzione **Tutte le attività di progetto**. | Quando **Solo le attività di progetto selezionate** viene selezionato nella pagina del progetto, la scheda **Impostazione fatturazione attività** consente di selezionare attività specifiche per associarle a questa riga dell'offerta. Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Includi tempo | Un contrassegno **Sì**/**No** indica se le transazioni temporali o i costi di manodopera sul progetto selezionato saranno inclusi nella stima su questa riga dell'offerta. Un valore **No** indica che le transazioni temporali o i costi di manodopera non saranno inclusi nella stima su questa riga dell'offerta. Un valore **Sì** indica che le transazioni temporali o i costi di manodopera saranno inclusi nella stima su questa riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Includi spesa | Un contrassegno **Sì**/**No** indica se i costi di spesa sul progetto selezionato saranno inclusi nella stima su questa riga dell'offerta. Un valore **No** indica che i costi di spesa non saranno inclusi nella stima su questa riga dell'offerta. Un valore **Sì** indica che i costi di spesa saranno inclusi nella stima su questa riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Includi commissione | Un contrassegno **Sì**/**No** indica se le commissioni sul progetto selezionato saranno incluse nella stima su questa riga dell'offerta. Un valore **No** indica che le commissioni non saranno incluse nella stima su questa riga dell'offerta. Un valore **Sì** indica che le commissioni saranno incluse nella stima su questa riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Importo offerto | Questo è l'importo che verrà offerto al cliente per tutto il lavoro previsto in questa riga dell'offerta basata sul progetto. In un'offerta creata da un'opportunità, questo valore viene copiato dal campo **Budget cliente** nella riga dell'opportunità. Quando la riga dell'offerta basata sul progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo nei dettagli della riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Imposta stimata | Questo è un campo modificabile che consente all'utente di aggiungere l'importo delle imposte stimate nella riga dell'offerta. Quando una riga dell'offerta basata sul progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo delle imposte nei dettagli della riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Importo offerto al netto delle imposte | Questo campo rappresenta l'importo della riga dell'offerta al netto delle imposte ed è di sola lettura. L'importo in questo campo viene calcolato come *Importo offerto + imposte*. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Limite da non superare | Questo campo è modificabile ed è disponibile solo per le righe dell'offerta basate su progetto che hanno un metodo di fatturazione **Tempistica e materiali**. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Budget cliente | Questo campo è modificabile e viene copiato dal campo corrispondente nella riga dell'opportunità se l'offerta è stata creata da un'opportunità. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regole di convalida per i campi nella scheda Generale delle righe dell'offerta basate sul progetto

**Regola 1**: se il campo **Attività incluse** è vuoto o se è impostato su **Tutte le attività di progetto**, un progetto è incluso nella riga dell'offerta.

**Regola 2**: se il campo **Attività incluse** è vuoto o se è impostato su **Tutte le attività di progetto**, un progetto e una determinata classe di transazione possono essere inclusi solo in una riga di offerta basata su progetto di un'offerta.

**Regola 3**: se il campo **Attività incluse** è vuoto o se è impostato su **Solo le attività di progetto selezionate**, un progetto e una determinata classe di transazione possono essere inclusi in più righe di offerta basata su progetto di un'offerta.

**Regola 4**: se un'opportunità ha più offerte, possono esserci righe di offerta da offerte diverse che fanno tutte riferimento allo stesso progetto e includono la stessa classe di transazione.

**Regola 5**: se le offerte non appartengono alla stessa opportunità, non possono includere lo stesso progetto e la stessa classe di transazione.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Opportunità</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Offerta</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Riga di offerta</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
                <p>
                    <strong>Attività incluse</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Includi tempo</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Includi spesa</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Includi</strong>
                </p>
                <p>
                    <strong>Tariffa</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Valido/Non valido</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Motivo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Foglio bianco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Non valido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violazione della regola n. 2. Tempistica, spesa e commissioni sul progetto P1 sono incluse nelle righe dell'offerta QL1 e QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Foglio bianco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Foglio bianco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Non valido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violazione della regola n. 2. Tempistica e commissioni sul progetto P1 sono incluse nelle righe dell'offerta QL1 e QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Foglio bianco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Foglio bianco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Valido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
Tempistica e commissioni sul progetto P1 sono incluse in QL1.
La spesa sul progetto P1 è inclusa in QL2.
Non c'è sovrapposizione tra gli elementi inclusi in ogni riga dell'offerta ed è valido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Foglio bianco </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Solo le attività selezionate </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Non valido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violazione della regola n. 2 precedente </p>
                <p>
Q1 include tempistica, spese e commissioni per un sottoinsieme di attività nel progetto P1.
                </p>
                <p>
QL2 include tempistica, spese e commissioni per l'intero progetto P1 e si sovrappone a quanto incluso in Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Foglio bianco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Solo le attività selezionate </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Valido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
In base alla regola n. 3 precedente, </p>
                <p>
Q1 include tempistica, spese e commissioni per un sottoinsieme di attività nel progetto P1.
                </p>
                <p>
QL2 include tempistica, spese e commissioni per un sottoinsieme di attività nel progetto P1.
                </p>
                <p>
L'unica convalida aggiuntiva riguarda il sottoinsieme di attività in QL1 che è diverso dal sottoinsieme di attività in QL2. In questo modo si garantisce che non vi siano sovrapposizioni. Ciò viene eseguito dal sistema quando vengono associate le attività.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Solo le attività selezionate </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tutte le attività di progetto o vuoto </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="54" valign="top">
                <p>
Valido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
In base alla regola n. 5, Q1 e Q2 sono due offerte della stessa opportunità, quindi possono entrambe eseguire una stima per gli stessi componenti di un progetto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Secondo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tutte le attività di progetto o vuoto </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tutte le attività di progetto o vuoto </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="54" valign="top">
                <p>
Valido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
In base alla regola n. 4, Q1 e Q2 sono due offerte di opportunità diverse, quindi non possono eseguire una stima per gli stessi componenti dello stesso progetto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tutte le attività di progetto o vuoto </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="48" valign="top">
                <p>
Sì </p>
            </td>
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="54" valign="top">
                <p>
Non valido </p>
            </td>
        </tr>
    </tbody>
</table>

