---
title: Creazione di una fattura proforma manuale
description: Questo argomento fornisce informazioni sulla creazione manuale di una fattura proforma in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4079105"
---
# <a name="creating-a-manual-proforma-invoice"></a>Creazione di una fattura proforma manuale

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

In Dynamics 365 Project Operations, le fatture proforma possono essere create manualmente secondo necessità. Puoi creare manualmente una fattura proforma dalla pagina elenco **Contratti di progetto** o dalla pagina dei dettagli **Contratto di progetto**.

##  <a name="project-contracts-list-page"></a>Pagina elenco Contratti di progetto

Dalla pagina elenco **Contratti di progetto** seleziona uno o più contratti di progetto e crea le fatture per tutti i record selezionati.

Il sistema verifica quale dei contratti di progetto selezionati ha un backlog **Pronto per la fatturazione** datato prima della data odierna. Da questi contratti, il sistema crea bozze di fatture proforma. Se un contratto di progetto ha più clienti, potrebbe esserci una fattura creata per cliente e più fatture per contratto di progetto.

Tutte le fatture del progetto create sono disponibili nella pagina **Fattura** nella sezione **Fatturazione** dell'area **Vendite**.

## <a name="project-contract-details-page"></a>Pagina dei dettagli Contratto di progetto

È anche possibile creare una fattura proforma dalla pagina dei dettagli **Contratto di progetto** che crea la fattura per lo specifico contratto di progetto. Il sistema verifica che il contratto di progetto abbia un backlog **Pronto per la fatturazione** datato prima della data odierna. Da questi contratti, il sistema crea bozze di fatture proforma in base al numero di clienti su ciascuna voce di contratto.

Quando viene creata una singola fattura proforma, viene visualizzata la pagina **Fattura**. Se sono presenti più fatture create per quel contratto di progetto, la pagina elenco **Fatture** si apre per mostrare tutte le fatture create.
