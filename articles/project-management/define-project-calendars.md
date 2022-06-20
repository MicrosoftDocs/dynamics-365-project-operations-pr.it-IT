---
title: Definire i calendari del progetto
description: In questo articolo vengono fornite informazioni su come applicare un modello di calendario a un progetto per tenere traccia della pianificazione del progetto.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e195cdb0dc5acc2ea816fadce40811675a855de2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933543"
---
# <a name="define-project-calendars"></a>Definire i calendari del progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Per creare e gestire un progetto, è necessario applicare un modello di calendario al progetto. Il modello di calendario definisce i seguenti attributi del progetto:

- Orario lavorative, inclusa l'ora di inizio e di fine
- Giorni lavorativi
- Eccezioni di calendario come giorni non lavorativi

Il modello di calendario applicato a un progetto è una copia del modello di calendario definito nelle impostazioni dell'organizzazione.

> [!NOTE]
> Se modifichi il modello di calendario, tali modifiche non si propagano alle ore lavorative del progetto. Per modificare le ore lavorative del progetto, è necessario applicare un nuovo modello.

Per creare un modello di calendario per la tua organizzazione, ci sono due requisiti chiave:

- Definisci le ore lavorative desiderate del modello utilizzando una risorsa prenotabile nuova o esistente.
- Crea un nuovo modello di calendario e associa il modello alla risorsa prenotabile.

**Definisci le ore lavorative del modello**

1. Seleziona **Risorse** \> **Risorse**.
2. Crea una nuova risorsa a cui fare riferimento nel modello di calendario o seleziona una risorsa esistente.
3. Seleziona la scheda **Ore lavorative** della risorsa e completa le istruzioni in [Impostare le ore lavorative per una risorsa](/dynamics365/field-service/set-work-hours-resource) per configurare le regole del calendario.

**Creare un nuovo modello di calendario**

1. Vai a **Impostazioni** \> **Modello di calendario**.
2. Seleziona **Nuovo** e inserisci un nome, una descrizione e una risorsa modello.

> [!NOTE]
> Quando si fa riferimento a una risorsa in un modello di calendario, una copia del calendario della risorsa viene associata al modello di calendario. Se le ore lavorative del modello copiato cambiano, tali modifiche non verranno propagate al modello di calendario.

Ora puoi associare il modello di lavoro a un modello di calendario di progetto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

