---
title: Perché non posso eliminare record dall'entità Valori effettivi?
description: In questo argomento vengono fornite informazioni sul perché non è possibile eliminare record dall'entità Valori effettivi.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286073"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="396da-103">Perché non posso eliminare record dall'entità Valori effettivi?</span><span class="sxs-lookup"><span data-stu-id="396da-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="396da-104">Project Service Automation (PSA) non consente di eliminare valori effettivi in quanto questi fungono da origine di riferimento per le transazioni che hanno implicazioni finanziarie per eseguire il downstream di sistemi, ad esempio la contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="396da-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="396da-105">Se i valori effettivi potessero essere eliminati, l'integrità delle transazioni di report finanziari potrebbe essere messa in dubbio.</span><span class="sxs-lookup"><span data-stu-id="396da-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="396da-106">Per stabilire un audit trail, i clienti devono utilizzare i giornali di registrazione per creare transazioni di compensazione.</span><span class="sxs-lookup"><span data-stu-id="396da-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]