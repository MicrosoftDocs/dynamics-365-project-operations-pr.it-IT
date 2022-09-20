---
title: Creare fatture fornitore
description: Questo articolo descrive il concetto di fatture fornitore e spiega come crearle in Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475421"
---
# <a name="create-vendor-invoices"></a>Creare fatture fornitore

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Per utilizzare la funzionalità descritta in questo articolo, è necessario abilitare la funzionalità **Abilita l'elaborazione degli effettivi di conto lavoro con Project Operations per scenari basati sulle risorse** nell'area di lavoro **Gestione delle funzionalità**.

La fatturazione fornitore in Microsoft Dynamics 365 Project Operations può essere utilizzata per registrare i costi delle consegne di servizi e/o materiali in un progetto completato da fornitori.

Quando i servizi e/o i materiali vengono assegnati in conto lavoro a un fornitore, un conto lavoro rappresenta l'accordo contrattuale con quel fornitore. Quando il fornitore fornisce i servizi o i materiali vengono ricevuti e utilizzati per le attività di progetto, i costi vengono registrati nel progetto. Il venditore invia quindi periodicamente le fatture. Queste fatture vengono verificate e abbinate ai costi registrati nel progetto. Al termine del processo di verifica, la fattura fornitore viene confermata e rilasciata per il pagamento.

## <a name="scenarios-for-use"></a>Scenari per l'utilizzo

Le fatture fornitore in Project Operations possono essere utilizzate per supportare due scenari distinti:

- I clienti utilizzano le esperienze di conto lavoro complete.
- I clienti non utilizzano le esperienze di conto lavoro complete ma desiderano avere una visione unificata dei costi sui progetti in Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>I clienti utilizzano le esperienze di conto lavoro complete

Le esperienze di fattura fornitore forniscono un modo per verificare e abbinare gli inserimenti ore, l'utilizzo del materiale e le voci di spesa che fanno riferimento a componenti in conto lavoro con le righe di fattura fornitore. Questo processo può essere utilizzato per verificare l'accuratezza delle righe di fattura fornitore. Dopo che il processo di verifica è stato completato e la fattura fornitore è stata confermata, il sistema inverte i valori effettivi registrati dai registri di utilizzo di inserimento ore, spese e materiali approvati e creerà nuovi costi effettivi utilizzando le righe di fattura fornitore.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>I clienti non utilizzano le esperienze di conto lavoro complete ma desiderano avere una visione unificata dei costi sui progetti in Project Operations

Se stai monitorando il processo di conto lavoro in un sistema di terze parti, puoi registrare i costi da tale sistema di terze parti in Project Operations creando fatture fornitore che non fanno riferimento ai conti lavoro. In questo modo, i project manager possono avere una visione unica e unificata di tutti i costi di un determinato progetto.

## <a name="create-vendor-invoices-in-project-operations"></a>Creare fatture fornitore in Project Operations

Le fatture fornitore vengono create in Dynamics 365 Finance, utilizzando il modulo **Contabilità fornitori**. Non puoi creare fatture fornitore direttamente in Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Impostare la verifica di fatture fornitore

Se la fattura fornitore è intesa per un subappalto in Dataverse, è necessario abilitare il parametro **Verifica manuale dei PM necessaria**. L'impostazione dell'opzione determina se la fattura fornitore deve essere confermata automaticamente in Dataverse o se richiede una conferma manuale. L'intestazione di ogni fattura fornitore di progetto include un'opzione con lo stesso nome. Per impostazione predefinita, l'opzione nell'intestazione di tutte le fatture fornitore del progetto è impostata sul valore impostato qui. Tuttavia, puoi aggiornare il valore come richiesto nell'intestazione delle singole fatture fornitore.

Se l'opzione è impostata su **Sì**, la fattura fornitore creata in Finance e sincronizzata con Dataverse ha stato **Bozza**. La fattura deve quindi essere convalidata e verificata dal responsabile di progetto e confermata prima di essere elaborata e registrata nel progetto specifico e nei conti contabili in Finance.

Se l'opzione è impostata su **No**, la fattura fornitore viene automaticamente confermata. Non sono richieste altre azioni.

Per configurare la verifica delle fatture fornitore, procedi come segue.

