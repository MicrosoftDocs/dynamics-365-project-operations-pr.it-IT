---
title: Panoramica delle voci di contratto basate su progetto
description: Questo argomento fornisce informazioni sull'utilizzo delle voci di contratto basate su progetto.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 7da8a7f898e6f0bb46d4cf6de65812e3aabb7416a2fdf2f9d9c8bad07e77cd85
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999051"
---
# <a name="project-based-contract-lines-overview"></a>Panoramica delle voci di contratto basate su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le voci di contratto basate su progetto in Dynamics 365 Project Operations sono progettate per contenere i contratti di stima e fatturazione per componenti specifici del lavoro di progetto su un impegno. La struttura di una voce di contratto basata su progetto viene estesa per le stime di progetto e gli scenari di fatturazione con i seguenti concetti:

- Metodo di fatturazione
- Mapping di progetti e attività
- Classi di transazione incluse
- Limite da non superare
- Impostazione dell'esigibilità
- Stime utilizzando i dettagli della voce di contratto
- Clienti voce di contratto

La tabella seguente include i campi nella scheda **Generale** delle voci di contratto basate su progetto che aiutano a creare le basi per una stima dettagliata e iniziale e le modalità di fatturazione per il lavoro basato su progetto.

| Campo | Descrizione | Impatto downstream |
| --- | --- | --- |
| **Nome** | Nome della voce di contratto. Identifica il componente discreto del contratto che si sta stimando. Per un contratto di progetto creato da un'offerta, questo valore viene copiato da un valore corrispondente della riga di offerta basata su progetto. | Il nome copiato nella riga di fattura di progetto creata da questa voce di contratto quando viene creata la fattura. |
| **Metodo di fatturazione** | In un contratto di progetto creato da un'offerta, questo valore viene copiato dal campo corrispondente della riga di offerta. Questo è un set di opzioni che rappresenta i due principali modelli di contratto supportati da Project Operations:</br>- **Prezzo fisso**</br>- **Tempistica e materiali** | In base al metodo di fatturazione della voce di contratto a cui si fa riferimento, verrà elaborata la transazione effettiva. Se la voce di contratto a cui fa riferimento il valore effettivo dispone di un metodo di fatturazione di tempo e materiale, vengono creati i record dei costi e delle vendite non fatturate. Se la voce di contratto a cui fa riferimento il valore effettivo ha un metodo di fatturazione a prezzo fisso, viene creato solo un costo effettivo. |
| **Project** | Utilizza questo campo per identificare il progetto che verrà utilizzato per fornire il lavoro su questo impegno. | Questo valore verrà utilizzato insieme a **Attività incluse** e **Classi di transazione incluse** per risolvere il riferimento della voce di contratto in un record di riga effettivo o di stima. |
| **Attività incluse** | Indica se questa voce di contratto include tutte le attività di progetto per il progetto selezionato o solo un sottoinsieme delle attività. È un set di opzioni con i seguenti possibili valori:</br>- **Tutte le attività di progetto**</br>- **Solo le attività di progetto selezionate**. Un valore vuoto in questo campo è uguale alla selezione di **Tutte le attività di progetto**. | Se **Solo attività selezionate** è selezionato, puoi selezionare attività specifiche e associarle a questa voce di contratto nella scheda **Configurazione fatturazione attività** della pagina **Progetto**. Il valore verrà utilizzato insieme a **Progetto** e **Classi di transazione incluse** per risolvere il riferimento della voce di contratto in un record di riga effettivo o di stima. |
| **Includi tempo** | Un valore **Sì**/**No** indica se le transazioni di tempo o i costi di manodopera nel progetto selezionato saranno inclusi in questa voce di contratto. Il valore **No** indica che le transazioni di tempo o i costi di manodopera non verranno inclusi in questa voce di contratto. Il valore **Sì** indica che verranno inclusi. | Questo valore viene utilizzato insieme al progetto per risolvere il riferimento della voce di contratto in un record di riga effettiva o di stima. |
| **Includi spesa** | Un valore **Sì**/**No** indica se i costi di spesa nel progetto selezionato saranno inclusi in questa voce di contratto. Il valore **No** indica che i costi di spesa non verranno inclusi in questa voce di contratto. Il valore **Sì** indica che verranno inclusi. | Questo valore viene utilizzato insieme al progetto per risolvere il riferimento della voce di contratto in un record di riga effettiva o di stima. |
| **Includi materiali** | Un valore **Sì**/**No** indica se i costi di materiale nel progetto selezionato saranno inclusi in questa voce di contratto. Un valore **No** indica che i costi materiale non saranno inclusi in questa voce di contratto. Il valore **Sì** indica che verranno inclusi. | Questo valore viene utilizzato insieme al progetto per risolvere il riferimento della voce di contratto in un record di riga effettiva o di stima. |
| **Includi commissione** | Un valore **Sì**/**No** indica se le commissioni nel progetto selezionato saranno inclusi in questa voce di contratto. Il valore **No** indica che le commissioni non verranno incluse in questa voce di contratto. Il valore **Sì** indica che verranno inclusi. | Questo valore viene utilizzato insieme al progetto per risolvere il riferimento della voce di contratto in un record di riga effettiva o di stima. |
| **Importo contratto** | In una voce di contratto a prezzo fisso, questo importo è il valore concordato che verrà fatturato al cliente per tutti i componenti di lavoro associati a questa voce di contratto. In una voce di contratto tempo e materiale, questo importo è il valore stimato che verrà fatturato al cliente per tutti i componenti di lavoro associati a questa voce di contratto. In un contratto di progetto creato da un'offerta, questo valore viene copiato dal campo corrispondente della riga di offerta. Quando una voce di contratto basata su progetto include dettagli di riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo nei dettagli della voce di contratto. | Quando la voce di contratto include i dettagli della riga, questo valore può essere modificato modificando gli importi dei dettagli della riga. In una voce di contratto a prezzo fisso, questo valore viene utilizzato per generare l'importo prima delle imposte sui passaggi fondamentali di fatturazione periodica. |
| **Imposta stimata** | L'utente può modificare questo campo per inserire l'importo delle imposte stimato nella voce di contratto. Quando una voce di contratto basata su progetto include dettagli di riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo delle imposte nei dettagli della voce di contratto. | Quando la voce di contratto include i dettagli della riga, questo valore può essere modificato modificando gli importi delle imposte dei dettagli della riga. In una voce di contratto a prezzo fisso, questo valore viene utilizzato per generare le imposte sui passaggi fondamentali di fatturazione periodica. |
| **Importo contratto al netto delle imposte** | L'importo della voce di contratto al netto delle imposte. Questo campo è di sola lettura e viene calcolato come **importo di contratto + imposte**. | In una voce di contratto a prezzo fisso, questo valore viene utilizzato per generare i passaggi fondamentali di fatturazione periodica. |
| **Limite da non superare** | L'utente può modificare questo campo ed è disponibile solo sulle voci di contratto basate su progetto che hanno il metodo di fatturazione impostato come tempo e materiale. | L'utente può modificare questo campo. Quando un valore effettivo per tempo e materiale fa riferimento a questa voce di contratto per tempo e materiale, l'importo del valore effettivo viene valutato rispetto al limite da non superare della voce di contratto. Questa valutazione è completata dopo aver contabilizzato gli importi già spesi e impegnati. |
| **Budget cliente** | Questo campo è modificabile e viene viene copiato dal campo corrispondente della riga di offerta se il contratto è stato creato da un'offerta. | Questo campo è utilizzato solo per informazioni e non ha alcun significato downstream. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regole di convalida per le opzioni nella scheda Generale delle voci di contratto basate su progetto

