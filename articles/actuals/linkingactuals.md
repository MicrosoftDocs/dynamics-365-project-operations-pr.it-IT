---
title: "Origini della transazione: collegare i valori effettivi all'origine"
description: Questo articolo spiega come il concetto di origini delle transazioni viene utilizzato per collegare i valori effettivi ai record di origine originali, come registri di inserimento ore, spese o utilizzo del materiale.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921307"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Origini della transazione: collegare i valori effettivi all'origine

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

I record di origine delle transazioni vengono creati per collegare i valori effettivi alla loro origine, ad esempio inserimenti ore, voci di spesa, registri di utilizzo del materiale e fatture di progetto.

Nell'esempio seguente viene illustrata l'elaborazione tipica degli inserimenti ore in un ciclo di vita di progetto di Project Operations.

> ![Elaborazione di inserimenti ore in Project Operations.](media/basic-guide-17.png)
 
1. L'invio di un inserimento ore comporta la creazione di due righe di giornale di registrazione: una per il costo e una per le vendite non fatturate.
2. L'eventuale approvazione dell'inserimento ore comporta la creazione di due valori effettivi: uno per il costo e uno per le vendite non fatturate.
3. Quando l'utente crea una fattura di progetto, la transazione di riga fattura viene creata utilizzando i dati del valore effettivo delle vendite non fatturate.
4. Quando la fattura viene confermata, vengono creati due nuovi valori effettivi: uno storno delle vendite non fatturate e un valore effettivo delle vendite fatturate.

Ogni evento in questo flusso di lavoro di elaborazione attiva la creazione di record nell'entità Origine transazione per tenere traccia delle relazioni tra questi record creati nei dettagli di inserimenti ore, righe di giornale di registrazione, valori effettivi e righe fattura.

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
| GUID dei dettagli di riga fattura     | Dettaglio di riga fattura      | GUID del record Vendite fatturate          | Valore effettivo                            |                          |
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
| GUID della fattura di correzione      | Fattura                  | Nuovo GUID del valore effettivo vendite non fatturate    | Effettiva                            |                          |


L'illustrazione seguente mostra i collegamenti che vengono creati tra i valori effettivi e le loro origini in vari eventi utilizzando l'esempio degli inserimenti ore in Project Operations.

> ![Come i valori effettivi sono collegati ai record di origine in Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
