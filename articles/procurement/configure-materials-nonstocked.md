---
title: Configurare materiali non stoccati e fatture fornitore in sospeso
description: Questo argomento spiega come abilitare i materiali non stoccati e le fatture fornitore in sospeso.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 41191384c688c3b77d08a0e7990ddf0d9a48545c
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293052"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Configurare materiali non stoccati e fatture fornitore in sospeso

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

## <a name="minimum-version-requirement"></a>Requisito versione minima

L'uso di materiali non stoccati e fatture fornitore in sospeso per scenari basati su risorse/non stoccate Dynamics 365 Project Operations richiede le seguenti versioni:

Soluzioni Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 o versione successiva
- Soluzione di orchestrazione delle applicazioni a doppia scrittura - 2.2.2.23 o versione successiva

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) o versione successiva. Assicurati che il tuo ambiente Finance sia aggiornato e che tutti gli aggiornamenti di qualità vengano applicati per soddisfare i requisiti minimi di versione.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Esegui mappe a doppia scrittura per l'integrazione dei materiali non stoccati e delle fatture fornitori

Questa sezione fornisce informazioni sulle mappe specifiche richieste per i materiali non stoccati e le fatture fornitori. Verifica che le mappe dei prerequisiti elencate nell'argomento [Provisioning di un nuovo ambiente](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) siano in esecuzione nel tuo ambiente.

1. Vai a Lifecycle Services (LCS), vai al tuo progetto LCS e vai alla pagina **Dettagli ambiente**.
2. Nella sezione **Informazioni ambiente Common Data Service**, seleziona **Collegamento a CDS per app**. Dopo aver selezionato il collegamento, verrai reindirizzato all'elenco delle entità nei mapping.
3. Assicurati che le seguenti mappe siano in esecuzione. Se non sono in esecuzione, avviale e assicurati di includere tutte le mappe delle tabelle correlate.

    - CDS ha rilasciato prodotti distinti (prodotti)
    - Fornitori v2 (msdyn_vendors)
    - Tabella Project Operations per le stime dei materiali (msdyn_estimatelines)
    - Entità di esportazione fattura fornitore progetto integrazione Project Operations (msdyn_projectvendorinvoices)
    - Entità di esportazione riga fattura fornitore progetto integrazione Project Operations (msdyn_projectvendorinvoicelines)
    - Valori effettivi dell'integrazione di Project Operations (msdyn_actuals). Assicurati di eseguire la versione della mappa 1.0.0.14 o successiva. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Puoi attivare una nuova versione della mappa selezionando **Versione mappa tabella** e quindi salvando la versione selezionata.

Se stai utilizzando dati demo standard, potresti anche dover interrompere e riavviare le seguenti mappe di entità con la sincronizzazione iniziale:
  - Giorni di pagamento CDS V2 (msdyn_paymentdays)
  - Calendario dei pagamenti (msdyn_paymentschedules)
  - Condizioni di pagamento (msdyn_paymentterms)
  - Gruppi di fornitori (msdyn_vendorgroups)
  - Unità (uom)

> [!NOTE]
> La sincronizzazione iniziale per gruppi di fornitori e unità potrebbe non riuscire per alcuni record nel set di dati demo esistente. Puoi ignorare gli errori in quanto non ti impediranno di utilizzare i dati demo con Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Configurare i prerequisiti in Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Attivare il flusso di lavoro per creare account in base all'entità fornitore

