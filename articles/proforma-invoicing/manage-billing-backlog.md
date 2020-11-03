---
title: Gestire il backlog di fatturazione
description: Questo argomento fornisce informazioni su come visualizzare e lavorare con il backlog di fatturazione in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087975"
---
# <a name="manage-the-billing-backlog"></a>Gestire il backlog di fatturazione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations dispone di due visualizzazioni dedicate per aiutarti a lavorare e gestire il backlog di fatturazione. Le visualizzazioni sono **Passaggi fondamentali prezzo fisso** e **Backlog di fatturazione tempo e materiale**. Per selezionare una visualizzazione, nell'area **Vendite** di Project Operations, nella pagina di spostamento a sinistra, seleziona **Fatturazione**. I collegamenti del backlog di fatturazione vengono memorizzati qui.

## <a name="fixed-price-milestones"></a>Passaggi fondamentali prezzo fisso

Questa visualizzazione elenca tutti i passaggi fondamentali a prezzo fisso in tutte le voci del contratto di progetto nel sistema. Uno o più passaggi fondamentali possono essere contrassegnati come **Pronto per la fatturazione** o **Non pronto per la fatturazione** da questa vista. Quando contrassegni un passaggio fondamentale come **Pronto per la fatturazione** , il passaggio fondamentale diventa disponibile per una bozza di fattura.

Quando le voci di contratto per più clienti hanno un metodo di fatturazione a prezzo fisso, viene creato un passaggio fondamentale per ogni cliente nella voce di contratto. L'utente crea un passaggio fondamentale e tale passaggio fondamentale viene suddiviso internamente in record passaggio fondamentale specifico del cliente, in base alla suddivisione di percentuale di fatturazione definita per ogni cliente nella voce del contratto. Nella visualizzazione **Passaggi fondamentali a prezzo fisso** vedrai i record dei passaggi fondamentali specifici del cliente. Ciascuno di questi record passaggio fondamentale può essere contrassegnato come **Pronto per la fatturazione** separatamente da questa vista. Quando una o più suddivisioni di passaggio fondamentale correlate sono contrassegnate come **Pronto per la fatturazione** , l'intestazione passa nello stato **In corso** da **Non avviato**. Quando tutte le suddivisioni passaggio fondamentale sono state fatturate, lo stato del passaggio fondamentale dell'intestazione diventa **Completato**.

In questa visualizzazione viene mostrato un passaggio fondamentale in una bozza di fattura con lo stato di fatturazione **Fattura cliente creata**. Quando la bozza di fattura viene confermata, lo stato di fatturazione in questo record viene aggiornato a **Fattura registrata**. L'aggiornamento di questo valore di stato utilizzando il codice personalizzato non è consigliato. Project Operations non funzionerà correttamente se questi valori di stato vengono aggiornati con codice personalizzato.

## <a name="time-and-material-billing-backlog"></a>Backlog di fatturazione tempo e materiale

Questa visualizzazione elenca tutti i valori effettivi di vendita non fatturati che non sono state fatturati in tutti i contratti di progetto nel sistema. Uno o più valori effettivi di vendita non fatturati possono essere contrassegnati come **Pronto per la fatturazione** o **Non pronto per la fatturazione** da questa vista. Contrassegnando i valori effettivi di vendita non fatturati come **Pronto per la fatturazione** li rende disponibili per essere inseriti in una bozza di fattura.

I valori effettivi di vendita non fatturati con stato **Da non superare** di **Non riuscito** non possono essere contrassegnati come **Pronto per la fatturazione**. Se questi valori effettivi devono essere contrassegnati come tali, reimposta lo stato di altri valori effettivi nella voce di contratto di cui è stato eseguito il commit, quindi valuta lo stato **Da non superare**.

Nel caso di voci di contratto per più clienti che hanno un metodo di fatturazione di tempo e materiali, quando i tempi e le spese sono approvati, viene creato un valore effettivo di vendita non fatturato per ogni cliente nella voce di contratto in base alla ripartizione percentuale di fatturazione definita per ogni cliente nella voce di contratto. Nella visualizzazione **Backlog di fatturazione tempo e materiale** vedrai i valori effettivi di vendita non fatturati specifici del cliente. Ciascuno di questi record valori effettivi di vendita non fatturati può essere contrassegnato come **Pronto per la fatturazione** separatamente da questa vista.

In questa visualizzazione viene mostrato un valore effettivo di vendita non fatturato in una bozza di fattura con lo **stato di fatturazione** di **Fattura cliente creata**. Quando la bozza di fattura viene confermata, lo stato di fatturazione in questo record viene aggiornato a **Fattura cliente registrata**. L'aggiornamento del valore di questo stato utilizzando il codice personalizzato non è consigliato. Project Operations non funzionerà correttamente quando questi valori di stato vengono aggiornati con codice personalizzato.
