---
title: Panoramica della fatturazione interaziendale
description: Questo argomento fornisce informazioni ed esempi sulla fatturazione interaziendale per i progetti.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c343c5bf525574e496036793cd4e131394e8b1b471153147a66cfebe1acf3fce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005396"
---
# <a name="intercompany-invoicing-overview"></a>Panoramica della fatturazione interaziendale

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

La tua organizzazione potrebbe avere più divisioni, filiali e altre persone giuridiche che trasferiscono prodotti e servizi tra loro per i progetti. L'entità giuridica che fornisce il servizio o il prodotto è denominata *persona giuridica che effettua la concessione*. L'entità giuridica che riceve il servizio o il prodotto è denominata *persona giuridica richiedente*.

L'illustrazione seguente mostra uno scenario tipico in cui due persone giuridiche, Contoso Robotics USA (la persona giuridica mutuataria) e Contoso Robotics UK (la persona giuridica che concede il prestito) condivide le risorse per consegnare un progetto al cliente, Adventure Works. Per questo scenario, Contoso Robotics USA è incaricata di consegnare il lavoro ad Adventure Works.

![Fatturazione interaziendale.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations utilizza il flusso seguente per elaborare le transazioni interaziendali:

1. Le risorse della persona giuridica che effettua la concessione registrano le transazioni di tempo o di spesa interaziendali registrando tempi e costi a fronte dei progetti della persona giuridica richiedente.
2. I costi e tempi sono registrati nella società richiedente utilizzando il listino prezzi unitario di costo della società richiedente.
3. Le transazioni di vendita non fatturate interaziendali sono registrate nella società richiedente utilizzando il listino prezzi unitario di costo della società richiedente.
4. I ricavi non fatturati vengono registrati nella società richiedente utilizzando il listino prezzi di vendita del contratto di progetto. Il cliente può essere fatturato quando vengono registrati i ricavi non fatturati. Il cliente non deve attendere il completamento dell'elaborazione della fattura interaziendale.
5. Le fatture dei clienti interaziendali vengono create periodicamente nella società che effettua la concessione. Le fatture vengono create manualmente o utilizzando un processo periodico automatizzato. È possibile creare un'unica fattura per ciascuna persona giuridica debitrice oppure è possibile creare fatture separate per progetto.
6. Quando viene registrata una fattura cliente interaziendali nella persona giuridica che effettua la concessione, la fattura fornitore in sospeso corrispondente viene creata nella persona giuridica richiedente. I costi nella fattura fornitore in sospeso verranno registrati nel registro secondario del progetto quando la fattura viene registrata.

Il diagramma seguente illustra la fatturazione interaziendale in quanto si riferisce a eventi contabili e registrazioni previste nella contabilità generale.

![Flusso interaziendale.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Risorse aggiuntive

- [Configurare la fatturazione interaziendale](configure-intercompany-invoicing.md)
- [Registrare transazioni interaziendali](create-intercompany-transactions.md)
- [Creare fatture interaziendali per clienti e fornitori](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]