---
title: Integrazione della fattura fornitore
description: Questo argomento fornisce informazioni sull'Integrazione della fattura fornitore in Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d4f1b0ad94b71dc4adc5b2b3423340c5fdb171eb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002275"
---
# <a name="vendor-invoice-integration"></a>Integrazione della fattura fornitore

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

L'approvvigionamento relativo al progetto in Dynamics 365 Project Operations può essere registrato andando in **Contabilità fornitori** > **Fatture** > **Fatture fornitore in sospeso** e utilizzando un documento di fattura fornitore in sospeso. Per ulteriori informazioni, vedi [Acquistare materiali non stoccati usando una fattura fornitore in sospeso](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Prima di utilizzare la funzionalità descritta in questo argomento, esamina e applica le configurazioni richieste. Per ulteriori informazioni, vedi [Abilitare materiali non stoccati e fatture fornitore in sospeso](../procurement/configure-materials-nonstocked.md).

In Project Operations, le fatture fornitore relative al progetto vengono registrate utilizzando regole di registrazione speciali:

- Il costo relativo al progetto (inclusa l'imposta non recuperabile) non viene registrato immediatamente nel conto dei costi del progetto nella contabilità generale. Il costo viene invece registrato nel **Conto di integrazione approvvigionamento**. Questo conto è configurato in **Gestione progetti e contabilità** > **Configura** > **Parametri di gestione progetti e contabilità** nella scheda **Project Operations in Dynamics 365 Customer Engagement**.
- La doppia scrittura sincronizza i dettagli della fattura fornitore con Microsoft Dataverse utilizzando le seguenti mappe d tabella:

     - **Entità di esportazione fattura fornitore progetto integrazione Project Operations (msdyn_projectvendorinvoices)**: Questa mappa di tabella sincronizza le informazioni di intestazione della fattura fornitore. Vengono sincronizzate solo le fatture fornitore con almeno una riga che contiene un ID progetto Dataverse.
     - **Entità di esportazione riga fattura fornitore progetto integrazione Project Operations (msdyn_projectvendorinvoicelines)**: Questa mappa di tabella sincronizza le informazioni di riga della fattura fornitore. Vengono sincronizzate solo le righe che contengono un ID progetto in Dataverse.

     > [!NOTE]
     > I dettagli della fattura fornitore in Dataverse non sono modificabili.

Registro secondario delle imposte, registro secondario del fornitore e altre registrazioni finanziarie vengono registrati come applicabili in Dynamics 365 Finance quando viene registrata la fattura fornitore.

![Integrazione della fattura fornitore](media/DW7VendorInvoice.png)

Quando i record vengono scritti in un'entità **Fattura fornitore** in Dataverse, inizia un processo automatizzato di approvazione dei record. Se necessario, lo stato del processo di approvazione automatizzato può essere rivisto in Dataverse andando in **Impostazioni avanzate** > **Sistema** > **Processi di sistema**. Dopo che l'approvazione è stata completata, il sistema crea i record della classe di transazione materiale nell'entità **Valori effettivi**.

I valori effettivi relativi al materiale vengono quindi elaborati utilizzando la mappa della tabella a doppia scrittura, **Valori effettivi dell'integrazione di Project Operations (msdyn_actuals)**. Per ulteriori informazioni, vedi [Stime e valori effettivi di progetto](resource-dual-write-estimates-actuals.md).

Il processo periodico, **Importa da gestione temporanea** crea righe di giornale di registrazione di integrazione Project Operations correlate alla fattura fornitore. L'impostazione predefinita del conto di contropartita è il conto di integrazione dell'approvvigionamento. Quando viene registrato il giornale di registrazione di integrazione, il saldo del conto viene compensato per la transazione della fattura fornitore e l'importo della riga viene spostato nel conto dei costi di progetto. Le transazioni di contabilità secondaria del progetto vengono create anche per la fatturazione a valle e per il riconoscimento dei ricavi.
