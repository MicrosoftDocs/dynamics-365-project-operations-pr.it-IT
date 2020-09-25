---
title: Modifiche a entità, controlli e interfaccia utente (Project Service Automation 3.x)
description: In questo argomento vengono descritte le modifiche a Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9f8828c6-541c-4945-8c99-5785118e191d
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 56aa0bb8272b886bcd15dadd0f74fff3bc43e26b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752675"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Modifiche a entità, controlli e interfaccia utente (Project Service Automation 3.x)
In seguito al rilascio di Microsoft Dynamics Project Service Automation (PSA) 3.x, molte modifiche sono state apportate a entità, controlli, viste e interfaccia utente. Il presente argomento fornisce informazioni su queste importanti modifiche.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Relazioni padre-figlio per le entità Documento di vendita, Riga documento di vendita, Dettagli riga documento di vendita
Nelle versioni di Dynamics 365 Project Service Automation (PSA) rilasciate prima della versione 3.0, alcune delle relazioni tra le entità Documento di vendita, Riga documento di vendita, Dettagli riga documento di vendita sono state implementate mediante campi di tipo stringa con una rappresentazione di stringa del GUID dell'entità correlata. Ciò era dovuto ai limiti della piattaforma che richiedevano codice personalizzato significativo sul lato server e client della soluzione affinché tali relazioni funzionassero come le relazioni di entità di Dynamics CRM tipiche e i campi di tipo stringa funzionassero come campi di ricerca.

PSA 3.0 è stato aggiornato per utilizzare le nuove relazioni tra le entità Documento di vendita e Riga documento di vendita.

Poiché i campi di ricerca possono ora essere utilizzati per indicare riferimenti a entità, i campi contenenti il valore di stringa del GUID dell'entità correlata nelle versioni precedenti non sono più necessari e quindi sono stati deprecati. Anche il codice personalizzato sul lato client e server che gestisce le relazioni definite dai campi di tipo stringa legacy è stato deprecato.

### <a name="entity-schema-changes"></a>Modifiche dello schema di entità
Nella tabella seguente viene fornito un elenco uno-a-uno dei campi di tipo stringa deprecati e dei nuovi campi di ricerca per le entità. 

 Entità |   Campo deprecato (stringa) | Nuovo campo (Ricerca)
--- | --- | ---
invoicedetail (Riga fattura) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Valore effettivo) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Pianificazione fatturazione voce di contratto di progetto) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Passaggio fondamentale voce di contratto di progetto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Fatto) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Dettagli di riga fattura) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Riga giornale di registrazione) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Categoria di risorsa voce di contratto di progetto) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Dettagli di voce di contratto di progetto) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Categoria di transazione voce di contratto di progetto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Classificazione di transazione voce di contratto di progetto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Pianificazione fatturazione riga di offerta) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Categoria di risorsa riga di offerta) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Passaggio fondamentale riga di offerta) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Dettagli riga di offerta) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Categoria di transazione riga di offerta) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Classificazione di transazione riga di offerta) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Riga ordine) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Viste e controlli personalizzati deprecati
I seguenti controlli e viste personalizzati e i relativi elementi sono stati deprecati.

- Vista Esigibilità.
- Controlli della griglia personalizzati per visualizzare dettagli di riga di offerta nella pagina **Informazioni sul progetto** per la riga di offerta.
- Controlli della griglia personalizzati per visualizzare dettagli di voce di contratto di progetto nella pagina **Informazioni sul progetto** per la riga di ordine di vendita.

> [!NOTE]
> Per un elenco completo delle risorse deprecate, vedi [Risorse Web deprecate in Project Service Automation 3.x](../developer-guides/web-resources-deprecated-v3.x.md).

## <a name="unified-client-interface-app-module"></a>Modulo app dell'interfaccia UCI
Con l'introduzione dei moduli app dell'interfaccia UCI, le voci della mappa del sito di PSA sono state rimosse dal sistema.  
La funzionalità relativa alla commutazione dei moduli per le entità Opportunità, Offerta, Ordine e Fattura è stata deprecata in quanto non più necessaria poiché il modulo app UCI include solo le versioni PSA dei moduli.  

Le risorse Web seguenti sono state deprecate:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Per un elenco completo delle risorse deprecate, vedi [Risorse Web deprecate in Project Service Automation 3.x](../developer-guides/web-resources-deprecated-v3.x.md).

