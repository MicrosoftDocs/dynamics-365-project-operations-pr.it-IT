---
title: Impostare i ruoli sui modelli di struttura di suddivisione del lavoro
description: Questo articolo fornisce informazioni sulla configurazione delle informazioni sui ruoli nei modelli di struttura di suddivisione del lavoro.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8721c5e5798c2b80c6f3eb65cef118d1ade5e680
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920801"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Impostare i ruoli sui modelli di struttura di suddivisione del lavoro

[!include [banner](../includes/banner.md)]

I project manager possono impostare modelli di struttura di suddivisione del lavoro che possono applicare quando creano una struttura di suddivisione del lavoro per nuovi progetti. I project manager possono aggiungere ruoli quando creano un modello. Utilizza la procedura seguente per assegnare un ruolo a un modello di struttura di suddivisione del lavoro.

1. Seleziona **Gestione progetti e contabilità** > **Imposta** > **Progetti** > **Modelli di struttura di suddivisione del lavoro**.
2. Seleziona **Dettagli** per un modello di struttura di suddivisione del lavoro selezionato.
3. Seleziona un'attività nell'elenco, quindi, nel campo **Ruolo** seleziona un ruolo da assegnare all'attività.

## <a name="work-with-a-wbs"></a>Utilizzare una struttura di suddivisione del lavoro

È possibile creare una nuova struttura di suddivisione del lavoro oppure copiare una struttura di suddivisione del lavoro da un modello di struttura di suddivisione del lavoro esistente. Un project manager può gestire facilmente le risorse assegnando ruoli a nuove attività sulla struttura di suddivisione del lavoro. I ruoli possono essere sostituiti dopo l'acquisizione di una risorsa o dopo l'identificazione di una risorsa confermata per lavorare sull'attività. Questa flessibilità consente ai project manager di eseguire le seguenti attività:

- Identificare il numero di risorse richieste per i pacchetti di lavoro della struttura di suddivisione del lavoro.
- Stimare i costi del progetto.
- Determinare un budget preliminare.
- Stimare la durata dell'attività, in base a ruoli e risorse.
- Sviluppare alcuni piani di gestione del progetto, sulla base delle informazioni di progetto disponibili.

Sono state aggiunte ulteriori opzioni nella struttura di suddivisione del lavoro per utilizzare meglio la funzionalità di risorse.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Assegnazioni risorse</td>
<td>Visualizza le risorse assegnate, le date, il numero di ore e il tipo di prenotazione per le attività sulla struttura di suddivisione del lavoro.</td>
</tr>
<tr class="even">
<td>Generare automaticamente il team</td>
<td>Aggiungi automaticamente le risorse pianificate utilizzando i ruoli associati a un'attività. Finance suggerisce automaticamente le risorse pianificate utilizzando l'analisi decisionale multicriterio basata sui ruoli. Dopo che i ruoli e lo sforzo (ore) sono stati impostati per le attività in una struttura di suddivisione del lavoro e dopo che la struttura è stata rilasciata, seleziona <strong>Genera automaticamente team</strong>. Il numero richiesto di risorse pianificate viene aggiunto alla struttura di suddivisione del lavoro e alla scheda <strong>Team progetto e programmazione</strong>.</td>
</tr>
<tr class="odd">
<td>Risorsa (elenco a discesa)</td>
<td>Nella pagina <strong>Avvia modulo di assegnazione risorse</strong>, puoi selezionare le risorse da prenotare definitivamente o temporaneamente in base alla durata specificata. Puoi modificare le impostazioni di visualizzazione per vedere e impostare la durata delle attività delle risorse. Puoi selezionare e assegnare risorse a livello di pacchetto di lavoro utilizzando le seguenti opzioni:
<ul>
<li><strong>Accetta</strong>: conferma le modifiche alla risorsa assegnata a un'attività.</li>
<li><strong>Annulla</strong>: annulla le modifiche alla risorsa assegnata a un'attività.</li>
<li><strong>Assegna automaticamente</strong>: una risorsa con personale disponibile che ha un ruolo corrispondente viene automaticamente selezionata e assegnata all'attività selezionata.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Nella pagina **Tutti i progetti**, seleziona il progetto **Fase di aggiornamento XYZ 2**.
2. Seleziona **Piano** > **Impegni** > **Struttura di suddivisione del lavoro**.
3. Seleziona **Nuovo** per aggiungere le seguenti attività di primo livello alla struttura di suddivisione del lavoro:

    - Avvio
    - Pianificazione
    - Esecuzione in corso
    - Monitoraggio e controllo
    - Chiuso

4. Imposta le date e lo sforzo (ore), come mostrato nell'illustrazione seguente.

    [![Impostazione delle date e dell'impegno.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Seleziona la riga attività **Avvio**, quindi, nel campo **Ruolo**, seleziona **Senior Project Manager**.
6. Seleziona **Pubblica**.
7. Sulla stessa riga, nel campo **Risorsa**, seleziona **Daniel Goldschmidt** e quindi seleziona **Accetta**.
8. Seleziona la riga attività **Pianificazione**, quindi, nel campo **Ruolo**, selezionare **Analista aziendale**.
9. Seleziona **Pubblica** e quindi seleziona **Generare automaticamente il team**.
10. Nella finestra del messaggio che verrà visualizzata, seleziona **Sì**.
11. Nel campo **Risorsa**, verifica che il valore sia **Analista aziendale 1**.
12. Per la risorsa **Analista aziendale 1**, apri la ricerca e seleziona **Avvia assegnazioni di risorse**. Quindi seleziona un lavoratore per l'attività.
13. Seleziona **Assegnazione temporanea** &gt; **Piena capacità**.

    > [!NOTE] 
    > Non ricevi un avviso che la risorsa specificata è ora 2, perché il numero di risorse rimane 1.

14. Nella pagina **Struttura di suddivisione del lavoro**, convalida l'assegnazione delle risorse sulla struttura di suddivisione del lavoro, quindi seleziona **Salva**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]