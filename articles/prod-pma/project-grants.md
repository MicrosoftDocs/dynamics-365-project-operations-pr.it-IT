---
title: Concessioni di progetto
description: Questo argomento spiega come creare o modificare una concessione.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 89801696d6a2924d78c85f6e9b4281409222dbb0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079057"
---
# <a name="project-grants"></a>Concessioni di progetto

[!include [banner](../includes/banner.md)]

Una concessione è un dono in denaro per uno scopo o un progetto specifico. Di solito, ci sono restrizioni su come una concessione può essere spesa. In Gestione progetti e contabilità, puoi inserire e tenere traccia delle concessioni e definire le relazioni per progetti e contratti di progetto. Ad esempio, puoi eseguire le attività seguenti:

- Associa le concessioni a progetti e fonti di finanziamento tramite i collegamenti alle pagine **Progetto** e **Dettagli del contratto di progetto**.
- Immetti e tieni traccia delle modifiche a una concessione mentre passa da uno stato a un altro.
- Immetti e traccia i costi, gli importi richiesti e gli importi assegnati.
- Crea concessioni principali e associa le concessioni secondarie.

Puoi creare una concessione inserendo tutti i dettagli in un nuovo record oppure è possibile copiare i dettagli da una concessione esistente e quindi aggiornarli.

## <a name="create-a-new-grant"></a>Creare una nuova concessione

1. Vai a **Gestione progetti e contabilità** \> **Concessioni** \> **Concessioni**.
2. Seleziona **Nuovo** \> **Concessione**.
3. Nella pagina dei dettagli della concessione, nella scheda dettaglio **Generale** nel campo **ID concessione** immetti un identificatore alfanumerico per la concessione.
4. Nel campo **Nome concessione** immetti un nome per la concessione.
5. Nel campo **Descrizione** aggiungi i dettagli sulla nuova concessione.

    La maggior parte degli altri campi della pagina sono opzionali e puoi inserire tutte le informazioni che desideri.

    Il seguente elenco descrive le informazioni specificate in ciascuna scheda dettaglio della pagina dei dettagli della concessione:

    - **Generale** - Immetti il nome, lo stato, la descrizione, lo scopo e l'importo della concessione.
    - **Informazioni sui contatti** - Immetti i dettagli sui membri del personale, il dipartimento che gestisce la concessione e il cliente della concessione o l'origine dell'organizzazione della concessione. Puoi anche indicare se la tua organizzazione è un'entità pass-through che riceve la concessione e poi la passa a un altro destinatario. Seleziona **Aggiungi** per aggiungere informazioni di contatto come numeri di telefono e indirizzi e-mail per l'organizzazione che fornisce la concessione.
    - **Date e scadenze** - Immetti le date relative alla concessione e alla domanda di concessione. Gli esempi includono la data di scadenza della domanda, la data di presentazione e la data in cui la concessione viene approvata o rifiutata.
    - **Progetti associati e contratti di progetto** - È possibile immettere informazioni in questa Scheda dettaglio solo se il campo **Stato di concessione** nella scheda dettaglio **Generale** è impostato su **Attivo** o **Assegnato**. Seleziona una delle seguenti opzioni per completare l'attività correlata:

        - **Aggiungi fonte di finanziamento** - Aggiungi una nuova fonte di finanziamento per la concessione. Puoi inserire tutti i dettagli adesso, oppure puoi usare le informazioni predefinite e aggiornarle successivamente.
        - **Aggiungi contratto di progetto** - Aggiungi o aggiorna le informazioni sul contratto di progetto.
        - **Aggiungi progetto** - Aggiungi o aggiorna i dettagli del progetto.

    - **Impostazione** - Immetti i dettagli sulla corrispondenza dei finanziamenti, se queste informazioni sono richieste. Molte organizzazioni che assegnano concessioni richiedono che i destinatari spendano un importo specifico del proprio denaro o risorse, per corrispondere all'importo assegnato nella concessione. Nel campo **Progetto locale o ID monitoraggio** puoi inserire un identificatore diverso dall'identificatore del progetto.

        > [!NOTE]
        > Se parte della concessione verrà assegnata a un'organizzazione diversa, imposta l'opzione **Concessione secondaria** su **Sì**. Per le concessioni assegnate negli Stati Uniti, è possibile specificare se una concessione verrà assegnata in base a un mandato statale o federale.

    - **Dettagli di prelievo** - Aggiungi o aggiorna le informazioni sulla frequenza con cui i fondi possono essere ritirati, fatturati o spesi.

## <a name="create-a-new-grant-from-a-copy"></a>Creare una nuova concessione da una copia

1. Vai a **Gestione progetti e contabilità** \> **Concessioni** \> **Concessioni**.
2. Seleziona **Nuovo** \> **Copia dalla concessione**.
3. Immetti un identificatore alfanumerico e un nome per la nuova concessione, quindi seleziona **OK**.
4. Nella pagina dei dettagli della concessione, rivedi i dettagli della concessione copiata e apporta le modifiche necessarie. La maggior parte dei campi della pagina sono opzionali.

## <a name="view-or-modify-grant-details"></a>Visualizzare o modificare i dettagli della concessione

1. Vai a **Gestione progetti e contabilità** \> **Concessioni** \> **Concessioni**.
2. Seleziona la concessione da modificare.
3. Nel riquadro azioni, nella scheda **Concessione** , nel gruppo **Mantieni** , seleziona **Modifica**.
4. Rivedi i dettagli della concessione e apporta le modifiche necessarie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]