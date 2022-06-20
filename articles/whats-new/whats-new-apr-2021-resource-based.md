---
title: Novità di aprile 2021 - Project Operations per scenari basati su risorse/materiali non stoccati
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di aprile 2021 di Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a060bdc4e4c9f37ec666b1cf4d078986ad1571db
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912429"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di aprile 2021 - Project Operations per scenari basati su risorse/materiali non stoccati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo articolo si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.9.0.221
- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.17

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

In questa release sono incluse le seguenti funzionalità:

- Materiali non stoccati per progetti. Le funzionalità chiave includono:
  - Stima e prezzo dei materiali non stoccati durante il ciclo di vendita di un progetto. Per ulteriori informazioni, vedi [Impostare le tariffe di vendita e costi per i prodotti del catalogo - semplice](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Monitoraggio dell'utilizzo di materiali non stoccati durante la consegna del progetto. Per ulteriori informazioni, vedi [Registrare l'utilizzo di materiale in progetti e attività di progetto](../material/material-usage-log.md).
  - La fatturazione ha utilizzato costi di materiali non stoccati. Per ulteriori informazioni, vedi [Gestire il backlog di fatturazione](../proforma-invoicing/manage-billing-backlog.md).
  - Per informazioni su come configurare questa funzione, vedi [Configurare materiali non stoccati e fatture fornitore in sospeso](../procurement/configure-materials-nonstocked.md)
- Fatturazione basata su attività: aggiunta la possibilità di associare attività di progetto a voci di contratto di progetto, sottoponendole così allo stesso metodo di fatturazione, frequenza di fatturazione e clienti della voce di contratto. Questa associazione garantisce fatturazione, contabilità, stima dei ricavi e riconoscimento accurati affinché siano conformi a questa impostazione nelle attività di progetto.
- Nuove API in Dynamics 365 Dataverse consentono l'esecuzione di operazioni di creazione, aggiornamento ed eliminazione con **Entità di pianificazione**. Per ulteriori informazioni, vedi [Utilizzare le API di pianificazione per eseguire operazioni con le entità di pianificazione](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

Il seguente elenco mostra le mappe a doppia scrittura che sono state modificate o aggiunte nella versione Project Operations di aprile 2021.

| **Mapping entità** | **Versione aggiornata** | **Commenti** |
| --- | --- | --- |
| Valori effettivi dell'integrazione di Project Operations (msdyn\_actuals) | 1.0.0.14 | Mappa modificata per sincronizzare i valori effettivi del progetto materiale. |
| Entità di integrazione di Project Operations per le stime di spesa (msdyn\_estimateslines) | 1.0.0.2 | Aggiunta la sincronizzazione della riga di contratto del progetto alle app per la finanza e le operazioni per il supporto della fatturazione basata sulle attività. |
| Entità di integrazione di Project Operations per le stime delle ore (msdyn\_resourceassignments) | 1.0.0.5 | Aggiunta la sincronizzazione della riga di contratto del progetto alle app per la finanza e le operazioni per il supporto della fatturazione basata sulle attività. |
| Tabella di integrazione Project Operations per le stime dei materiali (msdyn\_estimatelines) | 1.0.0.0 | Nuova mappa della tabella per sincronizzare le stime dei materiali da Dataverse alle app per la finanza e le operazioni. |
| Entità di esportazione fattura fornitore progetto integrazione Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Nuova mappa della tabella per sincronizzare le intestazioni fattura fornitore dalle app per la finanza e le operazioni a Dataverse. |
| Entità di esportazione riga fattura fornitore progetto integrazione Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Nuova mappa della tabella per sincronizzare le righe di fattura fornitore dalle app per la finanza e le operazioni a Dataverse. |