Regola 1: se il campo **Attività incluse** è vuoto o impostato su **Tutte le attività di progetto**, tutte le attività di progetto sono incluse nella voce di contratto.

Regola 2: quando il campo **Attività incluse** è vuoto o impostato esplicitamente su **Tutte le attività di progetto**, un progetto e una determinata classe di transazione possono essere inclusi solo in una voce di contratto basata su progetto di un contratto.

Regola 3: quando il campo **Attività incluse** impostato esplicitamente su **Solo le attività di progetto selezionate**, un progetto e una determinata classe di transazione possono essere inclusi in più voci di contratto basata su progetto di un contratto.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Contratto</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Voce di contratto</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
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
                    <strong>Includi materiali</strong>
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
            <td width="53" valign="top">
                <p>
                    <strong>Valido/Non valido</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Motivo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vuoto </p>
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
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Non valido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violazione della regola n. 2. Tempo, spesa, materiali e commissioni nel progetto P1 sono inclusi nelle voci di contratto CL1 e CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vuoto </p>
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
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vuoto </p>
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
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Non valido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violazione della regola n. 2. Tempo, materiali e commissioni nel progetto P1 sono inclusi nelle voci di contratto CL1 e CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vuoto </p>
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
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vuoto </p>
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
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Valido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Tempo, materiali e commissioni nel progetto P1 sono incluse in CL1.
                </p>
                <ul>
                    <li>
La spesa sul progetto P1 è inclusa in CL2.
                    </li>
                </ul>
                <p>
Nessuna sovrapposizione in ciò che viene incluso in ogni voce di contratto e quindi valido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vuoto </p>
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
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Non valido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violazione della regola n. 2 </p>
                <p>
C1 include tempo, materiali, spese e commissioni in un sottoinsieme di attività nel progetto P1.
                </p>
                <p>
CL2 include tempo, materiali, spese e commissioni per l'intero progetto P1 e quindi si sovrappone a quanto incluso in C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vuoto </p>
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
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Valido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Per la regola n. 3 </p>
                <p>
C1 include tempo, spese, materiali e commissioni in un sottoinsieme di attività nel progetto P1.
                </p>
                <p>
CL2 include tempo, spese, materiali e commissioni per un sottoinsieme di attività nel progetto P1.
                </p>
                <p>
L'unica convalida aggiuntiva riguarda il sottoinsieme di attività in CL1 che è diverso dal sottoinsieme di attività in CL2 per garantire che non vi siano sovrapposizioni. Ciò viene eseguito dal sistema quando vengono associate le attività.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sì </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
