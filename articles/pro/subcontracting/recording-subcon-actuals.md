---
title: Tempo di registrazione, spese e utilizzo di materiale per i componenti in conto lavoro
description: Questo articolo spiega in che modo tempo, spesa e utilizzo di materiale registrati nei progetti da componenti in conto lavoro vengono tracciati da Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522518"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Tempo di registrazione, spese e utilizzo di materiale nei progetti per i componenti in conto lavoro

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione lite: dalla transazione alla fatturazione proforma_

Questo articolo spiega in che modo tempo, spesa e utilizzo di materiale registrati nei progetti da componenti in conto lavoro vengono tracciati da Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Costo del tempo del terzista sui progetti
In Project Operations, i lavoratori a contratto possono registrare il tempo sui progetti in modo simile ai dipendenti. Quando si immette il tempo nei progetti e/o nelle attività progettuali, un lavoratore a contratto può selezionare un conto lavoro e una riga di conto lavoro specifici.

Quando il tempo inviato dai lavoratori a contratto viene approvato, il costo del progetto viene registrato utilizzando la tariffa di costo unitario impostata per quella risorsa del lavoratore a contratto nella sezione **Prezzi dei ruoli** del listino di acquisto sul conto lavoro.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Costo delle spese in conto lavoro sui progetti
Quando si inseriscono le spese sostenute per i progetti, è possibile selezionare un conto lavoro e una riga di conto lavoro nella voce di spesa. 

Quando la voce di spesa viene inviata e approvato, il costo della spesa viene registrato nel progetto in base alla tariffa di costo unitario impostata per la categoria di transazione nella sezione **Prezzi delle categorie** del listino di acquisto sul conto lavoro.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Costo dei materiali in conto lavoro sui progetti
Quando si inseriscono i materiali usati per i progetti, è possibile selezionare un conto lavoro e una riga di conto lavoro nel registro utilizzo materiali. Quando il registro utilizzo materiali viene inviato e approvato, il costo del materiale viene registrato nel progetto in base alla tariffa di costo unitario impostata per il prodotto nella sezione **Voci di listino** del listino prezzi di conto lavoro.

L'utilizzo del materiale può essere registrato nei progetti anche per i prodotti fuori catalogo. Questo tipo di utilizzo del materiale può anche essere collegato a un conto lavoro e a una riga di conto lavoro. Quando si registra l'utilizzo del materiale per i prodotti fuori catalogo, è necessario inserire il costo unitario del prodotto fuori catalogo. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
