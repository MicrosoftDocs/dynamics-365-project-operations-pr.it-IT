---
title: Creare fatture basate su progetto correttive
description: Questo argomento fornisce informazioni sulle fatture correttive in Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 27db247b5bcac47a44eb24ade07452cbccb8f968
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590527"
---
# <a name="create-corrective-project-based-invoices"></a>Creare fatture basate su progetto correttive 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Una fattura di progetto confermata può essere corretta per elaborare modifiche o crediti come negoziato con il cliente e il project manager.

Per apportare modifiche a una fattura confermata, apri la fattura confermata e seleziona **Correggi questa fattura**. 

> [!NOTE]
> Questa selezione non è disponibile se la fattura di progetto non è confermata.

Viene creata una nuova fattura in bozza dalla fattura confermata. Tutti i dettagli della riga della fattura confermata in precedenza vengono copiati nella nuova bozza. Di seguito sono riportati alcuni punti chiave per aiutarti a comprendere meglio i dettagli della riga nella nuova fattura corretta:

- Tutte le quantità vengono aggiornate a zero. Ciò presuppone che tutti gli articoli fatturati siano completamente accreditati. Se necessario puoi aggiornare manualmente queste quantità per riflettere la quantità che viene fatturata e non la quantità che viene accreditata. In base alla quantità immessa, l'applicazione calcola la quantità accreditata. Questo importo si riflette nei valori effettivi creati quando la fattura corretta viene confermata. Se stai apportando modifiche all'importo delle imposte, devi immettere l'importo delle imposte corretto e non l'importo delle imposte che viene accreditato.
- Le correzioni fondamentali vengono sempre elaborate come crediti completi.
- Gli importi di acconto o anticipo possono essere corretti se al cliente è stato fatturato un importo errato.
- Le riconciliazioni di acconti e anticipi possono essere corrette se è stato utilizzato un importo errato per la riconciliazione con gli addebiti di una fattura precedentemente confermata.

> [!IMPORTANT]
> Per i dettagli della riga fattura che sono correzioni ad altri addebiti già fatturati, il campo **Correzione** è impostato su **Sì**. Le fatture con i dettagli della riga fattura corretti hanno anche un campo chiamato **Include correzioni** impostato su **Sì**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Valori effettivi creati alla conferma di una fattura correttiva

La tabella seguente elenca i valori effettivi creati quando viene confermata una fattura correttiva.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Valori effettivi creati alla conferma</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Conferma la correzione di un anticipo o un acconto fatturato.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite non fatturate dell'acconto o dell'anticipo creato per la riconciliazione. Questo importo è positivo perché ha lo scopo di annullare il negativo che è stato creato al momento della fatturazione dell'acconto o dell'anticipo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Viene creato un valore effettivo di storno delle vendite fatturate per l'importo dell'acconto o dell'anticipo per stornare le vendite fatturate originali.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Viene creato un nuovo valore effettivo di vendite fatturate per l'importo corretto nella riga fattura corretta basata sull'anticipo o sull'acconto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un valore effettivo delle vendite non fatturate dell'importo negativo della riga fattura corretta basata sull'acconto o sull'anticipo che verrà utilizzata per la riconciliazione.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Una conferma della correzione di un acconto o un anticipo precedentemente riconciliato.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite non fatturate dell'acconto o dell'anticipo creato per la riconciliazione. Questo importo è positivo e ha lo scopo di annullare il negativo che è stato creato al momento della precedente riconciliazione.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un valore effettivo di storno delle vendite fatturate per l'importo della fattura precedente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo di vendite fatturate per l'importo dell'acconto corretto applicato nella fattura corretta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un valore effettivo delle vendite non fatturate con un importo negativo dell'acconto o dell'anticipo corretto rimanente che verrà utilizzato per la riconciliazione di fatture successive.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
La fatturazione del credito completo di una transazione temporale precedentemente fatturata.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite fatturate per le ore e l'importo nel dettaglio della riga fattura originale per il tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate per le ore e l'importo nel dettaglio della riga fattura originale per il tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
La fatturazione dell'accredito parziale su una transazione temporale.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite fatturate per le ore e l'importo fatturato nel dettaglio della riga fattura originale per il tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nel dettaglio della riga fattura modificata, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo rimanente dopo aver dedotto le cifre corrette nel dettaglio della riga fattura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
La fatturazione del credito completo di una transazione di spesa precedentemente fatturata.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la spesa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la spesa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
La fatturazione del credito parziale di una transazione di spesa precedentemente fatturata.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite fatturate per la quantità e l'importo fatturato nel dettaglio della riga fattura originale per una spesa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura corretta, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo rimanente dopo aver dedotto le cifre corrette nel dettaglio della riga fattura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
La fatturazione del credito completo di una transazione di commissione precedentemente fatturata.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la commissione.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la commissione.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
La fatturazione del credito parziale di una transazione di commissione precedentemente fatturata.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite fatturate per la quantità e l'importo fatturato nel dettaglio della riga fattura originale per la commissione.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura correttiva modificata, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
La fatturazione del credito completo di un passaggio fondamentale precedentemente fatturato.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite fatturate per l'importo nel dettaglio della riga fattura originale per il passaggio fondamentale.
                </p>
                <p>
Lo stato della fattura nel passaggio fondamentale viene aggiornato da <b>Fattura cliente registrata</b> a <b>Pronto per la fatturazione</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
La fatturazione del credito parziale di un passaggio fondamentale precedentemente fatturato.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Non supportato </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