La soluzione Dual Write Orchestration fornisce [l'integrazione dei dati master dei fornitori](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Come prerequisito per questa funzione, i dati del fornitore devono essere creati nell'entità **Account**. Attiva un processo di flusso di lavoro modello per creare fornitori nella tabella **Account** come descritto in [Passare da una finestra di progettazione del fornitore all'altra](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Impostare i prodotti da creare come attivi

I materiali non stoccati devono essere configurati come **Prodotti rilasciati** in Finance. La soluzione Dual Write Orchestration fornisce un'[integrazione dei prodotti rilasciati nel catalogo prodotti Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping) predefinita. Per impostazione predefinita, i prodotti di Finance vengono sincronizzati con Dataverse in uno stato di bozza. Per sincronizzare il prodotto in uno stato attivo in modo che possa essere usato direttamente nei documenti di utilizzo del materiale o nelle fatture del fornitore in sospeso, vai a **Sistema** > **Amministrazione** > **Amministrazione di sistema** > **Impostazioni di sistema** e nella scheda **Vendite**, imposta **Crea prodotti in stato attivo** su **Sì**.

## <a name="configure-prerequisites-in-finance"></a>Configurare i prerequisiti in Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Abilitare il tasto funzione per le fatture fornitore in sospeso

Completa i seguenti passaggi per abilitare la funzionalità per aggiungere i dettagli del progetto nelle righe di fattura fornitore in sospeso.

1. In Finance, vai all'area di lavoro **Gestione funzionalità**.
2. Nell'elenco delle funzionalità, trova la funzionalità **Abilita fatture fornitore in sospeso in Project Operations per scenari basati su risorse/non stoccate** e seleziona **Abilita**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definire gruppi di categorie e categorie di progetto per gli articoli

Configura almeno un gruppo di categorie per tipo di transazione **Articolo** e almeno una categoria di progetto che utilizza questo gruppo. Per ulteriori informazioni, vedi [Configurare le categorie di progetto](../project-accounting/configure-project-categories.md#category-groups).

Rivedi i profili dei costi e dei ricavi del progetto e configura l'impostazione della registrazione contabile per le transazioni degli articoli. Per ulteriori informazioni, vedi [Configurare la contabilità per i progetti fatturabili](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Configurare un prodotto fuori catalogo

In Project Operations, è possibile registrare le stime e l'utilizzo dei materiali per i prodotti di catalogo configurati nel catalogo prodotti rilasciato e per i prodotti fuori catalogo. L'utilizzo di prodotti fuori catalogo richiede un unico prodotto rilasciato configurato in Finance per questo scopo. Completa i seguenti passaggi per configurare un prodotto fuori catalogo. Ripeti questi passaggi in ogni persona giuridica che utilizza Project Operations per scenari di risorse/non stoccate.

1. In Finance, vai a **Gestione informazioni sui prodotti** > **Prodotti** > **Prodotti rilasciati** e seleziona **Nuovo**.
2. Nel campo **Tipo di prodotto** seleziona **Articolo** e nel campo **Sottotipo di prodotto** seleziona **Prodotto**.
3. Immetti il numero del prodotto (WRITEIN) e il nome del prodotto (prodotto a doppia scrittura).
4. Seleziona il gruppo di modelli di articolo. Assicurati che il gruppo di modelli di articolo selezionato abbia il campo **Criteri inventario Prodotto stoccato** impostato su **Falso**.
5. Seleziona i valori nei campi **Gruppo di articoli**, **Gruppo di dimensioni di archiviazione**, e **Gruppo di dimensioni di rilevamento**. Usa **Dimensione di immagazzinamento** per **Sito** solo, e nel campo **Dimensioni di tracciabilità**, seleziona **Nessuna**.
6. Seleziona i valori nel campo **Unità di inventario**, **Unità di acquisto**, e **Unità di vendita**, quindi salva le modifiche.
7. Nella scheda **Piano** imposta le impostazioni dell'ordine predefinite e nella scheda **Inventario** imposta il sito e il magazzino predefiniti.
8. Vai a **Gestione progetti e contabilità** > **Configura** > **parametri di gestione progetti e contabili** e apri **Project Operations su Dynamics 365 Dataverse**. 
9. Nella scheda **Materiali** nel campo **Prodotto fuori catalogo** seleziona il prodotto che hai creato.
10. Nel tuo ambiente Dataverse, nella mappa del sito, apri l'entità **Prodotti** e trova il record del prodotto fuori catalogo. 
11. Apri i dettagli del record e imposta lo stato del prodotto su **Ritirato**. Questo stato del prodotto impedisce a chiunque di utilizzare accidentalmente questo record direttamente nelle stime dei materiali e nei documenti di utilizzo.

### <a name="set-up-a-procurement-integration-account"></a>Creare un account di integrazione approvvigionamento

L'account di integrazione approvvigionamento viene utilizzato come conto di compensazione quando si registra una fattura fornitore in sospeso con righe attribuite a un progetto.

Quando il sistema registra una fattura fornitore in sospeso, questo conto viene utilizzato per l'importo del costo del progetto. I dettagli della fattura fornitore vengono elaborati in Dataverse e viene creato un effettivo progetto corrispondente. Le informazioni dall'effettivo progetto vengono aggiunte al giornale di registrazione integrazione Project Operations. Quando registri il giornale di registrazione integrazione, l'importo viene cancellato dal conto di integrazione dell'approvvigionamento e registrato nel costo del progetto.

1. Per impostare il conto di integrazione approvvigionamento vai a **Gestione progetti e contabilità** > **Configura** > **parametri di gestione progetti e contabili** e apri **Project Operations su Dynamics 365 Dataverse**. 
2. Seleziona la scheda **Materiali** e seleziona un valore nel campo **Conto di integrazione approvvigionamento**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Impostare i valori predefiniti della categoria di progetto per un articolo

1. In Finance vai a **Gestione progetti e contabilità** > **Configura** > **parametri di gestione progetti e contabili** e apri **Project Operations su Dynamics 365 Dataverse**. 
2. Nella scheda **Valori predefiniti della categoria di progetto** nel campo **Articolo** seleziona un valore. Questa categoria di progetto viene utilizzata per le transazioni di materiale se la categoria di progetto non è stata impostata nel record dei valori effettivi del progetto.
