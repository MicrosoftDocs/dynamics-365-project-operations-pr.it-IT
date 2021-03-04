---
title: Utilizzare una categoria di transazione come dimensione di determinazione dei prezzi
description: In questo argomento vengono fornite informazioni sull'utilizzo di un campo per la categoria delle transazioni come dimensione di determinazione dei prezzi.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bace11455d34fdda95e08be1a7cc37850a0cf589
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513996"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Utilizzare una categoria di transazione come dimensione di determinazione dei prezzi


_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


In questo argomento viene descritto come utilizzare un campo **Categoria transazione** come dimensione di determinazione dei prezzi. 

## <a name="prerequisites"></a>Prerequisiti
Prima di completare le procedure in questo argomento, devi disporre di una nuova soluzione per la dimensione dei prezzi per la tua organizzazione. Se non ne hai già creato uno, vedi [Crea campi ed entità personalizzati come dimensioni di prezzo](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Aggiungi il campo Categoria transazione ai moduli e alle viste
Per rendere il file **Categoria di transazione** visibile nella soluzione dimensione prezzo, è necessario aggiungere il campo a tutti i moduli e le viste come entità.

La tabella seguente elenca tutti i moduli e le visualizzazioni predefiniti, per entità. Sarà inoltre necessario aggiungere il nuovo campo a eventuali moduli o visualizzazioni aggiuntivi nelle entità personalizzate.

|  Entity        | Form     |Visualizzazioni        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prezzo ruolo| Informazioni |- Prezzi categorie di risorse attivi<br> - Associato a prezzo categoria di risorsa |
|  Ricarico prezzo ruolo| Informazioni|- Ricarico prezzo ruolo attivo<br>- Vista associata ricarichi prezzo ruolo |
|  Dettagli riga di offerta|- Informazioni sul progetto<br>- Creazione rapida progetti| - Dettagli di riga di offerta attiva<br>- Dettagli di riga di offerta combinata<br>- Visualizzazione associata dettagli di riga di offerta |
|  Dettagli di voce di contratto di progetto|- Informazioni sul progetto<br>- Creazione rapida progetti|- Dettagli voce di contratto combinati<br>- Dettagli voce di contratto attivi<br>- Associata a dettaglio voce di contratto |
|  Attività di progetto|- Informazioni<br>- Nuovo modulo| &nbsp; |
|  Membro del team di progetto|- Informazioni<br>- Nuovo modulo|- Membri del team di progetto attivi<br>- Membri del team di progetto<br>- Visualizzazione associata membri del team di progetto |
|  Inserimento ore|- Informazioni<br>- Crea inserimento ore|- Inserimenti ore personali per data<br>- Inserimenti ore personali per questa settimana<br>- Inserimenti ore per l'approvazione|
|  Riga giornale di registrazione|- Informazioni<br>- Creazione rapida|- Righe giornale di registrazione attive<br>- Visualizzazione associata riga giornale di registrazione|
|  Dettagli di riga fattura|- Informazioni<br>- Creazione rapida|- Dettagli di riga fattura attiva<br>- Transazioni fattura addebitabili<br>- Transazioni fattura gratuite<br>- Visualizzazione associata dettagli di riga fattura <br>- Transazione fattura non addebitabile|
|  Effettiva|- Informazioni<br>- Valori effettivi attivi| Associata a valore effettivo |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Impostare il campo Categoria transazione come dimensione di determinazione dei prezzi

1. Vai a **Impostazioni** > **Parametri**. 
2. Nella pagina **Parametri**, nella scheda **Dimensioni di determinazione dei prezzi basate su importo**, verifica che la griglia nella scheda mostra i record nell'entità **Dimensioni di determinazione dei prezzi**.
3. Aggiungi **Categoria di transazione** a questo elenco e imposta i campi **Costo applicabile a** **Vendite applicabili a** su **Sì**.
4. Nel campo **Tipo di dimensione**, seleziona **Basata su importo** e quindi seleziona la priorità per **Categoria di transazione** relativa a costo e vendite.


[!INCLUDE[footer-include](../includes/footer-banner.md)]