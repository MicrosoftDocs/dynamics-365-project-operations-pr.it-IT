---
title: Progetti e stime di vendita
description: In questo argomento vengono fornite informazioni su come utilizzare la pianificazione e le stime nel processo di vendita.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752624"
---
# <a name="sales-estimates-and-projects"></a>Progetti e stime di vendita

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Durante il processo di vendita, puoi creare stime di vendita collegando un progetto a un'offerta di vendita. In questo modo, la stima deterministica può avvenire durante il processo di vendita, in modo da utilizzare le funzionalità di stima e pianificazione del progetto. Se la vendita viene eseguita, la pianificazione utilizzata per scopi di stima delle vendite può essere utilizzata come base per un ulteriore perfezionamento del piano di progetto.

## <a name="linking-a-project-to-a-quote-line"></a>Collegamento di un progetto a una riga di offerta

Quando crei una riga di offerta basata su progetto, puoi creare un nuovo progetto o associare un progetto esistente nella pagina **Riga di offerta**. 

> ![Modulo Riga di offerta](media/project-8.png)
 
Quando crei un nuovo progetto a partire dai dettagli della riga di offerta, puoi utilizzare i modelli di progetto. I modelli di progetto sono progetti che rappresentano i piani di progetto standard e stime finanziarie tipici di un'organizzazione. Possono anche rappresentare copie di stime e piani di progetto di progetti passati.

> ![Dettagli riga di offerta](media/project-9.png)
  
Quando crei il progetto a partire dall'offerta, questo viene automaticamente associato alla riga di offerta.

## <a name="components-of-estimates-in-a-project"></a>Componenti di stime in un progetto

Una pianificazione ti consente di dividere il lavoro in attività, gestire una gerarchia di attività, determinare quali risorse sono necessarie per completare un'attività e assegnare una stima del lavoro necessario per completare un'attività.

Puoi definire il lavoro richiesto e pianificare le stime utilizzando i campi nella scheda **Pianifica** della pagina **Progetto**. Poiché un listino prezzi è associato al progetto, le stime finanziarie vengono calcolate utilizzando prezzi di costo e vendita definiti nel listino prezzi.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importazione di stime da un progetto in un'offerta

Dopo aver definito le stime di progetto, puoi importarle nella riga di offerta. Nella pagina **Dettagli riga di offerta**, seleziona **Importa da stime** nella barra multifunzione per riepilogare stime di progetto per tipo di transazione, ruolo o livello di attività.
