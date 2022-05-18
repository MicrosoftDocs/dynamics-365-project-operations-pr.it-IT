---
title: Panoramica delle righe di offerta basate su progetto
description: Questo argomento fornisce informazioni sull'utilizzo delle righe di offerta basate su progetto per il lavoro del progetto.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a9661d9b91ffeece4c66b129846632b30ebebc8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591087"
---
# <a name="project-based-quote-lines-overview"></a>Panoramica delle righe di offerta basate su progetto 

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma, Project Operations per scenari basati su risorse/materiali non stoccati_

Le righe di offerta basate su progetto sono progettate per aiutare a stimare il lavoro del progetto per un impegno. La struttura di una riga di offerta basata su progetto è estesa per le stime di progetto con i seguenti concetti:

- Metodo di fatturazione
- Mapping di progetti e attività
- Classi di transazione incluse
- Limite da non superare
- Impostazione dell'esigibilità
- Stima che utilizza i dettagli della riga di offerta
- Clienti riga di offerta

La tabella seguente fornisce informazioni sui campi nella scheda **Generale** della riga di offerta basata su progetto. Questi campi aiutano a creare le basi per una stima dettagliata e completa del lavoro del progetto.

| **Campo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- |
| Nome | Il nome della riga di offerta che ti consente di identificare la componente discreta dell'offerta che viene stimata. | Copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Metodo di fatturazione | In un'offerta creata da un'opportunità, questo valore viene copiato dal campo corrispondente nella riga dell'opportunità. Questo campo include i due principali modelli di contratto supportati da Dynamics 365 Project Operations:</br>- Prezzo fisso</br>- Tempistica e materiali.| Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita. |
| Project | Utilizza questo campo facoltativo per identificare il progetto che verrà utilizzato per fornire il lavoro su questo impegno. Quando un progetto viene mappato a una riga dell'offerta, viene semplificata l'impostazione delle attività addebitabili e anche l'inserimento di una stima basata sul progetto nella riga dell'offerta come dettagli della riga di offerta. Quando un progetto non è mappato a una riga di offerta basata su progetto, la stima deve essere creata manualmente creando ogni dettaglio della riga dell'offerta. | Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.|
| Attività incluse | Indica se questa riga dell'offerta viene utilizzata per tutte o alcune delle attività di progetto per il progetto selezionato. Di seguito sono riportati i valori possibili di questo campo:</br>- Tutte le attività di progetto</br>- Solo le attività di progetto selezionate</br>Un valore vuoto in questo campo equivale all'opzione **Tutte le attività di progetto**. | Quando è selezionata l'opzione **Solo le attività di progetto selezionate** nella pagina del progetto, la scheda **Configurazione fatturazione attività** consente di selezionare attività specifiche per associarle a questa riga di offerta. Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita. |
| Includi tempo | Un valore **Sì**/**No** indica se le transazioni temporali o i costi di manodopera nel progetto selezionato saranno inclusi nella stima in questa riga di offerta. Un valore **No** indica che le transazioni temporali o i costi di manodopera non saranno inclusi nella stima su questa riga dell'offerta. Un valore **Sì** indica che le transazioni temporali o i costi di manodopera saranno inclusi nella stima su questa riga dell'offerta. | Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita. |
| Includi spesa | Un valore **Sì**/**No** indica se i costi della spesa nel progetto selezionato saranno inclusi nella stima in questa riga di offerta. Un valore **No** indica che i costi di spesa non saranno inclusi nella stima su questa riga dell'offerta. Un valore **Sì** indica che i costi di spesa saranno inclusi nella stima su questa riga dell'offerta. | Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita. |
| Includi materiale | Un valore **Sì**/**No** indica se i costi materiale nel progetto selezionato saranno inclusi nella stima in questa riga di offerta. Un valore **No** indica che i costi materiale non saranno inclusi nella stima in questa riga di offerta. Un valore **Sì** indica che i costi materiale non saranno inclusi nella stima in questa riga di offerta. | Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita. |
| Includi commissione | Un valore **Sì**/**No** indica se le commissioni nel progetto selezionato saranno incluse nella stima in questa riga di offerta. Un valore **No** indica che le commissioni non saranno incluse nella stima in questa riga di offerta. Un valore **Sì** indica che le commissioni saranno incluse nella stima in questa riga di offerta. | Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita. |
| Importo offerto | Si tratta dell'importo dell'offerta al cliente per tutto il lavoro previsto in questa riga di offerta basata su progetto. In un'offerta creata da un'opportunità, questo valore viene copiato dal campo **Budget cliente** nella riga dell'opportunità. Quando la riga di offerta basata su progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo nei dettagli della riga di offerta. | Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita. |
| Imposta stimata | Questo è un campo modificabile che consente all'utente di aggiungere l'importo delle imposte stimate nella riga dell'offerta. Quando una riga di offerta basata su progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo delle imposte nei dettagli della riga di offerta. | Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita. |
| Importo offerto al netto delle imposte | Questo campo rappresenta l'importo della riga dell'offerta al netto delle imposte ed è di sola lettura. L'importo in questo campo viene calcolato come *Importo offerto + imposte*. | Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita. |
| Limite da non superare | Questo campo è modificabile ed è disponibile solo per le righe dell'offerta basate su progetto che hanno un metodo di fatturazione **Tempistica e materiali**. | Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita. |
| Budget cliente | Questo campo è modificabile e viene copiato dal campo corrispondente nella riga dell'opportunità se l'offerta è stata creata da un'opportunità. | Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regole di convalida per i campi nella scheda Generale delle righe di offerta basate su progetto

