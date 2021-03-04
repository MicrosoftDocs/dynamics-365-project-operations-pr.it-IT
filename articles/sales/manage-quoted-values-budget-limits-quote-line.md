---
title: Panoramica delle righe dell'offerta basate su progetto
description: Questo argomento fornisce informazioni sull'utilizzo delle righe dell'offerta basate sul progetto per il lavoro del progetto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181862"
---
# <a name="project-based-quote-lines-overview"></a>Panoramica delle righe dell'offerta basate su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Le righe dell'offerta basate sul progetto sono progettate per aiutare a stimare il lavoro del progetto per un impegno. La struttura di una riga dell'offerta basata sul progetto è estesa per le stime di progetto con i seguenti concetti:

- Metodo di fatturazione
- Mapping del progetto
- Classi di transazione incluse
- Limite da non superare
- Impostazione dell'esigibilità
- Stima utilizzando i dettagli della riga dell'offerta
- Clienti riga di offerta

La tabella seguente fornisce informazioni sui campi nella scheda **Generale** della riga dell'offerta basata sul progetto. Questi campi aiutano a creare le basi per una stima dettagliata e completa del lavoro del progetto.

| **Campo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- |
| Nome | Il nome della riga dell'offerta che dovrebbe aiutarti a identificare il componente discreto dell'offerta che viene stimata. | Copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Metodo di fatturazione | In un'offerta creata da un'opportunità, questo valore viene copiato dal campo corrispondente nella riga dell'opportunità. Questo campo include i due principali modelli di contratto supportati da Dynamics 365 Project Operations:</br>- Prezzo fisso</br>- Tempistica e materiali.| Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Project | Utilizza questo campo facoltativo per identificare il progetto che verrà utilizzato per fornire il lavoro su questo impegno. Quando un progetto viene mappato a una riga dell'offerta, viene semplificata l'impostazione delle attività addebitabili e anche l'inserimento di una stima basata sul progetto nella riga dell'offerta come dettagli della riga dell'offerta. Quando un progetto non è mappato a una riga dell'offerta basata sul progetto, la stima deve essere creata manualmente creando ogni dettaglio della riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Includi tempo | Un contrassegno **Sì**/**No** indica se le transazioni temporali o i costi di manodopera sul progetto selezionato saranno inclusi nella stima su questa riga dell'offerta. Un valore **No** indica che le transazioni temporali o i costi di manodopera non saranno inclusi nella stima su questa riga dell'offerta. Un valore **Sì** indica che le transazioni temporali o i costi di manodopera saranno inclusi nella stima su questa riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Includi spesa | Un contrassegno **Sì**/**No** indica se i costi di spesa sul progetto selezionato saranno inclusi nella stima su questa riga dell'offerta. Un valore **No** indica che i costi di spesa non saranno inclusi nella stima su questa riga dell'offerta. Un valore **Sì** indica che i costi di spesa saranno inclusi nella stima su questa riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Includi commissione | Un contrassegno **Sì**/**No** indica se le commissioni sul progetto selezionato saranno incluse nella stima su questa riga dell'offerta. Un valore **No** indica che le commissioni non saranno incluse nella stima su questa riga dell'offerta. Un valore **Sì** indica che le commissioni saranno incluse nella stima su questa riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Importo offerto | Questo è l'importo che verrà offerto al cliente per tutto il lavoro previsto in questa riga dell'offerta basata sul progetto. In un'offerta creata da un'opportunità, questo valore viene copiato dal campo **Budget cliente** nella riga dell'opportunità. Quando la riga dell'offerta basata sul progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo nei dettagli della riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Imposta stimata | Questo è un campo modificabile che consente all'utente di aggiungere l'importo delle imposte stimate nella riga dell'offerta. Quando una riga dell'offerta basata sul progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo delle imposte nei dettagli della riga dell'offerta. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Importo offerto al netto delle imposte | Questo campo rappresenta l'importo della riga dell'offerta al netto delle imposte ed è di sola lettura. L'importo in questo campo viene calcolato come *Importo offerto + imposte*. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Limite da non superare | Questo campo è modificabile ed è disponibile solo per le righe dell'offerta basate su progetto che hanno un metodo di fatturazione **Tempistica e materiali**. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |
| Budget cliente | Questo campo è modificabile e viene copiato dal campo corrispondente nella riga dell'opportunità se l'offerta è stata creata da un'opportunità. | Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regole di convalida per i campi nella scheda Generale delle righe dell'offerta basate sul progetto

**Regola 1**: una determinata classe di transazione sul progetto selezionato può essere inclusa solo in una riga dell'offerta basata sul progetto di un'offerta.

**Regola 2**: se un'opportunità ha più offerte, possono esserci righe di offerta da offerte diverse che fanno tutte riferimento allo stesso progetto e includono la stessa classe di transazione.

**Regola 3**: se le offerte non appartengono alla stessa opportunità, non possono includere lo stesso progetto e la stessa classe di transazione.

<table border="1" cellspacing="0" cellpadding="0">
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
            <td width="48" valign="top">
                <p>
                    <strong>Includi tempistica</strong>
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
                    <strong>Commissione</strong>
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
Violazione della regola n. 1. Tempistica, spesa e commissioni sul progetto P1 sono inclusi in entrambe le righe dell'offerta, QL1 e QL2.
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
Violazione della regola n. 1. Tempistica e commissioni sul progetto P1 sono incluse in entrambe le righe dell'offerta, QL1 e QL2.
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
Non c'è sovrapposizione tra gli elementi inclusi in ogni riga dell'offerta quindi è valido.
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
Violazione della regola n. 1 precedente </p>
                <p>
Q1 include tempistica, spese e commissioni per l'intero progetto P1.
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
In base alla regola n. 2, Q1 e Q2 sono due offerte della stessa opportunità, quindi possono entrambe eseguire una stima per gli stessi componenti di un progetto.
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
QL1 su Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
In base alla regola n. 3, Q1 e Q2 sono due offerte di opportunità diverse, quindi non possono eseguire una stima per gli stessi componenti dello stesso progetto.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]