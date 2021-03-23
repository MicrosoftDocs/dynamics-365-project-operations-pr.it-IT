---
title: Progetti di stima dei ricavi a prezzo fisso
description: In questo argomento vengono fornite informazioni sui ricavi a prezzo fisso nei progetti.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278918"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Progetti di stima dei ricavi a prezzo fisso 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Quando crei una riga di contratto di progetto con i seguenti attributi in Dynamics 365 Project Operations in Microsoft Dataverse, il sistema crea automaticamente un progetto di stima dei ricavi a prezzo fisso. Le informazioni in questo progetto si basano su quanto segue:

  - Un metodo di fatturazione a prezzo fisso.
  - Un progetto associato.
  - Almeno una passaggio fondamentale definito nella scheda **Pianificazione fatture** nella pagina **Riga contratto di progetto**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Revisione dei progetti delle stime dei ricavi a prezzo fisso
Per rivedere i progetti delle stime dei ricavi a prezzo fisso, completare i seguenti passaggi:

1. Nell'ambiente Dynamics 365 Finance, vai a **Contabilità e gestione progetti** > **Progetti** > **Progetti di stima dei ricavi a prezzo fisso**.
2. Seleziona il progetto che desideri visualizzare e fai doppio clic su **Stima ID del progetto** per aprire il record e rivedere i dettagli del progetto.
3. Espandi la schedaa **Progetto**. Vedrai un progetto nella griglia **Progetti selezionati**. Il sistema utilizza questo progetto come predefinito perché è il progetto associato alla riga di contratto di progetto. 
4. Per modificare l'associazione, seleziona altri progetti e aggiungili alla griglia **Progetti selezionati**. Se in questa griglia vengono selezionati più progetti, la percentuale di completamento del progetto e le stime dei ricavi vengono calcolate insieme per tutti i progetti selezionati.

  Il costo del progetto, il profilo dei ricavi, il modello di costo e il codice del periodo possono essere impostati manualmente. Se non vengono impostati manualmente, i valori vengono impostati come predefiniti durante il primo calcolo della stima per il progetto utilizzando le regole configurate per i profili di costi e ricavi del progetto.



[!INCLUDE[footer-include](../includes/footer-banner.md)]