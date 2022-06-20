---
title: Novità della versione di ottobre 2021 - Distribuzione di Project Operations Lite
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di ottobre 2021 della distribuzione lite di Project Operations.
author: sigitac
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7199853bea7e8e99a2a1ce19d6ce88736edb38f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921951"
---
# <a name="whats-new-october-2021---project-operations-lite-deployment"></a>Novità della versione di ottobre 2021 - Distribuzione di Project Operations Lite

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo articolo si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

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
