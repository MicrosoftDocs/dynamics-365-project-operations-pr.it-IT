---
title: Novità o modifiche nella versione di aggiornamento 33 di Project Service Automation V3
description: Questo articolo elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 33 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915421"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Novità o modifiche nella versione di aggiornamento 33 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate nella versione di aggiornamento 33 di Project Service Automation V3. Questa versione ha il numero di build V3.10.54.98 ed è generalmente disponibile tramite un aggiornamento automatico di luglio 2021.

## <a name="update-release-33"></a>Rilascio 33 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Ore e spesa**

Sono stati risolti i seguenti problemi:

- Due campi bloccati, **msdyn_description** e **msdyn_externaldescription** sono modificabili dopo l'invio.
- Viene visualizzato un messaggio di errore se viene creata una spesa non correlata a un progetto.
- Quando viene creato un inserimento ore, per impostazione predefinita il ruolo della risorsa viene impostato su un ruolo inattivo.
- Le righe del giornale di registrazione associate a una spesa richiamata ed eliminata non vengono eliminate.
- Nel **Modulo di creazione rapida inserimento ore**, aggiorna la vista **Elenco attività di progetto** per modificare la data visualizzata per impostazione predefinita con la data di inizio dell'attività.
- Quando crei un inserimento ore dalla scheda **Correlato** della risorsa prenotabile, l'inserimento ore viene creato in modo errato per l'utente che ha eseguito l'accesso anziché per la risorsa prenotabile padre.
- Nuovi campi sono stati aggiunti alla finestra di dialogo **Approvazione in blocco MDD**.

**Pianificazione di un progetto**

Sono stati risolti i seguenti problemi:
- Prestazioni lente nella creazione del progetto quando i modelli di ore di lavoro del progetto vengono applicati con calendari complessi.
- Quando la data di inizio è successiva alla data di fine, viene visualizzato un errore sul modello del progetto di copia a causa delle differenze nel componente temporale di ciascun campo.

**Gestione delle risorse**

Sono stati risolti i seguenti problemi:
- Viene utilizzato un parametro errato nella query sull'utilizzo delle risorse e l'XML porta a risultati di filtro errati nella griglia **Utilizzo delle risorse**.
- La **Conferma estensione prenotazioni** mostra una data di fine errata per le prenotazioni.

**Vendite**

Sono stati risolti i seguenti problemi:
- Viene visualizzato un messaggio di errore se viene creato un prezzo di categoria con valori mancanti.
- Viene visualizzato un messaggio di errore se viene creato un passaggio fondamentale della voce di contratto senza una riga d'ordine.
