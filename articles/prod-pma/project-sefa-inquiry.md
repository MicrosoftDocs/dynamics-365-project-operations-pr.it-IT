---
title: Richiesta Schedule of Expenditures of Federal Awards
description: Questo argomento fornisce informazioni sulla richiesta Schedule of Expenditures of Federal Awards.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: d0cc3db3fd05fa809f707b15a50380753ac8f9f779f45c13f707321d2b0e0841
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007241"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Richiesta Schedule of Expenditures of Federal Awards

[!include [banner](../includes/banner.md)]

Ai sensi dell'Office of Management and Budget Circular A-133, le agenzie che ricevono fondi federali sono soggette sono soggetti a requisiti di controllo, noti anche come controlli singoli. Il processo di controllo viene utilizzato per segnalare le entrate e le spese relative a sovvenzioni federali su base ricorrente. Parte del report del controllo singolo include la richiesta Schedule of Expenditures of Federal Awards (SEFA).

La richiesta Schedule of Expenditures of Federal Awards include il titolo e il numero del Catalog of Federal Domestic Assistance (CFDA), il numero della sovvenzione, l'anno della sovvenzione, il nome dell'agenzia federale che fornisce i fondi e il nome dell'entità pass-through. La richiesta è per un periodo specifico. In genere, il periodo corrisponde al periodo del rendiconto finanziario, ovvero un anno fiscale.

La richiesta include le sovvenzioni con le date di proiezione comprese nell'intervallo di date selezionato. La colonna **Agenzia concedente** della richiesta mostra il cliente della sovvenzione o, per una sovvenzione pass-through, l'agenzia concedente. Per una sovvenzione pass-through, la colonna **Agenzia pass-through** mostra il cliente della sovvenzione. Se la sovvenzione non è pass-through, la colonna **Agenzia pass-through** è vuota.

## <a name="set-up-the-cfda-clusters"></a>Impostare i cluster CFDA

È necessario impostare i cluster CFDA che possono essere associati ai numeri CFDA nella richiesta Schedule of Expenditures of Federal Awards.

1. Vai a **Gestione progetti e contabilità \> Imposta \> Sovvenzioni \> Cluster Catalog of Federal Domestic Assistance**.
2. Seleziona **Nuovo** per creare un cluster CFDA.
3. Immetti il nome del cluster.
4. Selezionare **Salva** per salvare le modifiche.

## <a name="set-up-cfda-numbers"></a>Impostare i numeri CFDA

È necessario impostare i numeri CFDA che possono essere aggiunti alle sovvenzioni e inclusi nella richiesta Schedule of Expenditures of Federal Awards.

1. Vai a **Gestione progetti e contabilità \> Imposta \> Sovvenzioni \> Numeri Catalog of Federal Domestic Assistance**.
2. Seleziona **Nuovo** per creare un numero CFDA.
3. Nella colonna **Numero** immettere il numero CFDA.
4. Premi il tasto **Tabulazione**.
5. Nella colonna **Descrizione** immetti il titolo CFDA.
6. Premi il tasto **Tabulazione**.
7. Facoltativo: nel campo **Cluster programma** aggiungi il cluster CFDA appropriato.
8. Selezionare **Salva** per salvare le modifiche.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Impostare sovvenzioni da dichiarare per la richiesta Schedule of Expenditures of Federal Awards

1. Vai a **Gestione progetti e contabilità \> Sovvenzioni \> Sovvenzioni** e seleziona una sovvenzione esistente.
2. Nella scheda dettaglio **Impostazione** nel campo **Catalog of Federal Domestic Assistance** assegna il numero CFDA. Il numero CFDA sulla sovvenzione determina il cluster CFDA per la dichiarazione.
3. Nella scheda dettaglio **Informazioni sul contatto** immetti le informazioni sul concedente procedendo nel seguente modo:

    1. Nel campo **Cliente sovvenzione** inserisci il cliente responsabile della sovvenzione. Per una sovvenzione esistente, queste informazioni potrebbero essere già state inserite.
    2. Indicare se il cliente della sovvenzione è il finanziatore. Se il cliente della sovvenzione è il finanziatore, lascia la casella di controllo **Pass-through** deselezionata. Se il finanziatore è un altro cliente e il cliente della sovvenzione è responsabile della spesa e del monitoraggio del denaro, seleziona la casella di controllo **Pass-through**.

4. Se hai selezionato la casella di controllo **Pass-through** nel passaggio precedente, nel campo **Agenzia concedente** immetti il cliente che ha fornito la sovvenzione. L'agenzia concedente e il cliente della sovvenzione non possono essere lo stesso cliente.

Ecco un esempio di sovvenzione pass-through:

Il governo federale ha finanziato un progetto infrastrutturale per uno stato. Il governo federale ha dato i soldi allo stato da spendere. In questo caso, il governo federale è l'agenzia concedente e lo stato è il cliente della sovvenzione.

> [!NOTE] 
> Quando si attiva per la prima volta la funzione, i numeri CFDA iniziali verranno inseriti utilizzando i numeri esistenti sulle sovvenzioni.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Escludere le sovvenzioni dalla dichiarazione SEFA in base al tipo di sovvenzione

1. Vai a **Gestione progetti e contabilità \> Imposta \> Concessioni \> Tipi di concessione**.
2. Nella scheda dettaglio **Informazioni predefinite** seleziona la casella di controllo **Escludi da Schedule of Expenditures of Federal Awards**.
3. Selezionare **Salva** per salvare le modifiche.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Eseguire la richiesta Schedule of Expenditures of Federal Awards

1. Vai a **Gestione progetti e contabilità \> Report e richieste di informazioni \> Richiesta di sovvenzione \> Schedule of Expenditures of Federal Awards**.
2. Nella sezione **Parametri** segui questi passaggi:

    1. Nel campo **Intervallo date** seleziona il codice per l'intervallo di date. In alternativa, nei campi **Data iniziale** e **Data finale** definisci l'intervallo di date.
    2. Facoltativo: per includere solo le transazioni fatturate come entrate nella richiesta, imposta l'opzione **Includi solo ricavi fatturati** su **Sì**.

## <a name="columns"></a>Colonne

La richiesta Schedule of Expenditures of Federal Awards include le seguenti colonne:

- Nome del cluster Catalog of Federal Domestic Assistance
- Agenzia concedente
- Agenzia pass-through
- Nome della sovvenzione
- ID sovvenzione
- ID applicazione sovvenzione
- Catalog of Federal Domestic Assistance
- Ricevute
- Spese


[!INCLUDE[footer-include](../includes/footer-banner.md)]