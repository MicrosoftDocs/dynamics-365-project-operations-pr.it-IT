---
title: Concetti univoci per offerte basate su progetto
description: Questo articolo fornisce informazioni sulle offerte di progetto in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824332"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Concetti univoci per offerte basate su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Prima di iniziare a utilizzare le offerte di progetto in Microsoft Dynamics 365 Project Operations, devi essere a conoscenza dei seguenti concetti chiave.

## <a name="owning-company"></a>Società proprietaria

La società proprietaria rappresenta la persona giuridica proprietaria della fornitura del progetto. Il cliente dell'offerta deve essere un cliente valido in quella persona giuridica nelle app per la finanza e le operazioni. La valuta della società proprietaria e la valuta dell'unità di contratto selezionata in un'offerta basata su progetto devono corrispondere.

## <a name="contracting-unit"></a>Unità contratto

L'unità contratto rappresenta la divisione o il reparto responsabile della consegna del progetto. È possibile impostare i costi delle risorse per ciascuna unità contratto. Quando si specificano i costi per una risorsa nell'unità contratto, sarà anche possibile impostare tassi di costo diversi per le risorse da cui questa unità contratto prende in prestito o altre divisioni o reparti all'interno dell'azienda. Queste tariffe del costo sono indicate come prezzi di trasferimento, prestito di risorse o prezzi di cambio. Quando si imposta il costo del prestito di risorse da altre divisioni, è anche possibile scegliere di impostare tali tassi di costo nella valuta della divisione mutuante.

## <a name="cost-currency"></a>Valuta costi

La valuta dei costi in Project Operations è la valuta in cui vengono riportati i costi. Questa valuta è derivata dalla valuta collegata al campo **Unità contratto** dell'offerta, del contratto e del progetto. I costi possono essere registrati in qualsiasi valuta per un progetto. Tuttavia, è presente la conversione di valuta dalla valuta in cui sono stati registrati i costi nella valuta dei costi del progetto.

Poiché i tassi di cambio nella piattaforma Dataverse (CDS) non possono dipendere dalla data, i totali sullo schermo per i costi potrebbero cambiare nel tempo se aggiorni i tassi di cambio delle valute. Tuttavia, i costi registrati nel database rimangono invariati perché gli importi vengono memorizzati nella valuta in cui sono stati sostenuti.

## <a name="sales-currency"></a>Valuta di vendita

La valuta di vendita in Project Operations è la valuta in cui vengono registrati e visualizzati gli importi delle vendite stimati ed effettivi. Questa è anche la valuta in cui verrà emessa la fattura al cliente per la trattativa. Per un'offerta di progetto, la valuta di vendita è quella predefinita dal record del cliente o dell'account e può essere modificata quando viene creata l'offerta. Tuttavia dopo che l'offerta è stata salvata, la valuta di vendita non può essere modificata. I listini prezzi predefiniti dei prodotti e dei progetti vengono impostati in base alla valuta di vendita dell'offerta.

A differenza dei costi, i valori di vendita possono essere registrati **solo** nella valuta di vendita.

## <a name="billing-method"></a>Metodo di fatturazione

I progetti generalmente hanno modelli di contratto a costi fissi e basati sul consumo. In Project Operations, il modello di contratto di progetto è rappresentato dal metodo di fatturazione. Il metodo di fatturazione ha due valori: tempistica e materiali e prezzo fisso.

- **Tempistica e materiali:** si tratta di un modello di contratto basato sul consumo in cui ogni costo sostenuto è supportato da ricavi corrispondenti. Man mano che si stimano o si sostengono più costi, aumentano anche le vendite stimate ed effettive corrispondenti. È possibile specificare limiti da non superare nelle righe di offerta che hanno questo metodo di fatturazione. In questo modo, puoi limitare i ricavi effettivi. I ricavi stimati non sono influenzati dai limiti da non superare.
- **Prezzo fisso**: un modello di contratto a costi fissi che indica che i valori di vendita saranno indipendenti dai costi sostenuti. Il valore di vendita è fisso e non cambia se si stimano o si sostengono costi maggiori.

## <a name="project-price-lists"></a>Listini prezzi del progetto

