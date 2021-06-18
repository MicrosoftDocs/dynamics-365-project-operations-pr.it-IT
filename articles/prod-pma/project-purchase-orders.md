---
title: Ordini di acquisto per un progetto
description: In questo articolo vengono descritti i vari metodi che puoi utilizzare per creare ordini di acquisto per un progetto. Il metodo utilizzato dipende dallo scopo dell'ordine di acquisto e da quando gli articoli vengono utilizzati e addebitati in un progetto.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999361"
---
# <a name="purchase-orders-for-a-project"></a>Ordini di acquisto per un progetto

[!include [banner](../includes/banner.md)]

In questo articolo vengono descritti i vari metodi che puoi utilizzare per creare ordini di acquisto per un progetto. Il metodo utilizzato dipende dallo scopo dell'ordine di acquisto e da quando gli articoli vengono utilizzati e addebitati in un progetto.

### <a name="methods-for-creating-a-purchase-order"></a>Metodi per creare un ordine di acquisto

Puoi utilizzare uno dei seguenti metodi per creare un ordine di acquisto in Gestione progetti e contabilità. Lo scopo dell'ordine di acquisto determina quando l'ordine di acquisto viene consumato e, di conseguenza, quando gli articoli vengono addebitati in un progetto.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metodo</th>
<th>Scopo</th>
<th>Utilizzo di articoli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Crea un ordine di acquisto direttamente da un progetto.</td>
<td>Utilizza questo metodo per acquistare articoli da un fornitore esterno per l'utilizzo in un progetto. L'ordine di acquisto può essere creato in due modi:
<ul>
<li>Dal progetto stesso. In questo caso, il progetto è già definito per l'ordine di acquisto.</li>
<li>Mediante accesso all'ordine di acquisto del progetto. Devi selezionare sia il fornitore che il progetto per cui creare l'ordine di acquisto.</li>
</ul></td>
<td>Gli articoli vengono utilizzati quando la fattura fornitore viene aggiornata.</td>
</tr>
<tr class="even">
<td>Crea un ordine di acquisto da un ordine di vendita.</td>
<td>Utilizza questo metodo per acquistare articoli quando crei un ordine di vendita da un progetto.</td>
<td>Gli articoli vengono utilizzati quando l'ordine di vendita viene fatturato al cliente.</td>
</tr>
<tr class="odd">
<td>Crea un ordine di acquisto da un requisito articolo.</td>
<td>Utilizza questo metodo per acquistare articoli quando crei un requisito articolo da un progetto.</td>
<td>Gli articoli vengono utilizzati quando viene aggiornato il documento di trasporto del requisito articolo.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Quando aggiorni la fattura fornitore o il documento di trasporto, viene richiesto di aggiornare il documento di trasporto relativo al requisito dell'articolo.

Per altre informazioni, vedi [Ricevere gli articoli nell'ordine di acquisto dal requisito dell'articolo](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]