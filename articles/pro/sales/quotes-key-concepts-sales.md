---
title: Concetti chiave dell'offerta - semplice
description: Questo argomento fornisce informazioni su come utilizzare le offerte di progetto in Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 279e7dd47d3d61b02227b307a5833ca0bac66f4a774b5ff23cb69aac417e2f0e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009446"
---
# <a name="concepts-unique-to-project-quotes"></a>Concetti esclusivi delle offerte di progetto

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_


Questo argomento fornisce i concetti chiave di cui essere a conoscenza prima di iniziare a utilizzare le offerte di progetto in Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unità contratto

L'unità contratto rappresenta la divisione o il reparto responsabile della consegna del progetto. È possibile impostare i costi delle risorse per ciascuna unità contratto. Quando si specifica il costo delle risorse per una risorsa nell'unità contratto, sarà anche possibile impostare tassi di costo diversi per le risorse da cui questa unità contratto prende in prestito o altre divisioni o reparti all'interno dell'azienda. Questi sono indicati come prezzi di trasferimento, prestito di risorse o prezzi di cambio. Quando si imposta il costo del prestito di risorse da altre divisioni, è anche possibile scegliere di impostare tali tassi di costo nella valuta della divisione mutuante.

## <a name="cost-currency"></a>Valuta costi

La valuta dei costi in Project Operations è la valuta in cui vengono riportati i costi. Questa valuta è derivata dalla valuta collegata al campo **Unità contratto** dell'offerta, contratto e progetto. I costi possono essere registrati in qualsiasi valuta in un progetto. Tuttavia, è presente la conversione di valuta dalla valuta in cui sono stati registrati i costi nella valuta dei costi del progetto.

Poiché i tassi di cambio nella piattaforma CDS non possono dipendere dalla data, i totali sullo schermo per i costi potrebbero cambiare nel tempo se aggiorni i tassi di cambio delle valute. Tuttavia, i costi registrati nel database rimangono invariati perché gli importi vengono memorizzati nella valuta in cui sono stati sostenuti.

## <a name="sales-currency"></a>Valuta di vendita

La valuta di vendita in Project Operations è la valuta in cui vengono registrati e visualizzati gli importi delle vendite stimati ed effettivi. Questa è anche la valuta in cui verrà emessa la fattura al cliente per la trattativa. In un'offerta di progetto, la valuta di vendita è quella predefinita dal record del cliente o dell'account e può essere modificata quando viene creata l'offerta. Dopo che l'offerta è stata salvata, la valuta di vendita non può essere modificata. I listini prezzi dei prodotti e dei progetti vengono impostati in modo predefinito in base alla valuta di vendita dell'offerta.

A differenza dei costi, i valori di vendita possono essere registrati solo nella valuta di vendita.

## <a name="billing-method"></a>Metodo di fatturazione

I progetti generalmente hanno modelli di contratto a costi fissi e basati sul consumo. Questo viene rappresentato in Project Operations come **Metodo di fatturazione** e ha due valori, tempistica e materiali e prezzo fisso.

- **Tempistica e materiali:** si tratta di un modello di contratto basato sul consumo in cui ogni costo sostenuto è supportato da ricavi corrispondenti. Man mano che si stimano o si sostengono più costi, aumenteranno anche le vendite stimate ed effettive corrispondenti. È possibile specificare limiti da non superare nelle righe di offerta che hanno questo metodo di fatturazione. Questo applicherà un limite massimo ai ricavi effettivi. I ricavi stimati non sono influenzati dai limiti da non superare.
- **Prezzo fisso:** questo è un modello di contratto a costi fissi che indica che i valori di vendita saranno indipendenti dai costi sostenuti. Il valore di vendita è fisso e non cambia se si stimano o si sostengono costi maggiori.

## <a name="project-price-lists"></a>Listini prezzi del progetto

I listini prezzi del progetto sono listini prezzi utilizzati per impostare in modo predefinito i prezzi, non i tassi di costo, per la tempistica, le spese e altri componenti relativi al progetto. Possono essere presenti più listini prezzi e ogni elenco può avere la propria data di validità per ogni offerta di progetto. La sovrapposizione della validità delle date dei listini prezzi di progetto non è supportata in Project Operations.

## <a name="product-price-lists"></a>Listini prezzi del prodotto

I listini prezzi dei prodotti sono listini prezzi utilizzati per impostare in modo predefinito i prezzi, non i tassi di costo, per le righe basate sul prodotto in un'offerta. È disponibile solo un listino prezzi dei prodotti per offerta.

## <a name="transaction-classes"></a>Classi di transazione

Project Operations supporta quattro tipi di classi di transazione:

- Ore
- Spesa
- Materiale
- Tariffa

I valori dei costi e delle vendite possono essere stimati e sostenuti in base alle classi di transazione di tempistica, spesa e materiali. Il costo è una classe di transazioni solo per ricavi.

## <a name="work-entities-and-billing-entities"></a>Entità di lavoro ed entità di fatturazione

Le entità che rappresentano il lavoro sono progetti e attività. Le entità che rappresentano la fatturazione sono le righe di offerta e le voci di contratto. È possibile collegare entità di lavoro diverse alle opzioni di fatturazione associandole alle righe di offerta o voci di contratto.

## <a name="multi-customer-deals"></a>Trattative con più clienti

Le trattative con più clienti si verificano quando è presente più di un cliente a cui fatturare. Esempi comuni includono:

- **Aziende OEM e partner:** partner e rivenditori vendono un prodotto con servizi a valore aggiunto. Si tratta di solito di uno scenario in cui durante una particolare transazione con un cliente, l'OEM si offre di finanziare una parte del progetto. 

- **Progetti del settore pubblico:** più dipartimenti di un governo locale accettano di finanziare un progetto e le fatture vengono emesse in base a una suddivisione concordata in precedenza. Ad esempio, un distretto scolastico e il dipartimento del governo cittadino o locale accettano di finanziare la costruzione di una piscina.

## <a name="invoice-schedules"></a>Pianificazioni di fatturazione

Le pianificazioni delle fatturazioni sono specifiche per ciascuna riga di offerta e sono facoltative. Le pianificazioni delle fatturazioni vengono create in base a determinate date di inizio e fine e alla frequenza della fatturazione. Le pianificazioni delle fatturazioni vengono utilizzate nella fase del contratto in cui viene configurato il processo di creazione automatica delle fatture. In fase di offerta, le pianificazioni sono facoltative. Quando vengono create le pianificazioni delle fatturazioni nella fase **Offerta**, vengono copiate nel contratto di progetto creato quando viene acquisita un'offerta di progetto.

## <a name="changes-from-dynamics-365-sales-quote"></a>Modifiche rispetto all'offerta di Dynamics 365 Sales:

Le offerte di Project Operations sono basate sulle offerte di Dynamics 365 Sales. Tuttavia, ci sono alcune importanti differenze nella funzionalità di cui tenere conto:

- Le azioni **Aggiorna** e **Attiva** non sono supportate.
- Le offerte di Project Operations hanno due diversi tipi di righe. Uno è per i progetti e l'altro per i prodotti.
- Le offerte di Project Operations hanno il proprio modulo ed elementi dell'interfaccia utente, regole di business, logica di business nei plug-in e script lato client che le rendono uniche rispetto alle offerte di Sales.

Per questi motivi, non è consigliabile utilizzare un'offerta di Sales e un'offerta di Project Operations in modo intercambiabile.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
