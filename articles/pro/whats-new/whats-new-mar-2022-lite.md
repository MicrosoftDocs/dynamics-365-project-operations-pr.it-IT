---
title: Novità di marzo 2022 - Distribuzione semplice di Project Operations
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di marzo 2022 della distribuzione di Project Operations Lite.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934233"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Novità di marzo 2022 - Distribuzione semplice di Project Operations

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.30.0.99

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

- Conto lavoro: creazione di fatture fornitore ed esperienze di corrispondenza

## <a name="quality-updates"></a>Aggiornamenti di qualità

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Tempistica e spesa | 2388011 | Mostra i commenti di rifiuto ai mittenti di inserimenti ore durante l'approvazione in blocco. |
| Pianificazione e rilevamento dei progetti | 2495294 | I dettagli del progetto non devono essere modificabili sulla pagina **Dettagli attività**. |
| Determinazione dei prezzi e fatturazione | 2499605 | I passaggi fondamentali del contratto creati dai passaggi fondamentali dell'offerta vengono erroneamente contrassegnati come di sola lettura. |
| Pianificazione e rilevamento dei progetti | 2506050 | Il set di operazioni rimane in sospeso per un'ora se non ci sono modifiche da salvare. Il set viene quindi contrassegnato erroneamente come **non riuscito**, mentre dovrebbe essere completato immediatamente. |
| Determinazione dei prezzi e fatturazione | 2507401 | Le unità di contratto predefinite vengono immesse in modo errato nei progetti a causa di una memorizzazione nella cache errata. |
| Determinazione dei prezzi e fatturazione | 2541660 | **Convalida della creazione dell'ordine di vendita** in doppia scrittura deve essere solo per ordini basati su progetto. |
| Determinazione dei prezzi e fatturazione | 2552745 | L'imposta non viene suddivisa tra i clienti che hanno impostato regole di fatturazione divise. |
| Determinazione dei prezzi e fatturazione | 2558859 | Messaggi di errore migliorati per l'impostazione delle dimensioni dei prezzi. |
| Determinazione dei prezzi e fatturazione | 2558933 | **Importa da stime di progetto** non riesce quando **msdyn\_project** viene aggiunto come dimensione di prezzo. |
| Determinazione dei prezzi e fatturazione | 2559101 | L'eliminazione dei parametri di progetto non è bloccata e causa problemi. |
| Gestione delle opportunità | 2570390 | Il plug-in a doppia scrittura forza il tipo di conto su offerte, ordini e opportunità come **Cliente**, anche quando quel tipo di conto non è corretto. |
| Determinazione dei prezzi e fatturazione | 2586097 | I costi effettivi fatturati suddivisi non vengono stornati quando un progetto viene rimosso da una riga di contratto di progetto. |
| Determinazione dei prezzi e fatturazione | 2589619 | L'imposta sul materiale fuori catalogo viene propagata alle vendite effettive non fatturate e alla fattura. |
| Gestione delle opportunità | 2594015 | Un'offerta non può essere chiusa come acquisita per i clienti che hanno condizioni di pagamento **Net60**. |
| Pianificazione e rilevamento dei progetti | 2595841 | In Project for the Web, gli utenti ricevono un messaggio di errore su un **msdyn\_actualstart** mancante quando creano una nuova richiesta di risorse. |
| Ore e spesa | 2602511 | Il campo **Rifiutato da** per gli inserimenti ore mostra **Sistema** invece di un utente nominato come autore del rifiuto. |
| Ore e spesa | 2602528 | Un responsabile dell'approvazione del progetto può approvare il tempo sui progetti per i quali non è elencato come responsabile dell'approvazione. |
| Determinazione dei prezzi e fatturazione | 2608550 | Una fattura correttiva può essere confermata anche se non ci sono modifiche all'originale. |

## <a name="removed-and-deprecated-features"></a>Funzionalità rimosse e deprecate

L'articolo [Funzionalità rimosse o deprecate in Project Operations](../../whats-new/removed-depreciated-features-project.md) descrive le funzionalità che sono state rimosse o deprecate per Dynamics 365 Project Operations.

- Una funzionalità rimossa non è più disponibile nel prodotto.
- Una funzionalità deprecata non si trova nella fase attiva di sviluppo e potrebbe essere rimossa in un aggiornamento futuro.

Nell'articolo verrà visualizzato un avviso di ritiro [Funzionalità rimosse o deprecate in Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 mesi prima della rimozione di qualsiasi funzionalità dal prodotto.