I listini prezzi del progetto sono listini prezzi utilizzati per impostare in modo predefinito i prezzi, non i tassi di costo, per la tempistica, le spese e altri componenti relativi al progetto. Possono essere presenti più listini prezzi e ogni elenco può avere la propria data di validità per ogni offerta di progetto. Project Operations non supporta la sovrapposizione di date di validità nei listini prezzi di progetto.

## <a name="product-price-lists"></a>Listini prezzi del prodotto

I listini prezzi dei prodotti sono listini prezzi utilizzati per impostare in modo predefinito i prezzi, non i tassi di costo, per le righe basate sul prodotto in un'offerta. È disponibile solo un listino prezzi dei prodotti per offerta.

## <a name="transaction-classes"></a>Classi di transazione

Project Operations supporta quattro tipi di classi di transazione:

- Ore
- Spesa
- Materiale
- Tariffa

I valori di costi e vendite possono essere stimati e inseriti nelle classi di transazione **Tempo**, **Spese** e **Materiale**, mentre **Commissioni** è una classe di transazione di soli ricavi.

## <a name="work-entities-and-billing-entities"></a>Entità di lavoro ed entità di fatturazione

Progetti e attività sono le entità che rappresentano il lavoro. Righe di offerta e voci di contratto sono le entità che rappresentano la fatturazione. È possibile collegare entità di lavoro diverse alle opzioni di fatturazione associandole alle righe di offerta o voci di contratto.

## <a name="multi-customer-deals"></a>Trattative con più clienti

Le trattative con più clienti si verificano quando è presente più di un cliente per fattura. Di seguito sono riportati alcuni esempi tipici:

- **Aziende Original equipment manufacturer (OEM) e partner:** partner e rivenditori vendono un prodotto con servizi a valore aggiunto. Si tratta di solito di uno scenario in cui durante una particolare transazione con un cliente, l'OEM si offre di finanziare una parte del progetto.
- **Progetti del settore pubblico:** più dipartimenti di un governo locale accettano di finanziare un progetto e le fatture vengono emesse in base a una suddivisione concordata in precedenza. Ad esempio, un distretto scolastico e il dipartimento del governo cittadino o locale accettano di finanziare la costruzione di una piscina.

## <a name="invoice-schedules"></a>Pianificazioni di fatturazione

Le pianificazioni delle fatturazioni sono specifiche per ciascuna riga di offerta e sono facoltative. Le pianificazioni delle fatturazioni vengono create in base a determinate date di inizio e fine e alla frequenza della fatturazione. Vengono utilizzate nella fase del contratto in cui viene configurato il processo di creazione automatica delle fatture. Durante la fase di offerta, le pianificazioni fatturazione sono facoltative. Quando vengono create nella fase offerta, vengono copiate nel contratto di progetto creato quando viene acquisita un'offerta di progetto.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Differenze rispetto alle offerte di Dynamics 365 Sales

Le offerte di Project Operations sono basate sulle offerte di Dynamics 365 Sales. Tuttavia, ci sono alcune importanti differenze nella funzionalità di cui tenere conto:

- Le offerte di Project Operations hanno due diversi tipi di righe, una per i progetti e una per i prodotti.
- Le offerte di Project Operations hanno la propria pagina ed elementi dell'interfaccia utente, regole di business, logica di business nei plug-in e script lato client che le rendono uniche rispetto alle offerte di Sales.
- In Sales puoi associare più ordini a una singola offerta di vendita, in Project Operations puoi associare un solo contratto di progetto a un'offerta di progetto.
- Quando concludi un'offerta di vendita, l'opportunità correlata può rimanere aperta. Dopo l'acquisizione di un'offerta di progetto, la relativa opportunità viene chiusa.
- Un'offerta di vendita non include alcuni campi e i concetti inclusi in un'offerta di progetto. Questi campi sono **Unità contratto**, **Gestione account** e **Nome contatto fatturazione**.
- Le offerte di vendita e di progetto sono inoltre identificate dal campo basato su set di opzioni **Tipo**. Per un'offerta di vendita, il valore di questo campo è **Basato su articolo**. Per un'offerta di progetto, il valore è **Basato su lavoro**.

A causa delle differenze, ti consigliamo di non utilizzare le offerte in Sales e Project Operations in modo intercambiabile.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
