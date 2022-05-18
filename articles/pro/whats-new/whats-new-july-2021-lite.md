---
title: Novità di luglio 2021 - Distribuzione semplice di Project Operations
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di luglio 2021 della distribuzione semplice di Project Operations.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 475ceea3a6c6db9fe63e3950eaca5d9074faa766
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583957"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Novità di luglio 2021 - Distribuzione semplice di Project Operations

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

  - Project Operations in ambiente Dataverse versione 4.12.0.148 o 4.12.0.152.

## <a name="quality-updates"></a>Aggiornamenti di qualità
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
| GeneralE                       | 2376405              | Risolto problema di aggiornamento guidato dall'editore (l'aggiornamento della qualità è disponibile nella versione 4.12.0.152)                                                                                                                     |
