---
title: Creare transazioni interaziendali
description: Questo argomento fornisce informazioni su come creare transazioni interaziendali.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 88e5658c9087fdb19adce1c23bc5cad0ad0fa434
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599979"
---
# <a name="create-intercompany-transactions"></a>Creare transazioni interaziendali

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Le transazioni interaziendali sono transazioni di tempi e costi di un contratto di progetto che appartengono a una società o un'unità organizzativa, mentre le risorse del contratto di progetto fanno parte di una società o unità organizzativa diversa.

Quando una transazione interaziendale viene approvata, vengono create le seguenti transazioni effettive

| **Tipo di transazione** | **Listino prezzi applicato** | **Valuta delle transazioni** |
| --- | --- | --- |
| Costo | Listino prezzi di costo unitario contrattuale | Valuta sulla riga del prezzo |
| Vendite non fatturate. Vengono create solo per i valori effettivi associati a una riga di contratto con il tipo di fatturazione, l'ora e il materiale. | Listino prezzi delle vendite del progetto del contratto | Valuta del contratto |
| Costo unità gestione risorse | Listino prezzi di costo unitario della gestione risorse | Valuta sulla riga del prezzo |
| Vendite unità interorganizzative | Listino prezzi di costo unitario contrattuale | Valuta sulla riga del prezzo |

Il costo, il costo unitario delle risorse e il prezzo delle transazioni di vendita delle unità interorganizzative e la valuta è basata su **unità organizzative**. Questo è importante da ricordare quando si decide come strutturare le società e le unità organizzative nella propria implementazione.

Quando si creano record di opportunità, preventivi, contratti di progetto e progetti, il sistema verifica che la valuta dell'unità contraente corrisponda alla valuta contabile della società contraente. Quando non sono la stessa cosa, questi record non possono essere creati. La valuta dell'unità organizzativa è definita in Dynamics 365 Project Operations andando a **Dataverse** > **Impostazioni** > **Unità organizzative**. La valuta contabile di una società viene definita in Dynamics 365 Finance andando in **Contabilità generale** > **Impostazioni contabilità generale** > **Contabilità generale**. La valuta è sincronizzata con il tuo ambiente Dataverse utilizzando la mappa Ledgers Dual Write.

Il sistema crea il costo unitario delle risorse e le vendite delle unità interorganizzative tra le unità organizzative nelle seguenti situazioni:

  - Quando l'unità che fornisce risorse è diversa dall'unità contratto
  - Quando la società di gestione risorse è diversa dalla società contraente

Tuttavia, solo le transazioni che hanno una società di gestione risorse diversa dalla società contratto verranno trasferite all'ambiente Dynamics 365 Finance per la contabilità aggiuntiva.

La contabilità dei valori effettivi del progetto viene registrata nel giornale di registrazione di integrazione Project Operations in Finance. Il sistema crea le seguenti righe del giornale di registrazione.

| **Tipo di transazione** | **Persona giuridica** | **Crea la transazione del progetto durante la registrazione** | **Valori predefiniti delle dimensioni finanziarie** | **Fatturazione della fascia IVA predefinita e gruppo IVA articolo di fatturazione** |
| --- | --- | --- | --- | --- |
| Costo | Non viene aggiunto al giornale di integrazione | N/A | N/A | N/A |
| Vendite non fatturate | Il giornale di integrazione della persona giuridica richiedente | Sì | Project | **Fatturazione della fascia IVA**: basata sul **cliente del contratto** <br/> **Gruppo IVA articolo di fatturazione**: dalla categoria di progetto della persona giuridica corrente nella riga del giornale di registrazione |
| Costo unità gestione risorse | Giornale di integrazione della persona giuridica che effettua la concessione | No | Cliente interaziendale | **Fatturazione della fascia IVA**: basata sul **cliente interaziendale** <br/> **Gruppo IVA articolo di fatturazione**: dalla categoria di progetto della persona giuridica corrente nella riga del giornale di registrazione |
| Vendite interorganizzative | Giornale di integrazione della persona giuridica che effettua la concessione | No | Cliente interaziendale | **Fatturazione della fascia IVA**: basata sul **cliente interaziendale** <br/> **Gruppo IVA articolo di fatturazione**: dalla categoria di progetto della persona giuridica corrente nella riga del giornale di registrazione |

### <a name="example-intercompany-transactions"></a>Esempio: transazioni interaziendali

Molly Clark, sviluppatore impiegato in GBPM registra 10 ore di lavoro contro un progetto USPM Adventure Works, che è approvato dal responsabile del progetto. Il costo dello sviluppatore in GBPM è di 88 GBP l'ora. GBPM fatturerà 120 USD a USPM per ciascuna ora dello sviluppatore. USPM fatturerà al cliente Adventure Works, 200 USD per il lavoro svolto dalla risorsa GBPM. Per ulteriori informazioni, vedere [Configurare la fatturazione interaziendale](configure-intercompany-invoicing.md).

