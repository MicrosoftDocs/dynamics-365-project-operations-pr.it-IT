---
title: Utilizzare le categorie di approvvigionamento con ordini di acquisto di progetto e fatture fornitore in sospeso
description: Questo articolo descrive come configurare le categorie di approvvigionamento che possono essere utilizzate con gli ordini di acquisto di progetto e le fatture fornitore in sospeso.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028615"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Utilizzare le categorie di approvvigionamento con ordini di acquisto di progetto e fatture fornitore in sospeso

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

I professionisti degli acquisti possono creare e gestire cataloghi degli articoli e dei servizi che possono essere utilizzati negli ordini di acquisto di progetto e nelle fatture fornitore in sospeso. [Cataloghi di approvvigionamento](/dynamics365/supply-chain/procurement/procurement-catalogs) ti offre un modo semplice per classificare gli acquisti senza dover configurare e utilizzare un catalogo di prodotti rilasciato. Ciascuna categoria di approvvigionamento può essere mappata a una categoria di progetto per transazioni di tempo, spese o articoli. Dopo che una fattura fornitore in sospeso che utilizza una categoria di approvvigionamento è stata registrata, il sistema creerà i valori effettivi di progetto per tempo, spese o materiali, le transazioni di progetto e i movimenti contabili secondari.

## <a name="minimum-version-requirements"></a>Requisiti di versione minima

Le versioni seguenti sono necessarie per utilizzare le categorie di approvvigionamento con gli ordini di acquisto del progetto per scenari Microsoft Dynamics 365 Project Operations basati su risorse/materiali non stoccati:

- Soluzione Project Operations Dataverse versione 4.41.0.45 o successiva
- Ambiente delle app per la finanza e le operazioni versione 10.0.26 o successiva

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Eseguire mappe a doppia scrittura per il supporto delle categorie di approvvigionamento

Assicurati che la mappatura per **Entità di esportazione riga di fattura fornitore progetto integrazione Project Operations msdyn\_projectvendorinvoicelines** utilizzi la versione 1.0.0.4 o successiva.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Abilitare la chiave di funzionalità per le categorie di approvvigionamento

Attieniti alla seguente procedura per abilitare la funzionalità per l'utilizzo delle categorie di approvvigionamento con gli ordini di acquisto del progetto.

1. In Dynamics 365 Finance, apri l'area di lavoro **Gestione funzionalità**.
1. Nell'elenco delle funzionalità, trova la funzionalità **Utilizza le categorie di approvvigionamento in Project Operations per scenari basati su risorse/materiali non stoccati** e seleziona **Abilita**.

> [!IMPORTANT]
> Come prerequisito, devi anche abilitare la funzionalità **Abilita le fatture fornitore in sospeso su Project Operations per scenari basati su risorse/materiali non stoccati**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mappare le categorie di progetto nella gerarchia delle categorie di approvvigionamento

Attieniti alla seguente procedura per mappare le categorie di progetto alle categorie di approvvigionamento nella gerarchia **Categoria di approvvigionamento**:

1. Passa a **Approvvigionamento \> Categorie di approvvigionamento**.
1. Seleziona **Modifica gerarchia di categorie**.
1. Seleziona il nodo della gerarchia di categorie desiderato, quindi nella scheda **Assegna categorie di progetto**, associa il nodo alla categoria di progetto dalla categora di progetto **Tempo**, **Spese**, o, **Articolo** (cioè la categoria **Tempo predefinito** o **Spesa predefinita**).
1. Seleziona **Salva**.
1. Chiudi la pagina.

> [!NOTE]
> La mappatura di una categoria di approvvigionamento in una categoria di progetto è facoltativa. Se una categoria di approvvigionamento non è mappata, il sistema utilizzerà il valore impostato nel campo **Articolo** della sezione **Valori predefiniti della categoria di progetto** nella scheda **Project Operations in Dynamics 365 Customer Engagement** della pagina **Parametri Gestione progetti e contabilità**.
