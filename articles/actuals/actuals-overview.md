---
title: Valori effettivi
description: Questo argomento fornisce informazioni su come utilizzare i valori effettivi in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581289"
---
# <a name="actuals"></a>Valori effettivi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

I valori effettivi rappresentano l'avanzamento finanziario e programmato rivisto e approvato di un progetto. Vengono creati quando vengono approvate le voci di tempo, spese e utilizzo del materiale, le scritture contabili e le fatture.

> [!IMPORTANT]
> I valori effettivi non devono essere modificati o eliminati dal sistema. In caso contrario, l'integrità finanziaria e qualsiasi integrazione con altri sistemi finanziari e contabili potrebbero risentirne. Microsoft Dynamics 365 Project Operations ti consente di utilizzare lo storno e la sostituzione dei valori effettivi per modificare i valori effettivi in vari punti del ciclo di vita dei processi aziendali dei progetti.

## <a name="recording-actuals-based-on-project-events"></a>Registrare effettivi basati su eventi di progetto

Project Operations registra come effettive le transazioni finanziarie che si verificano durante il ciclo di vita dell'impegno di progetto. La creazione di valori effettivi in vari eventi nel ciclo di vita varia a seconda che l'impegno di progetto utilizzi il modello di fatturazione di tempi e materiali o il modello di fatturazione a prezzo fisso e se si trova nella fase di prevendita o se si tratta di un progetto interno.

I seguenti argomenti spiegano l'impatto sulla tabella Valori effettivi in vari eventi per diverse variazioni:

- [Impatto effettivo in un impegno di tempo e materiali](ActualsonTM.md)
- [Impatto dei valori effettivi in un impegno a prezzo fisso](ActualonFP.md)
- [Impatto dei valori effettivi durante la fase di prevendita di un impegno](ActualonPreSales.md)
- [Impatto dei valori effettivi per un progetto interno](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
