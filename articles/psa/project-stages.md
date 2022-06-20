---
title: Tipi di fasi del progetto
description: In questo articolo vengono fornite informazioni sulle fasi di progetto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8d772acce152b08c7986739ac557818e6f97d0fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919065"
---
# <a name="project-stage-types"></a>Tipi di fasi del progetto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Le fasi del progetto sono ideate per riflettere lo stato del progetto durante l'esecuzione dello stesso. Le personalizzazioni possono essere utilizzate per aggiornare automaticamente le fasi con i flussi di processi aziendali, Power Automate o estensioni plug-in.

Le fasi seguenti sono definite nel processo aziendale predefinito:

- Nuovo elemento
- Offerta
- Piano
- Consegna
- Completo
- Chiusura 

## <a name="new"></a>Nuovo

Quando crei un progetto, la fase di progetto è impostata su **Nuovo**. Se il progetto è stato creato a partire da un modello, potrebbe includere dati relativi a pianificazione, stime e team. In caso contrario, è solo un abbozzo di progetto ed è necessario immettere gli altri componenti.

## <a name="quote"></a>Offerta

Quando associ un progetto a un'offerta o quando crei un progetto da un'offerta, la fase di progetto diventa **Offerta** e le date di inizio e di fine stimate vengono aggiornate. Sebbene il progetto sia nella fase **Offerta**, nella scheda **Vendita** della pagina **Entità progetto** vengono visualizzati i dettagli dell'offerta.

## <a name="plan"></a>Piano

Quando acquisisci un'offerta associata a un progetto e il progetto passa alla fase **Contratto**, la fase di progetto diventa **Piano**. Quando il progetto è nella fase **Piano**, la pagina **Entità progetto** visualizza i dettagli del contratto.

## <a name="deliver"></a>Consegna

Quando il piano di progetto viene completato e sei pronto a iniziare il progetto, il responsabile di progetto deve aggiornare la fase di progetto a **Consegna** per indicare che il progetto è stato iniziato.

## <a name="complete"></a>Completo 

Quando il lavoro del progetto viene completato, il responsabile di progetto può aggiornare la fase a **Completo**. Aggiornando la fase di progetto a **Completo**, il responsabile di progetto indica che il lavoro è completato al 100 per cento, ma che rimane aperto di modo che sia possibile registrare qualsiasi inserimento ore o voce di spesa in sospeso.

## <a name="close"></a>Chiusura

Quando tutte le registrazioni sono registrate per il progetto, il responsabile di progetto può aggiornare la fase a **Chiusura**. A quel punto, nessuna transazione può essere registrata e il progetto diventa di sola lettura.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
