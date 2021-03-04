---
title: Creare fatture interaziendali per clienti e fornitori
description: Questo argomento fornisce informazioni su come creare fatture fornitori e clienti interaziendali.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595496"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Creare fatture interaziendali per clienti e fornitori

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Un contabile di progetto in una persona giuridica che effettua la concessione crea una fattura cliente interaziendale per i costi del progetto che vengono trasferiti all'entità richiedente. Dopo che la fattura cliente interaziendale è stata approvata e registrata, la persona giuridica che effettua la concessione invia la fattura interaziendale alla persona giuridica richiedente.

Il contabile di progetto per la persona giuridica che effettua la concessione può impostare un processo batch per generare fatture interaziendali su base ricorrente. Il contabile di progetto specifica i criteri, ad esempio progetti specifici, per creare fatture interaziendali in un batch.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Creare manualmente una fattura cliente interaziendale per le transazioni di progetto 

Utilizzare questa procedura per creare manualmente una fattura cliente interaziendale per le transazioni di progetto. Cerca le ore registrate dai lavoratori sui progetti nelle persone giuridiche che effettuano la concessione e le spese sostenute dalla persona giuridica per conto delle persone giuridiche richiedenti. È possibile eseguire la ricerca per nome della persona giuridica, numero di contratto di progetto, numero di progetto, intervallo di date o qualsiasi combinazione di queste opzioni. Nei risultati della ricerca selezionare le transazioni da aggiungere a una fattura interaziendale.

1. In Dynamics 365 Finance, vai a **Contabilità e gestione dei progetti** > **Fatture di progetto** > **Fatture cliente interaziendale**. Nella pagina dell'elenco **Fatture clienti interaziendali**, nel riquadro azioni selezionare **Nuovo**.
2. Nella pagina **Crea fattura interaziendale**, nel campo **Entità legale**, selezionare una persona giuridica richiedente.
3. Facoltativo: immettere un contratto di progetto specifico e un numero di progetto.
4. Restringere la ricerca selezionando un intervallo di date. Immettere date specifiche nei campi **Data d'inizio** e **Data di fine**. Nei risultati della ricerca vengono visualizzate solo le transazioni interaziendali registrate in questo intervallo di date.
5. Imposta **Parametro della riga di giornale di registrazione avanzata del progetto** su **Sì** e seleziona **Ricerca**.
6. Nei risultati della ricerca, seleziona le transazioni da includere nella proposta di fatturazione interaziendale, quindi seleziona **OK**.
7. Nella pagina **Fattura cliente interaziendale**, vengono visualizzate le transazioni del progetto interaziendale selezionate dai risultati della ricerca. Per modificare le transazioni prima di inviare la fattura alla persona giuridica richiedente, effettuare le seguenti operazioni:
  
    1. Aprire la pagina **Crea proposta di fattura**. Seleziona ulteriori transazioni interaziendali per la fattura corrente, quindi seleziona **Aggiungi riga**.
    2. Per rimuovere una riga, selezionarla, quindi selezionare **Rimuovi**.
    3. Visualizza commenti, motivi, dimensioni finanziarie e altre informazioni su una selezionata nella scheda dettaglio **Righe fattura**.
    
8. Per registrare la fattura cliente interaziendale, nel riquadro azioni, seleziona **Registra**.

> [!NOTE]
> Se la tua organizzazione richiede che le fatture interaziendali vengano riviste prima di essere registrate, un amministratore di sistema potrebbe impostare un flusso di lavoro per le fatture interaziendali. Se un flusso di lavoro non è impostato per le fatture interaziendali, è possibile registrare la fattura interaziendale.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Crea un processo batch per le fatture interaziendali

Puoi creare più fatture interaziendali contemporaneamente per tutte le persone giuridiche che effettuano la concessione. Utilizzando la funzionalità di ricerca, è possibile, ad esempio, cercare tutte le transazioni registrate da lavoratori in prestito e correlate a progetti gestiti da altre persone giuridiche. Quindi, per ciascuna persona giuridica che richiedente, è possibile creare una fattura interaziendale per le transazioni fornite nei risultati della ricerca.

1. Vai a **Contabilità e gestione dei progetti** > **Periodico** > **Fatture progetto** > **Crea fatture interaziendali per clienti**.
2. Nella pagina **Crea fatture cliente interaziendali**, nel campo **Azienda**, selezionare una persona giuridica da fatturare. Se non si seleziona una società, tutte le transazioni che soddisfano i criteri di ricerca vengono visualizzate per tutte le persone giuridiche che effettuano la concessione.
3. In **Crea una fattura per**, seleziona se creare una fattura per transazioni interaziendali basate su un progetto o su una persona giuridica richiedente.
4. Facoltativo: per selezionare un progetto specifico e un contratto di progetto per cui creare fatture interaziendali, fare clic su **Seleziona**. Nella pagina **Richiesta di informazioni**, nel campo **Criteri**, seleziona il contratto di progetto, il numero di progetto o entrambi, quindi seleziona **OK**.
5. Nella scheda **Batch**, imposta un processo batch per creare fatture interaziendali su base ricorrente. Per ulteriori informazioni, vedi [Invia un processo di elaborazione batch da un modulo](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Per registrare le fatture interaziendali, nel riquadro azioni, seleziona **Registra**.

> [!NOTE]
> Se la tua organizzazione richiede che le fatture interaziendali vengano riviste prima di essere registrate, un amministratore di sistema potrebbe impostare un flusso di lavoro per le fatture interaziendali. Se un flusso di lavoro non è impostato per le fatture interaziendali, è possibile registrare le fatture interaziendali.

## <a name="post-the-intercompany-vendor-invoice"></a>Registrare la fattura fornitore interaziendale

Un contabile di progetto nella persona giuridica richiedente può rivedere le fatture fornitore interaziendali in sospeso quando viene registrata la fattura cliente interaziendale corrispondente. In Finance, nella persona giuridica richiedente, vai a **Contabilità fornitori** > **Fatture** > **Fattura fornitore in sospeso**. Il numero della fattura in sospeso corrisponderà al numero della fattura del cliente interaziendale. Verifica che la fattura sia corretta, quindi registra la fattura. La registrazione di una fattura fornitore interaziendale crea un registro secondario del progetto e una transazione di contabilità generale che riflette i costi di transazione nella persona giuridica debitrice.


[!INCLUDE[footer-include](../includes/footer-banner.md)]