---
title: Confermare una fattura proforma - semplice
description: Questo argomento fornisce informazioni sulla conferma di una fattura proforma in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176526"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Confermare una fattura proforma - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_


Dopo la conferma di una fattura proforma, lo stato della fattura di progetto viene aggiornato su **Confermato**. Quando una fattura viene confermata, diventa di sola lettura. In futuro, la fattura può essere corretta solo se sono presenti correzioni o accrediti avviati dal cliente o se la fattura è contrassegnata come pagata.

Nella tabella seguente sono elencati i valori effettivi creati dal sistema. Questi valori effettivi vengono creati quando vengono eseguite determinate operazioni sulla bozza della fattura di progetto prima che venga confermata.

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
Fatturazione di un anticipo o di un acconto </p>
            </td>
            <td width="408" valign="top">
                <p>
Un valore effettivo della vendita fatturata di tipo <strong>Acconto</strong> viene creato per l'importo dell'anticipo o dell'acconto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un valore effettivo delle vendite non fatturate di un importo negativo dell'acconto o dell'anticipo da utilizzare per la riconciliazione.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Dopo aver riconciliato completamente un acconto o un anticipo su una fattura.
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
Un valore effettivo delle vendite fatturate per l'importo della fattura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Dopo aver riconciliato parzialmente un acconto o un anticipo su una fattura.
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
Un valore effettivo delle vendite fatturate per l'importo della fattura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un valore effettivo negativo delle vendite non fatturate di un importo dell'acconto o dell'anticipo rimanente da utilizzare per la riconciliazione nelle future fatture.
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
Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate non addebitabile per le ore e l'importo rimanenti dopo la deduzione delle cifre corrette nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite e un valore effettivo delle vendite fatturate equivalente.
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
Un valore effettivo delle vendite fatturate per la quantità e l'importo sull'approvazione della spesa originale </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
La fatturazione della voce di contratto basata su prodotto.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Un valore effettivo delle vendite fatturate per la riga di prodotto con la quantità e l'importo provenienti dalla voce di contratto basata su prodotto.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]