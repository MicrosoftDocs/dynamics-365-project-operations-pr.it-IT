---
title: Determinare stime di manodopera, costi e ricavi
description: Come determinare le stime dei ricavi e dei costi del progetto in Project Service
author: ruhercul
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5d1bdde3c376a74952d54a1e7fade1f48e675d2f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580231"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Determinare stime di manodopera, costi e ricavi 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Le stime di progetto offrono la visualizzazione finanziaria per il lavoro stimato e pianificato nella struttura di suddivisione del lavoro del progetto. La visualizzazione delle stime informa dell'impatto dei costi e dei ricavi del lavoro pianificato. La visualizzazione delle stime fornisce uno strumento per visualizzare le informazioni in un numero di dimensioni predefinite per informare meglio dell'impatto finanziarie del progetto.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Valore di costi e vendite del progetto  
I listini prezzi di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] definiscono i tassi di vendita o fatturazione per i ruoli utilizzati dai progetti. In base ai ruoli associati alle attività nella struttura di suddivisione del lavoro di progetto, puoi definire l'impatto dei costo e dei ricavi del lavoro interessato.  
  
## <a name="cost-price-defaulting"></a>Impostazione predefinita del prezzo di costo  
Ogni progetto appartiene a un'organizzazione (indicata in **Unità proprietaria** nel progetto). Il listino prezzi associato all'unità organizzativa proprietaria determina il prezzo di costo unitario. Le funzionalità di [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] determinano i prezzi di costo per i ruoli cercando la combinazione di ruolo, unità e unità organizzativa nel listino prezzi di costo per ottenere il prezzo di costo corretto per la data effettiva nelle righe dei valori.  
  
Se la combinazione di ruolo, unità e unità organizzativa non dà come risultato un prezzo di costo dal listino prezzi dell'unità di proprietà, l'unità viene ignorata in favore della combinazione del ruolo e della unità organizzativa. Se c'è un prezzo di costo, questo viene convertito nell'unità scelta nella riga di stima.  
  
Se la combinazione di ruolo e unità organizzativa non dà come risultato un prezzo di costo, l'unità organizzativa viene ignorata in favore della combinazione ruolo e unità e il prezzo verrà impostato come predefinito dopo avere applicato la conversione, se richiesto.  
  
 Se non c'è un prezzo per il ruolo, allora il prezzo di costo viene impostato su 0,00 nella riga di stima.  
  
 Tutti gli importi del costo nelle righe di stima del costo di progetto sono nella valuta dell'unità organizzativa proprietaria.  
  
## <a name="sales-price-defaulting"></a>Impostazione predefinita del prezzo di vendita  
Il listino prezzi di vendita si basa sull'entità di vendita a cui il progetto è allegato. Il listino prezzi di vendita associato all'offerta o al contratto determina il prezzo di vendita. Se l'offerta o il contratto ha un listino prezzi personalizzato, questo è il listino prezzi predefinito per le stime di progetto. Se non esiste un'associazione alle entità di vendita, allora il listino prezzi di vendita predefinito configurato nelle impostazioni dei parametri sarà il listino prezzi di vendita predefinito per il progetto. Ogni riga di stima ha un'unità organizzativa della risorsa associata per indicare l'unità organizzativa da cui le risorse verranno prenotate per il completamento dell'attività. Il prezzo di vendita per i ruoli associati viene determinato cercando la combinazione di ruolo, unità e unità organizzativa della risorsa nel listino prezzi di vendita per ottenere il prezzo di vendita corretto per la data effettiva nelle righe di stima.  
  
Se la combinazione di ruolo, unità e unità organizzativa della risorsa non dà come risultato un prezzo di vendita dal listino prezzi di vendita, il sistema ignorerà l'unità e la ricerca per la combinazione del ruolo e dell'unità organizzativa delle risorse. Se viene rilevato un prezzo di vendita, questo viene convertito nell'unità scelta nella riga di stima delle vendite.  
  
Se il sistema non trova un prezzo per il ruolo, allora il prezzo di vendita deve essere impostato su 0,00 nella riga di stima.  
  
Le stime vengono visualizzate in una griglia che mostra una griglia piana delle righe di stima con i costi unitari, totali e i prezzi di vendita.  
  
