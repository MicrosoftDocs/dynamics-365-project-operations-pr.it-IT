---
title: Perché non posso eliminare record dall'entità Valori effettivi?
description: In questo argomento vengono fornite informazioni sul perché non è possibile eliminare record dall'entità Valori effettivi.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752599"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="cad61-103">Perché non posso eliminare record dall'entità Valori effettivi?</span><span class="sxs-lookup"><span data-stu-id="cad61-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cad61-104">Project Service Automation (PSA) non consente di eliminare valori effettivi in quanto questi fungono da origine di riferimento per le transazioni che hanno implicazioni finanziarie per eseguire il downstream di sistemi, ad esempio la contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="cad61-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="cad61-105">Se i valori effettivi potessero essere eliminati, l'integrità delle transazioni di report finanziari potrebbe essere messa in dubbio.</span><span class="sxs-lookup"><span data-stu-id="cad61-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="cad61-106">Per stabilire un audit trail, i clienti devono utilizzare i giornali di registrazione per creare transazioni di compensazione.</span><span class="sxs-lookup"><span data-stu-id="cad61-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

