---
title: Chiudere un'offerta - semplice
description: Questo argomento fornisce informazioni sulla chiusura di un'offerta in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175716"
---
# <a name="close-a-quote---lite"></a>Chiudere un'offerta - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Un'offerta di progetto può essere chiusa come acquisita o persa. Le operazioni Attiva e Aggiorna sulle offerte non sono supportate in Microsoft Dynamics 365 Project Operations, quindi è possibile chiudere un'offerta in bozza.

## <a name="close-a-quote-as-won"></a>Chiudere un'offerta come acquisita

La chiusura di un'offerta di progetto come acquisita chiuderà l'offerta con lo stato impostato su Chiusa e il motivo stato impostato su Acquisita. La chiusura dell'offerta rende l'offerta di progetto di sola lettura e crea un contratto di progetto in bozza che contiene le informazioni sull'offerta. Viene visualizzata una finestra di dialogo di conferma prima che vengano apportate le modifiche poiché un'offerta chiusa non può essere riaperta e le modifiche sono irreversibili.

Se l'offerta è collegata a un'opportunità, qualsiasi altra offerta di progetto dell'opportunità viene automaticamente chiusa come persa.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impatto finanziario della chiusura di un'offerta come acquisita

Se sono stati registrati dei valori effettivi per il tempo in un progetto mentre è ancora collegato a un'offerta in bozza, viene registrato solo il costo del tempo o della spesa. Dopo che un'offerta è stata chiusa come acquisita, l'applicazione effettuerà il refactoring dei costi annullando i valori effettivi di costo precedenti e ricreando nuovi valori effettivi di costo. L'applicazione elaborerà questi valori effettivi di costo in base al metodo di fatturazione della voce di contratto di progetto associata. Se i valori effettivi di costo fanno riferimento a una voce di contratto di tempistica e materiali, il sistema creerà automaticamente i valori effettivi di vendita non fatturati corrispondenti quando l'offerta viene chiusa e il contratto di progetto viene creato. Se i valori effettivi di costo fanno riferimento a una voce di contratto a prezzo fisso, l'applicazione interromperà la rielaborazione dei valori effettivi di costo in base alle regole di fatturazione separata per i clienti del contratto di progetto.

## <a name="closing-a-quote-as-lost"></a>Chiusura di un'offerta come persa:

La chiusura di un'offerta come persa imposterà lo stato su Chiusa e il motivo stato su Persa. La chiusura dell'offerta rende l'offerta di progetto di sola lettura. Poiché un'offerta chiusa non può essere riaperta, prima di chiudere un'offerta una finestra di dialogo di conferma confermerà le modifiche.

Se l'offerta di progetto chiusa come persa fa riferimento a un progetto in una delle sue righe, anche quel progetto viene contrassegnato come chiuso e tutte le prenotazioni di risorse da quel giorno in poi vengono annullate.

> [!NOTE]
> In Project Operations, la chiusura di un'offerta come acquisita o persa non influirà sullo stato dell'opportunità, che rimarrà aperta fino a quando non verrà chiusa manualmente.
