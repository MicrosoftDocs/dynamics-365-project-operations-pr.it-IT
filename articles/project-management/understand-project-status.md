---
title: Informazioni sullo stato del progetto
description: Questo argomento fornisce informazioni sullo stato assegnato ai progetti in Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9efa6135bbaa98f8968e09fcf38c9dd4fde84fe4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578897"
---
# <a name="understand-project-status"></a>Informazioni sullo stato del progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


La sezione **Stato** nella pagina **Entità progetto** fornisce un riepilogo dello stato di un progetto in base al costo e al lavoro richiesto.


## <a name="status-summary-fields"></a>Campi di riepilogo dello stato

- Il campo **Stato di progetto generale** è un campo modificabile che mostra lo stato globale del progetto. Questo campo utilizza la codifica con colori, come verde, giallo e rosso, per indicare il rischio crescente. 
- Il campo **Commenti** consente al responsabile di progetto di immettere specifici commenti sullo stato. 
- Il campo **Data aggiornamento stato** non è modificabile. Il valore in questo campo è un timestamp che indica quando lo stato è stato aggiornato l'ultima volta.
- I campi **Prestazioni di pianificazione** e **Prestazioni costo** sono impostati in base alla griglia di tracciabilità. Quando lo scostamento pianificazione e lo scostamento costo per il nodo radice nella vista **Tracciabilità risorse** sono positivi, questi campi vengono impostati su **In anticipo**. Quando lo scostamento pianificazione e lo scostamento costo per il nodo radice sono negativi, questi campi vengono impostati su **In ritardo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]