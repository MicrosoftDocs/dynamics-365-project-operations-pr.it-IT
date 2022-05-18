---
title: Modelli di progetto
description: In questo argomento vengono fornite informazioni su come utilizzare modelli di progetto per una rapida configurazione dei progetti.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: aff6fc5bb855fe1e9007933fdc1a88eb020da0ad
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586027"
---
# <a name="project-templates"></a>Modelli di progetto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Un modello di progetto è un framework predefinito che consente di iniziare facilmente e velocemente un progetto. Puoi utilizzare un modello predefinito per creare un nuovo progetto con un singolo clic. Quanto ai progetti, devi definire i prerequisiti per i modelli di progetto. Devi definire un calendario di progetto per ogni modello di progetto e ruoli e listini prezzi devono essere predefiniti nell'organizzazione, di modo che i componenti del modello abbiano dati utili.

Un modello di progetto include tre componenti: una pianificazione, stime di progetto e membri del team di progetto.

## <a name="schedule"></a>Pianifica

Una pianificazione in un modello di progetto include lo stesso set di elementi di una pianificazione in un progetto. Puoi creare una gerarchia di attività, associare ruoli ad attività, definire attributi di pianificazione e impostare dipendenze. Una pianificazione in un modello di progetto supporta inoltre modalità di attività per ogni attività. Pertanto, supporta il motore di pianificazione. Devi associare un calendario di progetto al progetto. Quando crei una pianificazione del lavoro, non c'è differenza tra un modello di progetto e un progetto.

## <a name="project-estimates"></a>Stime di progetto

Il funzionamento delle stime di progetto in un modello di progetto è uguale a quello delle stime di progetto in un progetto. Tuttavia, i prezzi di costo e vendita sono estratti dai listini prezzi di costo e vendita predefiniti definiti nei parametri.

## <a name="creating-a-project-from-a-template"></a>Creare un progetto da un modello
 
Esistono vari modi di creare un progetto da un modello di progetto:

- Quando crei un progetto da un'offerta, puoi selezionare un modello di progetto nella finestra di dialogo **Creazione rapida: Progetto**.

> ![Finestra di dialogo Creazione rapida: Progetto.](media/project-11.png)

- Quando crei un progetto selezionando **Nuovo progetto**, viene visualizzata la pagina **Progetto** prima del salvataggio del record. Nel campo **Seleziona un modello**, seleziona uno dei modelli di progetto predefiniti nell'organizzazione.
- Utilizza **Crea progetto da un modello** nella pagina **Entità modello**.

## <a name="copying-components-of-template-to-project"></a>Copiare componenti di un modello in un progetto

Quando copi i componenti di un modello di progetto in un progetto, possono verificarsi alcune sostituzioni, a seconda delle impostazioni nel progetto.

### <a name="copying-the-schedule"></a>Copiare la pianificazione

Quando copi la pianificazione da un modello di progetto, se il progetto ha un calendario di progetto differente rispetto al modello, le ore lavorative nel calendario del progetto vengono applicate alla pianificazione delle attività. In questo modo la pianificazione viene modificata affinché corrisponda al calendario di progetto di backup. Analogamente, la prima attività nella pianificazione acquisisce la data iniziale del progetto e la pianificazione del resto della gerarchia viene aggiornata in base alla durata e alle dipendenze specificate nel modello. 

### <a name="copying-project-estimates"></a>Copiare stime di progetto 

Quando copi nelle righe di stima del progetto, i listini prezzi vengono aggiornati. Per il listino prezzi di costo, questi aggiornamenti sono basati sull'unità proprietaria del progetto. Per il listino prezzi di vendita, sono basati sul cliente. Per i progetti associati a un'entità Vendite, il costo unitario e i prezzi di vendita vengono determinati in base a questi listini prezzi.

### <a name="copying-a-project-team"></a>Copiare un team di progetto

Quando un team di progetto viene copiato da un modello di progetto in un progetto, le risorse generiche vengono copiate insieme alle competenze e alle qualifiche definite nel modello. Anche le assegnazioni di risorse generiche vengono gestite come se fossero nel modello di progetto. Le risorse denominate non sono supportate nei modelli di progetto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
