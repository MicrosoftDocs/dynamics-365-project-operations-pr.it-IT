---
title: Novità della versione di ottobre 2021 - Distribuzione di Project Operations Lite
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di ottobre 2021 della distribuzione di Project Operations Lite.
author: sigitac
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 928e3b4ce4220c9044a8ae4c209049485af82cc4
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606775"
---
# <a name="whats-new-october-2021---project-operations-lite-deployment"></a>Novità della versione di ottobre 2021 - Distribuzione di Project Operations Lite

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

  - Project Operations in ambiente Microsoft Dataverse versione 4.25.0.91


## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

In questa release sono incluse le seguenti funzionalità:

[Gestione conto lavoro](../subcontracting/managing-subcontracts-overview.md): questa funzione offre la possibilità di creare un contratto di conto lavoro con il fornitore, elencare tutti gli acquisti come voci del contratto di conto lavoro, modificare i prezzi e associare i contatti.


## <a name="quality-updates"></a>Aggiornamenti di qualità

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Determinazione dei prezzi e fatturazione | 2209402 | Sono state corrette le convalide che impedivano la fatturazione degli importi degli acconti alla conferma di un contratto di progetto. |
| Gestione delle opportunità | 2227414 | Nei campi **Prodotto**, **Fuori catalogo** e **IsProductOverriden** vengono copiati nei dettagli della riga dell'offerta e nei dettagli della riga del contratto. |
| Determinazione dei prezzi e fatturazione | 2338357 | La valuta nel registro di utilizzo dei materiali deve essere predefinita dalla valuta del progetto quando il progetto viene selezionato. |
| Tempistica e spesa | 2414777 | La cancellazione di un'approvazione quando la voce di spesa o di tempo ha più di un'approvazione di progetto associata deve essere possibile. |
