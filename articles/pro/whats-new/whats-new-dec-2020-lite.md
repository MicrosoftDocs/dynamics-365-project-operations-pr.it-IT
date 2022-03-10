---
title: 'Novità di dicembre 2020 - Distribuzione semplice di Project Operations: dalla transazione alla fatturazione proforma'
description: 'Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di dicembre 2020 di Distribuzione semplice di Project Operations: dalla transazione alla fatturazione proforma.'
author: sigitac
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 81a5556e98d333fa86d73b1c7f03245a23a454372168f8bd7c79fc4425387734
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009356"
---
# <a name="whats-new-december-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Novità di dicembre 2020 - Distribuzione semplice di Project Operations: dalla transazione alla fatturazione proforma

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

  - Project Operations in ambiente Dataverse versione 4.5.0.134 

La tabella seguente elenca gli aggiornamenti di Project Operations in ambiente Dataverse versione 4.5.0.134.

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Prezzi e fatturazione | 1986009 | Le righe del giornale di registrazione create manualmente hanno prestazioni incoerenti se confermate prima che il progetto sia collegato o scollegato da una voce di contratto. |
| Prezzi e fatturazione | 2014153 | I prodotti non vengono fatturati se eseguiti dalla pianificazione fattura. |
| Prezzi e fatturazione | 2014159 | I prodotti non vengono estratti quando la fattura viene aggiornata per le transazioni. |
| Prezzi e fatturazione | 2028174 | Gli aggiornamenti per fatturare i dettagli della riga devono seguire la logica del giornale di registrazione correzione. |
| Prezzi e fatturazione | 2028315 | Correzioni modificabili del comportamento della griglia nidificata. |
| Prezzi e fatturazione | 2031070 | La rettifica dei dettagli della riga della fattura correttiva deve seguire la logica del giornale di registrazione delle correzioni. |
| Prezzi e fatturazione | 2034186 | Deve essere in grado di aggiornare un progetto su una riga di contratto. |
| Prezzi e fatturazione | 2034206 | Lo stato della rettifica deve essere impostato durante l'effettivo annullamento durante lo scollegamento di un progetto da una riga di contratto. |
| Prezzi e fatturazione | 2040871 | Consenti gli aggiornamenti delle celle delle unità e dei gruppi di unità nella griglia Stime spese. |
| Prezzi e fatturazione | 2053754 | I dati effettivi creati dalle modifiche alle fatture non sono contrassegnati con lo stato di rettifica e lo stato di fatturazione. |
| Prezzi e fatturazione | 2057874 | Collegamento della transazione corretto creato durante la modifica dei dettagli della riga della fattura. |
| Prezzi e fatturazione | 2057875 | Origini della transazione corrette create durante la modifica dei dettagli della riga della fattura. |
| Prezzi e fatturazione | 2057944 | Stato da non superare impostato come Impegnato per i valori effettivi che non sono pronti per la fatturazione da una correzione della fattura. |
| Prezzi e fatturazione | 2057963 | Creazione divisa\_Privilegio prodotto da creazione\_Privilegio ProjectContract. |
| Prezzi e fatturazione | 2067622 | L'icona di elaborazione dovrebbe essere visualizzata durante la generazione dei passaggi fondamentali. |
| Prezzi e fatturazione | 2067624 | L'importo contrattato deve essere contrassegnato come Consigliato dall'azienda durante la generazione dei passaggi fondamentali. |
| Prezzi e fatturazione | 2086880 | Nascondere il pulsante **Suggerimento** sulla barra multifunzione per le righe di preventivo basate sul progetto. |
| Distribuzione e configurazione | 2101152 | Nuovo ambiente creato utilizzando il modello Project Operations dall'interfaccia di amministrazione di Power Platform deve avere eseguito tutte le operazioni successive all'installazione. |
|   Gestione delle opportunità | 2022204 | Griglia di fatturazione basata sul progetto nella scheda **Fatturazione attività** su **Progetto** dovrebbe nascondere la griglia basata sul progetto se non è presente alcuna riga di preventivo/contratto con **Tutte le attività** e viceversa. |
|   Gestione delle opportunità | 2086601 | I ruoli e le categorie disattivati non devono essere copiati in Ruoli addebitabili ed Elenco categorie addebitabili nelle righe di preventivo e nelle voci del contratto. |
| Pianificazione e rilevamento dei progetti | 1949065 | La visibilità dei dati funziona correttamente con uno zoom del 200% |
| Pianificazione e rilevamento dei progetti | 2046317 | Possibilità di rinominare l'entità del progetto in Project Operations |
| Pianificazione e rilevamento dei progetti | 2057171 | Messaggio di errore aggiornato quando il campo **Data di inizio del progetto** è vuoto nella pagina **Progetto**. |
| Pianificazione e rilevamento dei progetti | 2057197 | La copia della riga della stima con riferimento all'attività non è supportata. |
| Pianificazione e rilevamento dei progetti | 2060687 | L'avviso sul fuso orario ora scompare dopo una durata specifica. |
| Gestione delle risorse | 1832887 | L'ID della categoria della risorsa predefinita deve essere statico per garantire caricamenti di dati ripetibili per ambienti Dataverse e Finance. |
| Tempistica e spesa | 2034882 | Il pulsante **Nuovo** viene visualizzato due volte sulla barra dei comandi per le voci di tempo quando Dynamics 365 Field Service è installato. |
| Tempistica e spesa | 2056028 | Aggiornare la pagina **Modifica ora** per includere la sequenza temporale. |
| Tempistica e spesa | 1983747 | Il grafico di inserimenti ore mostra dati aggiuntivi. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]