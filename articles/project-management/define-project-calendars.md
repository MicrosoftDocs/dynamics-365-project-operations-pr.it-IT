---
title: Definire i calendari del progetto
description: Questo argomento fornisce informazioni sull'utilizzo di un calendario di progetto per tenere traccia della pianificazione del progetto.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131663"
---
# <a name="define-project-calendars"></a>Definire i calendari del progetto

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Per creare una pianificazione di progetto, creai un modello di calendario di progetto che definisce il numero di ore lavorative giornaliere e le chiusure aziendali. Per creare un modello di calendario di progetto, associ un modello di lavoro al campo **Modello calendario** del progetto. Segui questi passaggi per creare un modello di lavoro.

1. Seleziona **Risorse** nel riquadro di spostamento di sinistra. 
2. Nella pagina elenco **Risorse**, apri un record utente, quindi seleziona **Mostra ore lavorative**.

  > [!NOTE]
  > Verifica che le finestre pop-up siano consentite nella pagina del browser. Ciò consente di visualizzare le ore lavorative impostate per la risorsa.
  
3. Nella scheda **Vista mensile**, seleziona **Configura**. Viene visualizzato un elenco con tre opzioni: 

  - Nuova pianificazione settimanale
  - Pianificazione lavorativa per un giorno
  - Indisponibilità

4. Seleziona **Nuova pianificazione settimanale** e quindi imposta le opzioni per questa pianificazione delle risorse. Puoi impostare una pianificazione settimanale ricorrente, parametri orari giornalieri, chiusure aziendali e altro ancora.
5. Imposta l'intervallo di date, seleziona **Salva** e quindi seleziona **Chiudi**. 
6. Torna alla pagina elenco **Risorse** e seleziona la risorsa per la quale imposti le ore lavorative. 
7. Seleziona **Imposta calendario come** per impostare il modello di lavoro. 
8. Nella finestra di dialogo **Modello di lavoro**, immetti un nome per il modello di lavoro e quindi seleziona **Applica**. 

Ora puoi associare il modello di lavoro a un modello di calendario di progetto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]