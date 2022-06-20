---
title: Elaborazione della ricevuta spesa
description: Questo articolo fornisce informazioni sull'elaborazione OCR (riconoscimento ottico dei caratteri) per le ricevute. Questa funzionalità è progettata per migliorare l'esperienza utente quando vengono create note spese in Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 5a72802e3c52b6a9e55ac779aa36c32072dc8b8b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911417"
---
# <a name="expense-receipt-processing"></a>Elaborazione della ricevuta spesa

L'immissione delle spese è stata migliorata grazie all'introduzione dell'elaborazione del riconoscimento ottico dei caratteri (OCR) per le ricevute. Questa funzionalità è progettata per migliorare l'esperienza dell'utente durante la creazione di ricevute spesa.

## <a name="key-features"></a>Funzionalità chiave

- Il nome, la data e l'importo totale del commerciante vengono estratti dalle ricevute.
- Il sistema tenta di abbinare le ricevute non allegate alle transazioni di spesa non associate.
- Gli utenti possono creare transazioni di spesa inserite manualmente dalle ricevute.

## <a name="usage-examples"></a>Esempio di utilizzo

Per allegare automaticamente le ricevute che includono transazioni con carta di credito quando viene creata una nota spese, esegui i seguenti passaggi:

  1. Apri l'area di lavoro **Gestione delle spese**.
  2. Nella scheda **Ricevute** verifica che esistano ricevute non allegate. Puoi anche caricare le ricevute nella scheda **Ricevute**.
  3. Nella scheda **Spese** verifica che esistano spese non allegate. In genere, l'amministratore importa queste spese dal fornitore della carta di credito.
  4. Seleziona **Nuova nota spese**. Nota che ora puoi includere anche spese e ricevute quando crei una nota spese. Se aggiungi sia le spese che le ricevute, viene attivato l'abbinamento automatico delle ricevute rispetto alle spese.

Per creare una spesa o abbinare una spesa da una ricevuta, esegui i seguenti passaggi:

  1. In una nota spese, nella scheda **Ricevute**, allega una ricevuta selezionando **Aggiungi ricevute**.
  2. Sotto l'immagine caricata della ricevuta, nota le opzioni **Crea** e **Abbina**.

      - Seleziona **Crea** per creare una transazione di spesa inserita manualmente e compilare i valori estratti dalla ricevuta.
      - Se selezioni **Abbina**, il sistema cerca di abbinare una spesa esistente alla ricevuta.

## <a name="installation"></a>Installazione

Questa funzione utilizza in combinazione la funzione **Note spese riprogettate** per semplificare l'esperienza di spesa. Questa funzione è disponibile solo per gli ambienti superiori al livello 2 che sono sandbox e di produzione.

Per utilizzare queste funzionalità di spesa avanzate, installa il componente aggiuntivo Servizio gestione spese per Microsoft Dynamics 365 Finance e attiva le funzionalità nella tua istanza. Puoi accedere al componente aggiuntivo dal tuo progetto in Microsoft Dynamics Lifecycle Services (LCS).

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

Per ulteriori informazioni sulla funzione Note spese riprogettate, vedi [Note spese riprogettate](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Domande frequenti

**Microsoft utilizza i miei dati per i suoi modelli?**

No, Microsoft ha creato un modello generale di apprendimento automatico per il suo servizio di elaborazione delle ricevute. Questo modello non si basa sulle ricevute che carichi.

**Dove è disponibile e viene elaborata questa funzione?**

Attualmente sono supportati gli Stati Uniti.

**Dove vanno le mie ricevute?**

Finance contatta Cognitive Services per estrarre i dati sul campo. Cognitive Services conserveranno una copia della ricevuta per un massimo di 24 ore durante l'elaborazione. Una volta completata l'elaborazione, Cognitive Services rimuoveranno la ricevuta. Le ricevute sono ancora archiviate in Finance.

Per ulteriori informazioni, vedi [Abilitare la comprensione delle ricevute con la nuova funzionalità di riconoscimento modulo](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]