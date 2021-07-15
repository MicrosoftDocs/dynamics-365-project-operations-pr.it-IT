---
title: Novità di luglio 2021 - Project Operations per scenari di risorse/materiali non stoccati
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di luglio 2021 di Project Operations per scenari di risorse/materiali non stoccati.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5dbf9c7158ce7d9e568e270791e7e7aaf8ce731d
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433523"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di luglio 2021 - Project Operations per scenari di risorse/materiali non stoccati

*Si applica a: Project Operations per scenari basati su risorse/materiali non stoccati*

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

   - Project Operations in ambiente Microsoft Dataverse versione 4.12.0.148.
   - Gestione progetti e contabilità in ambiente Dynamics 365 Finance versione 10.0.20.

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

In questa release sono incluse le seguenti funzionalità:

- Possibilità per gli amministratori di visualizzare i registri PSS e i registri di set di operazioni dal menu delle impostazioni. I log vengono conservati per 90 giorni.

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

Non sono disponibili aggiornamenti per le mappe a doppia scrittura di Project Operations in questa versione.

Per un elenco corrente e le versioni delle mappe a doppia scrittura di Project Operations, vedi [Versioni della mappa a doppia scrittura di Project Operations](../environment/resource-dual-write-maps.md).

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità e capacità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella pagina **Doppia scrittura** nella colonna **Versione**. Attiva una nuova versione della mappa selezionando **Versioni mappa della tabella**, selezionando la versione più recente, quindi salvando la versione selezionata. Se hai personalizzato una mappa di tabella predefinita, riapplica le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema con le colonne della tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi di scrittura doppia.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Area funzionalità**              | **Numero di riferimento** | **Aggiornamento di qualità**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prezzi e fatturazione           | 2224046              | Il campo **Classe di transazione** è modificabile nella scheda **Dettagli riga offerta**, ma è bloccato se stai lavorando nella pagina **Dettagli riga offerta**.                                                                     |
| Prezzi e fatturazione           | 2224400              | L'azione **Chiudi offerta come acquisita** non riesce quando un'offerta non ha passaggi fondamentali di data.                                                                                                                                    |
| Prezzi e fatturazione           | 2234089              | Quando inserisci manualmente una descrizione del prodotto, viene cancellata dopo aver inserito una quantità per una stima del materiale.                                                                                                                         |
| Prezzi e fatturazione           | 2234100              | La griglia **Impostazione fatturazione attività** non include la colonna **Materiale** e il valore nella scheda **Fatturazione attività** del progetto.                                                                                                       |
| Prezzi e fatturazione           | 2277409              | L'ID prodotto non è disponibile nei dettagli della riga di contratto per una riga di tipo di materiale.                                                                                                                                        |
| Prezzi e fatturazione           | 2281728              | La creazione di una riga di contratto rivaluta inutilmente i valori effettivi causando aumenti significativi del volume di dati, che influiscono sulle prestazioni.                                                                                |
| Prezzi e fatturazione           | 2298668              | Le righe del giornale di registrazione associate a una spesa richiamata ed eliminata non vengono rimosse.                                                                                                                                     |
| Prezzi e fatturazione           | 2300192              | Quando più utenti modificano una fattura, è possibile creare un nuovo dettaglio riga fattura su una fattura confermata.                                                                                   |
| Prezzi e fatturazione           | 2301569              | Le fatture non possono essere corrette se una ritenuta di importo pari a \$0 è stata applicata.                                                                                                                                        |
| Prezzi e fatturazione           | 2307965              | Viene visualizzato un errore se viene creato un prezzo di categoria con valori mancanti.                                                                                                                           |
| Prezzi e fatturazione           | 2326870              | Si verifica un errore in **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** se **producttypecode** è null.                                                                            |
| Prezzi e fatturazione           | 2332732              | Viene visualizzato un errore se viene creato un passaggio fondamentale della voce di contratto senza una riga d'ordine.                                                                                                                |
| Pianificazione e rilevamento dei progetti | 2181094              | L'API di pianificazione del progetto ora supporta i registri PSS e i registri di set di operazioni che vengono archiviati per 90 giorni.                                                                                                                  |
| Pianificazione e rilevamento dei progetti | 2254201              | L'etichetta **Modalità di pianificazione** viene aggiornata con dettagli che descrivono la logica predefinita.                                                                                                                                      |
| Pianificazione e rilevamento dei progetti | 2300252              | La cache delle risposte **openProject** viene aggiornata e include il proprietario del token nella chiave della cache, **URL di base**, e **URL del segmento** così che **URL richiesta** può sempre essere ricreato se **URL di base** cambia. |
| Pianificazione e rilevamento dei progetti | 2301312              | **msdyn_membershipstatus** è stato rimosso dalla visualizzazione **Membro del team di progetto**.                                                                                                                                        |
| Pianificazione e rilevamento dei progetti | 2302759              | I prodotti vengono recuperati inutilmente nelle schede **Assegnazione delle risorse**, **Stime**, e **Stime di spesa**.                                                                                                        |
| Pianificazione e rilevamento dei progetti | 2308050              | **CopyProject** non riesce con l'errore "Impossibile ottenere il token per dialogare con il servizio remoto".                                                                                                                           |
| Pianificazione e rilevamento dei progetti | 2322650              | La visualizzazione **Elenco delle attività di progetto** è stata aggiornata per visualizzare la data dell'attività per impostazione predefinita.                                                                                                            |
| Pianificazione e rilevamento dei progetti | 2327266              | **CopyProject** genera l'errore "Chiave non trovata nel dizionario" durante la copia delle stime.                                                                                                      |
| Pianificazione e rilevamento dei progetti | 2328123              | **CopyProject** genera l'errore "Impossibile ottenere il token per dialogare con il servizio remoto".                                                                                                                          |
| Pianificazione e rilevamento dei progetti | 2336258              | **CopyProject** copia erroneamente i nomi delle posizioni delle risorse.                                                                                                                                                 |
| Prezzi e fatturazione           | 2224476              | Il campo **Risorsa prenotabile** non è impostato correttamente sull'utente che ha effettuato l'accesso nella pagina **Utilizzo del materiale**.                                                                                                            |
| Gestione risorse           | 2277249              | Si verifica un errore quando viene aggiornato un requisito di risorse non basato sul progetto.                                                                                                            |
| Gestione risorse           | 2323869              | L'utilizzo delle risorse non riconosce correttamente le risorse filtrate.                                                                                                                                             |
| Ore e spesa              | 2176538              | Gli operatori di filtro non corretti vengono applicati al controllo **Inserimento ore**.                                                                                                                                                   |
| Ore e spesa              | 2177462              | L'eliminazione di un inserimento ore nella griglia non aggiorna lo stato dei pulsanti **Invia**, **Richiama**, **Elimina**, e **Modifica voce** come previsto.                                                                                        |
| Ore e spesa              | 2299985              | **TimeEntriesImportFromResourceAssignment** non mantiene l'ora di inizio/fine dai contorni di assegnazione.                                                                                                  |
| Ore e spesa              | 2318426              | Dopo aver inviato un inserimento ore, i campi bloccati possono ancora essere modificati.                                                                                                                                   |
| Ore e spesa              | 2323749              | Si verifica un errore quando viene creata una spesa dalla scheda **Correlato** di una risorsa prenotabile.                                                                                                      |
| Ore e spesa              | 2327678              | Quando crei un inserimento ore dalla scheda **Correlato** di una risorsa prenotabile, la risorsa padre non viene passata al controllo dell'inserimento ore.                                                                            |
| Generali                       | 2296857              | Monitoraggio dello stato di avanzamento per lavori di lunga durata.                                                                                                                                                                        |
| Generali                       | 2253682              | La soluzione doppia scrittura di Project Operations non deve essere installata quando il core doppia scrittura è installato in un ambiente senza la soluzione di orchestrazione doppia scrittura.                                                |
| Generali                       | 2316420              | Il provisioning di base di Project Service non riesce se la business unit dell'utente dell'applicazione viene modificata.                                                                                                                     |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Contabilità e gestione dei progetti in Dynamics 365 Finance

