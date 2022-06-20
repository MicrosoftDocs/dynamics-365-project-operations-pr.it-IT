---
title: Confermare un contratto di progetto
description: In questo articolo vengono fornite informazioni su come confermare un contratto in Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e92dc42c4ff6bdc40c479511c80d3e500df781a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930001"
---
# <a name="confirm-a-project-contract"></a>Confermare un contratto di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Un contratto di progetto in Dynamics 365 Project Operations può essere attivo con il motivo **Confermato** o chiuso con il motivo **Perso**. Quando confermi un contratto di progetto, lo stato viene aggiornato da **Bozza** ad **Attivo** e il motivo dello stato è **Confermato**. Un contratto attivo o chiuso non può essere modificato o riaperto. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Impatto finanziario della conferma di un contratto di progetto

Dopo che un contratto di progetto viene confermato, l'applicazione ricalcola i costi stornando i valori effettivi di costo precedenti e creando nuovi valori effettivi di costo. I nuovi valori effettivi vengono elaborati in base al metodo di fatturazione della voce di contratto di progetto associata. Se i valori effettivi di costo fanno riferimento a una voce di contratto per tempistica e materiali, l'applicazione ricrea automaticamente i valori effettivi di vendita non fatturati corrispondenti. Se i costi effettivi fanno riferimento a una voce di contratto a prezzo fisso, l'applicazione interrompe la rielaborazione dei valori effettivi di costo.

I limiti da non superare, l'impostazione dell'esigibilità e la determinazione del prezzo e dei costi sui valori effettivi vengono valutati e quindi aggiornati come parte del processo di conferma.

## <a name="close-a-project-contract-as-lost"></a>Chiudere un contratto di progetto come perso

Quando chiudi un contratto di progetto come perso, lo stato del contratto viene aggiornato a **Chiuso** e il motivo dello stato è **Perso**. Il contratto di progetto diventa di sola lettura. Viene visualizzata una finestra di dialogo di conferma prima del completamento delle modifiche poiché non è possibile riaprire un contratto di progetto chiuso.

Se il contratto di progetto chiuso come perso fa riferimento a un progetto nelle righe, anche quel progetto viene contrassegnato come chiuso. Qualsiasi prenotazione di risorse da quel giorno in poi viene annullata. Eventuali valori effettivi di vendita non fatturati nel contratto di progetto che non sono già presenti in una fattura verranno stornati.

> [!NOTE]
> In Dynamics 365 Project Operations, la chiusura di un contratto di progetto come perso non influisce sullo stato dell'opportunità associata. L'opportunità rimarrà aperta e dovrà essere chiusa manualmente.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]