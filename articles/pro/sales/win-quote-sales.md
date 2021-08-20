---
title: Chiudere un'offerta - semplice
description: Questo argomento fornisce informazioni sulla chiusura di un'offerta in Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ae5e14220ffecab5bcfa016d8d18e6ccfbc5b04be9a4e66cee26f8885125d31
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994326"
---
# <a name="close-a-quote---lite"></a>Chiudere un'offerta - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Un'offerta di progetto può essere chiusa come acquisita o persa. Una bozza di offerta può essere chiusa perché le operazioni di attivazione e revisione sulle offerte non sono supportate in Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Chiudere un'offerta come acquisita

Quando chiudi un'offerta di progetto come Acquisita, lo stato viene impostato su Chiuso e il motivo dello stato è Acquisito. La chiusura dell'offerta rende l'offerta di progetto di sola lettura e crea un contratto di progetto in bozza che contiene le informazioni sull'offerta. Poiché un'offerta chiusa non può essere riaperta, una finestra di dialogo chiederà di confermare le modifiche.

Se l'offerta è collegata a un'opportunità, qualsiasi altra offerta di progetto dell'opportunità viene automaticamente chiusa come persa.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impatto finanziario della chiusura di un'offerta come acquisita

Se sono presenti valori effettivi per l'ora in un progetto mentre è ancora collegato a una bozza di offerta, viene registrato solo il costo dell'ora o della spesa. Dopo che un'offerta è stata chiusa come acquisita, l'applicazione effettuerà il refactoring dei costi annullando i valori effettivi di costo precedenti e ricreando nuovi valori effettivi di costo. L'applicazione elaborerà questi valori effettivi di costo in base al metodo di fatturazione della voce di contratto di progetto associata. Se i valori effettivi dei costi fanno riferimento a una riga di contratto di tempo e materiali, vengono creati i valori effettivi di vendita non fatturati corrispondenti per quando l'offerta viene chiusa e il contratto di progetto viene creato. Se i costi effettivi fanno riferimento a una riga di contratto a prezzo fisso, l'applicazione interromperà la rielaborazione dei costi effettivi basati sulle regole di fatturazione suddivisa per i clienti del contratto di progetto.

## <a name="closing-a-quote-as-lost"></a>Chiusura di un'offerta come persa:

Quando chiudi un'offerta di progetto come Persa, lo stato viene impostato su Chiuso e il motivo dello stato è Perso. La chiusura dell'offerta rende l'offerta di progetto di sola lettura. Poiché un'offerta chiusa non può essere riaperta, prima di chiudere un'offerta una finestra di dialogo di conferma confermerà le modifiche.

Se l'offerta di progetto chiusa come Persa fa riferimento a un progetto in una delle sue righe, anche quel progetto viene contrassegnato come Chiuso. Qualsiasi prenotazione di risorse da quel giorno in poi viene annullata.

> [!NOTE]
> In Project Operations, la chiusura di un'offerta come acquisita o persa non influirà sullo stato dell'opportunità, che rimarrà aperta fino a quando non verrà chiusa manualmente.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]