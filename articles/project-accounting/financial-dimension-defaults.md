---
title: Valori predefiniti della dimensione finanziaria
description: Questo argomento fornisce informazioni su come impostare i valori predefiniti della dimensione finanziaria.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950134"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]