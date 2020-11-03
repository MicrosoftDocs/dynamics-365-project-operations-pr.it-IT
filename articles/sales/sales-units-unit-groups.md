---
title: Unità e unità di vendita
description: Questo argomento fornisce informazioni su come creare unità e unità di vendita in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078999"
---
# <a name="units-and-unit-groups"></a>Unità e unità di vendita

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le unità sono le quantità o le misure in cui vengono venduti i prodotti o i servizi. Ad esempio, se si vendono forniture di giardinaggio, si potrebbero vendere i semi in unità tipo pacchetti, scatole e pallet. Un'unità di vendita è una raccolta di tali diverse unità.

Per completare i passaggi in questo argomento, assicurati di essere stato assegnato al ruolo Amministratore di sistema o Responsabile Sales Professional o di disporre di autorizzazioni equivalenti.

## <a name="create-a-unit-group"></a>Creare un'unità di vendita

1. Nella mappa del sito, seleziona **Unità**.
2. Seleziona **Nuovo** e nella finestra di dialogo **Crea unità di vendita** immetti il nome dell'unità.
3. Nel campo **Unità primaria** immetti l'unità di misura comune più piccola che verrà utilizzata per la vendita del prodotto. Ad esempio, potresti inserire "pezzo" o "oncia".
4. Seleziona **OK**.

## <a name="add-units-to-a-unit-group"></a>Aggiungere unità a un'unità di vendita

1. Apri un'unità di vendita e nella scheda **Correlato** seleziona **Unità**. Vedrai che l'unità primaria è già aggiunta.
2. Seleziona **Aggiungi nuova unità** e nella pagina **Creazione rapida: unità** nel campo **Nome** inserisci il nome dell'unità.
3. Nel campo **Quantità** immetti la quantità che l'unità conterrà. Ad esempio, se una scatola contiene 2 pezzi, immetti "2". 
4. Nel campo **Unità base** seleziona un'unità di base per stabilire l'unità di misura più bassa per l'unità. Ad esempio, potresti selezionare "Pezzo".
5. Seleziona **Salva**.
