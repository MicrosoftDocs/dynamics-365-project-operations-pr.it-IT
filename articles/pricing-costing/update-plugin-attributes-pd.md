---
title: Aggiornamento degli attributi dei plug-in con nuove dimensioni di determinazione dei prezzi
description: In questo argomento vengono fornite informazioni su come aggiornare gli attributi di plug-in per le dimensioni di determinazione dei prezzi.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 54b87a993929edbf89ef48741ba0a06c6c42ec4e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004626"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Aggiornare gli attributi dei plug-in con nuove dimensioni di determinazione dei prezzi

In questo argomento vengono fornite informazioni su come aggiornare gli attributi di plug-in per le dimensioni di determinazione dei prezzi.

> [!NOTE]
> Questo argomento è applicabile solo alle funzionalità di preventivo e contratto in Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Prerequisiti
Prima di completare i passaggi in questo argomento, è necessario aver completato le procedure nei seguenti argomenti:

  - [Creazione di campi ed entità personalizzati](create-custom-fields-entities-pricing-dimensions.md) 
  - [Aggiungere campi personalizzati all'impostazione e alle entità transazionali ](add-custom-fields-price-setup-transactional-entities.md)
  - [Configurare campi personalizzati come dimensioni di determinazione dei prezzi](set-up-custom-fields-pricing-dimensions.md). 
  
Se non hai completato queste procedure, completale prima di leggere questo argomento.

## <a name="register-a-plug-in"></a>Registrare un plug-in
Quando un dettaglio di una riga di preventivo viene creato nella pagina **Riga di offerta** per una riga di preventivo di progetto, il sistema crea due righe di preventivo. Una riga è per i costi della stima e l'altra è per le vendite. Questo è ciò che avviene anche per le voci di contratto di progetto.

Quando modifichi la quantità o un campo nel lato costo, quella modifica viene propagata al lato vendite. Ciò è possibile perché i plug-in PreOperation su Quotelinedetail e le entità di dettaglio della linea di contratto collegano attributi specifici dal lato dei costi al lato delle vendite della transazione. Se è necessario che le modifiche apportate ai valori della dimensione del prezzo sul lato delle vendite vengano apportate anche sul lato del costo, i seguenti plug-in devono essere registrati nuovamente dopo aver apportato le modifiche a una dimensione del prezzo.

Questi sono i plug-in per aggiornare e registrare nuovamente:

- PreOperationContractLineDetailUpdate: **Aggiorna msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate: **Aggiorna msdyn_quotelinetransaction**

Completare i seguenti passaggi per aggiornare e registrare nuovamente i plug-in.

1. Apri **PluginRegistrationTool** e connettiti al tuo ambiente Project Operations Dataverse.
2. Seleziona **Ricerca** e digita le prime lettere del plug-in da aggiornare.
3. Una volta trovato il plug-in, selezionalo e fai clic su **Seleziona nel modulo principale**.
4. Seleziona il passaggio **Aggiorna msdyn_orderlinetransaction**, fai clic con il pulsante destro del mouse e quindi scegli **Aggiorna**.
5. Nella finestra di dialogo **Aggiorna**, fai clic sui puntini di sospensione (**...**) negli attributi di filtro.
6. La finestra degli attributi di filtro viene aperta; fornisce un elenco di tutti gli attributi nell'entità e le dimensioni di determinazione dei prezzi. Seleziona le caselle di controllo per gli attributi di determinazione dei prezzi.
7. Seleziona **OK** per chiudere la pagina, quindi seleziona **Aggiorna passaggio**.
8. Ripeti i passaggi da 2 a 7 per il secondo plug-in, **PreOperationQuoteLineDetail**. Per questo plug-in, devi aggiornare il passaggio **Aggiorna of msdyn_quotelinetransaction**.
9. Chiudi **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]