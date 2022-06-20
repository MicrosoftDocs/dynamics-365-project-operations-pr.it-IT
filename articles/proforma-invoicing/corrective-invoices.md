---
title: Fatture basate su progetto correttive
description: Questo articolo fornisce informazioni su come creare e confermare fatture correttive basate su progetto in Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eecaf3dedeab5ff72d12808eb3144f9161313009
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931105"
---
# <a name="corrective-project-based-invoices"></a>Fatture basate su progetto correttive

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Una fattura di progetto confermata può essere corretta per elaborare modifiche o crediti come negoziato con il cliente e il project manager.

Per apportare modifiche a una fattura confermata, apri la fattura confermata e seleziona **Correggi questa fattura**. 

> [!NOTE]
> Questa selezione non è disponibile a meno che una fattura di progetto non venga confermata o la fattura basata su progetto non contenga anticipi o acconti o riconciliazioni di anticipi o acconti.

Viene creata una nuova fattura in bozza dalla fattura confermata. Tutti i dettagli della riga della fattura confermata in precedenza vengono copiati nella nuova bozza. Di seguito sono riportati alcuni dei punti chiave da comprendere sui dettagli della riga sulla nuova fattura corretta:

- Tutte le quantità vengono aggiornate a zero. Dynamics 365 Project Operations presuppone che tutti gli articoli fatturati siano completamente accreditati. Se necessario puoi aggiornare manualmente queste quantità per riflettere la quantità che viene fatturata e non la quantità che viene accreditata. In base alla quantità immessa, l'applicazione calcola la quantità accreditata. Questo importo si riflette nei valori effettivi creati quando la fattura corretta viene confermata. Se stai apportando modifiche all'importo delle imposte, devi immettere l'importo delle imposte corretto e non l'importo delle imposte che viene accreditato.
- Le correzioni fondamentali vengono sempre elaborate come crediti completi.


> [!IMPORTANT]
> Per i dettagli della riga fattura che sono correzioni ad altri addebiti già fatturati, il campo **Correzione** è impostato su **Sì**. Per le fatture con dettagli della riga fattura corretti, il campo **Include correzioni** è impostato su **Sì**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Valori effettivi creati quando una fattura correttiva viene confermata

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
Fatturazione dell'intero credito di una transazione materiale precedentemente fatturata.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno vendite fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per il materiale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo di vendita non fatturata per la quantità e l'importo nel dettaglio della riga fattura originale per il materiale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fatturazione dell'accredito parziale in una transazione materiale.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno vendite fatturate per la quantità e l'importo fatturato nel dettaglio della riga fattura originale per il materiale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura modificata, un relativo storno e un valore effettivo delle vendite fatturate equivalente.
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
Lo stato della fattura del passaggio fondamentale viene aggiornato da <b>Fattura cliente registrata</b> a <b>Pronto per la fatturazione</b>.
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
Questo scenario non è supportato.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