**Regola 1**: se il campo **Attività incluse** è vuoto o se è impostato su **Tutte le attività di progetto**, un progetto è incluso nella riga dell'offerta.

**Regola 2**: se il campo **Attività incluse** è vuoto o se è impostato su **Tutte le attività di progetto**, un progetto e una determinata classe di transazione possono essere inclusi solo in una riga di offerta basata su progetto di un'offerta.

**Regola 3**: se il campo **Attività incluse** è vuoto o se è impostato su **Solo le attività di progetto selezionate**, un progetto e una determinata classe di transazione possono essere inclusi in più righe di offerta basata su progetto di un'offerta.

**Regola 4**: se un'opportunità ha più offerte, possono esserci righe di offerta da offerte diverse che fanno tutte riferimento allo stesso progetto e includono la stessa classe di transazione.

**Regola 5**: se le offerte non appartengono alla stessa opportunità, non possono includere lo stesso progetto e la stessa classe di transazione.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Opportunità</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Offerta</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Riga di offerta</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Attività incluse</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Includi tempo</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Includi spesa</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Includi materiale</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Includi</strong>
                </p>
                <p>
                    <strong>Commissione</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Valido/Non valido</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Motivo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vuoto </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non valido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violazione della regola n. 2. Tempo, spesa e commissioni nel progetto P1 sono incluse nelle righe di offerta QL1 e QL2. </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vuoto </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vuoto </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non valido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violazione della regola n. 2. Tempo, materiale e commissioni nel progetto P1 sono incluse nelle righe di offerta QL1 e QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vuoto </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vuoto </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Tempo, materiale e commissioni nel progetto P1 sono incluse in QL1 <br>
La spesa nel progetto P1 è inclusa in QL2 <br>
Nessuna sovrapposizione in ciò che viene incluso in ogni riga di offerta e quindi valido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vuoto </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Solo le attività selezionate </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non valido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violazione della regola n. 2 </p>
                <p>
Q1 include tempo, materiale, spese e commissioni in un sottoinsieme di attività nel progetto P1 </p>
                <p>
QL2 include tempo, spese e commissioni per l'intero progetto P1 e quindi si sovrappone a quanto incluso in Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vuoto </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Solo le attività selezionate </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Per la regola n. 3 </p>
                <p>
Q1 include tempo, materiale, spese e commissioni in un sottoinsieme di attività nel progetto P1.
                </p>
                <p>
QL2 include tempo, materiale, spese e commissioni per un sottoinsieme di attività nel progetto P1.
                </p>
                <p>
L'unica convalida aggiuntiva riguarda il sottoinsieme di attività in QL1 che è diverso dal sottoinsieme di attività in QL2 per garantire che non vi siano sovrapposizioni. Ciò viene eseguito dal sistema quando vengono associate le attività.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Solo le attività selezionate </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tutte le attività di progetto o vuoto </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Secondo la regola n. 5, Q1 e Q2 sono due offerte della stessa opportunità, quindi possono entrambe stimare gli stessi componenti di un progetto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Secondo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tutte le attività di progetto o vuoto </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tutte le attività di progetto o vuoto </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non valido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Secondo la regola n. 4, Q1 e Q2 sono due offerte di differenti opportunità, quindi non possono stimare gli stessi componenti di un stesso progetto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
Primo trimestre </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tutte le attività di progetto o vuoto </p>
            </td>
            <td width="45" valign="top">
                <p>
Sì </p>
            </td>
            <td width="46" valign="top">
                <p>
Sì </p>
            </td>
            <td width="43" valign="top">
                <p>
Sì </p>
            </td>
            <td width="41" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
