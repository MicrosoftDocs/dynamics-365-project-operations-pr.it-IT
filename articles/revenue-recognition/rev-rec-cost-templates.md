---
title: Configurare i modelli di costo
description: Questo argomento fornisce informazioni su come creare e utilizzare i modelli di costo in Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f4a515db31a31028af4a60927ab360be6c261a3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013896"
---
# <a name="set-up-cost-templates"></a>Configurare i modelli di costo

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_


Questo argomento fornisce informazioni su come creare e utilizzare i modelli di costo in Project Operations. Un modello di costo determina:

- Le categorie di progetto per le transazioni previste ed effettive da includere in una percentuale del calcolo del completamento del progetto. Il valore della percentuale di completamento viene quindi utilizzato per calcolare l'ammontare dei ricavi riconosciuti.
- In caso la percentuale di completamento possa essere modificata se viene calcolata automaticamente.
- Se la percentuale di completamento viene calcolata in base a importi o unità.

## <a name="cost-template-example"></a>Esempio di modello di costo

Stai lavorando a un progetto di design di un sito Web per un cliente in cui addebiti un prezzo fisso di 10.000 dollari. Prevedi che saranno necessarie 100 ore (5.000 USD) per completare il progetto. Prevedi anche due biglietti aerei e quattro notti in hotel per recarti al sito del cliente (1.800 USD). Ciò si traduce in un costo totale previsto di 6.800 dollari.

Quando esegui il processo di riconoscimento dei ricavi a prezzo fisso per creare una stima alla fine del mese, scopri di aver lavorato 35 ore al progetto. Questo non include ancora i costi per volo o hotel. Hai anche chiesto a un assistente di eseguire cinque ore di ricerca per il progetto al costo di 100 dollari, che non avevi pianificato.

Quando calcoli il valore di completamento percentuale per questo progetto, puoi effettuare le seguenti scelte:

- Vuoi includere tutti i costi (ore e spese) o solo le ore?
- Vuoi includere tutte le ore o solo le ore pianificate?
- Vuoi calcolare la percentuale di completamento in base al costo in dollari delle ore pianificate (5.000 USD) o semplicemente il numero di ore (100)?

Le risposte a queste domande determinano le opzioni impostate nel modello di costo e le categorie selezionate nelle righe del modello di costo.

La tabella seguente illustra i risultati dei diversi metodi di calcolo del valore di percentuale di completamento per questo scenario.

| Completamento basato su | Costo o unità in dollari | Percentuale di completamento | Calcolo |
| --- | --- | --- | --- |
| Tutte le ore, nessuna spesa | Costo in dollari | 37% 35 x USD 50 + USD 100 = USD 1.850 USD 1.850/USD 5.000 |
| Tutte le ore, nessuna spesa | Insieme unità misura | 40 % | 40 ore/100 ore (comprese cinque ore non pianificate) |
| Ore pianificate, nessuna spesa | Costo o unità in dollari | 35% | 35/100 ore o 35 x 50/5.000 USD |
| Tutte le ore e le spese | Costo in dollari | 27,2 % | USD 1.850/USD 6.800 |

La decisione relativa a quale approccio adottare per creare un modello di costo può dipendere da diverse considerazioni:

- Se includi ore non pianificate nel modello di costo, rischi di raggiungere il 100 percento di completamento prima che il progetto sia finito. Questo perché le ore effettive saranno maggiori delle ore pianificate. Se utilizzi uno dei primi due metodi elencati nella tabella, dovresti modificare il piano (unità previste) quando ti accorgi delle deviazioni. In questo caso, dovresti aggiungere o sottrarre ore in base alla tua conoscenza di ciò che è necessario per completare il progetto. Se il progetto richiederà altre 65 ore per essere completato, aggiungerai cinque ore al piano per un totale di 105. Se sai che il tuo assistente eseguirà altre cinque ore di ricerca, il totale diventerà 110 ore.
- Se utilizzi il terzo metodo elencato nella tabella, aggiorneresti solo le ore pianificate per il tuo tempo per mantenere accurato il calcolo della percentuale di completamento. La tua redditività cambierà quando vengono registrate ore non pianificate, ma rimarrai su una traiettoria percentuale di completamento nota.
- Se utilizzi il quarto metodo elencato nella tabella, il rischio è che le spese si verifichino in tempi irregolari e potrebbero non riflettersi nell'avanzamento del completamento. Pertanto, se le spese sono incluse, possono far fluttuare la percentuale di completamento più del necessario. Ad esempio, poiché non hai ancora preso un volo, la tua percentuale di completamento era del 27% invece che del 35% o del 37% se avessi basato il calcolo solo sul tempo. Se avessi fatto un viaggio per due notti e avessi previsto con precisione i costi del volo e dell'hotel, la percentuale di completamento sarebbe stata del 40,4% (1.850 USD per il lavoro e 900 USD per le spese = USD 2.750/6.800 USD = 40,4%). Pertanto, sostenere le spese per un solo viaggio in aereo cambierebbe la percentuale di completamento dal 27% al 40%.

## <a name="create-cost-templates"></a>Crea modelli di costo
Per creare modelli di costo, seguire questi passaggi:

1. Per accedere ai modelli di costo, nell'ambiente Dynamics 365 Finance, vai a **Contabilità e gestione dei progetti** > **Configurazione** > **Stime** > **Modello di costo**.
2. Selezionare **Nuovo** per creare un nuovo modello di costo. Immetti un nome e una descrizione.
3. Fornisci l'ID della riga di costo per ogni tipo di transazione.
4. Seleziona un metodo di completamento predefinito:

  - **Automatico**: la percentuale di completamento viene calcolata automaticamente su un progetto. Non puoi modificare il valore risultante.
  - **Manuale**: la percentuale di completamento viene calcolata automaticamente su un progetto. Puoi modificare il valore risultante.

  > [!NOTE]
  > Per i calcoli manuali, la percentuale di completamento viene mantenuta in **Calcolo manuale** nella scheda **Generale** nella pagina **Stima**.

5. In **Completamento basato su**, seleziona uno dei seguenti valori:

  - **Quantità** : l'importo in valuta di contabilizzazione calcola la percentuale di completamento.
  - **Unità**: la quantità calcola la percentuale di completamento.
  - **Linea retta**: il sistema calcola la percentuale di completamento su base proporzionale utilizzando le date di inizio e di fine del progetto per determinare la durata del progetto.

6. Selezionare **Righe dei costi** per rivedere le righe di costo del modello di costo. È richiesta almeno una riga di costo per ogni tipo di transazione. Tuttavia, è possibile creare più righe di costo per gli stessi tipi di transazione e impostare gli attributi desiderati per queste righe.
7. Nella scheda **Categorie**, selezionare le categorie di progetto da includere nella riga del modello di costo.
8. Nella scheda **Generale**, selezionare se questa riga sarà inclusa nel calcolo della percentuale di completamento.
9. Selezionare il costo per completare il metodo da utilizzare nel calcolo della percentuale di completamento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]