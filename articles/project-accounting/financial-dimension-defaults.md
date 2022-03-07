---
title: Valori predefiniti della dimensione finanziaria
description: Questo argomento fornisce informazioni su come impostare i valori predefiniti della dimensione finanziaria.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c1eb71d13ca7fc59118d15fef7ac914577b3b0e
ms.sourcegitcommit: fe5610464fdb5be756aa6a6a5b3c9a991dea0ed8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922943"
---
# <a name="financial-dimension-defaults"></a>Valori predefiniti della dimensione finanziaria

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations utilizza il framework [Dimensioni finanziarie](/dynamics365/finance/general-ledger/financial-dimensions) in Dynamics 365 Finance per fornire ulteriori informazioni sulle transazioni di contabilità generale e contabilità secondaria del progetto.

Le dimensioni finanziarie predefinite possono essere impostate su un cliente, una fonte di finanziamento del progetto, un passaggio fondamentale, una voce di contratto di progetto o un progetto.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definire le dimensioni finanziarie predefinite per un cliente

I valori predefiniti della dimensione del cliente sono specificati in Finance. Completa i seguenti passaggi per impostare i valori predefiniti delle dimensioni.

1. Vai a **Contabilità clienti** > **Clienti** > **Tutti i clienti**.
2. Nella pagina **Clienti** nella scheda **Dimensioni finanziarie** imposta i valori di dimensione finanziaria per un cliente specifico.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definire le dimensioni finanziarie predefinite per contratti di progetto

I contratti di progetto vengono creati e gestiti in Common Data Service (CDS). Gli attributi contabili per i contratti di progetto sono impostati nel modulo **Gestione progetti e contabilità** in Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Impostare le dimensioni finanziarie per una fonte di finanziamento del progetto

1. Vai a **Gestione progetti e contabilità** > **Progetti** > **Contratti di progetto**.
2. Seleziona il record che desideri aggiornare e nella scheda **Contratto di progetto** seleziona **Mostra contabilità predefinita**.
3. Espandi **Informazioni correlate** e seleziona la scheda **Fonti di finanziamento**.
4. Imposta i valori predefiniti della dimensione finanziaria. Tieni presente che le dimensioni finanziarie sono predefinite dal conto cliente.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Impostare le dimensioni finanziarie per una voce di contratto di progetto

1. Vai a **Gestione progetti e contabilità** > **Progetti** > **Contratti di progetto**.
2. Seleziona il record che desideri aggiornare e nella scheda **Contratto di progetto** seleziona **Mostra contabilità predefinita**.
3. Espandi **Informazioni correlate** e seleziona la scheda **Voci di contratto**.
4. Imposta i valori predefiniti della dimensione finanziaria. Le impostazioni predefinite della dimensione finanziaria sono applicabili e possono essere utilizzate solo con le voci di contratto a prezzo fisso (passaggio fondamentale).

Questi valori predefiniti vengono utilizzati nelle transazioni di conto di progetto e nelle righe fattura correlate.

## <a name="define-default-financial-dimensions-for-projects"></a>Definire le dimensioni finanziarie predefinite per i progetti

I progetti vengono creati e gestiti in CDS. Gli attributi contabili per i progetti sono impostati nel modulo **Gestione progetti e contabilità** in Finance.

1. Vai a **Gestione progetti e contabilità** > **Progetti** > **Tutti i progetti**.
2. Seleziona il record che desideri aggiornare e nella scheda **Progetto** seleziona **Mostra contabilità predefinita**.
3. Espandi **Informazioni correlate** e seleziona la scheda **Configurazione**.
4. Imposta i valori predefiniti della dimensione finanziaria. Tieni presente che le dimensioni finanziarie sono predefinite dal conto cliente. Se il progetto è associato a una voce di contratto con più clienti di contratto di progetto, il cliente principale viene utilizzato per le dimensioni finanziarie predefinite.

Le dimensioni finanziarie predefinite del progetto vengono utilizzate per impostare i valori predefiniti della riga di giornale di registrazione per le transazioni di ore, spese e commissioni nel **Giornale di registrazione integrazione Project Operations** e sulle righe di fattura di progetto correlate.

## <a name="apply-financial-dimensions-for-project-time-entries"></a>Applicare dimensioni finanziarie per gli inserimenti ore del progetto
Per applicare le dimensioni finanziarie per gli inserimenti ore del progetto, tieni presente che il valore della dimensione predefinita si basa sul seguente ordine:

1. Risorsa
2. Project
3. Fonte di finanziamento

Ad esempio, se la dimensione predefinita è specificata su una risorsa, verrà applicata su una dimensione predefinita specificata nel progetto. Allo stesso modo, una dimensione di progetto predefinita verrà applicata a quella predefinita specificata nella fonte di finanziamento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
