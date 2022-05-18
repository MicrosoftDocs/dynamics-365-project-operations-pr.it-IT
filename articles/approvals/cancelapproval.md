---
title: Annullare l'approvazione di voci approvate precedentemente
description: Questo argomento spiega come un project manager può annullare l'approvazione di voci di tempo, spese o utilizzo del materiale precedentemente approvate.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584785"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Annullare l'approvazione di voci approvate precedentemente

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Un project manager o un responsabile approvazione che ha precedentemente approvato voci relative a tempi, spese o utilizzo del materiale può annullare l'approvazione di tali voci. 

Segui questi passaggi per annullare l'approvazione di una voce di tempo, spesa o utilizzo del materiale precedentemente approvata.

1. Seleziona **Progetti** \> **Attività personali** \> **Approvazioni**.
2. La pagina elenco **Approvazioni** mostra tutti gli inserimenti ore in attesa di approvazione. Cambia la vista in **Approvazioni personali passate**.
3. Seleziona le approvazioni di tempo, spesa o materiale da annullare. Quindi, nel riquadro Azioni seleziona **Annulla approvazione**.
4. Nella finestra del messaggio di conferma che appare, seleziona **OK** per confermare l'operazione.

> [!IMPORTANT]
> Non è possibile annullare l'approvazione di una voce di tempo, spesa e utilizzo del materiale precedentemente approvata che è già stata fatturata al cliente. Se ci provi, riceverai un messaggio in cui si afferma che non è possibile annullare l'approvazione perché è stata già fatturata. In questo caso, puoi annullare l'approvazione solo se viene utilizzata una fattura correttiva per emettere un credito completo o un rimborso al cliente sulla fattura originale.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Impatto dell'annullamento dell'approvazione di una voce approvata precedentemente

Quando si annulla un'approvazione, si ha un impatto operativo e un impatto finanziario.

### <a name="operational-impact"></a>Impatto operativo

Se l'approvazione di una voce viene annullata, il record di approvazione viene contrassegnato come **Inviato**. Lo stato della voce viene cambiato in **Inviato**. In questa fase, un membro del team di progetto può richiamare la voce senza inviare una richiesta di richiamo.

Il responsabile dell'approvazione può modificare i valori **Quantità fatturabile** e **Tipo di fatturazione**, quindi approvare la voce ancora una volta.

### <a name="financial-impact"></a>Impatto finanziario

Se l'approvazione di una voce viene annullata, i valori effettivi corrispondenti per costo e vendite vengono aggiornati nel modo seguente:

- Il campo **Stato rettifica** diventa **Rettificato**.
- Il campo **Stato fatturazione** diventa **Annullato**.

Quindi, nella tabella Valori effettivi vengono create scritture di storno. Per creare scritture di storno, il sistema copia i valori di campo dai valori effettivi originali. I soli valori che non vengono copiati sono i valori di quantità. Questi valori vengono invece stornati. Valori effettivi stornati vengono creati per i valori effettivi **Costo** e **Vendite non fatturate**. Il campo **Stato rettifica** dei valori effettivi stornati viene impostato su **Non rettificabile** e il campo **Stato di fatturazione** viene impostato su **Annullato**. A seguito di tali modifiche, la spesa registrata e il backlog dei ricavi del progetto non includono più gli importi che questi valori effettivi rappresentano.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
