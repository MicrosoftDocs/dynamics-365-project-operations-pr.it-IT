---
title: Informazioni sullo stato del progetto
description: Questo argomento fornisce informazioni sullo stato assegnato ai progetti in Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965681"
---
# <a name="understand-project-status"></a>Informazioni sullo stato del progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


La sezione **Stato** nella pagina **Entità progetto** fornisce un riepilogo dello stato di un progetto in base al costo e al lavoro richiesto.


## <a name="status-summary-fields"></a>Campi di riepilogo dello stato

- Il campo **Stato di progetto generale** è un campo modificabile che mostra lo stato globale del progetto. Questo campo utilizza la codifica con colori, come verde, giallo e rosso, per indicare il rischio crescente. 
- Il campo **Commenti** consente al responsabile di progetto di immettere commenti specifici sullo stato. 
- Il campo **Data aggiornamento stato** non è modificabile. Il valore in questo campo è un timestamp che indica quando lo stato è stato aggiornato l'ultima volta.
- I campie **Prestazioni di pianificazione** e **Prestazioni costo** sono impostati in base alla griglia di registrazione. Quando lo scostamento pianificazione e lo scostamento costo per il nodo radice nella vista **Registrazione lavoro richiesto** sono positivi, questi campi vengono aggiornati su **In anticipo**. Quando lo scostamento pianificazione e lo scostamento costo per il nodo radice sono negativi, questi campi vengono impostati su **In ritardo**.
