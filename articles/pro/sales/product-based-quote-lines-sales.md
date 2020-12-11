---
title: Panoramica delle righe dell'offerta basate su prodotto - semplice
description: Questo argomento fornisce informazioni sull'utilizzo delle righe di offerta basate su prodotto.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178193"
---
# <a name="product-based-quote-lines-overview---lite"></a>Panoramica delle righe dell'offerta basate su prodotto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Puoi creare righe di offerta basate su prodotto in Dynamics 365 Project Operations. Le righe di offerta basate su prodotto possono essere aggiunte manualmente oppure possono essere articoli del catalogo prodotti.

## <a name="product-catalog"></a>Catalogo prodotti

Ogni prodotto nel catalogo prodotti ha un'unità e un'unità di vendita predefinite. Se più prodotti condividono lo stesso set di attributi, puoi creare una famiglia di prodotti che ha anch'essa tali attributi. 

Ad esempio, una società vende licenze di sottoscrizione per diversi tipi di software. Tutti i software con sottoscrizione hanno i due seguenti attributi:

- Numero di utenti
- Durata della sottoscrizione misurata in mesi

Per gestire questo tipo di catalogo crea una famiglia di prodotti denominata **Software con sottoscrizione** che ha il numero di utenti e la durata sottoscrizione come attributi. Successivamente, puoi aggiungere singoli prodotti alla famiglia di prodotti **Software con sottoscrizione**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Aggiungere articoli del catalogo prodotti a un'offerta di progetto

Le pagine **Offerta di progetto** e **Contratto di progetto** presentano sezioni per righe basate su progetto e righe basate su prodotto. Per le righe basate su prodotto, l'elenco a discesa nella riga di offerta o nella voce di contratto di progetto include tutti i prodotti e unità nel listino prezzi prodotto. Puoi anche aggiungere prodotti che non fanno parte del listino prezzi di prodotto.

Inoltre, puoi selezionare prodotti in altri listini prezzi oppure direttamente dal catalogo prodotti. Quando selezioni prodotti direttamente da un catalogo prodotti, il listino prezzi predefinito di quel prodotto viene utilizzato per ottenere il prezzo di vendita del prodotto. Se un listino prezzi predefinito non è impostato, il prezzo è zero (0).

Quando una riga di offerta è basata su un catalogo prodotti, puoi sostituire il prezzo di vendita direttamente nella riga di offerta. Una riga di offerta nel campo **Prezzi** con due valori disponibili:

- **Sostituisci prezzo**
- **Usa predefinita**

Se selezioni **Sostituisci prezzo**, il prezzo predefinito non è impostato. Devi quindi immettere un prezzo per il prodotto nella riga di offerta. Se selezioni **Usa predefinito**, viene utilizzato il prezzo di vendita predefinito e il campo è bloccato per la modifica.

I prezzi di vendita predefiniti vengono immessi nelle righe basate su prodotto di un'offerta. Il campo **Prezzi** viene quindi impostato su **Sostituisci prezzo** di modo che sia possibile modificare il prezzo predefinito nelle righe di offerta. Si tratta di una sostituzione specifica di Project Operations al comportamento delle righe basate su prodotto in Dynamics 365 Sales.