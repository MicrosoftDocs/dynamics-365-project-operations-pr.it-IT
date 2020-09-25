---
title: Aggiornare attributi di plug-in per includere nuove dimensioni di determinazione dei prezzi
description: In questo argomento vengono fornite informazioni sull'aggiornamento degli attributi di plug-in per le dimensioni di determinazione dei prezzi.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752683"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Aggiornare attributi di plug-in per includere nuove dimensioni di determinazione dei prezzi

> [!NOTE]
> Se non utilizzi le funzionalità Offerte e Contratti di Project Service Automation (PSA) puoi ignorare questo argomento.

Questo argomento presuppone che tu abbia completato le procedure negli argomenti [Creare campi ed entità personalizzati](create-custom-fields-entities.md), [Aggiungere campi personalizzati alla configurazione dei prezzi e ad entità transazionali](field-references.md) e [Impostare campi personalizzati come dimensioni di determinazione dei prezzi](set-up-pricing-dimensions.md). Se non hai completato queste procedure, completale prima di leggere questo argomento.

Quando si creano i dettagli di una riga di offerta nella pagina **Riga di offerta** per una riga di offerta di progetto, il sistema crea due righe di stima in background: una riga per il lato costo della stima e una per il lato vendite. Questo è ciò che avviene anche per le voci di contratto di progetto.

Quando modifichi la quantità o un campo nel lato costo, quella modifica viene propagata al lato vendite. Ciò è possibile in quanto i seguenti plug-in devono essere registrati di nuovo dopo una modifica alle dimensioni di determinazione dei prezzi.

- PreOperationContractLineDetailUpdate - Aggiorna **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Aggiorna **msdyn_quotelinetransaction**.

La procedura seguente consente di eseguire la registrazione dei plug-in.

1. Apri **PluginRegistrationTool** e connettiti all'istanza online.
2. Fai clic su **Cerca** e cerca il plug-in da aggiornare.

 ![Screenshot della struttura di ricerca](media/PRT-1.png)

3. Una volta trovato il plug-in, selezionalo e fai clic su **Seleziona nel modulo principale**.

4. Seleziona il passaggio del plug-in da aggiornare, fai clic con il pulsante destro del mouse e quindi scegli **Aggiorna**.

 ![Screenshot del plug-in da aggiornare](media/PRT-2.png)
 
5. Nella finestra di aggiornamento, fai clic sui puntini di sospensione (**...**) negli attributi di filtro.

 ![Screenshot delle informazioni di configurazione di Aggiorna passaggio esistente](media/PRT-3.png)
 
6. Seleziona le caselle di controllo degli attributi di determinazione dei prezzi.

 ![Screenshot che mostra la selezione delle caselle di controllo degli attributi di determinazione dei prezzi](media/PRT-4.png)

7. Fai clic su **OK** per chiudere la pagina e quindi seleziona **Aggiorna passaggio**.

 ![Screenshot con il pulsante "Aggiorna passaggio"](media/PRT-5.png)
 
8. Ripeti questa procedura per il secondo plug-in. **PreOperationQuoteLineDetail - Aggiornamento di msdyn_quotelinetransaction**.

9. Chiudi lo strumento per la registrazione di plug-in.
