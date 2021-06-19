---
title: Acquisire una ricevuta utilizzando OCR
description: Questo argomento fornisce informazioni sull'elaborazione del riconoscimento ottico dei caratteri (OCR) per le ricevute.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c7fa8a805acbf7c75edd49c4c49aa159493f525
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002016"
---
# <a name="capture-a-receipt-using-ocr"></a>Acquisire una ricevuta utilizzando OCR

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

L'immissione delle spese è stata migliorata grazie all'introduzione dell'elaborazione del riconoscimento ottico dei caratteri (OCR) per le ricevute. Questa funzionalità è progettata per migliorare l'esperienza dell'utente durante la creazione di note spese.

## <a name="key-features"></a>Funzionalità chiave

- Il sistema estrae il nome, la data e l'importo totale del commerciante dalle ricevute.
- Il sistema tenterà di abbinare le ricevute non allegate alle transazioni di spesa non associate.
- Puoi creare transazioni di spesa inserite manualmente dalle ricevute.

## <a name="attach-receipts-to-an-expense-report"></a>Allegare le ricevute a una nota spese

Per allegare automaticamente le ricevute che includono transazioni con carta di credito quando viene creata una nota spese, completa i seguenti passaggi.

  1. Apri l'area di lavoro **Gestione delle spese**.
  2. Nella scheda **Ricevute** verifica che esistano ricevute non allegate. Puoi anche caricare le ricevute nella scheda **Ricevute**.
  3. Nella scheda **Spese** verifica che esistano spese non allegate. In genere, l'amministratore importa queste spese dal fornitore della carta di credito.
  4. Seleziona **Nuova nota spese**. Nota che ora puoi includere anche spese e ricevute quando crei una nota spese. Se aggiungi sia le spese che le ricevute, viene attivato l'abbinamento automatico delle ricevute rispetto alle spese.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Creare o abbinare le ricevute a una nota spese
Per creare una spesa o abbinare una spesa da una ricevuta, completa i seguenti passaggi.

  1. In una nota spese, nella scheda **Ricevute**, allega una ricevuta selezionando **Aggiungi ricevute**.
  2. Sotto l'immagine caricata della ricevuta, nota le opzioni **Crea** e **Abbina**.

      - Seleziona **Crea** per creare una transazione di spesa inserita manualmente e compilare i valori estratti dalla ricevuta.
      - Se selezioni **Abbina**, il sistema cerca di abbinare una spesa esistente alla ricevuta.

## <a name="installation"></a>Installazione

Per utilizzare queste funzionalità avanzate di spesa, installa il componente aggiuntivo Servizio gestione delle spese per Microsoft Dynamics 365 Finance e attiva le funzionalità nella tua istanza. Puoi accedere al componente aggiuntivo dal tuo progetto in Microsoft Dynamics Lifecycle Services (LCS).

1. Accedi a LCS e apri l'ambiente desiderato.
2. Vai a **Dettagli completi**.
3. Seleziona **Gestisci** o scorri verso il basso fino alla scheda dettaglio **Componenti aggiuntivi per l'ambiente**.
4. Seleziona **Installa un nuovo componente aggiuntivo**.
5. Seleziona **Servizio gestione delle spese**.
6. Segui la guida all'installazione e accetta le condizioni.
7. Seleziona **Installa**.

Nell'area di lavoro **Gestione delle funzionalità**, attiva le seguenti funzionalità:

- Note spese riprogettate
- Abbina automaticamente e crea spesa dalla ricevuta

Quando attivi queste funzionalità, si verificano le seguenti azioni:

- L'area di lavoro esistente **Gestione delle spese** viene sostituita con la nuova area di lavoro.
- Viene aggiunta una nuova voce di menu per la visibilità del campo di spesa.
- Puoi ancora aprire la pagina **Note spese** precedente andando a **Gestione delle spese > Le mie spese > Note spese**.
- I flussi di lavoro e le eventuali approvazioni ti portano comunque alla pagina delle note spese esistenti.
- Le ricevute verranno elaborate tramite Microsoft Azure Cognitive Services e i metadati verranno estratti e aggiunti.
- Viene aggiunta un'opzione che consente di creare una nota spese che include ricevute non allegate abbinate.
- Un'opzione aggiunta alle note spese consente di creare una riga di spesa da una ricevuta o di tentare di abbinare una ricevuta esistente a una riga di spesa esistente.

## <a name="frequently-asked-questions"></a>Domande frequenti

**Microsoft utilizza i miei dati per i suoi modelli?**

No, Microsoft ha creato un modello generale di apprendimento automatico per il suo servizio di elaborazione delle ricevute. Questo modello non si basa sulle ricevute che carichi.

**Dove è disponibile e viene elaborata questa funzione?**

Attualmente sono supportati gli Stati Uniti.

**Dove vanno le mie ricevute?**

Finance contatta Cognitive Services per estrarre i dati sul campo. Cognitive Services conserveranno una copia della ricevuta per un massimo di 24 ore durante l'elaborazione. Una volta completata l'elaborazione, Cognitive Services rimuoveranno la ricevuta. Le ricevute sono ancora archiviate in Finance.

Per ulteriori informazioni, vedi [Abilitare la comprensione delle ricevute con la nuova funzionalità di riconoscimento modulo](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
