---
title: Creare un team di progetto
description: In questo argomento vengono fornite informazioni su come creare e gestire i team di progetto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079041"
---
# <a name="create-a-project-team"></a>Creare un team di progetto

[!include [banner](../includes/banner.md)]

Per utilizzare i ruoli precedentemente configurati in un progetto, un project manager deve associare i ruoli al progetto. È possibile assegnare più ruoli per un progetto. Per evitare confusione, questi ruoli vengono etichettati automaticamente durante la prenotazione. Ad esempio, se il project manager richiede tre ingegneri software, tre ruoli di ingegnere software che hanno **ingegnere software 1** , **ingegnere software 2** e **ingegnere software 3** come loro etichette vengono generati automaticamente. Se le caratteristiche del ruolo erano state precedentemente impostate per il ruolo, vengono applicate come filtro durante le ricerche di una risorsa. Ulteriori caratteristiche possono essere aggiunte secondo necessità per affinare ulteriormente la ricerca.

Le impostazioni di visualizzazione possono anche essere personalizzate per fornire una migliore visualizzazione della disponibilità delle risorse. Sono disponibili opzioni per mostrare la disponibilità oraria, giornaliera, settimanale, mensile, trimestrale e annuale. Esiste anche un'opzione per mostrare la capacità disponibile e rimanente sulle risorse. Questa opzione è utile per la gestione del tempo, quando si stima il tempo disponibile per le attività o la disponibilità delle risorse.

Il project manager può selezionare un ruolo nella pagina e quindi, se è disponibile una risorsa che soddisfa il requisito, selezionare per prenotare una risorsa per ricoprire il ruolo. Tieni presente che le risorse non devono essere prenotate a questo punto della fase di pianificazione. Quando crei una struttura di suddivisione del lavoro, puoi sostituire i ruoli con risorse di personale per il progetto. Se i ruoli vengono sostituiti con risorse con personale nella struttura di suddivisione del lavoro, la configurazione delle risorse aggiorna automaticamente l'elenco e la pianificazione del team di progetto.

[![Elenco del team di progetto che include sia i ruoli che le risorse effettive](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Il project manager ha varie opzioni per prenotare una risorsa per un progetto, ad esempio **Capacità rimanente** , **Piena capacità** , **Percentuale di capacità** e **Specifica orari**. Queste opzioni di prenotazione possono essere annullate in qualsiasi momento se le assegnazioni delle risorse cambiano. Sono supportati due tipi di prenotazione:

- **Prenotazione definitiva** : la prenotazione della risorsa è stata approvata e confermata per lavorare sull'impegno per la durata specificata.
- **Prenotazione temporanea** : le prenotazioni della risorsa sono state temporaneamente impostate per lavorare sull'impegno per la durata specificata.

La procedura seguente illustra come creare un team di progetto.

## <a name="create-a-project-team"></a>Creare un team di progetto

1. Nella pagina elenco **Tutti i progetti** , seleziona un progetto, quindi seleziona **Modifica**.
2. Nella scheda **Team progetto e programmazione** , nel campo **Data di fine della pianificazione** immetti la data di inizio della pianificazione più un mese. Ad esempio, se la data di inizio della pianificazione è il 24 giugno 2017 (24/06/2017), immetti **24/07/2017**.
3. Seleziona **Aggiungi**.
4. Nel riquadro  **Aggiungi ruoli al progetto** , nel campo **Ruolo** , seleziona **Senior Project Manager**.
5. Seleziona **Competenze richieste**.
6. Nella pagina **Scegli caratteristiche** , le caratteristiche precedentemente impostate per il ruolo di Senior project manager sono selezionate per impostazione predefinita. Seleziona **OK**.
7. Nella pagina **Aggiungi ruoli al progetto** , nel campo **Numero di risorse** , inserisci **1**.
8. Nel campo **Risorsa** , la ricerca mostra tutte le risorse che hanno le competenze richieste. Seleziona **Daniel Goldschmidt** , quindi seleziona **Crea**.
9. Nella pagina **Progetto** seleziona **Aggiungi**.
10. Nel riquadro  **Aggiungi ruoli al progetto** , nel campo **Ruolo** , seleziona **Membro del team**. Nel campo **Numero di risorse** , immetti **5**.
11. Seleziona **Crea**.
12. Nella pagina **Progetti** , seleziona **Soddisfa capacità risorsa**.

## <a name="monitor-project-teams"></a>Monitorare i team di progetto
1. Nella pagina **Tutti i progetti** , seleziona il collegamento **ID progetto** per il progetto **Aggiornamento XYZ Fase 2**.
2. Nella Scheda dettaglio **Team progetto e programmazione** , verifica che le risorse del progetto elencate siano corrette.
