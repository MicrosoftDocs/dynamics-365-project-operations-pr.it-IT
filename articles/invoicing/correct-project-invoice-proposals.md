---
title: Correggere la contabilità sulle proposte di fattura di progetto in bozza
description: Questo argomento spiega come modificare le informazioni relative alla contabilità in una bozza di proposta di fattura.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999321"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Correggere la contabilità sulle proposte di fattura di progetto in bozza

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

I *dettagli operativi* per le fatture di progetto vengono mantenuti dal responsabile di progetto in una fattura pro forma. Questi dettagli includono la decisione su ore, spese, materiali o passaggi fondamentali che devono essere fatturati, le tariffe e l'applicazione degli importi di anticipo e acconto. Dopo aver confermato la fattura pro forma originale, puoi modificare i dettagli operativi creando e confermando una [fattura pro forma correttiva](../proforma-invoicing/corrective-invoices.md).

I *dettagli contabili* per le fatture di progetto vengono mantenuti in un documento di fattura rivolto al cliente. Questi dettagli includono il calcolo dell'IVA e le dimensioni finanziarie applicate alla fattura. Questo argomento fornisce le indicazioni su come questi dettagli contabili possono essere rettificati su una bozza di proposta di fattura del progetto.

## <a name="adjust-sales-tax"></a>Rettificare l'IVA

Le fasce IVA di fatturazione predefinite e le fasce IVA di articoli possono essere rettificate direttamente nel documento di proposta di fattura. Per regolare questi gruppi, seleziona **Modifica**, quindi, in ciascuna riga della proposta di fattura progetto, immetti un nuovo valore nel campo **Fascia IVA** o **Fascia IVA articolo**.

## <a name="adjust-financial-dimensions"></a>Rettificare le dimensioni finanziarie

Le dimensioni finanziarie non possono essere modificate direttamente in una riga della proposta di fattura progetto. Segui invece questi passaggi per rettificare le dimensioni finanziarie su una proposta di fattura progetto.

1. Nella proposta di fattura del progetto, seleziona **Elimina tutto** per rimuovere le righe della proposta di fattura progetto.

    > [!NOTE]
    > Il pulsante **Elimina tutto** è disponibile solo dopo che l'amministratore di sistema abilita la funzionalità **Eliminare righe della proposta di fattura quando si utilizza Project Operations per scenari basati su risorse/non stoccati** nell'area di lavoro **Gestione delle funzionalità**.

2. Rettifica le dimensioni finanziarie:

    - **Transazioni in acconto (passaggi fondamentali fatturazione):** Vai a **Tutti i progetti** \> **Gestisco** \> **Transazioni in acconto** e seleziona il passaggio fondamentale che richiede la rettifica. Poi, nella scheda **Dimensioni finanziarie** aggiorna i valori come richiesto.
    - **Transazioni di tempo, spese e materiali:** Nella pagina **Transazioni di progetto registrate** seleziona **Rettifica contabilità** per aggiornare le dimensioni finanziarie.

3. Dopo aver finito di rettificare i valori della dimensione finanziaria, vai in **Gestione del progetto e contabilità** \> **Periodico** \> **Integrazione di Project Operations** e seleziona **Importa da tabella di staging** per eseguire il processo periodico. Tale processo utilizza i valori della dimensione finanziaria aggiornati per ricreare le righe della proposta di fattura progetto. I valori aggiornati vengono quindi utilizzati nella contabilità ausiliaria del progetto e nella contabilità generale quando viene registrata la fattura del progetto.
