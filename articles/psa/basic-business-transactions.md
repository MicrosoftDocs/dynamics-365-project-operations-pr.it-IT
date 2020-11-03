---
title: Transazioni commerciali
description: In questo argomento vengono fornite informazioni sulle transazioni commerciali.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d82f5d75de69b32b39c9a55d77287c0719930eb4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078998"
---
# <a name="business-transactions"></a>Transazioni commerciali

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In Dynamics 365 Project Service Automation, *transazione commerciale* è un concetto astratto che non è rappresentato da alcuna entità. Tuttavia, alcuni campi e processi comuni delle entità sono progettati per utilizzare il concetto di transazioni commerciali. Le seguenti entità utilizzano questo concetto:

- Dettagli riga di offerta
- Dettagli voce di contratto
- Righe di stima
- Righe giornale di registrazione
- Valori effettivi

Tra queste entità, Dettagli riga di offerta, Dettagli voce di contratto e Righe di stima sono mappate alla fase di stima nel ciclo di vita del progetto. Le entità Righe giornale di registrazione e Valori effettivi sono mappate alla fase di esecuzione nel ciclo di vita del progetto.

PSA tratta i record in queste cinque entità come transazioni commerciali. La sola distinzione è che i record nelle entità mappate alla fase di stima sono considerati previsioni commerciali, mentre i record nelle entità mappate alla fase di esecuzione sono considerati come fatti commerciali già accaduti.

