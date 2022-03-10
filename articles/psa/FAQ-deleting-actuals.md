---
title: Perché non posso eliminare record dall'entità Valori effettivi?
description: In questo argomento vengono fornite informazioni sul perché non è possibile eliminare record dall'entità Valori effettivi.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: d60a3586fd1f0f688bcd2626d039ebc1aa6b0925c90d676f0e716400d8e8d6dd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002876"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Perché non posso eliminare record dall'entità Valori effettivi?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) non consente di eliminare valori effettivi in quanto questi fungono da origine di riferimento per le transazioni che hanno implicazioni finanziarie per eseguire il downstream di sistemi, ad esempio la contabilità generale. Se i valori effettivi potessero essere eliminati, l'integrità delle transazioni di report finanziari potrebbe essere messa in dubbio. Per stabilire un audit trail, i clienti devono utilizzare i giornali di registrazione per creare transazioni di compensazione.



[!INCLUDE[footer-include](../includes/footer-banner.md)]