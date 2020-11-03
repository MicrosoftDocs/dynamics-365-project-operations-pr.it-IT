---
title: Aggiungere nuovi moduli di entità personalizzate (Project Service Automation 2.x)
description: In questo argomento vengono fornite informazioni su come aggiungere moduli di entità personalizzate per opportunità, offerte, ordini o fatture in Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079070"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Aggiungere nuovi moduli di entità personalizzate (Project Service Automation 2.x)

## <a name="type-field"></a>Campo Tipo 

Dynamics 365 Project Service Automation utilizza il campo **Tipo** ( **msdyn\_ordertype** ) delle entità Opportunità, Offerta, Ordine e Fattura per distinguere le versioni **basate su lavoro** di queste entità dalle versioni **basate su articolo** e **basate su servizio**. Le versioni basate su lavoro di queste entità sono gestite da PSA. Molte delle regole di business sul lato client e sul lato server della soluzione dipendono dal campo **Tipo**. Pertanto, è importante che il campo sia inizializzato con un valore corretto alla creazione delle entità. Un valore errato può causare comportamenti inappropriati e alcune regole di business potrebbero non essere eseguite correttamente.

## <a name="automatic-form-switching"></a>Commutazione automatica dei moduli

Per evitare un potenziale danneggiamento dei dati e comportamenti imprevisti causati dall'inizializzazione e dalla modifica non corrette di record delle entità di vendita, ora PSA include la logica per la commutazione automatica dei moduli nei moduli predefiniti. Questa logica instrada gli utenti al modulo corretto per l'utilizzo con la versione basata su lavoro o qualsiasi altro tipo di entità Opportunità, Offerta, Ordine o Fattura. Quando un utente apre la versione basata su lavoro di un'entità Opportunità, Offerta, Ordine o Fattura, il modulo passa a **Informazioni sul progetto**.

La logica di commutazione automatica dei moduli si basa sul mapping tra il valore **formId** e il campo **msdyn\_ordertype**. Tutti i moduli predefiniti sono stati aggiunti a quel mapping. Tuttavia, i moduli personalizzati devono essere aggiunti manualmente per indicare quale versione dell'entità devono gestire. Ciò è basato sul campo **msdyn\_ordertype**. Se la commutazione dei moduli non è presente nel mapping, la logica passerà al modulo predefinito, in base al valore salvato nel campo **msdyn\_ordertype** dell'entità.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Aggiungere moduli personalizzati e attivare la logica di commutazione dei moduli

Nell'esempio seguente viene illustrato come aggiungere un modulo personalizzato, **Informazioni di progetto personali** , di modo che sia utilizzabile con le opportunità basate su lavoro. La stessa procedura viene utilizzata per aggiungere moduli personalizzati di modo che siano utilizzati con offerte, ordini e fatture.

Segui la procedura esposta di seguito per creare una versione personalizzata del modulo **Informazioni sul progetto**.

1. Nell'entità Opportunità, apri il modulo **Informazioni sul progetto** e salva una copia con il nome **Informazioni di progetto personali**.
2. Apri il nuovo modulo e quindi, nelle proprietà, verifica che gli script di inizializzazione del modulo **Informazioni sul progetto** siano presenti. 

    > [!IMPORTANT]
    > Non rimuovere gli script. In caso contrario, alcuni dati potrebbero essere inizializzati in modo errato.

3. Verifica che il campo **Tipo** ( **msdyn\_ordertype** ) sia presente nel modulo. 

    > [!IMPORTANT]
    > Non rimuovere questo campo. In caso contrario, gli script di inizializzazione avranno esito negativo.

4. Trova il valore **formId** del nuovo modulo. Puoi completare questo passaggio in due modi:

    - Esporta il modulo **Informazioni di progetto personali** come parte di una soluzione non gestita e quindi cerca il valore **formId** nel file customization.xml della soluzione esportata.
    - Apri il modulo **Informazioni di progetto personali** nell'editor di moduli e quindi cerca l'identificatore univoco globale (GUID) accanto al parametro **fromId** nell'URL, come illustrato nella figura seguente.

    ![Il valore formId del nuovo modulo nell'URL](media/how-to-add-custom-forms-in-v2.0.png)

5. Crea un mapping **msdyn\_ordertype** per il valore **formId** modificando la risorsa Web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Rimuovi il codice dalla risorsa e sostituiscilo con il codice seguente.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Salva e quindi pubblica le personalizzazioni.
