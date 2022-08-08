---
title: Fasi del progetto
description: Questo articolo fornisce informazioni sulle fasi del progetto disponibili in Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a8c8e63a2d8c238f582b67348f88b7285a0b1e12
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177384"
---
# <a name="project-stages"></a>Fasi del progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione lite: dalla transazione alla fatturazione proforma_

Le fasi del progetto sono ideate per riflettere lo stato del progetto durante l'esecuzione dello stesso. Le personalizzazioni possono essere utilizzate per aggiornare automaticamente le fasi con i flussi di processi aziendali, Power Automate o estensioni plug-in.

Le fasi seguenti sono definite nel flusso del processo aziendale predefinito:

- Nuovo elemento
- Offerta
- Piano
- Consegna
- Completamento
- Chiuso 

## <a name="new"></a>Nuovo elemento

Quando crei un progetto, la fase di progetto è impostata su **Nuovo**. Se il progetto è stato creato a partire da un modello, potrebbe includere dati relativi a pianificazione, stime e team. In caso contrario, è un abbozzo di progetto ed è necessario immettere gli altri componenti.

## <a name="quote"></a>Offerta

Quando associ un progetto a un'offerta o quando crei un progetto da un'offerta, la fase di progetto diventa **Offerta** e le date di inizio e di fine stimate vengono aggiornate. Sebbene il progetto sia nella fase **Offerta**, nella scheda **Vendita** della pagina **Entità progetto** vengono visualizzati i dettagli dell'offerta.

## <a name="plan"></a>Piano

Quando acquisisci un'offerta associata a un progetto e il progetto passa alla fase **Contratto**, la fase di progetto diventa **Piano**. Sebbene il progetto sia nella fase **Piano**, nella scheda **Vendita** della pagina **Entità progetto** vengono visualizzati i dettagli del contratto.

## <a name="deliver"></a>Consegna

Quando il piano di progetto viene completato e sei pronto a iniziare il progetto, il responsabile di progetto deve aggiornare la fase di progetto a **Consegna** per indicare che il progetto è stato iniziato.

## <a name="complete"></a>Completo 

Quando il lavoro del progetto viene completato, il responsabile di progetto può aggiornare la fase a **Completo**. Aggiornando la fase di progetto a **Completo**, il responsabile di progetto indica che il lavoro è completato al 100 per cento, ma che rimane aperto di modo che sia possibile registrare qualsiasi inserimento ore o voce di spesa in sospeso.

## <a name="close"></a>Chiusura

Quando tutte le registrazioni sono registrate per il progetto, il responsabile di progetto può aggiornare la fase a **Chiusura**. A quel punto, nessuna transazione può essere registrata e il progetto diventa di sola lettura.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
