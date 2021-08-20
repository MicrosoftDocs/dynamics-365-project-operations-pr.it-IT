---
title: Creare contratti avanzati per la fatturazione in base allo stato di avanzamento
description: Questo argomento spiega come creare contratti di progetto in modo da poter generare fatture per i clienti, in base a una percentuale del lavoro completato.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 661e8aa0be70e9c8aadcb3a3d9dd6d39d1bcb2fd55d198b3c9af19fc2d0ae9d3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000986"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Creare contratti avanzati per la fatturazione in base allo stato di avanzamento
[!include [banner](../includes/banner.md)]

Questo argomento spiega come creare contratti di progetto in modo da poter creare fatture per i clienti, in base a una percentuale del lavoro completato. Gli importi delle fatture vengono calcolati automaticamente per le categorie di budget di lavoro impostate per un progetto. La tempistica della fatturazione viene impostata quando si negozia il contratto di progetto con il cliente.

Utilizza le procedure in questo argomento per impostare un contratto, un progetto associato e le regole di fatturazione che calcolano gli importi delle fatture per le categorie di budget di lavoro impostate per il progetto.

Dopo aver creato il contratto e il progetto, puoi impostare i dettagli del progetto. Ad esempio, puoi definire attività e assegnare lavoratori al progetto.

## <a name="example"></a>Esempio

La tua organizzazione è una società di sviluppo software. Accetti di sviluppare un pacchetto di contabilità retributiva per un cliente per una tariffa totale di 20.000 USD. La tua organizzazione accetta di fatturare al cliente quando completi percentuali specifiche del progetto. Puoi impostare le seguenti categorie di progetto per il lavoro, in modo da poterle utilizzare nel processo di fatturazione:

- Fabbricazione di articoli in gomma e plastica
- Progettazione
- Installazione

Inoltre configuri le regole di fatturazione che calcolano automaticamente gli importi delle fatture per la percentuale di lavoro completata per ciascuna categoria.

Il responsabile del budget crea un budget per le categorie di progetto. La quantità di lavoro completato viene calcolata automaticamente come percentuale del lavoro effettivo rispetto agli importi preventivati.

## <a name="prerequisites"></a>Prerequisiti

Prima di creare un progetto che utilizza le regole di fatturazione, è necessario impostare le sequenze numeriche per le regole di fatturazione e un giornale di registrazione delle commissioni utilizzato per registrare l'avanzamento delle fatture.

1. Vai a **Gestione progetti e contabilità** \> **Imposta** \> **Parametri Gestione progetti e contabilità**.
2. Nella pagina **Parametri di gestione progetti e contabilità** nella scheda **Sequenze numeriche** imposta la sequenza numerica che desideri utilizzare quando vengono create le regole di fatturazione.
3. Vai a **Gestione progetti e contabilità** \> **Giornali di registrazione** \> **Commissione**.
4. Nella pagina **Giornale di registrazione commissioni** seleziona **Nuovo** e inserisci il nome del giornale di registrazione.

## <a name="create-a-contract-for-progress-billings"></a>Creare un contratto per l'avanzamento della fatturazione

Utilizza questa procedura per creare un contratto di progetto per un progetto a prezzo fisso. Crei una fattura di progetto quando il lavoro completato sul progetto raggiunge una percentuale specificata.

1. Vai a **Gestione progetti e contabilità** \> **Progetti** \> **Contratti di progetto**.
2. Nella pagina **Contratti di progetto** seleziona **Nuovo**.
3. Nella finestra di dialogo **Nuovo contratto di progetto** imposta i seguenti campi:

    - **Nome**
    - **Tipo di finanziamento**
    - **Fonte di finanziamento**
    - **Valuta di vendita** - Per impostazione predefinita, questa valuta viene utilizzata per le fatture cliente associate al contratto di progetto. Tuttavia, puoi modificare la valuta di vendita per una specifica fattura cliente.

4. Seleziona **OK**. Le informazioni vengono copiate nell'intestazione della pagina **Contratti di progetto**.
5. Nella pagina **Contratti di progetto** inserisci il resto delle informazioni richieste per il progetto.

## <a name="create-a-project-for-progress-billings"></a>Creare un progetto per l'avanzamento della fatturazione

Segui questi passaggi per creare un progetto e tutti i sottoprogetti associati a un contratto di progetto.

1. Vai a **Gestione progetti e contabilità** \> **Progetti** \> **Tutti i progetti**.
2. Nella pagina **Tutti i progetto** seleziona **Nuovo**.
3. Nella finestra di dialogo **Nuovo progetto** nel campo **Tipo di progetto** seleziona **Tempo e materiali**.
4. Seleziona un gruppo di progetti. Un gruppo di progetti definisce le informazioni di registrazione per i progetti assegnati al gruppo.
5. Seleziona **Crea progetto**.
6. Dopo aver creato il progetto, imposta la fase del progetto su **In corso**.

## <a name="create-a-budget-for-a-project"></a>Creare un budget per un progetto

Le categorie di budget vengono usate per calcolare automaticamente gli importi delle fatture per la percentuale di lavoro completata per ciascuna categoria. Segui questi passaggi per creare le categorie di budget per i costi stimati.

1. Vai a **Gestione progetti e contabilità** \> **Progetti** \> **Tutti i progetti**.
2. Nella pagina **Tutti i progetti** seleziona e apri il progetto che desideri.
3. Nella pagina **Progetti** nel riquadro azioni, nella scheda **Piano** nel gruppo **Budget** seleziona **Budget di progetto**.
4. Nella pagina **Budget di progetto** immetti il costo stimato per ciascuna categoria nel progetto.

## <a name="create-billing-rules-for-progress-billings"></a>Creare regole di fatturazione per la fatturazione in corso

1. Vai a **Gestione progetti e contabilità** \> **Progetti** \> **Contratti di progetto**.
2. Nella pagina elenco **Contratti di progetto**, seleziona e apri un contratto di progetto.
3. Nella pagina del contratto di progetto, nella scheda dettaglio **Regole di fatturazione** seleziona **Aggiungi**.
4. Nella pagina **Regola di fatturazione** nel campo **Tipo di riga** seleziona **Avanzamento**.
5. Nella scheda dettaglio **Dettagli riga regola di fatturazione** nel campo **Valore di contratto** immetti il valore totale del contratto.
6. Nel campo **Categoria** seleziona la categoria in cui registrare la transazione relativa alle commissioni.
7. Nel campo **Progetto** seleziona il progetto che utilizza questa regola di fatturazione.
8. Facoltativo: assegna la regola di fatturazione a progetti aggiuntivi. Nella scheda dettaglio **Progetto** nella sezione **Progetti disponibili**, seleziona un progetto, quindi seleziona il pulsante freccia destra per aggiungere il progetto alla sezione **Progetti selezionati**.
9. Facoltativo: calcola l'importo percentuale che il cliente trattiene dai pagamenti su una fattura. Nella scheda dettaglio **Condizioni di trattenimento dei pagamenti** seleziona la fonte di finanziamento, quindi nel campo **Percentuale di trattenimento** inserisci la percentuale di trattenimento.
10. Ripetere questi passaggi per creare regole di fatturazione aggiuntive per il contratto di progetto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]