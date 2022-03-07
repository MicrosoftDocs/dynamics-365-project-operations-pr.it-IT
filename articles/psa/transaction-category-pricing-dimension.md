---
title: Utilizzare una categoria di transazione come dimensione di determinazione dei prezzi
description: In questo argomento vengono fornite informazioni sull'utilizzo di una categoria di transazione come dimensione di determinazione dei prezzi.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 776327ddca9b5013ca05eb4058145f4196e4143509098c82d0f452bc9709b673
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988868"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Utilizzare una categoria di transazione come dimensione di determinazione dei prezzi

[!include [banner](../includes/psa-now-project-operations.md)]

In questo argomento viene descritto come utilizzare una categoria di transazione come dimensione di determinazione dei prezzi. Prima di iniziare, crea una soluzione per le dimensioni di determinazione dei prezzi se non lo hai già fatto. Se disponi già di tale soluzione, puoi apportare le modifiche in quella soluzione. Se non hai ancora creato questa soluzione per l'organizzazione, completa le procedure nell'argomento [Creare campi ed entità personalizzati](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Aggiungere una categoria di transazione a moduli e viste
Per rendere la categoria di transazione visibile nell'interfaccia utente della soluzione per le dimensioni di determinazione dei prezzi, devi esaminare tutti i moduli e viste delle entità principali e aggiungere questi campi a moduli e viste di queste entità.
La tabella seguente è un elenco completo di moduli e viste predefinite, elencati per entità, che devono essere aggiornati con i nuovi campi. Se nelle personalizzazioni di queste entità sono presenti ulteriori viste o moduli, aggiungici anche i nuovi campi.

|  Entità        | Moduli     |Viste        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prezzo ruolo|• Informazioni |• Prezzi categorie di risorse attivi<br> • Vista Prezzo categoria di risorsa associata|
|  Ricarico prezzo ruolo|• Informazioni|• Ricarico prezzo ruolo attivo<br>• Vista Ricarico prezzo ruolo associata|
|  Dettagli riga di offerta|• Informazioni sul progetto<br>• Creazione rapida progetti|• Dettagli di riga di offerta attiva<br>• Dettagli di riga di offerta combinata<br>• Vista Dettagli riga di offerta associata|
|  Dettagli di voce di contratto di progetto|• Informazioni sul progetto<br>• Creazione rapida progetti|• Dettagli voce di contratto combinati<br>• Dettagli voce di contratto attivi<br>• Vista Dettaglio riga di contratto associata|
|  Attività di progetto|• Informazioni<br>• Nuovo modulo||
|  Membro del team di progetto|• Informazioni<br>• Nuovo modulo|• Membri del team di progetto attivi<br>• Membri del team di progetto<br>• Vista Membri del team di progetto associata|
|  Inserimento ore|• Informazioni<br>• Crea inserimento ore|• Inserimenti ore personali per data<br>• Inserimenti ore personali per questa settimana<br>• Inserimenti ore per l'approvazione.|
|  Riga giornale di registrazione|• Informazioni<br>• Creazione rapida|• Righe giornale di registrazione attive<br>• Vista Riga giornale di registrazione associata|
|  Dettagli di riga fattura|• Informazioni<br>• Creazione rapida|• Dettagli di riga fattura attiva<br>• Transazioni fattura addebitabili<br>• Transazioni fattura gratuite<br>• Vista Dettagli di riga fattura associata<br>• Transazione fattura non addebitabile|
|  Valore effettivo|• Informazioni<br>• Valori effettivi attivi|• Vista Valore effettivo associata|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Impostare una categoria di transazione come dimensione di determinazione dei prezzi

1. Nell'interfaccia Web, seleziona **Project Service** > **Impostazioni** > **Parametri**. 
2. Nella pagina **Parametri**, nella scheda **Dimensioni di determinazione dei prezzi basate su importo**, nota che la griglia nella scheda mostra i record nell'entità **Dimensioni di determinazione dei prezzi**.
3. Aggiungi **Categoria di transazione** a questo elenco e imposta i campi **Costo applicabile a** **Vendite applicabili a** su **Sì**.
4. Nel campo **Tipo di dimensione**, seleziona **Basata su importo** e quindi seleziona la priorità per **Categoria di transazione** relativa a costo e vendite.


[!INCLUDE[footer-include](../includes/footer-banner.md)]