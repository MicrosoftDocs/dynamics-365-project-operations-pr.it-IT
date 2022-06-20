---
title: Note sulle approvazioni per gli sviluppatori
description: Questo articolo fornisce ulteriori informazioni per gli sviluppatori sull'utilizzo delle approvazioni.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924757"
---
# <a name="developer-notes-for-approvals"></a>Note sulle approvazioni per gli sviluppatori

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations include la logica di convalida che garantisce la corretta transizione dei record attraverso le fasi di approvazione. Le corrette transizioni dei record garantiscono: 

  - Tutte le righe di supporto vengono create nelle tabelle correlate, come giornali di registrazione e valori effettivi.
  - Il responsabile approvazione di progetto è contrassegnato come **Responsabile approvazione di progetto** nel progetto prima di procedere.


[!INCLUDE[footer-include](../includes/footer-banner.md)]