Devi eseguire sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance and Operations. Alcune funzionalità e capacità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Puoi attivare una nuova versione della mappa selezionando **Versioni mappa tabella** e quindi selezionando l'ultima versione e salvando la versione selezionata. Se hai personalizzato una mappa di tabella predefinita, riapplica le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema con l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi di doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations in Dynamics 365 Dataverse

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Determinazione dei prezzi e fatturazione | 2124532 | Il pulsante **Correggi fattura** è visualizzato su una fattura proforma quando l'importo dell'acconto o l'importo dell'acconto applicato è presente nella fattura originale. Il pulsante viene visualizzato solo per ambienti con Finance versione 10.0.19 o successiva. |
| Determinazione dei prezzi e fatturazione | 2224568 | Aggiunta logica per abilitare le personalizzazioni che implicano il richiamo del plug-in di conferma della fattura. |
| Determinazione dei prezzi e fatturazione | 2101098 | Migliorata la logica dei campi predefiniti per la fattura proforma: i valori di **Indirizzo di fatturazione**, **Nome fatturazione** e **Condizioni di pagamento** ora coincidono con il record Cliente contratto di progetto corrispondente. |
| Determinazione dei prezzi e fatturazione | 2021413 | Aggiornati i campi **Costo effettivo** e **Vendite** nell'entità **Attività** per includere i valori di vendita delle spese non fatturate e fatturate delle attività. |
| Determinazione dei prezzi e fatturazione | 2182110 | Quando si copia un contratto di progetto, l'ID voce di contratto viene rigenerato nel contratto di progetto di destinazione per garantirne l'univocità. |
| Gestione delle opportunità | 2186741 | Aggiunte convalide per impedire l'aggiornamento dei campi **Origine** e **Tipo di transazione** nei dettagli della riga di offerta esistente. |
| Gestione delle opportunità | 2191353 | I passaggi fondamentali non devono essere creati in una voce di contratto di tempo e materiale. |
| Gestione delle opportunità | 2216956 | Risolti i problemi con **Aggiorna prezzi**. |
| Pianificazione e rilevamento | 2182979 | Migliorata la funzione di copia del progetto per garantire che le righe di stima delle spese vengano copiate dal progetto originale. |
| Pianificazione e rilevamento | 2184144 | Migliorata la funzione di copia del progetto per garantire che il nome della posizione della risorsa sia copiato dal progetto originale. |
| Pianificazione e rilevamento | 2184799 | Copia del progetto: controllo rafforzato per garantire che la data di inizio stimata non possa essere modificata durante la copia. |
| Pianificazione e rilevamento | 2185134 | Copia del progetto: la data di inizio stimata del progetto di destinazione è impostata sulla data odierna. |
| Pianificazione e rilevamento | 2196373 | Copia del progetto: assicurati che i record Responsabile di progetto e Membro del team non siano duplicati nel team di progetto. |
| Pianificazione e rilevamento | 2211833 | Copia del progetto: le assegnazioni delle risorse vengono copiate dall'attività del progetto di origine nel progetto di destinazione. |
| Pianificazione e rilevamento | 2186541 | Risolti i problemi nella griglia **Stime** durante il raggruppamento per risorsa. |
| Pianificazione e rilevamento | 2166906 | La categoria di transazione di un'attività deve essere copiata nell'entità **Assegnazione risorse**. |
| Gestione risorse | 2125362 | Risolti i problemi con la creazione di un membro del team generico utilizzando un metodo di allocazione basato sulle ore. |
| Ore e spesa | 2113603 | Risolto il problema relativo alla personalizzazione con la rimozione di attributi dalla pagina **Inserimento ore**. Il sistema ora controlla se l'attributo esiste nella pagina prima di accedervi utilizzando uno script. |
| Ore e spesa | 2204377 | I fogli presenze copiati devono essere visualizzati automaticamente quando selezioni **Copia settimana** durante l'inserimento ore. |
| Ore e spesa | 2209059 | Il campo **Stato** può essere modificato per gli inserimenti ore di Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestione progetti e contabilità in Dynamics 365 Finance

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Contabilità e gestione dei progetti | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | L'eliminazione della stima stornata non funziona nella sezione **Periodico**.  |
| Contabilità e gestione dei progetti | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | La funzionalità **Adeguamento contabile** crea un problema con i conti CoGe per i quali l'opzione **Non consentire immissione manuale** è selezionato. |
| Contabilità e gestione dei progetti | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Aggiunta logica di business per elaborare fatture di correzione, incluso l'importo dell'acconto o l'importo dell'acconto applicato. |
| Contabilità e gestione dei progetti | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP: il valore delle vendite che si registra nella fatturazione del progetto interaziendale preleva da un conto imprevisto. |
| Contabilità e gestione dei progetti | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Quando si utilizzano acconti in Project Operations, la modifica del progetto predefinito in un contratto dopo la fatturazione dei pagamenti anticipati causa problemi con le detrazioni in entrata. |
| Contabilità e gestione dei progetti | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | In Project Operations, la rimozione di un progetto da un contratto deve reimpostare il progetto predefinito del contratto, se necessario. |
| Contabilità e gestione dei progetti | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | In Project Operations, linee di spesa errate vengono visualizzate nell'elenco **Aggiungi riga** nella fattura interaziendale. |
| Contabilità e gestione dei progetti | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | In Project Operations, la pagina **Contratto d'acquisto** non è visibile nelle persone giuridiche finanziarie integrate con Project Operations. |
| Contabilità e gestione dei progetti | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | A causa di un errore di integrazione di Dataverse, non è possibile convertire un'offerta acquisita in Project Operations. |
| Contabilità e gestione dei progetti | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** può impostare l'indirizzo di fatturazione della fonte di finanziamento da un cliente diverso.  |
| Contabilità e gestione dei progetti | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | In Project Operations, nessuna dimensione viene selezionata quando si crea una fattura di registrazione per una transazione. |
| Viaggi e spese | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Il saldo dell'anticipo in contanti non viene aggiornato per una nota spese se è approvato e registrato riga per riga. |
| Viaggi e spese | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Le imposte per le note spese interaziendali dettagliate non vengono calcolate correttamente. |
| Viaggi e spese | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Campi aggiuntivi relativi ai progetti sono visualizzati nella pagina **Note spese interaziendali** riprogettata. |
| Viaggi e spese | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Un messaggio di errore non corretto viene visualizzato sulle ricevute di intestazione delle note spese. |
| Viaggi e spese | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Una nota spese viene registrata in modo errato in uno scenario interaziendale se l'IVA viene registrata nella persona giuridica di destinazione. |
| Viaggi e spese | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Le date di presentazione delle note non vengono stampate sulle note spesa approvate. |
| Viaggi e spese | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | I campi **Data di approvazione** e **Data di rifiuto** non vengono compilati dopo l'approvazione di una spesa. |
| Viaggi e spese | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Una richiesta di viaggio creata per un lavoratore può essere utilizzata per la nota spese di un altro lavoratore. |
| Viaggi e spese | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Le categorie di spesa vengono bloccate quando si aggiunge una nuova riga di spesa. |
| Viaggi e spese | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Dettagliare ulteriormente le righe di note spese genera una registrazione incompleta del giustificativo Contabilità fornitori\Contabilità generale e interrompe la funzionalità Esplora origine contabilità poiché **TRVEXPTRANS.SOURCEDOCUMENTLINE** è duplicato. |
| Viaggi e spese | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | I criteri delle richieste di viaggio non funzionano come previsto. |
| Viaggi e spese | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Il nome dell'account fornitore non è visualizzato nelle transazioni di progetto registrate per le note spese. |
| Viaggi e spese | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | In Project Operations, non è possibile approvare il tempo con un'attività di un progetto interaziendale. |
| Viaggi e spese | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | La categoria dei resi con anticipo in contanti non aggiorna i saldi degli anticipi in contanti quando vengono registrati. |
| Viaggi e spese | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Il prezzo di vendita viene calcolato in modo errato nelle note spese create in una valuta estera utilizzando transazioni di carte di credito importate e associate a un progetto. |
| Viaggi e spese | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Rollback dell'entità di dati **TrvRequisitionLine** e dell'indice univoco associato. |
| Viaggi e spese | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Aggiunta strumentazione alla generazione **SOURCEDOCUMENTLINE**. |
| Viaggi e spese | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Un giornale di registrazione secondario non corretto viene visualizzato in uno scenario interaziendale se l'IVA viene registrata nella persona giuridica di destinazione. |
| Viaggi e spese | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | In Project Operations, le stime di spesa non vengono eliminate da Finance quando eliminate da Dataverse. |
| Viaggi e spese | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Quando una categoria di spesa è una categoria non di progetto, le dimensioni finanziarie selezionate nella pagina **Spesa** non vengono copiate nella nota spese. |
