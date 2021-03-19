---
title: Configurare una pianificazione acconti
description: Questo argomento fornisce informazioni su come impostare una pianificazione di acconti in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d90781407f11c93b9fb9e0cd2446e102e216b8db
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272274"
---
# <a name="set-up-a-retainer-schedule"></a>Configurare una pianificazione acconti

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le pianificazioni di acconti sono impostate nella pagina **Contratto di progetto** in Dynamics 365 Project Operations.

1. Nella pagina **Contratto di progetto** nella scheda **Anticipi e acconti** seleziona **Configura pianificazione acconti**.
2. Nella pagina di dialogo che si apre, vengono mostrati i campi elencati nella seguente tabella. La tabella fornisce un'idea di come i valori immessi influiscono o influenzano la pianificazione degli acconti che verrà creata.

| Campo | Descrizione | Impatto downstream |
| --- | --- | --- |
| Cliente contratto di progetto | A quale cliente del contratto verrà fatturato questo anticipo o acconto. | Se hai più clienti nel contratto e vuoi fatturare a ciascuno di essi un acconto o un importo anticipato specifico, crea manualmente una fattura per ogni cliente. |
| Avvio pianificazione acconti | Immetti la data di inizio della panificazione acconti. | Questa data potrebbe non essere la data in cui viene creato il primo acconto o anticipo. La data in cui viene creato il primo acconto o anticipo è influenzata anche dalla frequenza di fatturazione. |
| Fine pianificazione acconti | Immetti la data di fine della panificazione acconti. | Questa data potrebbe non essere la data in cui viene creato l'ultimo acconto o anticipo. La data in cui viene creato l'ultimo acconto o anticipo è influenzata anche dalla frequenza di fatturazione. |
| Numero di acconti da creare | Quando immetti il numero di utilità di acconti da creare, il sistema utilizza la data di inizio e la frequenza per creare il numero in questo campo. | Quando questo campo viene aggiornato manualmente, il sistema ignora il valore nel campo **Fine pianificazione acconti** e crea invece il numero specifico di acconti o anticipi. |
| Frequenza di fatturazione | Con quale frequenza l'applicazione creerà acconti e anticipi. | Questo valore influenza direttamente il numero di acconti e anticipi e le date di creazione. |
| Totale importo | L'importo totale è l'importo che viene suddiviso nei singoli pagamenti di acconto o anticipo che verranno creati. | Non vi è alcun impatto downstream per questo campo. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]