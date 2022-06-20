---
title: Modalità di pianificazione
description: Questo articolo fornisce informazioni sulle modalità di pianificazione.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3cbe14f8d458c5d9631e0595912afa8cbb87b9de
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923653"
---
# <a name="scheduling-modes"></a>Modalità di pianificazione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


Dynamics 365 Project Operations fornisce la possibilità alle organizzazioni di definire come gestire le modifiche alle variabili chiave nelle attività all'interno della struttura di suddivisione del lavoro. In base alle esigenze specifiche dell'organizzazione, i responsabili di progetto possono apportare modifiche alla modalità di pianificazione quando viene creato un progetto.

Sono disponibili tre modalità di pianificazione in Project Operations:

  - Durata fissa (questa è la modalità predefinita)
  - Lavoro fisso (*Lavoro*)
  - Unità fisse

I valori influenzati dalla definizione di una specifica modalità di pianificazione sono determinati dalla seguente formula:

  Lavoro = Durata x Unità

Quando definisci la modalità di pianificazione di un progetto, imposti uno di questi valori che poi non può più essere modificato. Mantenere questo valore come costante pone una priorità su quel valore, che notifica al sistema di non cambiarlo quando cambiano gli altri due valori. La tabella seguente fornisce informazioni sugli impatti della selezione di una modalità specifica.

| **In questa attività**             | **Se rivedi le unità**   | **Se rivedi la durata** | **Se rivedi il lavoro**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Attività unità fisse     | La durata viene ricalcolata. | Il lavoro viene ricalcolato.    | La durata viene ricalcolata. |
| Attività lavoro fisso    | La durata viene ricalcolata. | Le unità vengono ricalcolate.    | La durata viene ricalcolata. |
| Attività durata fissa  | Il lavoro viene ricalcolato.   | Il lavoro viene ricalcolato.    | Le unità vengono ricalcolate.   |

Per ulteriori informazioni sulle implicazioni di una determinata modalità, vedi [Modificare il tipo di attività per una pianificazione più accurata](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). Nell'articolo, il termine **Lavoro** viene utilizzato al posto di **Impegno**.

## <a name="change-the-organizations-scheduling-mode"></a>Modificare la modalità di pianificazione dell'organizzazione

Completa i seguenti passaggi per definire la modalità di pianificazione di un'organizzazione.

1. Vai a **Impostazioni** \> **Generale** \> **Parametri** e quindi seleziona il parametro del progetto. 
2. Nella pagina **Parametri di progetto** seleziona la modalità di pianificazione predefinita per l'organizzazione, quindi definisci la possibilità per il responsabile di progetto di sovrascrivere l'impostazione durante la creazione di un nuovo progetto.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Modificare l'impostazione della modalità di pianificazione in un progetto

Se un'organizzazione consente al responsabile di progetto di sovrascrivere la modalità di pianificazione predefinita, il responsabile di progetto può apportare questa modifica quando crea un nuovo progetto. Tuttavia, dopo che il progetto è stato salvato, la modalità di pianificazione non può più essere modificata.

## <a name="copied-projects"></a>Progetti copiati

Poiché un progetto viene creato quando viene eseguita l'azione di copia progetto, il responsabile di progetto non può impostare la modalità di pianificazione. Il progetto di destinazione sarà sempre predefinito nella modalità definita a livello organizzativo.

## <a name="copied-tasks"></a>Attività copiate

Quando un'attività viene copiata da un progetto a un altro, l'attività eredita la modalità di pianificazione del progetto di destinazione.
