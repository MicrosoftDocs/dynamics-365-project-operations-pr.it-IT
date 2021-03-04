---
title: Anticipi e contratti basati su acconto
description: Questo argomento fornisce informazioni sui modelli di contratto basato su acconto o sugli anticipi in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1aee64bf683b7d8d0bcde284f2d5d484e689c4d2
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596107"
---
# <a name="advances-and-retainer-based-contracts"></a>Anticipi e contratti basati su acconto


_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations supporta contratti basati su acconto. Un contratto basato su acconto è una serie negoziata di pagamenti equamente distribuiti che verranno fatturati al cliente per tutta la durata di un progetto. Questo tipo di contratto viene generalmente utilizzato per modelli di fatturazione basati su tempo e materiali o consumo in cui è necessario fornire al cliente una fatturazione e una pianificazione dei pagamenti prevista. I ricavi effettivi maturati in ciascun periodo vengono riconciliati con il pagamento ricevuto dal cliente all'inizio del periodo. In accordo con il concetto del modello di fatturazione Tempo e materiali, i valori dei ricavi maturati in ciascun periodo possono variare in base ai costi sostenuti. Se le entrate maturate sono superiori all'importo ricevuto all'inizio del periodo, la società di consegna del progetto può:

- Fatturare al cliente solo l'eccedenza 
- Rinviare la riconciliazione dei ricavi al periodo di fatturazione successivo ed eseguire una fattura finale alla fine del progetto per eventuali entrate non riconciliate rimanenti

La differenza principale tra un modello di contratto basato su acconto e un modello di contratto a prezzo fisso in Project Operations è che nel modello di contratto a prezzo fisso, l'importo della fattura non è collegato o legato ai costi sostenuti. La fatturazione segue un approccio basato su passaggio fondamentale allineato ai costi sostenuti per quel periodo. In un contratto basato su acconto, i ricavi che possono essere fatturati vengono registrati in base al metodo di fatturazione nella voce di contratto. Quando il metodo di fatturazione è tempo e materiali, il ricavo fatturabile è legato ai costi sostenuti in un determinato periodo e può variare da un periodo all'altro. Tuttavia, al cliente viene fatturato solo l'importo dell'acconto periodico. Il sistema utilizza un'altra fattura alla fine del periodo per riconciliare i ricavi fatturabili registrati durante il periodo con l'importo che è stato fatturato al cliente all'inizio del periodo.

Il vantaggio di questo metodo è che i costi del cliente diventano prevedibili nella pianificazione degli acconti diversamente da un tipico modello di tempo e materiali. L'organizzazione che consegna il progetto ha anche spazio per coprire il rischio di recuperare i costi sostenuti a causa di eventuali aumenti di ambito che un modello a prezzo fisso non avrebbe consentito.

Oltre a una pianificazione periodica basata su acconto, Project Operations può registrare un anticipo una tantum da un cliente e riconciliarlo con i diversi componenti di costo del progetto.

L'acconto in Project Operations non è disponibile per l'uso fino a quando non viene fatturato al cliente. Ciò è indicato dai seguenti campi nella griglia secondaria per anticipi e acconti.

| Campo | Descrizione | Impatto downstream |
| --- | --- | --- |
| Importo disponibile | L'importo disponibile per essere utilizzato nel record di acconto o anticipo. | Fino a quando l'anticipo o l'acconto non viene fatturato, non è disponibile per essere utilizzato, il che significa che l'importo disponibile è zero. |
| Importo utilizzato | L'importo già utilizzato nell'acconto o nell'anticipo. | Un anticipo o un acconto può essere parzialmente riconciliato su una fattura con i costi effettivi che hanno una parte contrassegnata come già utilizzata o consumata. Il resto dell'importo dell'anticipo o dell'acconto è disponibile per la riconciliazione su una fattura futura con i costi effettivi. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]