1. In Project Operations, vai a **Risorse** e seleziona **Marcella Trentini** dall'elenco. Nella scheda **Pianificazione**, nel campo **Azienda**, selezionare **GBPM**.
2. Vai a **Vendite** > **Clienti** e seleziona **Nuovo** per creare un nuovo record del cliente per Adventure Works.
    1. Impostare l'azienda su **USPM**.
    2. Impostare **Tipo di relazione** su **Cliente**.
    3. Selezionare **Gruppo di clienti 10 - Domestico**.
    4. Impostare la valuta su **USD**.
    5. Salvare il record.
3. Vai a **Vendite** > **Contratti di progetto** e crea un nuovo contratto di progetto per Adventure Works.
    1. Imposta la società proprietaria su **USPM** e l'unità appaltante su **Contoso Robotics US**.
    2. Seleziona Adventure Works come cliente.
    3. Seleziona un listino prezzi del prodotto e salva il record.
    4. Nella scheda **Voci di contratto**, crea una nuova voce di contratto. Imposta un nome e seleziona **Tempistica e materiali** come metodo di fatturazione.
    5. Crea un nuovo progetto e associalo a questa voce di contratto.
4. Accedi come risorsa, **Marcella Trentini**. Vai a **Progetti** > **Inserimenti ore** e crea una voce di tempistica per il progetto Adventure Works.
5. Accedi come responsabile di progetto. Vai a **Progetti** > **Approvazioni** e approva la transazione di registrazione dell'ora registrata da Marcella Trentini.
6. Passa al progetto Adventure Works e seleziona **Elementi correlati** > **Valori effettivi**. Vengono create le seguenti transazioni effettive.

| **Tipo di transazione** | **Prezzo** | **Valuta delle transazioni** | **Importo** |
| --- | --- | --- | --- |
| Costo | 120 | USD | 1200 |
| Vendite non fatturate | 200 | USD | 2000 |
| Costo unità gestione risorse | 88 | GBP | 880 |
| Vendite unità interorganizzative | 120 | USD | 1200 |

7. Accedi come contabile USPM. Apri l'istanza Finance di Project Operations e seleziona la società **USPM**. 
8. Vai a **Contabilità e gestione dei progetti** > **Periodico** > **Project Operations su Customer Engagement** > **Importa da staging** e seleziona l'esecuzione del processo periodico. Questo processo periodico riempirà il giornale di integrazione di Project Operations.
9. Vai a **Gestione del progetto e contabilità** > **Giornali** > **Giornale di integrazione di Project Operations** e rivedere le righe del giornale di registrazione. Il sistema crea le seguenti righe.

    | **Tipo di transazione** | **Prezzo** | **Valuta delle transazioni** | **Importo** |
    | --- | --- | --- | --- |
    | Vendite non fatturate | 200 | USD | 2000 |

    Se il sistema è impostato per accumulare ricavi per questo progetto, viene registrato quanto segue:

    - Debito: Progetto - Valore delle vendite WIP 200 USD
    - Credito: Progetto - Ricavi maturati 200 USD

    Questa vendita non fatturata è ora pronta per la fatturazione. La fattura per il cliente Adventure Works può essere registrata finanziariamente quando necessario.

10. Accedi come contabile **GBPM**. Apri l'istanza Finance di Project Operations e apri l'azienda **GBPM**. 
11. Vai a **Gestione progetti e contabilità** > **Periodico** > **Integrazione di Project Operations** > **Importa dalla tabella di gestione temporanea** ed esegui il processo periodico per compilare il giornale di integrazione di Project Operations.
12. Vai a **Gestione del progetto e contabilità** > **Giornali** > **Giornale di integrazione di Project Operations** e rivedere le righe. Il sistema crea le seguenti righe.

    | **Tipo di transazione** | **Prezzo** | **Valuta delle transazioni** | **Importo** |
    | --- | --- | --- | --- |
    | Costo unità gestione risorse | 88 | GBP | 880 |
    | Vendite unità interorganizzative | 120 | USD | 1200 |

    La registrazione di questi record genera le seguenti transazioni giustificative:

    - Debito: costo del progetto 88 GBP
    - Credito: Allocazione retribuzioni 88 GBP

    Se il sistema è impostato per accumulare ricavi interaziendali, viene registrato quanto segue:

    - Debito: Progetto - Valore delle vendite WIP 120 USD
    - Credito: Progetto - Ricavi maturati 120 USD

    Il sistema è ora pronto per creare una fattura cliente interaziendale.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
