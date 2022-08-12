---
title: Configurare il chilometraggio utilizzando i livelli di tariffa chilometrica
description: Questo articolo fornisce informazioni sulle tariffe chilometriche e sui livelli di tariffa chilometrica.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9689bbaf4c4f88ad9f746c3f98676f97e634ab6c
ms.sourcegitcommit: 5e1f549a2e55a87351b2979e3aff402ed35487e1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9064283"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Configurare il chilometraggio utilizzando i livelli di tariffa chilometrica

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Quando viene segnalata una spesa e la categoria di spesa selezionata è **Indennità trasferta**, l'importo per quella riga di spesa è calcolato secondo l'importo *tariffa per chilometraggio*. Questo importo viene determinato utilizzando livelli di tariffe chilometriche definiti o se non sono state impostati, seguendo una tariffa chilometrica standard. 

I livelli tariffari chilometrici possono essere configurati andando a **Gestione spese** > **Configurazione** > **Generale** > **Categorie di spesa** > **Indennità trasferta** > **Configurazione categorie**.

Dopo l'aggiornamento alla versione 10.0.18, se l'organizzazione usa la categoria di spesa di chilometraggio, prendi in considerazione l'abilitazione della funzionalità di chilometraggio dopo aver analizzato le modifiche alla progettazione qui di seguito. 

La nuova progettazione dei livelli di tariffa chilometrica influisce sul modo in cui viene elaborato il valore nel campo **Quantità**. Prima del rilascio della versione 10.0.18, il valore nel campo **Quantità** è stato considerato il limite inferiore. Quando l'accumulo ha superato tale valore, è stato utilizzato il tasso corrispondente.  A partire dalla versione 10.0.18, il valore nel campo **Quantità** è considerato il limite superiore. La tariffa corrispondente viene utilizzata quando l'accumulo di chilometraggio è inferiore al valore nel campo **Quantità**.  Il nuovo modello per i livelli di chilometraggio aiuta con coerenza tra i livelli di chilometraggio e una migliore usabilità.   

Tutte le note spese approvate verranno ricalcolate durante la registrazione in base alla nuova progettazione.

## <a name="example"></a>Esempio
 
### <a name="before-version-10018"></a>Prima della versione 10.0.18
Con due livelli tariffari chilometrici, il campo **Quantità** su ciascun livello rappresenta il limite di chilometraggio inferiore. Attualmente, il livello uno ha un valore di zero (0) e un tasso di 0,45 e il livello due ha un valore di 1.000 e un tasso di 0,25. Se le miglia o i chilometri accumulati superano il valore nel campo, viene utilizzata la relativa tariffa. Se non c'è una riga con quantità zero, il sistema utilizza la tariffa chilometrica definita in Gestione spese. 
 
Se un dipendente invia una nota spese con 1.500 miglia, le due righe di chilometraggio sulla nota spese registrata sarebbero: 1.000 (tasso 0,45) + 500 (tasso 0,25) = 575.

### <a name="after-version-10018"></a>Dopo la versione 10.0.18
Nella versione 10.0.18, il campo **Quantità** in ogni livello rappresenta il limite superiore del livello. Attualmente, il livello uno ha un valore di zero 999 e un tasso di 0,45 e il livello due ha un valore di 999.999.999 e un tasso di 0,25. Se le miglia o i chilometri accumulati superano il valore nel campo **Quantità**, viene utilizzata la relativa tariffa. Se tutti i limiti superiori vengono superati, il sistema utilizza la tariffa chilometrica definita in Gestione spese. 
 
Per calcolare correttamente lo stesso scenario, è necessario modificare l'impostazione del livello. Il campo **Quantità** nel livello uno ha un valore di 999 e un valore di 999.999.999 nel livello due. Se un dipendente supera la quantità totale di miglia o chilometri nel livello uno, il sistema utilizza la tariffa di chilometraggio definita in Gestione spese. 
  
Se un dipendente invia una nota spese con 1.500 miglia, le due righe di chilometraggio sulla nota spese registrata sarebbero: 1.000 (tasso 0,45) + 500 (tasso 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Abilita il calcolo dell'importo del chilometraggio per più livelli di chilometraggio con la stessa funzione tariffaria

La funzionalità **Calcolo dell'importo del chilometraggio per più livelli di chilometraggio con la stessa tariffa** migliora il calcolo della tariffa del chilometraggio. Completa i seguenti passaggi per abilitare questa funzione.

1. Vai a **Aree di lavoro** > **Gestione funzionalità**. 
2. Nell'elenco, individua e seleziona **Calcolo dell'importo delle miglia per più livelli di miglia con la stessa tariffa**, quindi seleziona **Abilita ora**.

Dopo aver abilitato la funzione, reimposta i livelli di chilometraggio in modo che riflettano correttamente il valore del campo **Quantità**. 

## <a name="enable-the-mileage-totals-calculation-by-fiscal-year-feature"></a>Abilitare la funzionalità Calcolo chilometraggio totale per anno fiscale

La funzionalità **Calcolo chilometraggio totale per anno fiscale** abilita una nuova impostazione nei parametri di gestione delle spese che esegue i calcoli del chilometraggio totale per anno fiscale anziché per anno solare. Completa i seguenti passaggi per abilitare questa funzione.

1. Vai a **Aree di lavoro** > **Gestione funzionalità**.
1. Nell'elenco, individua e seleziona **Calcolo chilometraggio totale per anno fiscale**, quindi seleziona **Abilita ora**.
1. Vai a **Gestione spese** > **Impostazioni** > **Generale** > **Parametri di gestione spese**.
1. Nella pagina **Parametri di gestione spese** individua e abilita **Usa anno fiscale per chilometraggio totale**.

Dopo aver abilitato **Usa anno fiscale per chilometraggio totale**, il chilometraggio totale viene calcolato per anno fiscale.

[!INCLUDE[footer-include](../includes/footer-banner.md)]