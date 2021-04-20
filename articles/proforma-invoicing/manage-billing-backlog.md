---
title: Gestire il backlog di fatturazione
description: Questo argomento fornisce informazioni su come visualizzare e lavorare con il backlog di fatturazione in Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e428b551a755220cee67d54b2e63dd7a3c2ca393
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866782"
---
# <a name="manage-billing-backlog"></a>Gestire il backlog di fatturazione

_ **Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati

Dynamics 365 Project Operations dispone di viste dedicate per aiutare a gestire il backlog di fatturazione. Per gestire il backlog di fatturazione, seleziona i collegamenti nell'area **Vendite** sotto **Fatturazione**. 

Sono disponibili le seguente visualizzazioni:

- Acconti e anticipi
- Acconti e anticipi disponibili
- Passaggi fondamentali prezzo fisso
- Backlog di fatturazione tempo e materiale

## <a name="retainers-and-advances"></a>Acconti e anticipi

La visualizzazione **Acconti e anticipi** elenca gli acconti e gli anticipi in tutti i contratti di progetto. Dopo che un acconto o un anticipo è stato fatturato, l'importo dell'anticipo diventa disponibile per l'uso.

## <a name="available-retainers-and-advances"></a>Acconti e anticipi disponibili

La visualizzazione **Acconti e anticipi disponibili** elenca tutti gli acconti e gli anticipi disponibili in tutti i contratti di progetto. Dopo che un acconto o un anticipo è stato fatturato, l'importo dell'anticipo diventa disponibile per l'uso e viene aggiunto all'elenco. Dopo che l'importo dell'account o dell'anticipo è stato utilizzato completamente, viene rimosso dall'elenco.

## <a name="fixed-price-milestones"></a>Passaggi fondamentali prezzo fisso

La visualizzazione **Passaggi fondamentali prezzo fisso** elenca tutti i passaggi fondamentali in tutte le voci di contratto di progetto. In questa visualizzazione, è possibile contrassegnare uno o più passaggi fondamentali come **Pronto per la fatturazione** o **Non pronto per la fatturazione**. Contrassegnando un passaggio fondamentale come **Pronto per la fatturazione** lo si rende disponibile per essere inserito in una bozza di fattura.

Quando le voci di contratto con più clienti hanno un metodo di fatturazione a prezzo fisso, viene creato un passaggio fondamentale per ogni cliente nella voce di contratto. È possibile creare un passaggio fondamentale e quindi suddividerlo in record di passaggi fondamentali specifici del cliente. Questa suddivisione è interna e si basa sulla suddivisione della percentuale di fatturazione definita per ciascun cliente nella voce del contratto. Nella visualizzazione **Passaggi fondamentali a prezzo fisso** vengono visualizzati i record di passaggi fondamentali specifici del cliente. Ciascuno di questi record passaggio fondamentale può essere contrassegnato come **Pronto per la fatturazione** separatamente da questa vista. Quando una o più delle suddivisioni dei passaggi fondamentali correlati sono contrassegnate come **Pronto per la fatturazione**, lo stato dell'intestazione passa da **In corso** a **Non iniziato**. Quando tutte le suddivisioni dei passaggi fondamentali vengono fatturate, lo stato del passaggio fondamentale dell'intestazione diventa **Completato**.

In questa visualizzazione viene mostrato un passaggio fondamentale in una bozza di fattura con lo stato di fatturazione **Fattura cliente creata**. Quando la bozza di fattura viene confermata, lo stato di fatturazione nel record viene impostato su **Fattura cliente registrata**. 

> [!NOTE] 
> Non aggiornare questo valore di stato utilizzando codice personalizzato. Project Operations non funziona correttamente quando questi valori di stato vengono aggiornati con codice personalizzato.

## <a name="time-and-material-billing-backlog"></a>Backlog di fatturazione tempo e materiale

La visualizzazione **Backlog di fatturazione tempo e materiale** tutti i valori effettivi delle vendite non fatturate in tutti i contratti di progetto nel sistema che non sono stati fatturati. Uno o più valori effettivi di vendita non fatturati possono essere contrassegnati come **Pronto per la fatturazione** o **Non pronto per la fatturazione** da questa vista. Contrassegnando i valori effettivi di vendita non fatturati come **Pronto per la fatturazione** li rende disponibili per essere inseriti in una bozza di fattura.

I valori effettivi delle vendite non fatturate con stato **Limite da non superare** di **Non riuscito** non possono essere contrassegnati come **Pronto per la fatturazione**. Se i valori effettivi devono essere contrassegnati come **Pronto per la fatturazione**, reimposta lo stato degli altri valori effettivi nella voce di contratto di cui è stato eseguito il commit, quindi valuta di nuovo lo stato **Da non superare**.

Se le righe di contratto con più clienti hanno un metodo di fatturazione di tempo e materiale, quando i tempi e le spese vengono approvati, viene creato un valore effettivo di vendita non fatturato per ogni cliente nella voce di contratto in base alla suddivisione in percentuale di fatturazione definita per ciascuno dei clienti. Nella visualizzazione **Backlog di fatturazione tempo e materiale** vengono visualizzati questi valori effettivi delle vendite non fatturate specifici del cliente. Ciascuno di questi record valori effettivi di vendita non fatturati può essere contrassegnato come **Pronto per la fatturazione** separatamente da questa vista.

In questa visualizzazione appare un valore effettivo di vendite non fatturate con uno stato di fatturazione **Fattura cliente creata**. Quando la bozza di fattura viene confermata, lo stato di fatturazione in questo record viene aggiornato a **Fattura cliente registrata**. 

> [!NOTE] 
> Non aggiornare questo valore di stato utilizzando codice personalizzato. Project Operations non funziona correttamente quando questi valori di stato vengono aggiornati con codice personalizzato.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
