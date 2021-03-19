---
title: Concetti chiave dei contratti di progetto - semplice
description: Questo argomento fornisce informazioni sui concetti chiave dei contratti di progetto.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55d1310de4338e50a1fc7d0af8cd83e63856db61
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273788"
---
# <a name="project-contracts---key-concepts---lite"></a>Concetti chiave dei contratti di progetto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Questo argomento fornisce i concetti chiave di cui essere a conoscenza prima di iniziare a utilizzare i contratti di Project in Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unità contratto

L'unità contratto rappresenta la divisione o il reparto responsabile della consegna del progetto. È possibile impostare i costi delle risorse per ciascuna unità contratto. Quando specifichi il costo di una risorsa, puoi anche impostare tariffe di costo diverse per le risorse. Questa unità contraente prende in prestito le risorse da altre divisioni o procedure all'interno dell'impresa. Le tariffe di costo delle risorse sono indicate come prezzi di trasferimento, prestito di risorse o prezzi di cambio. Quando imposti le tariffe di costo per il prestito di risorse da altre divisioni, usa la valuta della divisione mutuante.

## <a name="cost-currency"></a>Valuta costi

La valuta costi è la valuta in cui vengono riportati i costi sullo schermo. Questa valuta è derivata dalla valuta collegata al campo **Unità contratto** dell'offerta, del contratto e del progetto. I costi possono essere registrati in qualsiasi valuta in un progetto. Tuttavia, è presente la conversione di valuta dalla valuta in cui sono stati registrati i costi nella valuta dei costi del progetto visualizzati sullo schermo.

Poiché i tassi di cambio nella piattaforma Common Data Service (CDS) non possono dipendere dalla data, i totali sullo schermo per i costi potrebbero cambiare nel tempo se aggiorni i tassi di cambio delle valute. Tuttavia, i costi registrati nel database rimangono invariati perché gli importi vengono memorizzati nella valuta in cui sono stati sostenuti.

## <a name="sales-currency"></a>Valuta di vendita

La valuta di vendita in Project Operations è la valuta in cui vengono registrati e visualizzati gli importi delle vendite stimati ed effettivi. La valuta di vendita è la valuta in cui verrà emessa la fattura al cliente per la transazione. In un contratto di progetto, la valuta di vendita è quella predefinita dal record del cliente o dell'account e può essere modificata quando viene creata il contratto. Quando un contratto viene creato chiudendo un'offerta come acquisita, la valuta del contratto viene impostata per impostazione predefinita sulla valuta dell'offerta.

Quando crei un contratto di progetto da zero, il campo **Valuta di vendita** non può essere modificato. I listini prezzi dei prodotti e dei progetti vengono impostati in modo predefinito su questa valuta del contratto.

A differenza dei costi, i valori di vendita possono essere registrati solo nella valuta di vendita.

## <a name="billing-method"></a>Metodo di fatturazione

Sono generalmente disponibili due tipi di modello di contratto per i progetti: a costi fissi e basati sul consumo. Questi modelli sono rappresentati in Project Operations come metodi di fatturazione con due possibili valori:

- Tempistica e materiali: un modello di contratto basato sul consumo in cui ogni costo sostenuto è supportato da ricavi corrispondenti. Man mano che si stimano o si sostengono più costi, aumentano anche le vendite stimate ed effettive corrispondenti. Specifica i limiti da non superare nelle voci di contratto che hanno questo metodo di fatturazione che limita i ricavi effettivi. I ricavi stimati non sono influenzati dai limiti da non superare.
- Prezzo fisso: un modello di contratto a costi fissi che indica che i valori di vendita saranno indipendenti dai costi sostenuti. Il valore di vendita è fisso e non cambia se si stimano o si sostengono costi maggiori.

## <a name="project-price-lists"></a>Listini prezzi del progetto

I listini prezzi del progetto vengono utilizzati per impostare in modo predefinito i prezzi, non le tariffe di costo, per la tempistica, le spese e altri componenti relativi al progetto. Possono esserci più listini prezzi. Ogni listino prezzi ha una propria data di validità per ogni contratto di progetto. La sovrapposizione della validità delle date dei listini prezzi di progetto non è supportata in Project Operations.

Quando un contratto di progetto viene creato con l'acquisizione di un'offerta di progetto, i listini prezzi del progetto vengono copiati con il nome del contratto e la data inclusi. La copia di queste informazioni costituisce un prezzo personalizzato per i componenti del progetto in questo contratto di progetto.

## <a name="product-price-lists"></a>Listini prezzi del prodotto

I listini prezzi dei prodotti vengono utilizzati per impostare in modo predefinito i prezzi, non le tariffe di costo, per le righe basate su prodotto in un contratto. È disponibile solo un listino prezzi dei prodotti per contratto.

## <a name="transaction-classes"></a>Classi di transazione

Project Operations supporta quattro tipi di classi di transazione:

- Ore
- Spesa
- Materiale
- Tariffa

I valori dei costi e delle vendite possono essere stimati e sostenuti in base alle classi di transazione di tempistica, spesa e materiali. La tariffa è una classe di transazione solo per ricavi.

## <a name="work-entities-and-billing-entities"></a>Entità di lavoro ed entità di fatturazione

Le entità che rappresentano il lavoro sono progetti e attività. Le entità che rappresentano gli aspetti della fatturazione sono le voci di contratto. È possibile collegare entità di lavoro diverse alle opzioni di fatturazione associandole alle voci di contratto.

## <a name="multi-customer-deals"></a>Trattative con più clienti

Le transazioni con più clienti hanno più di un cliente a cui fatturare in una transazione. Esempi comuni prevedono:

- Imprese OEM e loro partner: partner e rivenditori vendono un prodotto con alcuni servizi a valore aggiunto, che in genere comportano una particolare transazione con il cliente. L'OEM si offre di finanziare una parte del progetto. 

- Progetti del settore pubblico: più dipartimenti di un governo locale accettano di finanziare un progetto e le fatture vengono emesse in base a una suddivisione concordata in precedenza. Ad esempio, un distretto scolastico e il governo locale accettano di finanziare la costruzione di una piscina.

## <a name="invoice-schedules"></a>Pianificazioni di fatturazione

Le pianificazioni di fatturazione sono specifiche per ogni voce di contratto e sono necessarie per il funzionamento della fatturazione automatica. Le pianificazioni delle fatturazioni vengono create in base a determinate date di inizio e fine e alla frequenza della fatturazione. Le pianificazioni vengono utilizzate nella fase del contratto in cui viene configurato il processo di creazione automatica delle fatture. Quando un contratto di progetto viene creato da un'offerta, la pianificazione della fatturazione viene copiata nel contratto di progetto dall'offerta.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Modifiche rispetto al contratto di Dynamics 365 Sales

I contratti di Project Operations sono basati sui contratti di Dynamics 365 Sales. Tuttavia, ci sono alcune importanti differenze e scostamenti nella funzionalità di cui tenere conto:

- I contratti di Project Operations hanno due diversi tipi di righe, una per i progetti e una per i prodotti.
- I contratti di Project Operations hanno il proprio modulo ed elementi dell'interfaccia utente, regole di business, logica di business nei plug-in e script lato client che le rendono uniche rispetto ai contratti di Sales.

Per questi motivi, non dovresti utilizzare un contratto di Sales e un contratto di Project in modo intercambiabile.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]