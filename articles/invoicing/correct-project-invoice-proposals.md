---
title: Correggere la contabilità sulle proposte di fattura di progetto in bozza
description: Questo articolo spiega come modificare le informazioni relative alla contabilità su una bozza di proposta di fattura.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921215"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Correggere la contabilità sulle proposte di fattura di progetto in bozza

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

I *dettagli operativi* per le fatture di progetto vengono mantenuti dal responsabile di progetto in una fattura pro forma. Questi dettagli includono la decisione su ore, spese, materiali o passaggi fondamentali che devono essere fatturati, le tariffe e l'applicazione degli importi di anticipo e acconto. Dopo aver confermato la fattura pro forma originale, puoi modificare i dettagli operativi creando e confermando una [fattura pro forma correttiva](../proforma-invoicing/corrective-invoices.md).

I *dettagli contabili* per le fatture di progetto vengono mantenuti in un documento di fattura rivolto al cliente. Questi dettagli includono il calcolo dell'IVA e le dimensioni finanziarie applicate alla fattura. Questo articolo fornisce informazioni su come questi dettagli contabili possono essere modificati in una bozza di proposta di fattura di progetto.

## <a name="adjust-sales-tax"></a>Rettificare l'IVA

Le fasce IVA di fatturazione predefinite e le fasce IVA di articoli possono essere rettificate direttamente nel documento di proposta di fattura. Per regolare questi gruppi, seleziona **Modifica**, quindi, in ciascuna riga della proposta di fattura progetto, immetti un nuovo valore nel campo **Fascia IVA** o **Fascia IVA articolo**.

## <a name="adjust-financial-dimensions"></a>Rettificare le dimensioni finanziarie

### <a name="header-dimensions"></a>Dimensioni dell'intestazione

Per impostazione predefinita, le dimensioni finanziarie della fattura vengono derivate dai record delle transazioni di progetto non fatturati che vengono fatturati. Tuttavia, le impostazioni di sistema consentono di utilizzare le dimensioni finanziarie nell'intestazione delle proposte di fattura del progetto per registrare i saldi dei clienti. Per abilitare questa funzionalità, seleziona **Consenti aggiornamenti alle dimensioni di progetto per contabilità clienti** nella scheda **Dati finanziari** della pagina **Parametri Gestione progetti e contabilità**.

Le dimensioni finanziarie sulle intestazioni delle fatture possono essere modificate prima della registrazione di una fattura. Sulla pagina **Proposta di fattura di progetto** passa alla vista **Intestazione** e quindi modifica i valori nella scheda **Dimensioni finanziarie**.

La vista **Intestazione** è disponibile solo dopo che l'amministratore di sistema ha abilitato la funzionalità **Utilizza proposta di fattura di progetto e moduli di giornali di registrazione fatture con la vista Intestazione e Righe** nell'area di lavoro **Gestione funzionalità**. Questa funzionalità richiede l'aggiornamento a Finance 10.0.25 o versione successiva.

### <a name="line-dimensions"></a>Dimensioni di riga

Le dimensioni finanziarie non possono essere modificate direttamente in una riga della proposta di fattura progetto. Segui invece questi passaggi per rettificare le dimensioni finanziarie su una proposta di fattura progetto.

1. Nella proposta di fattura del progetto, seleziona **Elimina tutto** per rimuovere le righe della proposta di fattura progetto.

    Il pulsante **Elimina tutto** è disponibile solo dopo che l'amministratore di sistema abilita la funzionalità **Eliminare righe della proposta di fattura quando si utilizza Project Operations per scenari basati su risorse/non stoccati** nell'area di lavoro **Gestione delle funzionalità**.

2. Rettifica le dimensioni finanziarie:

    - **Transazioni in acconto (passaggi fondamentali fatturazione):** Vai a **Tutti i progetti** \> **Gestisco** \> **Transazioni in acconto** e seleziona il passaggio fondamentale che richiede la rettifica. Poi, nella scheda **Dimensioni finanziarie** aggiorna i valori come richiesto.
    - **Transazioni di tempo, spese e materiali:** Nella pagina **Transazioni di progetto registrate** seleziona **Rettifica contabilità** per aggiornare le dimensioni finanziarie.

3. Dopo aver finito di rettificare i valori della dimensione finanziaria, vai in **Gestione del progetto e contabilità** \> **Periodico** \> **Integrazione di Project Operations** e seleziona **Importa da tabella di staging** per eseguire il processo periodico. Tale processo utilizza i valori della dimensione finanziaria aggiornati per ricreare le righe della proposta di fattura progetto. I valori aggiornati vengono quindi utilizzati nella contabilità ausiliaria del progetto e nella contabilità generale quando viene registrata la fattura del progetto.