| Area funzionalità                      | Numero di riferimento | Aggiornamento di qualità                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Contabilità e gestione dei progetti | 4620267          | Impossibile personalizzare i moduli per aggiungere un campo **Scopo** alle pagina **Transazione registrata del progetto**, **Creazione proposta fattura**, e **Proposta di fattura**.                                                                                                                                                                                         |
| Contabilità e gestione dei progetti | 4613449          | Quando si seleziona un ID contratto di progetto in Finance, l'ambiente integrato Project Operations apre la pagina per creare un nuovo record, invece della pagina per i contratti di progetto già creati.                                                                                                                                           |
| Contabilità e gestione dei progetti | 4614445          | Nella distribuzione dello scenario integrato Project Operations, non è possibile modificare il campo **Fascia IVA articolo** della proposta di fattura importata dallo staging. La fascia IVA articolo deve essere modificabile per una proposta di fattura aperta di tutti i tipi di transazione, inclusi conti, ore, spese, commissioni e articoli. |
| Contabilità e gestione dei progetti |                  | Impossibile registrare una proposta di fattura risultante da una correzione della transazione temporale negativa.                                                                                                                                                                                                                                              |
| Contabilità e gestione dei progetti |                  | Le righe della proposta di fattura sono duplicate a causa di più processi periodici **Importa da staging** in esecuzione contemporaneamente.                                                                                                                                                                                                                |

