---
title: Novità o modifiche nella versione di aggiornamento 27 di Project Service Automation V3
description: Questo articolo elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 27 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6c8f4f736f0659f9b6db25f4685ef1278c45d034
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912935"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Novità o modifiche nella versione di aggiornamento 27 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate nella versione di aggiornamento 27 di Project Service Automation V3. Questa versione ha il numero di build V3.10.45.98 ed è generalmente disponibile tramite un aggiornamento automatico in gennaio 2021.

## <a name="update-release-27"></a>Rilascio 27 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Generali**

Sono stati risolti i seguenti problemi:

- I log generati dai plug-in in Project Service Automation non sono stati impostati per l'eliminazione automatica.
- L'aggiornamento automatico non riesce perché la soluzione Project Service Automation contiene un NavBarArea null legacy e un elemento titolo.

**Ore e spesa**

Sono stati risolti i seguenti problemi:

- La griglia **Inserimento orario** visualizza dati errati per il comportamento della data **Indipendente da fuso orario**.
- La griglia **Inserimento orario** crea gli orari errati per il comportamento della data **Indipendente da fuso orario**.
- La ricerca delle attività non è limitata al progetto selezionato nella pagina **Modifica inserimento ore**.
- L'approvazione del tempo per voci di orario non di progetto blocca il sistema durante la ricerca di un responsabile approvazione del progetto.
- Le voci corrette sui valori effettivi visualizzano un messaggio di errore non corretto.
- Quando un'attività contiene un valore nullo per il costo effettivo e i totali del progetto vengono aggiornati, si verifica il seguente errore, "Chiave specificata non presente nel dizionario".
- In casi specifici, i filtri **Raggruppa per** nella scheda **Stima progetto** non mostra le stime di spesa.
- L'intervallo **Ora legale** non è corretto per gli inserimenti ore.

**Gestione progetti**

Sono stati risolti i seguenti problemi:

- Miglioramenti alla memorizzazione nella cache, che migliorano le prestazioni relative al caricamento della pagina **Progetto**.
- Regola aziendale obsoleta che impedisce il completamento delle attività del progetto.
- I profili del componente aggiuntivo di Microsoft Project non rispettano il calendario del componente aggiuntivo con conseguenti requisiti di risorse non corretti.
- La creazione di progetti da modelli imposta in modo errato le date di assegnazione e impedisce la possibilità di generare requisiti di risorse.
- L'utente non può accedere alle opzioni **Categoria**, **Descrizione**, **Stato** utilizzando la tastiera.
- I valori di vendita effettivi del progetto non includono i valori di vendita di commissioni e materiali.
- L'aggregazione delle vendite effettive e del costo effettivo viene eseguita in modo errato con tassi di cambio diversi.
- La descrizione nel **Modello orario di lavoro predefinito** è fuorviante.
- Il rientro di un'attività non rimuove **Categoria** nell'interfaccia utente fino a quando non viene aggiornato.
- La mancata convalida per garantire che lo spostamento di un progetto oltre la sua data di fine non sia consentito.

**Sales**

Sono stati risolti i seguenti problemi:

- Un'eccezione di riferimento nulla viene generata su una riga di offerta del progetto perché **Importa da stima di progetto** è visibile quando un progetto non è stato selezionato.
- Il seguente errore, "Riferimento a un oggetto non impostato su un'istanza di un oggetto" si verifica quando si chiude un'offerta come **Acquisita**.
- Lo stato della rettifica non è impostato durante l'effettivo annullamento durante lo scollegamento di un progetto da una riga di contratto.
- Quando Dynamics 365 Field Service e Project Service Automation sono entrambi installati, le opzioni **Blocca prezzi** e **Usa prezzo corrente** non vengono visualizzate contemporaneamente nella pagina **Fattura**.
- Per la lingua giapponese, c'è una traduzione incoerente con altre pagine basate sul calendario.
- **Attiva** e **Disattiva** sono stati rimossi dalle entità **Associazione listino prezzi** in Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
