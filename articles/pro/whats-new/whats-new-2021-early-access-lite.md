---
title: Accesso in anteprima alle novità 2021 ciclo 2 - distribuzione lite di Project Operations
description: Questo argomento fornisce informazioni sulle funzionalità disponibili nella versione in anteprima 2021 ciclo 2 della distribuzione lite di Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7b5f3528e4b4e615b8e7f24bfd3702746fd584c9
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723681"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Accesso in anteprima alle novità 2021 ciclo 2 - distribuzione lite di Project Operations

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

  - Project Operations in ambiente Dataverse versione 4.23.0.4

Il rilascio viene applicato solo quando un ambiente è [optato per l'accesso in anteprima](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

[Gestione del conto lavoro](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview): questa funzione offre una migliore visibilità e controllo su tutti gli aspetti del lavoro su un progetto. L'anteprima della gestione del conto lavoro include le seguenti funzionalità:

  - Un responsabile di progetto può creare un conto lavoro con un fornitore. Per impostazione predefinita, per il conto lavoro vengono utilizzati i listini prezzi associati al record del fornitore. Il conto fornitore ha un tipo di relazione di tipo **fornitore** o **venditore**.
  - Un responsabile di progetto può dettagliare tutti gli acquisti come voci nel conto lavoro. Le righe del conto lavoro possono riguardare tempi, spese o prodotti. La classe di transazione della voce di conto lavoro determina a cosa serve la riga.
  - L'account manager del fornitore e il project manager possono eseguire iterazioni sul conto lavoro. È possibile apportare modifiche ai prezzi nei listini prezzi di acquisto associati al conto lavoro.
  - Durante il processo, se la voce di conto lavoro è per le ore, l'account manager del fornitore può associare i contatti a ciascuna riga di conto lavoro. Questa associazione fornisce informazioni al project manager che sta lavorando sul conto lavoro. Quando un contatto fornitore è associato a una riga di conto lavoro, il sistema crea automaticamente una risorsa prenotabile dal contatto, se non esiste già una risorsa prenotabile.
  - Il metodo di fatturazione su ciascuna voce di conto lavoro può essere a prezzo fisso o tempo e materiale. Per le righe di conto lavoro a prezzo fisso viene impostata una pianificazione fattura basata su passaggi fondamentali.
