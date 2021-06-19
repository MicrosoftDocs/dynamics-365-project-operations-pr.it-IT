---
title: Confermare una fattura di progetto proforma
description: Questo argomento fornisce informazioni sulla conferma di fatture di progetto proforma in Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004131"
---
# <a name="confirm-a-proforma-project-invoice"></a>Confermare una fattura di progetto proforma 

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_


Dopo la conferma di una fattura proforma, lo stato della fattura di progetto viene aggiornato su **Confermato**. Quando una fattura viene confermata, diventa di sola lettura. In futuro, la fattura potrà essere corretta solo se sono presenti correzioni o accrediti avviati dal cliente.

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
Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate non addebitabile per le ore e l'importo rimanenti dopo la deduzione delle cifre corrette nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite e un valore effettivo delle vendite fatturate equivalente.
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
Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.
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
Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate non addebitabile per la quantità e l'importo rimanenti dopo la deduzione delle cifre corrette nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.
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
Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fatturazione di una transazione materiale senza modifiche nella bozza di fattura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno vendite non fatturate per la quantità e l'importo nell'approvazione dell'utilizzo di materiale originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un valore effettivo delle vendite fatturate per la quantità e l'importo nell'approvazione dell'utilizzo di materiale originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fatturazione di una transazione materiale modificata per ridurre la quantità.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno vendite non fatturate per la quantità e l'importo nell'approvazione del tempo originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate non addebitabile per la quantità e l'importo rimanenti dopo la deduzione delle cifre corrette nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fatturazione di una transazione materiale modificata per aumentare la quantità.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uno storno vendite non fatturate per la quantità e l'importo nell'approvazione dell'utilizzo di materiale originale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.
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
