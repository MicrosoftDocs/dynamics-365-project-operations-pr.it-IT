---
title: Novità dell'aggiornamento rilascio 15 di Project Service Automation V3
description: Questo argomento fornisce informazioni sulle novità dell'aggiornamento rilascio 15 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752643"
---
# <a name="project-service-automation-v3-update-release-15"></a>Aggiornamento rilascio 15 di Project Service Automation V3

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Dynamics 365 Project Service Automation (PSA). Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per aggiornare a questa versione, visitare l'interfaccia di amministrazione di Dynamics 365 online e andare alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 15 di PSA V3. Questa versione ha il numero di build V3.10.5.28 ed è generalmente disponibile tramite un aggiornamento automatico in gennaio 2020.

## <a name="update-release-15"></a>Rilascio 15 dell'aggiornamento 

### <a name="enhancements"></a>Miglioramenti

- Gestione progetti

### <a name="bug-fixes"></a>Correzioni di bug

- Tempo e spesa

  - Risolto: Aggiungere la gestione degli errori al caricamento nella visualizzazione di riconciliazione.
  - Risolto: Hub risorse di progetto: Rinominare **Importo** per ridurre l'ambiguità.
  - Risolto: Modificare la visualizzazione **Copia colonne inserimenti ore** per includere il tipo.
  - Risolto: La modifica della durata per l'inserimento ore nella visualizzazione griglia utilizzando i numeri decimali comporta errori sconosciuti per alcuni numeri.

- Gestione progetti

  - Risolto: Il menu a discesa per **Utilizza in visualizzazione tracciabilità** ora si espande in base alla larghezza delle opzioni.
  - Risolto: Durante la gestione dei progetti nel fuso orario +13, i calcoli delle attività possono visualizzare risultati imprecisi.
  - Risolto: **Ora di fine membro del team** è stato corretto quando si utilizza un calendario a 24 ore.
  - Risolto: Riattivato il **processo aziendale** nel modulo principale **msdyn_project**.
  - Risolto: Il calcolo delle assegnazioni non ignora più un giorno.
  - Risolto: un nuovo banner di notifica è stato aggiunto al modulo del progetto quando il fuso orario differisce tra utente e progetto.

- Sales

  - Risolto: la ricerca della categoria di stima delle spese può essere utilizzata per filtrare i duplicati.
  - Risolto: il codice in **PluginDomain.ExecuteInTryCatchBlock(..)** non nasconde più l'origine dell'eccezione.
  - Risolto: non viene più visualizzato un messaggio di errore **Ricerca progetto** nel modulo **Riga di offerta** quando ci sono più di 1000 progetti.
  - Risolto: la griglia **Stime** per le stime della manodopera e delle spese ora mostra il simbolo di valuta corretto.
  - Risolto: dopo che un'organizzazione aggiorna PSA dall'aggiornamento rilascio 14 all'aggiornamento rilascio 15, la scheda **Pianifica** non viene più visualizzata come vuota sul modulo **Progetto**.
