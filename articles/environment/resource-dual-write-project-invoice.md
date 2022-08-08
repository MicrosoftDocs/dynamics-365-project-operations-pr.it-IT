---
title: Integrazione di fatture di progetto
description: Questo articolo fornisce informazioni sull'integrazione della doppia scrittura di Project Operations per la fatturazione del cliente.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029029"
---
# <a name="project-invoice-integration"></a>Integrazione di fatture di progetto

Questo articolo fornisce informazioni sull'integrazione della doppia scrittura di Project Operations per la fatturazione del cliente.

In Project Operations, il responsabile di progetto gestisce il backlog di fatturazione del progetto e crea una fattura proforma per il cliente in Microsoft Dataverse. In base a questa fattura proforma, l'addetto alla contabilità clienti o il contabile del progetto crea una fattura per il cliente. L'integrazione a doppia scrittura assicura che i dettagli della fattura proforma siano sincronizzati con le app per la finanza e le operazioni. Dopo che la fattura destinata al cliente è stata registrata, il sistema aggiorna i valori effettivi del progetto rilevanti in Dataverse con il dettaglio contabile. Il grafico seguente fornisce una panoramica concettuale di alto livello di questa integrazione.

   ![Integrazione di fatture di progetto.](./media/DW5Invoicing.png)

Dopo che il project manager ha confermato la fattura proforma in Dataverse, le informazioni sull'intestazione della fattura proforma si sincronizzano con le app per la finanza e le operazioni utilizzando la mappa tabella a doppia scrittura, **Proposta di fattura di progetto V2 (fatture)**. Questa è un'integrazione unidirezionale da Dataverse alle app per la finanza e le operazioni. La creazione o l'eliminazione di proposte di fattura di progetto direttamente nelle app per la finanza e le operazioni non è supportata.

La conferma fattura in Dataverse attiva anche la logica aziendale per creare record relativi alla fatturazione nell'entità **Valori effettivi**. Questi record vengono sincronizzati con le app per la finanza e le operazioni utilizzando la mappa tabella a doppia scrittura **Valori effettivi per l'integrazione di Project Operations (msdyn\_actuals)**. Per ulteriori informazioni, vedi [Stime e valori effettivi di progetto](resource-dual-write-estimates-actuals.md). 

Le righe della proposta di fattura di progetto vengono create dal processo periodico **Importa modulo gestione temporanea**. Questo processo si basa sui dettagli delle vendite effettive fatturate nella tabella **Gestione temporanea valori effettivi**. Per ulteriori informazioni, vedi [Gestire le proposte di fatturazione di progetto](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
