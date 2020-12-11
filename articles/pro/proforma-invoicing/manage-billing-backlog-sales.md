---
title: Gestire il backlog di fatturazione - semplice
description: Questo argomento fornisce informazioni sulle varie visualizzazioni disponibili per l'uso durante la gestione del backlog di fatturazione.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e3ca167fa53a6923727eff3e7c34c8706dc7455
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176976"
---
# <a name="manage-the-billing-backlog---lite"></a>Gestire il backlog di fatturazione - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations dispone di viste dedicate per aiutare a gestire il backlog di fatturazione. Per gestire il backlog di fatturazione, seleziona i collegamenti nell'area **Vendite** sotto **Fatturazione**. 

Sono disponibili le seguente visualizzazioni:

- Acconti e anticipi
- Acconti e anticipi disponibili
- Passaggi fondamentali prezzo fisso
- Backlog di fatturazione prodotto
- Backlog di fatturazione tempo e materiale

## <a name="retainers-and-advances"></a>Acconti e anticipi

La visualizzazione **Acconti e anticipi** elenca tutte gli acconti e gli anticipi in tutti i contratti di progetto nel sistema. Dopo che un acconto o un anticipo è stato fatturato, l'importo dell'anticipo diventa disponibile per l'uso.

## <a name="available-retainers-and-advances"></a>Acconti e anticipi disponibili

La visualizzazione **Acconti e anticipi disponibili** elenca tutte gli acconti e gli anticipi disponibili in tutti i contratti di progetto nel sistema. Dopo che un acconto o un anticipo è stato fatturato, l'importo dell'anticipo diventa disponibile per l'uso e viene aggiunto all'elenco. Dopo che l'importo dell'acconto o dell'anticipo è stato utilizzato completamente, viene rimosso dall'elenco.

## <a name="fixed-price-milestones"></a>Passaggi fondamentali prezzo fisso

La visualizzazione **Passaggi fondamentali prezzo fisso** elenca tutti i passaggi fondamentali a prezzo fisso in tutte le voci di contratto di progetto nel sistema. Uno o più passaggi fondamentali possono essere contrassegnati come **Pronto per la fatturazione** o **Non pronto per la fatturazione** da questa visualizzazione. Contrassegnando un passaggio fondamentale come **Pronto per la fatturazione** lo si rende disponibile per essere inserito in una bozza di fattura.

Quando le voci di contratto con più clienti hanno un metodo di fatturazione a prezzo fisso, viene creato un passaggio fondamentale per ogni cliente nella voce di contratto. È possibile creare un passaggio fondamentale e quindi suddividerlo in record di passaggi fondamentali specifici del cliente. Questa suddivisione è interna e si basa sulla suddivisione della percentuale di fatturazione definita per ciascun cliente nella voce del contratto. Nella visualizzazione **Passaggi fondamentali a prezzo fisso** vengono visualizzati i record di passaggi fondamentali specifici del cliente. Ciascuno di questi record passaggio fondamentale può essere contrassegnato come **Pronto per la fatturazione** separatamente da questa vista. Quando una o più delle suddivisioni di passaggi fondamentali correlate sono contrassegnate come **Pronto per la fatturazione**, lo stato dell'intestazione viene impostato su **In corso** da **Non avviato**. Quando tutte le suddivisioni di passaggi fondamentali vengono fatturate, lo stato del passaggio fondamentale dell'intestazione viene impostato su **Completato**.

In questa visualizzazione viene mostrato un passaggio fondamentale in una bozza di fattura con lo stato di fatturazione **Fattura cliente creata**. Quando la bozza di fattura viene confermata, lo stato di fatturazione nel record viene impostato su **Fattura cliente registrata**. Non aggiornare questo valore di stato utilizzando codice personalizzato. Project Operations non funziona correttamente quando questi valori di stato vengono aggiornati con codice personalizzato.

## <a name="product-billing-backlog"></a>Backlog di fatturazione prodotto

La visualizzazione **Backlog di fatturazione prodotto** elenca tutte le voci di contratto basate su prodotto in tutti i contratti di progetto nel sistema. Uno o più voci di contratto basate su prodotto possono essere contrassegnate come **Pronto per la fatturazione** o **Non pronto per la fatturazione** da questa visualizzazione. Contrassegnando una voce di contratto basata su prodotto come **Pronto per la fatturazione** la si rende disponibile per essere inserita in una bozza di fattura.

Una voce di contratto basata su prodotto che si trova in una bozza di fattura viene visualizzata in questa visualizzazione con uno stato di fatturazione di **Fattura cliente creata**. Quando la bozza di fattura viene confermata, lo stato di fatturazione in questo record viene aggiornato a **Fattura cliente registrata**. Non aggiornare questo valore di stato utilizzando codice personalizzato. Project Operations non funziona correttamente quando questi valori di stato vengono aggiornati con codice personalizzato.

## <a name="time-and-material-billing-backlog"></a>Backlog di fatturazione tempo e materiale

La visualizzazione **Backlog di fatturazione tempo e materiale** tutti i valori effettivi delle vendite non fatturate in tutti i contratti di progetto nel sistema che non sono stati fatturati. Uno o più valori effettivi di vendita non fatturati possono essere contrassegnati come **Pronto per la fatturazione** o **Non pronto per la fatturazione** da questa vista. Contrassegnando i valori effettivi di vendita non fatturati come **Pronto per la fatturazione** li rende disponibili per essere inseriti in una bozza di fattura.

I valori effettivi delle vendite non fatturate con stato **Limite da non superare** di **Non riuscito** non possono essere contrassegnati come **Pronto per la fatturazione**. Se i valori effettivi devono essere contrassegnati come **Pronto per la fatturazione**, reimposta lo stato su altri valori effettivi nella voce di contratto di cui è stato eseguito il commit. Quindi rivaluta stato del limite **da non superare**.

Se le righe di contratto con più clienti hanno un metodo di fatturazione di tempo e materiale, quando i tempi e le spese vengono approvati, viene creato un valore effettivo di vendita non fatturato per ogni cliente nella voce di contratto in base alla suddivisione in percentuale di fatturazione definita per ciascuno dei clienti. Nella visualizzazione **Backlog di fatturazione tempo e materiale** vengono visualizzati questi dati effettivi delle vendite non fatturate specifici del cliente. Ciascuno di questi record valori effettivi di vendita non fatturati può essere contrassegnato come **Pronto per la fatturazione** separatamente da questa vista.

Un valore effettivo di vendita non fatturata che si trova in una bozza di fattura viene visualizzata in questa visualizzazione con uno stato di fatturazione di **Fattura cliente creata**. Quando la bozza di fattura viene confermata, lo stato di fatturazione in questo record viene aggiornato a **Fattura cliente registrata**. Non aggiornare questo valore di stato utilizzando codice personalizzato. Project Operations non funziona correttamente quando questi valori di stato vengono aggiornati con codice personalizzato.