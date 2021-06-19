---
title: Scenari con più valute (versione 3.x)
description: In questo argomento vengono fornite informazioni sugli scenari con più valute.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 70f27d29c74a82f0307bd0724347960e5755e3a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014796"
---
# <a name="multiple-currency-scenarios"></a>Scenari con più valute

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 comporta due concetti di valute:

- **Valuta transazioni** - La valuta di una transazione. 
- **Valuta di base** - La valuta dell'istanza di Dynamics 365. Questa valuta viene impostata durante il provisioning di Dynamics 365. e non può essere modificata.

Ad esempio, Contoso US ha venduto 100 magliette a un cliente nel Regno Unito al costo di 15 sterline (GBP) l'una. Nella tabella seguente viene mostrato come questa transazione viene registrata nell'entità Prodotto ordine.

| Prodotto | Quantità | Prezzo unitario | Valuta | Importo | Tasso di cambio | Prezzo unitario (base)| Importo (base)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Maglietta | 100      | 15             | GBP      | 1500   | 0.94          | 17.25 €               | 1,725 €       |

La colonna **Valuta** mostra la valuta transazioni, ovvero la valuta utilizzata nella vendita. La colonna **Tasso di cambio** è il tasso di cambio tra la valuta transazioni e la valuta di base. La valuta di base è il dollaro statunitense (USD). Questa valuta di base è stata impostata durante il provisioning dell'istanza di Dynamics 365.
Como mostrato nella tabella, ogni transazione viene registrata nella valuta transazioni e nella valuta di base. Dynamics 365 utilizza il tasso di cambio per calcolare gli importi nella valuta di base.

## <a name="project-service-automation-extensions"></a>Estensioni di Project Service Automation

Dynamics 365 Project Service Automation influenza la valuta transazioni in quanto le transazioni commerciali hanno in genere due aspetti: costi e vendite.

Le entità seguenti sono considerate transazioni commerciali:

- Dettagli riga di offerta
- Dettagli di voce di contratto di progetto
- Riga di stima
- Riga giornale di registrazione
- Dettagli di riga fattura
- Valore effettivo

In ognuna di queste entità, è presente un record che rappresenta l'importo dei costi o quello delle vendite. Come per qualsiasi entità di Dynamics 365 che ha un campo **Importo**, ogni record include gli importi nella valuta transazioni e nella valuta di base. 

PSA espande il concetto di valuta transazioni per i costi e le vendite nei modi seguenti:

- La valuta transazioni costi per le transazioni di tempo viene sempre ottenuta dalla valuta dell'unità organizzativa proprietaria del progetto o che lo gestisce. Questa unità organizzativa è nota come unità contratto.
- La valuta transazioni vendite per le transazioni di tempo e spese viene sempre ottenuta dalla valuta del contratto di progetto.
- La valuta transazioni costi per le spese viene ottenuta dalla valuta in cui la voce di spesa è stata creata.

## <a name="multiple-currency-scenario"></a>Scenario con più valute

In questa sezione viene descritto un progetto di esempio che Contoso UK consegna a un cliente, ovvero Fabrikam, Japan. Di seguito viene riportata la configurazione dello scenario:

1. La Sterlina britannica e lo Yen giapponese sono impostati in **Impostazioni** \> **Gestione aziendale** \> **Valute**. 
2. Viene configurato un account cliente, **Fabrikam - Japan**, e JPY viene utilizzato come valuta dell'account.
3. Viene impostata un'unità organizzativa denominata **Contoso UK** e GBP viene selezionato come valuta.
4. Viene creato un contratto di progetto, dove **Contoso UK** è specificato come unità contratto e **Fabrikam – Japan** come cliente.
5. Vengono create voci di contratto di progetto, in base alle disposizioni di fatturazione per le varie classi di transazioni del progetto, ad esempio fatturazione per il tempo e fatturazione per le spese.
6. Viene creato un progetto dove **Contoso UK** è specificato come unità contratto. Questo progetto viene creato e mappato alle voci di contratto di progetto.


Quando si esegue una stima che utilizza il dettaglio di riga di offerta, il dettaglio di voce di contratto di progetto o la riga di stima della pianificazione, nell'entità vengono sempre creati due record. Un record è per i costi e l'altro per le vendite.

- Per impostazione predefinita, la valuta transazioni del record di costo viene impostata sulla valuta dell'unità contratto del progetto. In questo esempio, la valuta è GBP.
- Per impostazione predefinita, la valuta transazioni del record di vendite viene impostata sulla valuta del contratto di progetto. In questo esempio, la valuta è JPY.

Quando i valori effettivi vengono creati per il tempo utilizzando l'inserimento ore o la riga giornale di registrazione, si ha il comportamento seguente:

- Per impostazione predefinita, la valuta transazioni del record di costo viene impostata sulla valuta dell'unità contratto del progetto.
- Per impostazione predefinita, la valuta transazioni del record di vendite viene impostata sulla valuta del contratto di progetto.

Quando i valori effettivi vengono creati per le spese utilizzando la voce di spesa o la riga giornale di registrazione, si ha il comportamento seguente:

- È possibile registrare l'importo delle spese in qualsiasi valuta. Seleziona la valuta utilizzando il selettore di valuta nella pagina **Voce di spesa** o nella pagina **Riga giornale di registrazione**. Per impostazione predefinita, la valuta transazioni per il record di costo viene impostata sulla valuta della voce di spesa. 
- Per impostazione predefinita, la valuta transazioni per il record di vendite è la valuta del contratto di progetto. Per impostare questa valuta, il sistema dapprima converte l'importo della transazione nella valuta specificata dall'utente come valuta di base. Quindi converte l'importo nella valuta del contratto di progetto. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Calcolare rollup quando i valori effettivi di progetto sono registrati in molteplici valute per le transazioni

Dynamics 365 gestisce automaticamente i rollup di importi in differenti valute. Di seguito è riportato un esempio.

| Classe di transazione | Tipo di transazione| Data   | Risorsa | Categoria di transazione | Quantità | Prezzo unitario | Importo      | Tasso di cambio | Importo in base |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Vendite non fatturate   | 14-Giu | Alfonso  |                      | 8 ore    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Time              | Vendite non fatturate   | 15-Giu | Alfonso  |                      | 8 ore    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Spesa           | Vendite non fatturate   | 16-Giu | Alfonso  | Hotel                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Spesa           | Vendite non fatturate   | 17-Giu | Alfonso  | Noleggio auto           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Per calcolare il valore totale delle vendite non fatturate del progetto, puoi creare un campo di rollup per il campo **Importo** per tutti i valori effettivi delle vendite non fatturate correlati. Il campo di rollup è un costrutto di Dynamics 365 che consente l'utilizzo di formule rapide nei record correlati.


[!INCLUDE[footer-include](../includes/footer-banner.md)]