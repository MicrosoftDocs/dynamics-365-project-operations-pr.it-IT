---
title: Progetti di stima dei ricavi a prezzo fisso
description: Questo articolo fornisce informazioni sui ricavi a prezzo fisso nei progetti.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928391"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Progetti di stima dei ricavi a prezzo fisso 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Quando crei una riga di contratto di progetto con i seguenti attributi in Dynamics 365 Project Operations in Microsoft Dataverse, il sistema crea automaticamente un progetto di stima dei ricavi a prezzo fisso. Le informazioni in questo progetto si basano su quanto segue:

  - Un metodo di fatturazione a prezzo fisso.
  - Un progetto associato.
  - Almeno una passaggio fondamentale definito nella scheda **Pianificazione fatture** nella pagina **Riga contratto di progetto**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Revisione dei progetti delle stime dei ricavi a prezzo fisso
Per rivedere i progetti delle stime dei ricavi a prezzo fisso, completare i seguenti passaggi:

1. Nell'ambiente Dynamics 365 Finance, vai a **Gestione progetti e contabilità** > **Progetti** > **Progetti di stima dei ricavi a prezzo fisso**.
2. Seleziona il progetto che desideri visualizzare e fai doppio clic su **Stima ID del progetto** per aprire il record e rivedere i dettagli del progetto.
3. Espandi la schedaa **Progetto**. Vedrai un progetto nella griglia **Progetti selezionati**. Il sistema utilizza questo progetto come predefinito perché è il progetto associato alla riga di contratto di progetto. 
4. Per modificare l'associazione, seleziona altri progetti e aggiungili alla griglia **Progetti selezionati**. Se in questa griglia vengono selezionati più progetti, la percentuale di completamento del progetto e le stime dei ricavi vengono calcolate insieme per tutti i progetti selezionati.

  Il costo del progetto, il profilo dei ricavi, il modello di costo e il codice del periodo possono essere impostati manualmente. Se non vengono impostati manualmente, i valori vengono impostati come predefiniti durante il primo calcolo della stima per il progetto utilizzando le regole configurate per i profili di costi e ricavi del progetto.



[!INCLUDE[footer-include](../includes/footer-banner.md)]