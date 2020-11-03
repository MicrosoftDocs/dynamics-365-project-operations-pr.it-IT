---
title: Impostare tariffe di vendita e costo per i prodotti in catalogo
description: Questo argomento fornisce informazioni su come configurare le tariffe di costo e vendita per le voci di un catalogo prodotti.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078943"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Impostare tariffe di vendita e costo per i prodotti in catalogo

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_


L'impostazione dei prezzi per gli articoli del catalogo prodotti in Dynamics 365 Project Operations è uguale a quella di Dynamics 365 Sales.

Poiché i prodotti non possono essere stimati o utilizzati nei progetti in Project Operations, non è necessario impostare i prezzi del catalogo prodotti sui listini prezzi di progetto per offerte e contratti.

I prezzi del catalogo prodotti devono essere impostati nel campo **Prezzo prodotto** di un'offerta, un contratto o un conto. Non impostare i prezzi del catalogo prodotti nei listini prezzi di progetto per queste entità. I listini prezzi di progetto sono esclusivi di Project Operations. Esiste una logica aziendale specifica dell'applicazione che copia i listini prezzi da un'offerta a un contratto. Il risultato è un listino prezzi di progetto specifico del contratto. L'operazione di copia può ritardare il processo di acquisizione dell'offerta se il listino prezzi di progetto dell'offerta diventa troppo grande. I listini prezzi dei prodotti non vengono copiati per creare listini prezzi personalizzati nei contratti. Ciò significa che i listini prezzi dei prodotti non influiscono sulle prestazioni del processo di acquisizione dell'offerta.
