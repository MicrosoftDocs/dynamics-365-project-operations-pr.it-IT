---
title: Impostare le tariffe di vendita e costi per i prodotti del catalogo - semplice
description: Questo argomento fornisce informazioni su come configurare le tariffe di costo e vendita per le voci di un catalogo prodotti.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764558"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Impostare le tariffe di vendita e costi per i prodotti del catalogo - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_


L'impostazione dei prezzi per gli articoli del catalogo prodotti in Dynamics 365 Project Operations è uguale all'impostazione in Dynamics 365 Sales.

In Project Operations, i prodotti non possono essere stimati o utilizzati nei progetti, quindi non è necessario impostare i prezzi del catalogo prodotti sui listini prezzi del progetto per offerte e contratti.

Usa il campo **Prezzo del prodotto** di un'offerta, un contratto o un conto per impostare i prezzi del catalogo prodotti. Non impostare i prezzi del catalogo prodotti nei listini prezzi del progetto. I listini prezzi di progetto sono esclusivi di Project Operations. La logica aziendale specifica dell'applicazione copia i listini prezzi da un'offerta a un contratto. Il risultato è un listino prezzi di progetto specifico del contratto. L'operazione di copia può ritardare il processo di acquisizione dell'offerta se il listino prezzi di progetto dell'offerta diventa troppo grande. I listini prezzi dei prodotti non vengono copiati per creare listini prezzi personalizzati nei contratti. Poiché non è coinvolta la copia, le prestazioni del processo di offerta non vengono influenzate.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]