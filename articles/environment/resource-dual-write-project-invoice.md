---
title: Integrazione di fatture di progetto
description: Questo argomento fornisce informazioni sull'integrazione a doppia scrittura di Project Operations per la fatturazione dei clienti.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996571"
---
# <a name="project-invoice-integration"></a>Integrazione di fatture di progetto

Questo argomento fornisce informazioni sull'integrazione a doppia scrittura di Project Operations per la fatturazione dei clienti.

In Project Operations, il responsabile di progetto gestisce il backlog di fatturazione del progetto e crea una fattura proforma per il cliente in Microsoft Dataverse. In base a questa fattura proforma, l'addetto alla contabilità clienti o il contabile del progetto crea una fattura per il cliente. L'integrazione della doppia scrittura garantisce che i dettagli della fattura proforma siano sincronizzati con le app Finance and Operations. Dopo che la fattura destinata al cliente è stata registrata, il sistema aggiorna i valori effettivi del progetto rilevanti in Dataverse con il dettaglio contabile. Il grafico seguente fornisce una panoramica concettuale di alto livello di questa integrazione.

   ![Integrazione di fatture di progetto](./media/DW5Invoicing.png)

Dopo che il responsabile di progetto conferma la fattura proforma in Dataverse, le informazioni sull'intestazione della fattura proforma vengono sincronizzate con le app Finance and Operations utilizzando la mappa della tabella a doppia scrittura **Proposta di fattura di progetto V2 (invoices)**. È un'integrazione unidirezionale da Dataverse alle app Finance and Operations. La creazione o l'eliminazione di proposte di fatturazione di progetto direttamente nelle app Finance and Operations non è supportata.

La conferma fattura in Dataverse attiva anche la logica aziendale per creare record relativi alla fatturazione nell'entità **Valori effettivi**. Questi record vengono sincronizzati con Finance and Operations utilizzando la mappa della tabella a doppia scrittura **Valori effettivi dell'integrazione di Project Operations (msdyn\_actuals).** Per ulteriori informazioni, vedi [Stime e valori effettivi di progetto](resource-dual-write-estimates-actuals.md). 

Le righe della proposta di fattura di progetto vengono create dal processo periodico **Importa modulo gestione temporanea**. Questo processo si basa sui dettagli delle vendite effettive fatturate nella tabella **Gestione temporanea valori effettivi**. Per ulteriori informazioni, vedi [Gestire le proposte di fatturazione di progetto](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
