---
title: Confermare un contratto di progetto
description: Questo argomento fornisce informazioni su come confermare un contratto in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128288"
---
# <a name="confirm-a-project-contract"></a>Confermare un contratto di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Un contratto di progetto in Dynamics 365 Project Operations può essere attivo con motivo **Confermato** o chiuso con un motivo **Perso**. Quando confermi un contratto di progetto, lo stato viene aggiornato da **Bozza** ad **Attivo** e il motivo dello stato è **Confermato**. Un contratto attivo o chiuso non può essere modificato o riaperto. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Impatto finanziario della conferma di un contratto di progetto

Dopo che un contratto di progetto viene confermato, l'applicazione ricalcola i costi stornando i valori effettivi di costo precedenti e creando nuovi valori effettivi di costo. I nuovi valori effettivi vengono elaborati in base al metodo di fatturazione della voce di contratto di progetto associata. Se i valori effettivi di costo fanno riferimento a una voce di contratto per tempistica e materiali, l'applicazione ricrea automaticamente i valori effettivi di vendita non fatturati corrispondenti. Se i costi effettivi fanno riferimento a una voce di contratto a prezzo fisso, l'applicazione interrompe la rielaborazione dei valori effettivi di costo.

I limiti da non superare, l'impostazione dell'esigibilità e la determinazione del prezzo e dei costi sui valori effettivi vengono valutati e quindi aggiornati come parte del processo di conferma.

## <a name="close-a-project-contract-as-lost"></a>Chiudere un contratto di progetto come perso

Quando chiudi un contratto di progetto come perso, lo stato del contratto viene aggiornato a **Chiuso** e il motivo dello stato è **Perso**. Il contratto di progetto diventa di sola lettura. Viene visualizzata una finestra di dialogo di conferma prima del completamento delle modifiche poiché non è possibile riaprire un contratto di progetto chiuso.

Se il contratto di progetto chiuso come perso fa riferimento a un progetto nelle righe, anche quel progetto viene contrassegnato come chiuso. Qualsiasi prenotazione di risorse da quel giorno in poi viene annullata. Eventuali valori effettivi di vendita non fatturati nel contratto di progetto che non sono già presenti in una fattura verranno stornati.

> [!NOTE]
> In Dynamics 365 Project Operations, la chiusura di un contratto di progetto come perso non influirà sullo stato dell'opportunità associata. L'opportunità rimarrà aperta e dovrà essere chiusa manualmente.