Per ulteriori informazioni, vedi [Stime](estimates.md) e [Valori effettivi](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Concetti specifici delle transazioni commerciali
I seguenti concetti sono specifici del concetto di transazioni commerciali:

- Tipo di transazione
- Classe di transazione
- Origine transazione
- Connessione della transazione

### <a name="transaction-type"></a>Tipo di transazione

Il tipo di transazione rappresenta il timing e il contesto dell'impatto finanziario su un progetto. È rappresentato da un set di opzioni che ha i seguenti valori supportati in PSA:
- Costo
- Contratto di progetto
- Vendite non fatturate
- Vendite fatturate
- Vendite interorganizzative
- Costo unità gestione risorse

### <a name="transaction-class"></a>Classe di transazione

La classe di transazione rappresenta i differenti tipi di costi sostenuti nei progetti. È rappresentato da un set di opzioni che ha i seguenti valori supportati in PSA:

- Time
- Spesa
- Materiale
- Commissione
- Passaggio fondamentale
- Imposte

Il valore **Passaggio fondamentale** viene in genere utilizzato dalla logica di business per la fatturazione a prezzo fisso in PSA.

### <a name="transaction-origin"></a>Origine transazione

Origine transazione è un'entità in cui è archiviata l'origine di ciascuna transazione aziendale. Man mano che procede l'esecuzione del progetto, ogni transazione aziendale darà origine a un'altra transazione aziendale che, a sua volta, ne creerà un'altra e così via. L'entità Origine transazione è stata progettata per archiviare i dati di ciascuna origine di transazione, così fa facilitare report e tracciabilità. 

### <a name="transaction-connection"></a>Connessione della transazione

Connessione della transazione è un'entità che archivia la relazione tra due transazioni commerciali simili, ad esempio il costo e i valori effettivi di vendita correlati, oppure storni di transazioni attivati dalle attività di fatturazione come la conferma o la correzione delle fatture.

Con l'utilizzo combinato delle entità Origine transazione e Connessione della transazione puoi tenere traccia delle relazioni tra transazioni commerciali e azioni che provocano la creazione di una specifica transazione commerciale.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Esempio: funzionamento di Origine transazione con Connessione della transazione

Nell'esempio seguente viene illustrata l'elaborazione tipica degli inserimenti ore in un ciclo di vita di progetto di PSA.

> ![Elaborare inserimenti ore in un ciclo di vita di Project Service](media/basic-guide-17.png)
 
1. L'invio di un inserimento ore comporta la creazione di due righe di giornale di registrazione: una per il costo e una per le vendite non fatturate.
2. L'eventuale approvazione dell'inserimento ore comporta la creazione di due valori effettivi: uno per il costo e uno per le vendite non fatturate.
3. Quando l'utente crea una fattura di progetto, la transazione di riga fattura viene creata utilizzando i dati del valore effettivo delle vendite non fatturate. 
4. Quando la fattura viene confermata, vengono creati due nuovi valori effettivi: uno storno delle vendite non fatturate e un valore effettivo delle vendite fatturate.

Ognuno di questi eventi genera la creazione di record nelle entità Origine transazione e Connessione delle transazioni per tenere traccia delle relazioni tra questi record creati nei dettagli di inserimenti ore, righe di giornale di registrazione, valori effettivi e righe fattura.

Nella tabella seguente vengono mostrati i record dell'entità Origine transazione per il flusso di lavoro precedente.

| Event                        | Origine                   | Tipo di origine                       | Transazione                       | Tipo di transazione         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Invio inserimento ore        | GUID del record Inserimento ore   | Inserimento ore                        | GUID del record Riga giornale di registrazione   | Riga giornale di registrazione             |
| GUID del record Inserimento ore       | Inserimento ore               | GUID del record Riga giornale di registrazione (vendite)  | Riga giornale di registrazione                      |                          |
| Approvazione tempo                | GUID del record Riga giornale di registrazione | Riga giornale di registrazione                      | GUID del record Vendite non fatturate        | Valore effettivo                   |
| GUID del record Inserimento ore       | Inserimento ore               | GUID del record Vendite non fatturate        | Valore effettivo                            |                          |
| GUID del record Riga giornale di registrazione     | Riga giornale di registrazione             | GUID del record Valore effettivo costo           | Valore effettivo                            |                          |
| GUID del record Inserimento ore       | Inserimento ore               | GUID del record Valore effettivo costo           | Valore effettivo                            |                          |
| Creazione fattura             | GUID del record Inserimento ore   | Inserimento ore                        | GUID della transazione riga fattura     | Transazione riga fattura |
| GUID del record Riga giornale di registrazione     | Riga giornale di registrazione             | GUID della transazione riga fattura     | Transazione riga fattura          |                          |
| Conferma fattura         | GUID della riga fattura        | Riga fattura                      | GUID del record Vendite fatturate          | Valore effettivo                   |
| GUID della fattura                 | Fattura                  | GUID del record Vendite fatturate          | Valore effettivo                            |                          |
| GUID dei dettagli di riga fattura     | Dettagli di riga fattura      | GUID del record Vendite fatturate          | Valore effettivo                            |                          |
| GUID del record Inserimento ore       | Inserimento ore               | GUID del record Vendite fatturate          | Valore effettivo                            |                          |
| GUID del record Riga giornale di registrazione     | Riga giornale di registrazione             | GUID del record Vendite fatturate          | Valore effettivo                            |                          |
| GUID del record Inserimento ore       | Inserimento ore               | GUID dello storno vendite non fatturate      | Valore effettivo                            |                          |
| GUID del record Riga giornale di registrazione     | Riga giornale di registrazione             | GUID dello storno vendite non fatturate      | Valore effettivo                            |                          |
| Correzione bozza della fattura     | GUID dei dettagli di riga fattura precedente             | Transazione riga fattura          | GUID dei dettagli di riga fattura di correzione               | Transazione riga fattura |
| GUILD della riga di fattura precedente                  | Riga fattura             | GUID dei dettagli di riga fattura di correzione               | Transazione riga fattura          |                          |
| GUID della fattura precedente             | Fattura                  | GUID dei dettagli di riga fattura di correzione               | Transazione riga fattura          |                          |
| GUID del record Inserimento ore       | Inserimento ore               | GUID dei dettagli di riga fattura di correzione               | Transazione riga fattura          |                          |
| GUID del record Riga giornale di registrazione     | Riga giornale di registrazione             | GUID dei dettagli di riga fattura di correzione               | Transazione riga fattura          |                          |
| Correzione fattura confermata | GUID dei dettagli di riga fattura precedente             | Transazione riga fattura          | GUID del valore effettivo vendite fatturate stornate | Valore effettivo                   |
| GUILD della riga di fattura precedente                  | Riga fattura             | GUID del valore effettivo vendite fatturate stornate | Valore effettivo                            |                          |
| GUID della fattura precedente             | Fattura                  | GUID del valore effettivo vendite fatturate stornate | Valore effettivo                            |                          |
| GUID del record Inserimento ore       | Inserimento ore               | GUID del valore effettivo vendite fatturate stornate | Valore effettivo                            |                          |
| GUID del record Riga giornale di registrazione     | Riga giornale di registrazione             | GUID del valore effettivo vendite fatturate stornate | Valore effettivo                            |                          |
| GUID dei dettagli di riga fattura precedente                 | Transazione riga fattura | Nuovo GUID del valore effettivo vendite non fatturate    | Valore effettivo                            |                          |
| GUILD della riga di fattura precedente                  | Riga fattura             | Nuovo GUID del valore effettivo vendite non fatturate    | Valore effettivo                            |                          |
| GUID della fattura precedente             | Fattura                  | Nuovo GUID del valore effettivo vendite non fatturate    | Valore effettivo                            |                          |
| GUID del record Inserimento ore       | Inserimento ore               | Nuovo GUID del valore effettivo vendite non fatturate    | Valore effettivo                            |                          |
| GUID del record Riga giornale di registrazione     | Riga giornale di registrazione             | Nuovo GUID del valore effettivo vendite non fatturate    | Valore effettivo                            |                          |
| GUID dei dettagli di riga fattura di correzione          | Transazione riga fattura | Nuovo GUID del valore effettivo vendite non fatturate    | Valore effettivo                            |                          |
| GUID della riga di fattura di correzione           | Riga fattura             | Nuovo GUID del valore effettivo vendite non fatturate    | Valore effettivo                            |                          |
| GUID della fattura di correzione      | Fattura                  | Nuovo GUID del valore effettivo vendite non fatturate    | Valore effettivo                            |                          |

Nella tabella seguente sono riportati i record dell'entità Origine transazione per il flusso di lavoro precedente.

| Event                          | Transazione 1                 | Ruolo transazione 1 | Tipo di transazione 1           | Transazione 2                | Ruolo transazione 2 | Tipo di transazione 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Invio inserimento ore          | GUID della riga giornale di registrazione (vendite)     | Vendite non fatturate     | msdyn_journalline            | GUID della riga giornale di registrazione (costo)     | Costo               | msdyn_journalline  |
| Approvazione tempo                  | GUID del valore effettivo non fatturato (vendite)  | Vendite non fatturate     | msdyn_actual                 | GUID del valore effettivo costo (costo)       | Costo               | msdyn_actual       |
| Creazione fattura               | GUID dei dettagli di riga fattura      | Vendite fatturate       | msdyn_invoicelinetransaction | GUID del valore effettivo vendite non fatturate   | Vendite non fatturate     | msdyn_actual       |
| Conferma fattura           | GUID del valore effettivo storno         | Storno          | msdyn_actual                 | GUID delle vendite non fatturate originale | Originale           | msdyn_actual       |
| GUID delle vendite fatturate              | Vendite fatturate                  | msdyn_actual       | GUID del valore effettivo vendite non fatturate   | Vendite non fatturate               | msdyn_actual       |                    |
| Correzione bozza della fattura       | GUID della transazione riga fattura | Sostituzione          | msdyn_invoicelinetransaction | GUID delle vendite fatturate            | Originale           | msdyn_actual       |
| Conferma correzione fattura     | GUID dello storno vendite fatturate    | Storno          | msdyn_actual                 | GUID delle vendite fatturate            | Originale           | msdyn_actual       |
| Nuovo GUID del valore effettivo vendite non fatturate | Sostituzione                     | msdyn_actual       | GUID delle vendite fatturate            | Originale                     | msdyn_actual       |                    |
