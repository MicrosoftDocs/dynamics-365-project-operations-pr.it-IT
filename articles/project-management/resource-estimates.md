---
title: Stime finanziarie del tempo delle risorse nei progetti
description: Questo argomento fornisce informazioni su come vengono calcolate le stime finanziarie relative al tempo.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aab5c11a7dc23331c935403a4f96ec7197ec1572
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592559"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Stime finanziarie del tempo delle risorse nei progetti

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le stime finanziarie relative al tempo sono calcolate in base a tre fattori: 

- Il tipo di membro del team generico o denominato assegnato a ciascuna attività del nodo foglia nel piano di progetto. 
- Il tipo o la complessità del lavoro.
- La diffusione dell'impegno per l'assegnazione della risorsa nell'attività. 

I primi due fattori influiscono sul costo unitario o sul tasso di fatturazione dell'assegnazione di una risorsa. Il costo unitario o il tasso di fatturazione dell'assegnazione di una risorsa è determinato dagli attributi della risorsa assegnata. Questi attributi includono l'unità organizzativa a cui appartiene la risorsa e il ruolo standard della risorsa. Puoi anche aggiungere attributi personalizzati pertinenti alla tua attività per la risorsa, come il titolo standard o il livello di esperienza, e fare in modo che influenzino il costo unitario o il tasso di fatturazione dell'assegnazione.
Oltre agli attributi della risorsa, anche gli attributi del lavoro, come l'attività, possono influire sul tasso di fatturazione unitario o il tasso di costo dell'assegnazione. Ad esempio, quando determinate attività sono più complesse, l'assegnazione della risorsa a tali attività specifiche comporta un costo unitario o un tasso di fatturazione più elevato rispetto alle attività meno complesse.   

Il terzo fattore fornisce la quantità di ore a quel tasso. Nei casi in cui un'attività copre due periodi di prezzo, è probabile che la prima parte dell'assegnazione di risorse per quell'attività abbia un costo e un prezzo diversi rispetto alla seconda parte dell'attività. La stima del lavoro richiesto in ciascuna assegnazione di risorse è un valore complesso memorizzato con la distribuzione giornaliera del lavoro al giorno.

Per istruzioni dettagliate su come impostare attributi personalizzati di lavoro e risorse come dimensioni di determinazione di prezzi e costi, vedi [Panoramica delle dimensioni di determinazione dei prezzi](../pricing-costing/pricing-dimensions-overview.md).

La stima finanziaria in ogni assegnazione di risorse viene calcolata come **tasso/ora per l'assegnazione moltiplicata per il numero di ore.**  Analogamente alla stima del lavoro, la stima finanziaria per costi e ricavi di ogni assegnazione di risorse è un valore complesso memorizzato con la distribuzione giornaliera dell'importo monetario al giorno. 

## <a name="summarizing-financial-estimates-for-time"></a>Riassumere le stime finanziarie relative al tempo
Una stima finanziaria relative al tempo in un'attività del nodo foglia è la somma delle stime finanziarie in tutte le assegnazioni di risorse per tale attività.

Una stima finanziaria relative al tempo in un'attività di riepilogo o padre è la somma delle stime finanziarie in tutte le relative attività figlio. Questo è il costo del lavoro stimato per il progetto. 

![Stime delle risorse.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Prezzo di costo e valuta di costo predefiniti

Il prezzo di costo predefinito proviene dai listini prezzi associati all'unità contratto del progetto. La valuta di costo di un progetto è sempre la valuta dell'unità contratto del progetto. In un'assegnazione di risorse, la stima finanziaria del costo viene archiviata nella valuta di costo del progetto. A volte, la valuta del tasso di costo nel listino prezzi è diversa dalla valuta di costo del progetto. In questi casi, l'applicazione converte la valuta del prezzo di costo nella valuta del progetto. Nella griglia **Stime**, tutte le stime dei costi sono visualizzate e riepilogate nella valuta di costo del progetto. 

## <a name="default-bill-rate-and-sales-currency"></a>Tasso di fatturazione e valuta di vendita predefiniti

Il prezzo di vendita predefinito proviene dai listini prezzi di progetto associati al contratto di progetto correlato se la transazione viene acquisita o dall'offerta di progetto correlata se la transazione è ancora in fase di prevendita. La valuta di vendita del progetto è sempre la valuta dell'offerta di progetto o del contratto di progetto. In un'assegnazione di risorse, la stima finanziaria delle vendite viene archiviata nella valuta di vendita del progetto. A differenza del costo, il prezzo di vendita impostato nel listino prezzi non può mai essere diverso dalla valuta di vendita del progetto. Non esiste uno scenario in cui è necessaria la conversione della valuta. Nella griglia **Stime**, tutte le stime di vendita sono visualizzate e riepilogate nella valuta di vendita del progetto. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