1. In Finance, vai a **Gestione progetti e contabilità** \> **Imposta** \> **Parametri Gestione progetti e contabilità**.
1. Nella scheda **Finanziario**, imposta l'opzione **Verifica manuale dei PM necessaria** su **Sì** se i criteri aziendali richiedono la verifica delle fatture dei fornitori del subappaltatore. Se la verifica da parte del responsabile di progetto non è richiesta in Dataverse, lascia set di opzioni su **No**. Per impostazione predefinita, l'impostazione verrà utilizzata nella pagina **Fattura fornitore in sospeso**.

> [!NOTE]
> Fatture fornitore create per i subappalti in Dataverse possono essere elaborate correttamente solo se l'opzione **Verifica manuale dei PM necessaria** è impostata su **Sì**. I costi effettivi di tempo, materiale e spese creati dai subappaltatori possono essere abbinati manualmente alle righe fattura fornitore dal responsabile di progetto solo se questa opzione è impostata su **Sì**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Creare un account di integrazione approvvigionamento per le fatture fornitore

Quando una fattura fornitore viene registrata in Finance for Project Operations – Ambiente integrato (non stock), i dati finanziari vengono registrati nell'account di integrazione Approvvigionamento. Il sistema genera gli effettivi in Dataverse per la fattura registrata. Questi effettivi vengono registrati in Finance utilizzando il giornale di registrazione di integrazione del progetto. La registrazione del giornale di integrazione di Project registra il costo effettivo e inverte l'account di integrazione Approvvigionamento.

Per impostare un account di integrazione Approvvigionamento per le fatture fornitore, segui questi passaggi.

1. In Finance, vai a **Gestione progetti e contabilità** \> **Imposta** \> **Parametri Gestione progetti e contabilità**.
1. Nella scheda **Project operations su Dynamics 365 Customer Engagement**, seleziona **Materiali** \> **Conto di integrazione approvvigionamento**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Creare e registrare fatture fornitori per conto lavoro

Quando un addetto alla contabilità fornitori riceve una fattura dal terzista, in Finance viene creata una nuova fattura.

1. In Finance, vai a **Contabilità fornitori** \> **Fatture** \> **Fatture fornitore in sospeso**.
1. Nel **riquadro Azioni**, seleziona **Nuovo** per creare una fattura fornitore.
1. Nell'intestazione della fattura, nel campo **Conto fattura**, seleziona **Terzista**.
1. Seleziona la data della fattura.
1. Nella scheda **Intestazione**, imposta l'opzione **Verifica manuale dei PM necessaria** su **Sì**. L'impostazione predefinita di questa opzione deriva dalla pagina **Parametri Gestione progetti e contabilità**. Tuttavia, può essere modificato a livello di fattura fornitore.
1. Nella Scheda dettaglio **Riga fattura**, seleziona **Aggiungi riga** per creare una riga di fattura fornitore.
1. Seleziona la categoria di approvvigionamento creata per le righe di conto lavoro e immetti il prezzo unitario, l'unità di misura e la quantità.
1. Nella sezione Righe fattura fornitore, nella scheda **Project**, seleziona il progetto rispetto al quale il terzista condivide la fattura di subappalto.
1. Seleziona la categoria di progetto. Può essere di qualsiasi tipo **Elemento**, **Spesa**, **Materiali** oppure **Ore**.
1. Seleziona il ruolo solo se la categoria di progetto selezionata è del tipo **Ora**.
1. Seleziona **Registra** per registrare la fattura fornitore.

In alternativa, puoi creare una fattura fornitore andando su **Contabilità fornitori** \> **Fatture** \> **Fatture fornitore aperte** e selezionando **Nuovo**.

Quando la fattura fornitore viene registrata, diventa disponibile in Dataverse per la verifica e l'elaborazione del responsabile di progetto.

## <a name="vendor-invoice-processing-in-dataverse"></a>Elaborazione delle fatture fornitore in Dataverse

Nella fattura fornitore creata in Dataverse, alcuni valori di campo provengono dalla fattura fornitore registrata in Finance. Gli altri valori sono valori predefiniti che provengono dal conto lavoro.

I seguenti campi e relativi record verranno copiati dal conto lavoro nell'intestazione della fattura fornitore:

- Valuta
- Unità contratto
- Condizioni di pagamento

Nelle righe della fattura fornitore, Project Operations utilizza i seguenti valori di campo per immettere il riferimento di riga di conto lavoro e conto lavoro predefinito:

- Classe di transazione
- Ruolo
- Categoria di transazione
- Campi di prodotto
- Project
- Attività

> [!NOTE]
> Le righe di conto lavoro a prezzo fisso non sono supportate in Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
