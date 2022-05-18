---
title: Considerazioni sull'aggiornamento per le approvazioni moderne
description: Il argomento copre i punti che gli amministratori dovrebbero considerare quando abilitano la funzionalità Approvazioni moderne.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578391"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Considerazioni sull'aggiornamento per le approvazioni moderne 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Come parte del primo ciclo di rilascio di aprile 2022, la funzionalità Approvazioni moderne sarà abilitata per impostazione predefinita. Questa funzionalità migliora l'affidabilità della logica di approvazione e garantisce la possibilità di determinare il motivo in caso di errore della logica di approvazione.

Come parte di questa modifica, le modifiche allo stato per le approvazioni dei progetti sono state aggiornate. Lo stato ora passa direttamente da **Inviato** ad **Approvato**. **In sospeso** non è più uno stato per le approvazioni. Per determinare se un'approvazione è in sospeso, verifica che l'approvazione faccia parte di una serie di approvazioni e verifica lo stato della serie di approvazioni allegata.

## <a name="before-you-upgrade"></a>Prima di aggiornare

Prima di eseguire l'aggiornamento ad Approvazioni moderne, assicurati di non avere approvazioni in sospeso. Modern Approvas non utilizza lo stato **In sospeso**. Pertanto, tutte le approvazioni che sono ancora contrassegnate come **In sospeso** dopo l'aggiornamento non verranno elaborate.

## <a name="after-you-upgrade"></a>Dopo l'aggiornamento

Dopo aver eseguito l'aggiornamento ad Approvazioni moderne, un amministratore deve convalidare che il flusso cloud che elabora le approvazioni sia abilitato.

1. Accedi a [flow.microsoft.com](https://flow.microsoft.com)
2. In alto a destra della pagina, cambia il tuo ambiente con l'ambiente che hai aggiornato.
3. Seleziona **Soluzioni** per elencare le soluzioni installate nell'ambiente.
4. Nell'elenco delle soluzioni, seleziona **Project Operations** o **Project Service**.
5. Passare dal filtro **Tutto** al filtro **Flussi cloud**.
6. Verifica che l'opzione **Project Service - Pianifica in modo ricorrente i set di approvazioni progetto** sia impostata su **Attivato**. In caso contrario, seleziona il flusso, quindi seleziona **Attiva**.
7. Verifica che l'elaborazione avvenga ogni cinque minuti esaminando l'elenco **Processi di sistema** nell'area **Impostazioni**.

## <a name="short-term-rollback"></a>Rollback a breve termine

Se non riesci ad accettare le modifiche o se riscontri un problema grave con questa funzione, puoi ripristinare temporaneamente il flusso di approvazione originale eseguendo i seguenti passaggi:
1. Accedi al tuo ambiente e verifica che non ci siano approvazioni in sospeso.
2. Passa a **Impostazioni** > **Parametri di progetto**.
3. Seleziona **Controllo funzionalità** e quindi seleziona **Approvazioni moderne** per disattivare la funzione.

## <a name="removing-the-feature-flag"></a>Rimozione del flag di funzionalità

Nell'aggiornamento del secondo ciclo di ottobre 2022, la possibilità di disattivare questa funzione verrà rimossa.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
