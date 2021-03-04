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
ms.openlocfilehash: 31986efed81892cc5722cb8f5e292cde14d8843d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144598"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="5bf58-103">Aggiungere nuovi moduli di entità personalizzate (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="5bf58-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="5bf58-104">Campo Tipo</span><span class="sxs-lookup"><span data-stu-id="5bf58-104">Type field</span></span> 

<span data-ttu-id="5bf58-105">Dynamics 365 Project Service Automation utilizza il campo **Tipo** (**msdyn\_ordertype**) delle entità Opportunità, Offerta, Ordine e Fattura per distinguere le versioni **basate su lavoro** di queste entità dalle versioni **basate su articolo** e **basate su servizio**.</span><span class="sxs-lookup"><span data-stu-id="5bf58-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="5bf58-106">Le versioni basate su lavoro di queste entità sono gestite da PSA.</span><span class="sxs-lookup"><span data-stu-id="5bf58-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="5bf58-107">Molte delle regole di business sul lato client e sul lato server della soluzione dipendono dal campo **Tipo**.</span><span class="sxs-lookup"><span data-stu-id="5bf58-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="5bf58-108">Pertanto, è importante che il campo sia inizializzato con un valore corretto alla creazione delle entità.</span><span class="sxs-lookup"><span data-stu-id="5bf58-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="5bf58-109">Un valore errato può causare comportamenti inappropriati e alcune regole di business potrebbero non essere eseguite correttamente.</span><span class="sxs-lookup"><span data-stu-id="5bf58-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="5bf58-110">Commutazione automatica dei moduli</span><span class="sxs-lookup"><span data-stu-id="5bf58-110">Automatic form switching</span></span>

<span data-ttu-id="5bf58-111">Per evitare un potenziale danneggiamento dei dati e comportamenti imprevisti causati dall'inizializzazione e dalla modifica non corrette di record delle entità di vendita, ora PSA include la logica per la commutazione automatica dei moduli nei moduli predefiniti.</span><span class="sxs-lookup"><span data-stu-id="5bf58-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="5bf58-112">Questa logica instrada gli utenti al modulo corretto per l'utilizzo con la versione basata su lavoro o qualsiasi altro tipo di entità Opportunità, Offerta, Ordine o Fattura.</span><span class="sxs-lookup"><span data-stu-id="5bf58-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="5bf58-113">Quando un utente apre la versione basata su lavoro di un'entità Opportunità, Offerta, Ordine o Fattura, il modulo passa a **Informazioni sul progetto**.</span><span class="sxs-lookup"><span data-stu-id="5bf58-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="5bf58-114">La logica di commutazione automatica dei moduli si basa sul mapping tra il valore **formId** e il campo **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="5bf58-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="5bf58-115">Tutti i moduli predefiniti sono stati aggiunti a quel mapping.</span><span class="sxs-lookup"><span data-stu-id="5bf58-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="5bf58-116">Tuttavia, i moduli personalizzati devono essere aggiunti manualmente per indicare quale versione dell'entità devono gestire.</span><span class="sxs-lookup"><span data-stu-id="5bf58-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="5bf58-117">Ciò è basato sul campo **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="5bf58-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="5bf58-118">Se la commutazione dei moduli non è presente nel mapping, la logica passerà al modulo predefinito, in base al valore salvato nel campo **msdyn\_ordertype** dell'entità.</span><span class="sxs-lookup"><span data-stu-id="5bf58-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="5bf58-119">Aggiungere moduli personalizzati e attivare la logica di commutazione dei moduli</span><span class="sxs-lookup"><span data-stu-id="5bf58-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="5bf58-120">Nell'esempio seguente viene illustrato come aggiungere un modulo personalizzato, **Informazioni di progetto personali**, di modo che sia utilizzabile con le opportunità basate su lavoro.</span><span class="sxs-lookup"><span data-stu-id="5bf58-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="5bf58-121">La stessa procedura viene utilizzata per aggiungere moduli personalizzati di modo che siano utilizzati con offerte, ordini e fatture.</span><span class="sxs-lookup"><span data-stu-id="5bf58-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="5bf58-122">Segui la procedura esposta di seguito per creare una versione personalizzata del modulo **Informazioni sul progetto**.</span><span class="sxs-lookup"><span data-stu-id="5bf58-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="5bf58-123">Nell'entità Opportunità, apri il modulo **Informazioni sul progetto** e salva una copia con il nome **Informazioni di progetto personali**.</span><span class="sxs-lookup"><span data-stu-id="5bf58-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="5bf58-124">Apri il nuovo modulo e quindi, nelle proprietà, verifica che gli script di inizializzazione del modulo **Informazioni sul progetto** siano presenti.</span><span class="sxs-lookup"><span data-stu-id="5bf58-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="5bf58-125">Non rimuovere gli script.</span><span class="sxs-lookup"><span data-stu-id="5bf58-125">Don't remove the scripts.</span></span> <span data-ttu-id="5bf58-126">In caso contrario, alcuni dati potrebbero essere inizializzati in modo errato.</span><span class="sxs-lookup"><span data-stu-id="5bf58-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="5bf58-127">Verifica che il campo **Tipo** (**msdyn\_ordertype**) sia presente nel modulo.</span><span class="sxs-lookup"><span data-stu-id="5bf58-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="5bf58-128">Non rimuovere questo campo.</span><span class="sxs-lookup"><span data-stu-id="5bf58-128">Don't remove this field.</span></span> <span data-ttu-id="5bf58-129">In caso contrario, gli script di inizializzazione avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5bf58-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="5bf58-130">Trova il valore **formId** del nuovo modulo.</span><span class="sxs-lookup"><span data-stu-id="5bf58-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="5bf58-131">Puoi completare questo passaggio in due modi:</span><span class="sxs-lookup"><span data-stu-id="5bf58-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="5bf58-132">Esporta il modulo **Informazioni di progetto personali** come parte di una soluzione non gestita e quindi cerca il valore **formId** nel file customization.xml della soluzione esportata.</span><span class="sxs-lookup"><span data-stu-id="5bf58-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="5bf58-133">Apri il modulo **Informazioni di progetto personali** nell'editor di moduli e quindi cerca l'identificatore univoco globale (GUID) accanto al parametro **fromId** nell'URL, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="5bf58-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Il valore formId del nuovo modulo nell'URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="5bf58-135">Crea un mapping **msdyn\_ordertype** per il valore **formId** modificando la risorsa Web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="5bf58-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="5bf58-136">Rimuovi il codice dalla risorsa e sostituiscilo con il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="5bf58-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="5bf58-137">Salva e quindi pubblica le personalizzazioni.</span><span class="sxs-lookup"><span data-stu-id="5bf58-137">Save and then publish the customizations.</span></span>