## <a name="time-phased-view-of-project-estimates"></a>Visualizzazione su scala cronologica delle stime di progetto  
Nella visualizzazione su scala cronologica per le stime di progetto, i dati relativi alle stime dalla visualizzazione a griglia vengono imperniati per impostazione predefinita in base al ruolo e mostrano una gamma di dati di stima nella scala cronologica scelta.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Allocazione delle stime lavoro in base alla modalità attività  
Nella visualizzazione su scala cronologica, il lavoro totale stimato per l'attività viene distribuito allocando un determinato numero di ore lavorative per periodo di tempo unitario della scala cronologica scelta. In Project Service la modalità attività determina lo sforzo allocato nella durata dell'attività. I due tipi di allocazione sono allocazione pari e allocazione basata sulle ore lavorative. 
  
## <a name="work-hours-based-allocation"></a>Allocazione basata su ore lavorative  
La modalità dell'attività di pianificazione automatica per un'attività la regola per il numero di risorse stimate nell'attività, esse sono stimate per essere utilizzare per tutte le ore lavorative del giorno. Si applica quando si alloca il lavoro suddividendolo per la durata delle attività anche nella visualizzazione su scala cronologica. Ad esempio, in una scala cronologica "Giorno", per un'attività il cui completamento è stimato da parte di una risorsa, il lavoro assegnato al giorno non supererà le ore lavorative giornaliere definite nel calendario del progetto. Pertanto, l'allocazione del lavoro assicura sempre che le risorse siano stimate per essere utilizzate il giorno intero.  
  
## <a name="even-distribution"></a>Distribuzione pari  
La modalità dell'attività pianificata manualmente non rispetta le ore lavorative, il calendario di progetto, nonché il numero di risorse definite nell'attività. La pianificazione dell'attività è basata sull'input utente. Per tali attività, l'allocazione del lavoro per periodo di tempo dell'unità della scala cronologica scelta non ha alcun fattore di limitazione. Il lavoro totale nell'attività è ugualmente suddiviso e assegnato per ogni periodo di tempo dell'unità sulla scala cronologica scelta.  
  
In questo modo, la modalità dell'attività definita nell'attività determina la distribuzione del lavoro o l'allocazione per periodo di tempo dell'unità in stime su scala cronologica.  
  
## <a name="grouping-and-time-phasing-options"></a>Opzioni di raggruppamento e suddivisione in fase  
Questa visualizzazione consente di conoscere la distribuzione delle stime di lavoro, costo e vendite su base giornaliera, settimanale o annuale. L'opzione Raggruppa per consente di imperniare i dati delle stime su due altre dimensioni: categoria e risorsa. Nella visualizzazione a griglia e nella visualizzazione su scala cronologica puoi scegliere i campi da visualizzare. I totali per ognuno degli intervalli di tempo vengono visualizzati nella parte inferiore che indica il lavoro stimato totale, il costo e le vendite per il giorno, la settimana, il mese o l'anno.  
  
Il prezzo di vendita e costo impostato come valore predefinito è basato sulla data. Quando le tariffe per il ruolo cambiano sarà più trasparente nella visualizzazione su scala cronologica rispetto a quando vengono visualizzati i dati di stima imperniati su "Risorsa" e su scala cronologica per settimana.  
  
## <a name="expense-estimates"></a>Stime di spesa  
Le spese che verranno affrontate nel progetto non direttamente correlate alla manodopera da spendere possono essere registrate nelle stime di progetto nella visualizzazione griglia. Tramite l'opzione **Aggiungi stime di spesa** nella visualizzazione griglia, puoi eseguire quanto segue. Le stime di spesa possono essere registrate per una specifica attività o per l'intero progetto. Puoi scegliere le categorie di spesa su queste righe e scegliere una data provvisoria in cui vuoi sostenere la spesa. Se il costo associato e il listino prezzi di vendita hanno prezzi predefiniti, o percentuali di ricarico definite per le categorie di spesa, questo verrà impostato come valore predefinito nella riga delle stime nell'associazione.  
  
### <a name="see-also"></a>Vedi anche  
 [Guida del responsabile di progetto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
