---
title: Determinare i tassi di costo per stime e valori effettivi basati su progetto
description: Questo articolo fornisce informazioni su come vengono determinati i tassi di costo nelle stime basate su progetto e nei valori effettivi.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475278"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Determinare i tassi di costo per stime e valori effettivi basati su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Per determinare i prezzi di costo su stime e valori effettivi in Microsoft Dynamics 365 Project Operations, il sistema utilizza prima la data e la valuta nella stima in entrata o nel valore effettivo per determinare il listino prezzi di vendita. Nel contesto attuale, in particolare, il sistema utilizza il campo **Data della transazione** per determinare quale listino prezzi è applicabile. Il valore di **Data della transazione** della stima in entrata o effettivo viene confrontato con i valori **Inizio validità (Indipendente da fuso orario)** e **Fine validità (Indipendente da fuso orario)** nel listino prezzi. Dopo che il listino prezzi di costo è stato determinato, il sistema determina la tariffa di costo.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Determinazione dei tassi di costo nelle stime e nei contesti attuali per il tempo

Il contesto di stima per **Ora** si riferisce a:

- Dettagli della riga di offerta per **Ora**.
- Dettagli della riga di offerta per **Ora**.
- Assegnazione delle risorse a un progetto.

Il contesto attuale per **Ora** si riferisce a:

- Scritture contabili di immissione e correzione per **Ora**.
- Le scritture contabili che vengono create quando viene inviato un inserimento ore.

Dopo che un listino prezzi di costo è stato determinato, il sistema completa i seguenti passaggi per impostare la tariffa di costo predefinita.

1. Il sistema utilizza la combinazione di campi **Ruolo**, **Società resourcing** e **Unità gestione risorse** nella stima o nel contesto attuale per **Ora** contro le righe di prezzo del ruolo nel listino prezzi. Questa corrispondenza presuppone che tu stia utilizzando le dimensioni di prezzo standard per il costo del lavoro. Se hai configurato il sistema per abbinare i campi al posto o in aggiunta a **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse**, verrà utilizzata una combinazione diversa per recuperare una riga di prezzo del ruolo corrispondente.
1. Se il sistema trova una riga di prezzo del ruolo con una tariffa di costo per la combinazione **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse**, questa tariffa di costo viene utilizzata per la tariffa di costo predefinita.
1. Se il sistema non può abbinare i valori **Ruolo**, **Società resourcing** e **Unità gestione risorse**, elimina la dimensione con la priorità più bassa, cerca le righe di prezzo del ruolo che hanno corrispondenze per gli altri due valori di dimensione e continua a eliminare progressivamente le dimensioni finché non viene trovata una riga di prezzo del ruolo corrispondente. La tariffa di costo di quel record verrà utilizzata come tariffa di costo predefinita. Se il sistema non trova una riga del prezzo del ruolo corrispondente, il prezzo verrà impostato su **0** (zero) per impostazione predefinita.

> [!NOTE]
> Se configuri una diversa priorità dei campi **Ruolo** e **Unità gestione risorse** oppure se hai altre dimensioni con priorità più alta, il precedente comportamento cambia di conseguenza. Il sistema recupera i record dei prezzi dei ruoli che hanno valori che corrispondono a ciascun valore della dimensione dei prezzi in ordine di priorità. Le righe con valori Null per quelle dimensioni vengono per ultime.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Determinazione delle tariffe di costo sulle righe di stima e valori effettivi per la spesa

Il contesto di stima per **Spesa** si riferisce a:

- Dettagli della riga di offerta per **Spesa**.
- Dettagli della voce di contatto per **Spesa**.
- Stime di spesa su un progetto.

Il contesto attuale per **Spesa** si riferisce a:

- Scritture contabili di immissione e correzione per **Spesa**.
- Le scritture contabili che vengono create quando viene inviata una spesa.

Dopo che un listino prezzi di costo è stato determinato, il sistema completa i seguenti passaggi per impostare la tariffa di costo predefinita.

1. Il sistema utilizza la combinazione di campi **Categoria** e **Unità** nella stima o nel contesto attuale per **Spesa** contro le righe di prezzo della categoria nel listino prezzi.
1. Se il sistema trova una riga di prezzo di categoria con una tariffa di costo per la combinazione di campi **Categoria** e **Unità**, questa riga è la tariffa di costo utilizzata come tariffa di costo predefinita.
1. Se il sistema non può abbinare i valori **Categoria** e **Unità**, il prezzo è impostato su **0** (zero) per impostazione predefinita.
1. Nel contesto della stima, se il sistema è in grado di trovare una riga di prezzo della categoria corrispondente ma il metodo di determinazione del prezzo è diverso da **Prezzo unitario**, la tariffa di costo è impostata su **0** (zero) per impostazione predefinita.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Determinazione dei tassi di costo nelle righe effettive e di stima per Materiale

Il contesto di stima per **Materiale** si riferisce a:

- Dettagli della riga di offerta per **Materiale**.
- Dettagli della voce di contatto per **Materiale**.
- Stime dei materiali in un progetto.

Il contesto attuale per **Materiale** si riferisce a:

- Scritture contabili di immissione e correzione per **Materiale**.
- Le scritture contabili che vengono create quando viene inviato un registro di uso dei materiali.

Dopo che un listino prezzi di costo è stato determinato, il sistema completa i seguenti passaggi per impostare la tariffa di costo predefinita.

1. Il sistema utilizza la combinazione di campi **Prodotto** e **Unità** nella stima o nel contesto attuale per **Materiale** contro le righe delle voci del listino prezzi nel listino prezzi.
1. Se il sistema trova una voce di listino prezzi con una tariffa di costo per la combinazione di campi **Prodotto** e **Unità**, questa riga è la tariffa di costo utilizzata come tariffa di costo predefinita.
1. Se il sistema non può far corrispondere i valori **Prodotto** e **Unità**, il costo unitario è impostato su **0** (zero) per impostazione predefinita.
1. Nel contesto della stima o attuale, se il sistema è in grado di trovare una riga della voce del prezzo della categoria corrispondente ma il metodo di determinazione del prezzo è diverso da **Importo in valuta**, l'unità di costo è impostata su **0** (zero) per impostazione predefinita. Questo comportamento si verifica perché Project Operations supporta solo il metodo di determinazione del prezzo **Importo in valuta** per i materiali utilizzati in un progetto.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
