---
title: Panoramica del processo di fatturazione
description: Questo articolo fornisce una panoramica del processo di fatturazione in Project Operations per scenari basati su risorse non stoccate.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923101"
---
# <a name="invoicing-process-overview"></a>Panoramica del processo di fatturazione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Project Operations per scenari basati su risorse/non stoccate offre funzionalità complete su misura per soddisfare le esigenze sia del Project manager che dell'addetto alla contabilità clienti/ contabile di progetto. Per il processo di fatturazione, il responsabile di progetto gestisce il backlog di fatturazione del progetto e l'addetto alla contabilità clienti/contabile di progetto crea un documento fattura conforme e accurato rivolto al cliente.

![Diagramma del flusso di fatturazione.](./media/invoicing-flow.png)

La riga del contratto di progetto definisce il metodo di fatturazione per le transazioni di progetto associate. Quando il responsabile di progetto approva le transazioni relative a tempo e spese, il sistema registra le transazioni nell'entità **Valori effettivi di progetto**, quindi invia le informazioni al modulo **Gestione progetti e contabilità** in Dynamics 365 Finance. Il contabile del progetto quindi rivede e registra i record utilizzando il [giornale Integrazione Project Operations](../project-accounting/project-operations-integration-journal.md). Questo giornale di registrazione include importanti dettagli contabili per i valori effettivi del progetto, come fatturazione, fascia IVA, fascia IVA articoli di fatturazione e dimensioni finanziarie.

Il responsabile di progetto può rivedere le transazioni di vendita non fatturate utilizzando il metodo di fatturazione tempo e materiali in [Backlog di fatturazione tempo e materiale](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) e la fatturazione a prezzo fisso in [Passaggi fondamentali prezzo fisso](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Queste visualizzazioni consentono di filtrare e selezionare le transazioni che devono essere incluse nel ciclo di fatturazione successivo e quindi contrassegnarle come **Pronto per la fatturazione**.

Puoi [creare manualmente una fattura proforma](../proforma-invoicing/create-manual-proforma-invoice.md) o usare un [processo periodico](../proforma-invoicing/configure-automated-invoice-creation.md). Il responsabile di progetto può [modificare una bozza di fattura proforma](../proforma-invoicing/manage-proforma-invoice.md) secondo necessità e quindi confermarla.

La fattura proforma confermata viene inviata al modulo **Gestione progetti e contabilità** in Finance. Il contabile di progetto formatta e aggiorna la proposta di fattura del progetto, quindi registra e stampa il documento. Le fatture di progetto registrate vengono registrate nella contabilità generale, nonché nei registri secondari del cliente e del progetto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]