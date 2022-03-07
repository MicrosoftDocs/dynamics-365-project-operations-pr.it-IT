---
title: Metodi Costi di completamento
description: Questo argomento fornisce informazioni sui metodi utilizzati per calcolare i costi di completamento di un progetto.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fe42ea0e1a5c562ec648fbf2a2924648af80381b9db8ffe0c209cb5247bb2ba2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997971"
---
# <a name="cost-to-complete-methods"></a>Metodi Costi di completamento

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento fornisce informazioni sui metodi utilizzati per calcolare i costi di completamento di un progetto. Esistono più metodi che puoi utilizzare per calcolare il costo di completamento di un progetto. 

Quando crei un preventivo per un progetto, nella pagina **Crea stima**, nel campo **Metodo Costo per il completamento**, è possibile selezionare uno dei seguenti metodi dei costi di completamento.

| Metodo Costo di completamento    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Costo totale: effettivo            | Immettere manualmente i costi stimati nei campi **Costo totale** o **Quantità totale** utilizzando il pulsante **Stima costi** nella **Pagina della stima**. Il sistema sottrae i costi effettivi dai totali inseriti. Il totale è il costo per completare il progetto. Questo metodo non utilizza le stime di spesa e le assegnazioni di risorse immesse in Project Operations create all'interno di Microsoft Dataverse. Il costo totale o la quantità totale possono essere aggiornati manualmente secondo necessità.  |
| Previsione totale: ricavi effettivi        | Le assegnazioni di risorse e le stime di spesa vengono utilizzate per determinare l'importo totale previsto del progetto. I costi effettivi vengono confrontati con questa previsione per calcolare il costo da completare.                                                                                                                                                                                                                                                                          |
| Come stima precedente         | Qui vengono utilizzati gli stessi metodi di stima utilizzati nel periodo precedente. Questo metodo richiede un modello previsionale se il periodo precedente richiedeva un modello previsionale.                                                                                                                                                                                                                                                                                                                           |
| Impostare il costo per completare su zero | Tipicamente utilizzato prima dell'eliminazione del progetto di stima, questo metodo abbina le stime totali con le transazioni effettive registrate e cancella la colonna **Costo per il completamento**. Al termine, il risultato è sempre 100 percento. Per ogni riga di costo creata, la casella di controllo **Previsioni** è deselezionata e la stima totale viene copiata dalla stima dei costi precedente. Il consumo effettivo per il periodo di stima viene detratto dal costo per completare il progetto.              |
| Dal modello di costo           | Il metodo Costo per il completamento è impostato nel modello di costo associato al progetto di stima selezionato.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]