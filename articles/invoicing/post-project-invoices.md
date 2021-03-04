---
title: Panoramica del processo di fatturazione
description: Questo argomento fornisce una panoramica del processo di fatturazione in Project Operations per scenari di risorse/materiali non stoccati.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fbc1519b6cbcf231cfa89df8b7843d11a8904e49
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089259"
---
# <a name="invoicing-process-overview"></a>Panoramica del processo di fatturazione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Project Operations per scenari basati su risorse/non stoccate offre funzionalità complete su misura per soddisfare le esigenze sia del Project manager che dell'addetto alla contabilità clienti/ contabile di progetto. Per il processo di fatturazione, il responsabile di progetto gestisce il backlog di fatturazione del progetto e l'addetto alla contabilità clienti/contabile di progetto crea un documento fattura conforme e accurato rivolto al cliente.

![Diagramma del flusso di fatturazione](./media/invoicing-flow.png)

La riga del contratto di progetto definisce il metodo di fatturazione per le transazioni di progetto associate. Quando il responsabile di progetto approva le transazioni di tempo e spese, il sistema registra le transazioni nell'entità **Valori effettivi di progetto** e invia le informazioni al modulo **Gestione progetti e contabilità** in Dynamics 365 Finance. Il contabile del progetto quindi rivede e registra i record utilizzando il [giornale Integrazione Project Operations](../project-accounting/project-operations-integration-journal.md). Questo giornale di registrazione include importanti dettagli contabili per i valori effettivi del progetto, come fatturazione, fascia IVA, fascia IVA articoli di fatturazione e dimensioni finanziarie.

Il responsabile di progetto può rivedere le transazioni di vendita non fatturate utilizzando il metodo di fatturazione tempo e materiali in [Backlog di fatturazione tempo e materiale](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) e la fatturazione a prezzo fisso in [Passaggi fondamentali prezzo fisso](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Queste visualizzazioni consentono di filtrare e selezionare le transazioni che devono essere incluse nel ciclo di fatturazione successivo e quindi contrassegnarle come **Pronto per la fatturazione**.

Puoi [creare manualmente una fattura proforma](../proforma-invoicing/create-manual-proforma-invoice.md) o usare un [processo periodico](../proforma-invoicing/configure-automated-invoice-creation.md). Il responsabile di progetto può [modificare una bozza di fattura proforma](../proforma-invoicing/manage-proforma-invoice.md) secondo necessità e quindi confermarla.

La fattura proforma confermata viene inviata al modulo **Gestione progetti e contabilità** in Finance. Il contabile di progetto formatta e aggiorna la proposta di fattura del progetto, quindi registra e stampa il documento. Le fatture di progetto registrate vengono registrate nella contabilità generale, nonché nei registri secondari del cliente e del progetto.
