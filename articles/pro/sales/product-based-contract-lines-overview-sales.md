---
title: Panoramica delle voci di contratto basate su prodotto - semplice
description: In questo argomento vengono fornite informazioni sulle voci di contratto basate su prodotto.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177876"
---
# <a name="product-based-contract-lines-overview---lite"></a>Panoramica delle voci di contratto basate su prodotto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Puoi creare voci di contratto basate su prodotto in Dynamics 365 Project Operations. Le voci di contratto basate su prodotto possono essere righe create manualmente oppure articoli del catalogo prodotti.

## <a name="product-catalog"></a>Catalogo prodotti

I prodotti nel catalogo prodotti hanno un'unità e un'unità di vendita predefinite. Se vari prodotti condividono lo stesso set di attributi, puoi creare una famiglia di prodotti che ha anch'essa tali attributi. Tutti i prodotti in una famiglia di prodotti ereditano lo stesso set di attributi.

Ad esempio, una società vende licenze di sottoscrizione per diversi tipi di software. Tutti i software con sottoscrizione hanno i due seguenti attributi:

- Numero di utenti
- Durata della sottoscrizione (in mesi)

Per mantenere questo tipo di catalogo, crea una famiglia di prodotti denominata **Software di sottoscrizione**. Aggiungi gli attributi **Numero di utenti** e **Durata sottoscrizione** alla famiglia di prodotti. Quindi, aggiungi i singoli prodotti alla famiglia di prodotti **Software di sottoscrizione**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Aggiungere articoli del catalogo prodotti a un contratto di progetto

I contratti di progetto presentano sezioni per due tipi di righe: basate su progetto e basate su prodotto. Le righe basate su prodotto includono tutti i prodotti e le unità nel listino prezzi del prodotto nel contratto. Puoi aggiungere prodotti che non fanno parte del listino prezzi del prodotto del contratto.

Puoi selezionare prodotti in altri listini prezzi, oppure direttamente dal catalogo prodotti. Quando selezioni prodotti direttamente da un catalogo prodotti, il listino prezzi predefinito di quel prodotto viene utilizzato per ottenere il prezzo di vendita del prodotto. Se un listino prezzi predefinito non è impostato, il prezzo è 0 (zero).

Se una voce di contratto è basata su un catalogo prodotti, puoi sostituire il prezzo di vendita direttamente nella riga. Una voce di contratto ha il campo **Prezzi** con due valori:

- **Sostituisci prezzo**
- **Predefinito dell'utente**

Se imposti il campo **Prezzi** su **Sostituisci prezzo**, il prezzo predefinito non è impostato. Immetti un prezzo per il prodotto nella voce di contratto. Se imposti il campo su **Usa predefinito**, viene utilizzato il prezzo di vendita predefinito e il campo non può essere modificato.

Dopo l'installazione di Project Operations, i prezzi di vendita predefiniti vengono immessi nelle righe basate su prodotto di un contratto. Il campo **Prezzi** viene quindi impostato su **Sostituisci prezzo** di modo che sia possibile modificare il prezzo predefinito nelle voci di contratto. Si tratta di una sostituzione specifica di Project Operations al comportamento delle righe basate su prodotto in Dynamics 365 Sales.
