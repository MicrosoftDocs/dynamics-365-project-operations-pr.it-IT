---
title: Creare una fattura proforma manuale - semplice
description: Questo argomento fornisce informazioni sulla creazione manuale di una fattura proforma in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274193"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Creare una fattura proforma manuale - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

In Dynamics 365 Project Operations, le fatture proforma possono essere create manualmente secondo necessità. Puoi creare manualmente una fattura proforma dalla pagina elenco **Contratti di progetto** o dalla pagina dei dettagli **Contratto di progetto**.

##  <a name="project-contracts-list-page"></a>Pagina elenco Contratti di progetto

Dalla pagina elenco **Contratti di progetto** seleziona uno o più contratti di progetto e crea le fatture per tutti i record selezionati.

Il sistema verifica quale dei contratti di progetto selezionati ha un backlog **Pronto per la fatturazione** datato prima della data odierna. Da questi contratti, il sistema crea bozze di fatture proforma. Se un contratto di progetto ha più clienti, potrebbe esserci una fattura creata per cliente e più fatture per contratto di progetto.

Tutte le fatture del progetto create sono disponibili nella pagina **Fattura** nella sezione **Fatturazione** dell'area **Vendite**.

## <a name="project-contract-details-page"></a>Pagina dei dettagli Contratto di progetto

Puoi creare una fattura proforma anche dalla pagina dei dettagli **Contratto di progetto**. Il sistema verifica che il contratto di progetto abbia un backlog **Pronto per la fatturazione** datato prima della data odierna. Da questi contratti, il sistema crea bozze di fatture proforma in base al numero di clienti su ciascuna voce di contratto.

Quando viene creata una singola fattura proforma, viene visualizzata la pagina **Fattura**. Se vengono create più fatture per quel contratto di progetto, viene visualizzata la pagina di elenco **Fatture** per mostrare tutte le fatture create.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]