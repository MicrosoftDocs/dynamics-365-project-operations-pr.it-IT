---
title: Dettaglio delle spese
description: Questo articolo spiega come dettagliare le spese utilizzando l'area di lavoro Spese riprogettata.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920939"
---
# <a name="expense-itemization"></a>Dettaglio delle spese

[!include [banner](../includes/banner.md)]

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Le organizzazioni spesso richiedono ai dipendenti di fornire una ripartizione dettagliata delle spese sostenute durante il viaggio. Ad esempio, la fattura dell'hotel può contenere diverse righe dettagliate per la tariffa della camera, le tasse, il parcheggio e altre spese varie sostenute ogni giorno durante la durata del soggiorno. Oppure la spesa del pasto potrebbe richiedere una suddivisione più granulare per colazione, pranzo o cena. Qualunque siano le esigenze dell'organizzazione, ogni categoria di spesa può essere impostata per riflettere le sottocategorie o le voci che compongono una spesa. Sebbene i dettagli siano sempre stati supportati in **Gestione spese**, l'area di lavoro **Spesa riprogettata** consente una suddivisione più efficiente quando la funzione **Possibilità di dettagliare rapidamente le spese ricorrenti** è abilitata.  

## <a name="enable-quick-itemization"></a>Abilitare i dettagli rapidi 

Puoi usare la funzionalità **Possibilità di dettagliare rapidamente le spese ricorrenti** per dettagliare rapidamente le spese ricorrenti evitando di dover inserire ogni volta le spese giornaliere per tutta la durata del soggiorno. Per abilitare i dettagli rapidi, completa i seguenti passaggi.

1. Vai nell'area di lavoro **Gestione funzionalità** e nell'elenco delle funzionalità, individua e seleziona **Note spese riprogettate**. 
2. Seleziona **Abilita ora**. 
3. Nell'elenco delle funzionalità, individua e seleziona **Possibilità di dettagliare rapidamente le spese ricorrenti**.
4. Seleziona **Abilita ora**. 

## <a name="itemization-grid"></a>Griglia di dettaglio 

Se una categoria di spesa ha sottocategorie o componenti diversi che compongono la spesa, può essere dettagliata. Per dettagliare una spesa, seleziona la riga di spesa nella nota spese e nel riquadro **Dettagli spese** seleziona **Azioni** > **Dettagli**. Il cursore **Dettagli** visualizza una griglia con i campi. La tabella seguente fornisce un esempio di ogni campo nella griglia e di come il campo viene visualizzato nella nota spese. 

|     Campo          |     Description                                                                                  |     Esempio              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Sottocategoria    |     L'elenco delle sottocategorie configurate sotto il tipo di categoria di spesa **Hotel**.             |     Tariffa giornaliera della camera      |
|     Data di inizio     |     La data in cui la voce di spesa è stata sostenuta per la prima volta.                                           |     13/09/2021           |
|     Tariffa giornaliera     |     L'importo sostenuto per la voce di spesa.                                                    |     200                  |
|     Quantità       |     Il numero di volte in cui la spesa viene ripetuta in un periodo continuo.                       |     3                    |

![Dettaglia la spesa.](media/Itemization%20screen%201.png)

Quando salvi un dettaglio, vedrai una singola riga dettagliata per la quantità specificata nella griglia Dettaglio. Ogni riga inizia nella data specificata nella griglia.

![Report dettagliato.](media/Itemization%20screen%202.png)

