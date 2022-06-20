---
title: Utilizzare una categoria di transazione come dimensione di determinazione dei prezzi
description: In questo articolo vengono fornite informazioni su come utilizzare il campo Categoria transazione come dimensione di determinazione dei prezzi.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911699"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Utilizzare una categoria di transazione come dimensione di determinazione dei prezzi


_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


In questo articolo viene descritto come utilizzare il campo **Categoria transazione** come dimensione di determinazione dei prezzi. 

## <a name="prerequisites"></a>Prerequisiti
Prima di completare le procedure in questo articolo, è necessario disporre di una nuova soluzione per la dimensione dei prezzi per la propria organizzazione. Se non ne hai già creato uno, vedi [Crea campi ed entità personalizzati come dimensioni di prezzo](create-custom-fields-entities-pricing-dimensions.md).

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