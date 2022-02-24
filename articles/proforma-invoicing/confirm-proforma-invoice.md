---
title: Confermare una fattura proforma
description: Questo argomento fornisce informazioni sulla conferma di una fattura proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128108"
---
# <a name="confirm-a-proforma-invoice"></a>Confermare una fattura proforma

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Dopo la conferma di una fattura proforma, lo stato della fattura di progetto viene aggiornato su **Confermato**. Quando una fattura viene confermata, diventa di sola lettura. In futuro, la fattura può essere corretta solo se sono presenti correzioni o accrediti avviati dal cliente o se è contrassegnata come pagata.

Nella tabella seguente sono elencati i valori effettivi creati dal sistema. Questi valori effettivi vengono creati quando vengono eseguite determinate operazioni sulla bozza della fattura di progetto prima che venga confermata.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Scenario</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Valori effettivi creati alla conferma</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fatturazione di una transazione di tempo senza modifiche sulla fattura in bozza.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite non fatturate per le ore e l'importo nell'approvazione del tempo originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un valore effettivo delle vendite fatturate per le ore e l'importo sull'approvazione del tempo originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
La fatturazione di una transazione temporale modificata per ridurre la quantità.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite non fatturate per le ore e l'importo nell'approvazione del tempo originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate non addebitabile per le ore e l'importo rimanenti dopo la deduzione delle cifre corrette nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
La fatturazione di una transazione temporale modificata per aumentare la quantità.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite non fatturate per le ore e l'importo nell'approvazione del tempo originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fatturazione di una transazione di spesa senza modifiche sulla fattura in bozza.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite non fatturate per la quantità e l'importo sull'approvazione della spesa originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un valore effettivo delle vendite fatturate per la quantità e l'importo sull'approvazione della spesa originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
La fatturazione di una transazione di spesa modificata per ridurre la quantità.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite non fatturate per la quantità e l'importo sull'approvazione della spesa originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate non addebitabile per la quantità e l'importo rimanenti dopo la deduzione delle cifre corrette nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
La fatturazione di una transazione di spesa modificata per aumentare la quantità.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite non fatturate per la quantità e l'importo sull'approvazione della spesa originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fatturazione di una commissione.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno delle vendite non fatturate per l'importo della commissione nella riga di registrazione originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un valore effettivo delle vendite fatturate per la quantità e l'importo nella riga di registrazione della commissione originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
La fatturazione di un passaggio fondamentale.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Un valore effettivo delle vendite fatturate per l'importo nel passaggio fondamentale della voce di contratto di progetto.
                </p>
            </td>
        </tr>
    </tbody>
</table>
