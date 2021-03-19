---
title: Implementare campi personalizzati per l'app per dispositivi mobili Microsoft Dynamics 365 Project Timesheet  su iOS e Android
description: Questo argomento fornisce modelli comuni per l'utilizzo delle estensioni per implementare i campi personalizzati.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270998"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="72e9a-103">Implementare campi personalizzati per l'app per dispositivi mobili Microsoft Dynamics 365 Project Timesheet  su iOS e Android</span><span class="sxs-lookup"><span data-stu-id="72e9a-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72e9a-104">Questo argomento fornisce modelli comuni per l'utilizzo delle estensioni per implementare i campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="72e9a-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="72e9a-105">Vengono trattati i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="72e9a-105">The following topics are covered:</span></span>

- <span data-ttu-id="72e9a-106">I vari tipi di dati supportati dal framework del campo personalizzato</span><span class="sxs-lookup"><span data-stu-id="72e9a-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="72e9a-107">Come mostrare i campi di sola lettura o modificabili negli inserimenti del foglio presenze e salvare i valori forniti dall'utente nel database</span><span class="sxs-lookup"><span data-stu-id="72e9a-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="72e9a-108">Come mostrare i campi di sola lettura nell'intestazione del foglio presenze</span><span class="sxs-lookup"><span data-stu-id="72e9a-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="72e9a-109">Come integrare altra logica aziendale personalizzata per inserire valori predefiniti nei campi ed eseguire ulteriori convalide</span><span class="sxs-lookup"><span data-stu-id="72e9a-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="72e9a-110">Destinatari</span><span class="sxs-lookup"><span data-stu-id="72e9a-110">Audience</span></span>

<span data-ttu-id="72e9a-111">Questo argomento è destinato agli sviluppatori che stanno integrando i propri campi personalizzati nell'applicazione per dispositivi mobili Microsoft Dynamics 365 Project Timesheet per Apple iOS e Google Android.</span><span class="sxs-lookup"><span data-stu-id="72e9a-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="72e9a-112">Il presupposto è che i lettori abbiano familiarità con le funzionalità di sviluppo X++ e del foglio presenze del progetto.</span><span class="sxs-lookup"><span data-stu-id="72e9a-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="72e9a-113">Contratto dati: classe TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="72e9a-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="72e9a-114">La classe **TSTimesheetCustomField** è la classe del contratto dati X++ che rappresenta le informazioni su un campo personalizzato per la funzionalità del foglio presenze.</span><span class="sxs-lookup"><span data-stu-id="72e9a-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="72e9a-115">Gli elenchi degli oggetti campo personalizzati vengono passati sia al contratto dati TSTimesheetDetails che al contratto dati TSTimesheetEntry per mostrare i campi personalizzati nell'app per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="72e9a-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="72e9a-116">**TSTimesheetDetails**: il contratto dell'intestazione del foglio presenze.</span><span class="sxs-lookup"><span data-stu-id="72e9a-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="72e9a-117">**TSTimesheetEntry**: il contratto di transazione del foglio presenze.</span><span class="sxs-lookup"><span data-stu-id="72e9a-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="72e9a-118">I gruppi di questi oggetti che hanno le stesse informazioni sul progetto e il valore **timesheetLineRecId** costituiscono una riga.</span><span class="sxs-lookup"><span data-stu-id="72e9a-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="72e9a-119">fieldBaseType (Tipi)</span><span class="sxs-lookup"><span data-stu-id="72e9a-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="72e9a-120">La proprietà **FieldBaseType** sull'oggetto **TsTimesheetCustom** determina il tipo di campo che appare nell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="72e9a-121">I valori **Tipi** seguenti supportati.</span><span class="sxs-lookup"><span data-stu-id="72e9a-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="72e9a-122">Valore Tipi</span><span class="sxs-lookup"><span data-stu-id="72e9a-122">Types value</span></span> | <span data-ttu-id="72e9a-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="72e9a-123">Type</span></span>              | <span data-ttu-id="72e9a-124">Note</span><span class="sxs-lookup"><span data-stu-id="72e9a-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="72e9a-125">0</span><span class="sxs-lookup"><span data-stu-id="72e9a-125">0</span></span>           | <span data-ttu-id="72e9a-126">Stringa (ed Enum)</span><span class="sxs-lookup"><span data-stu-id="72e9a-126">String (and Enum)</span></span> | <span data-ttu-id="72e9a-127">Il campo appare come un campo di testo.</span><span class="sxs-lookup"><span data-stu-id="72e9a-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="72e9a-128">1</span><span class="sxs-lookup"><span data-stu-id="72e9a-128">1</span></span>           | <span data-ttu-id="72e9a-129">Intero</span><span class="sxs-lookup"><span data-stu-id="72e9a-129">Integer</span></span>           | <span data-ttu-id="72e9a-130">Il valore viene visualizzato come un numero senza posizioni decimali.</span><span class="sxs-lookup"><span data-stu-id="72e9a-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="72e9a-131">2</span><span class="sxs-lookup"><span data-stu-id="72e9a-131">2</span></span>           | <span data-ttu-id="72e9a-132">Reale</span><span class="sxs-lookup"><span data-stu-id="72e9a-132">Real</span></span>              | <span data-ttu-id="72e9a-133">Il valore viene visualizzato come un numero che include posizioni decimali.</span><span class="sxs-lookup"><span data-stu-id="72e9a-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="72e9a-134">Per mostrare il valore reale come valuta nell'app, utilizza la proprietà **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="72e9a-135">Puoi utilizzare la proprietà **numberOfDecimals** per impostare il numero di posizioni decimali visualizzate.</span><span class="sxs-lookup"><span data-stu-id="72e9a-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="72e9a-136">3</span><span class="sxs-lookup"><span data-stu-id="72e9a-136">3</span></span>           | <span data-ttu-id="72e9a-137">Date</span><span class="sxs-lookup"><span data-stu-id="72e9a-137">Date</span></span>              | <span data-ttu-id="72e9a-138">I formati della data sono determinati dall'impostazione di **Formato di data, ora e numeri** dell'utente specificata in **Preferenza di lingua e paese/area geografica** in **Opzioni utente**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="72e9a-139">4</span><span class="sxs-lookup"><span data-stu-id="72e9a-139">4</span></span>           | <span data-ttu-id="72e9a-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="72e9a-140">Boolean</span></span>           | |
| <span data-ttu-id="72e9a-141">15</span><span class="sxs-lookup"><span data-stu-id="72e9a-141">15</span></span>          | <span data-ttu-id="72e9a-142">GUID</span><span class="sxs-lookup"><span data-stu-id="72e9a-142">GUID</span></span>              | |
| <span data-ttu-id="72e9a-143">16</span><span class="sxs-lookup"><span data-stu-id="72e9a-143">16</span></span>          | <span data-ttu-id="72e9a-144">Int64</span><span class="sxs-lookup"><span data-stu-id="72e9a-144">Int64</span></span>             | |

- <span data-ttu-id="72e9a-145">Se la proprietà **stringOptions** non è specificata nell'oggetto **TSTimesheetCustomField**, all'utente viene fornito un campo di testo libero.</span><span class="sxs-lookup"><span data-stu-id="72e9a-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="72e9a-146">La proprietà **stringLength** può essere utilizzata per impostare la lunghezza massima della stringa che gli utenti possono immettere.</span><span class="sxs-lookup"><span data-stu-id="72e9a-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="72e9a-147">Se la proprietà **stringOptions** viene specificata sull'oggetto **TSTimesheetCustomField**, quegli elementi dell'elenco sono gli unici valori che gli utenti possono selezionare utilizzando i pulsanti di opzione (pulsanti di opzione).</span><span class="sxs-lookup"><span data-stu-id="72e9a-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="72e9a-148">In questo caso, il campo stringa può fungere da valore enum ai fini dell'immissione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="72e9a-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="72e9a-149">Per salvare il valore nel database come enum, mappa manualmente il valore della stringa di nuovo al valore enum prima di salvare nel database utilizzando la catena di comando (vedi la sezione "Utilizzare la catena di comando sulla classe TSTimesheetEntryService per salvare un inserimento del foglio presenze dall'app al database" più avanti in questo argomento per un esempio).</span><span class="sxs-lookup"><span data-stu-id="72e9a-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="72e9a-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="72e9a-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="72e9a-151">Puoi utilizzare questa proprietà per formattare i valori reali come valuta.</span><span class="sxs-lookup"><span data-stu-id="72e9a-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="72e9a-152">Questo approccio è applicabile solo quando il valore **fieldBaseType** è **Reale**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="72e9a-153">**TSCustomFieldExtendedType:None**: nessuna formattazione applicata.</span><span class="sxs-lookup"><span data-stu-id="72e9a-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="72e9a-154">**TSCustomFieldExtendedType::Currency**: il valore viene formattato come valuta.</span><span class="sxs-lookup"><span data-stu-id="72e9a-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="72e9a-155">Quando la formattazione della valuta è attiva, il campo **stringValue** può essere utilizzato per passare il codice valuta che dovrebbe essere mostrato nell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="72e9a-156">Il valore è un valore di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="72e9a-156">The value is a read-only value.</span></span>

    <span data-ttu-id="72e9a-157">Il campo **realValue** contiene l'importo in denaro che deve essere salvato nel database.</span><span class="sxs-lookup"><span data-stu-id="72e9a-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="72e9a-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="72e9a-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="72e9a-159">Puoi utilizzare questa proprietà per specificare dove deve essere visualizzato il campo personalizzato nell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="72e9a-160">**TSCustomFieldSection::Header**: il campo verrà visualizzato nella sezione **Visualizza altri dettagli** dell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="72e9a-161">Questi campi sono sempre di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="72e9a-161">These fields are always read-only.</span></span>
- <span data-ttu-id="72e9a-162">**TSCustomFieldSection::Line**: il campo verrà visualizzato dopo i campi riga predefiniti tra le voci del foglio presenze.</span><span class="sxs-lookup"><span data-stu-id="72e9a-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="72e9a-163">Questi campi possono essere modificabili o di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="72e9a-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="72e9a-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="72e9a-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="72e9a-165">Questa proprietà identifica il campo quando i valori forniti dall'app vengono salvati di nuovo nel database.</span><span class="sxs-lookup"><span data-stu-id="72e9a-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="72e9a-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="72e9a-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="72e9a-167">Questa proprietà identifica il campo quando i valori forniti dall'app vengono salvati di nuovo nel database.</span><span class="sxs-lookup"><span data-stu-id="72e9a-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="72e9a-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="72e9a-168">isEditable (NoYes)</span></span>

<span data-ttu-id="72e9a-169">Imposta questa proprietà su **Sì** per specificare che il campo nella sezione di immissione del foglio presenze deve essere modificabile dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="72e9a-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="72e9a-170">Imposta la proprietà su **No** per impostare il campo di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="72e9a-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="72e9a-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="72e9a-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="72e9a-172">Imposta questa proprietà su **Sì** per specificare che il campo nella sezione di immissione del foglio presenze deve essere obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="72e9a-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="72e9a-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="72e9a-173">label (str)</span></span>

<span data-ttu-id="72e9a-174">Questa proprietà specifica l'etichetta che viene mostrata accanto al campo nell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="72e9a-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="72e9a-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="72e9a-176">Questa proprietà è applicabile solo quando **fieldBaseType** è impostata su **Stringa**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="72e9a-177">Se **stringOptions** è impostata, i valori di stringa disponibili per la selezione tramite i pulsanti di opzione (pulsanti di opzione) sono specificati dalle stringhe nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="72e9a-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="72e9a-178">Se non vengono specificate stringhe, è consentita l'immissione di testo libero nel campo della stringa (vedi la sezione "Utilizzare la catena di comando sulla classe TSTimesheetEntryService per salvare una voce del foglio presenze dall'app nel database" più avanti in questo argomento per un esempio ).</span><span class="sxs-lookup"><span data-stu-id="72e9a-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="72e9a-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="72e9a-179">stringLength (int)</span></span>

<span data-ttu-id="72e9a-180">Questa proprietà specifica la lunghezza massima per un campo stringa.</span><span class="sxs-lookup"><span data-stu-id="72e9a-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="72e9a-181">Questa proprietà è applicabile solo quando **fieldBaseType** è impostata su **Stringa**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="72e9a-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="72e9a-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="72e9a-183">Questa proprietà specifica il numero di posizioni decimali visualizzate per un campo reale.</span><span class="sxs-lookup"><span data-stu-id="72e9a-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="72e9a-184">Questa proprietà è applicabile solo quando **fieldBaseType** è impostata su **Reale**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="72e9a-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="72e9a-185">orderSequence (int)</span></span>

<span data-ttu-id="72e9a-186">Questa proprietà controlla l'ordine in cui i campi personalizzati vengono visualizzati nell'app quando viene specificato più di un campo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="72e9a-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="72e9a-187">I campi con numeri inferiori vengono visualizzati per primi.</span><span class="sxs-lookup"><span data-stu-id="72e9a-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="72e9a-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="72e9a-188">booleanValue (boolean)</span></span>

<span data-ttu-id="72e9a-189">Per i campi di tipo **Booleano**, questa proprietà passa il valore booleano del campo tra il server e l'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="72e9a-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="72e9a-190">guidValue (guid)</span></span>

<span data-ttu-id="72e9a-191">Per i campi di tipo **GUID**, questa proprietà passa il valore dell'identificatore univoco globale (GUID) del campo tra il server e l'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="72e9a-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="72e9a-192">int64Value (int64)</span></span>

<span data-ttu-id="72e9a-193">Per i campi di tipo **Int64**, questa proprietà passa il valore int64 del campo tra il server e l'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="72e9a-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="72e9a-194">intValue (int)</span></span>

<span data-ttu-id="72e9a-195">Per i campi di tipo **Int**, questa proprietà passa il valore int del campo tra il server e l'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="72e9a-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="72e9a-196">realValue (real)</span></span>

<span data-ttu-id="72e9a-197">Per i campi di tipo **Reale**, questa proprietà passa il valore reale del campo tra il server e l'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="72e9a-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="72e9a-198">stringValue (str)</span></span>

<span data-ttu-id="72e9a-199">Per i campi di tipo **Stringa**, questa proprietà passa il valore stringa del campo tra il server e l'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="72e9a-200">Viene utilizzato anche per i campi di tipo **Reale** formattati come valuta.</span><span class="sxs-lookup"><span data-stu-id="72e9a-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="72e9a-201">Per questi campi, la proprietà viene utilizzata per passare il codice della valuta all'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="72e9a-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="72e9a-202">dateValue (date)</span></span>

<span data-ttu-id="72e9a-203">Per i campi di tipo **Data**, questa proprietà passa il valore data del campo tra il server e l'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="72e9a-204">Mostra e salva un campo personalizzato nella sezione di immissione del foglio presenze</span><span class="sxs-lookup"><span data-stu-id="72e9a-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="72e9a-205">Di seguito è riportato uno screenshot dall'app per dispositivi mobili della creazione di una voce del foglio presenze.</span><span class="sxs-lookup"><span data-stu-id="72e9a-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="72e9a-206">Mostra i campi predefiniti e un campo personalizzato nella sezione "Inserimento ora" chiamato "Stringa di prova" con un valore di enum di "Seconda opzione" già impostato.</span><span class="sxs-lookup"><span data-stu-id="72e9a-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Campo personalizzato della stringa di prova nell'app](media/timesheet-entry.jpg)



<span data-ttu-id="72e9a-208">Di seguito è riportato uno screenshot dall'app per dispositivi mobili dell'utente che seleziona una delle opzioni di enumerazione disponibili per il campo personalizzato "Stringa di prova".</span><span class="sxs-lookup"><span data-stu-id="72e9a-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="72e9a-209">Le due opzioni sono "Prima opzione" e "Seconda opzione" mostrate come pulsanti di opzione.</span><span class="sxs-lookup"><span data-stu-id="72e9a-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="72e9a-210">La seconda opzione è attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="72e9a-210">The second option is currently selected.</span></span>

![Pulsanti di opzione (pulsanti di opzione) per il campo personalizzato Stringa di prova](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="72e9a-212">Estendi la tabella TSTimesheetLine in modo che abbia un campo personalizzato</span><span class="sxs-lookup"><span data-stu-id="72e9a-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="72e9a-213">In scenari tipici, è probabile che i dati per un campo personalizzato nella sezione di immissione del foglio presenze vengano salvati nella tabella TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="72e9a-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="72e9a-214">Tuttavia, è possibile utilizzare altre tabelle se i dati possono essere recuperati in base a un record TSTimesheetTrans fornito o se non dispone di un contesto di record specifico (ad esempio, se il campo è impostato come di sola lettura nei parametri del progetto) .</span><span class="sxs-lookup"><span data-stu-id="72e9a-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="72e9a-215">Tieni presente che i campi personalizzati non devono avere alcun record del database di supporto.</span><span class="sxs-lookup"><span data-stu-id="72e9a-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="72e9a-216">Possono essere generati dinamicamente in base alla logica X++.</span><span class="sxs-lookup"><span data-stu-id="72e9a-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="72e9a-217">Questo approccio può essere utile in scenari di sola lettura (vedi la sezione "Utilizzare la catena di comando sulla classe TSTimesheetDetails, metodo buildCustomFieldListForHeader per compilare i dettagli del foglio presenze" per un esempio di valori di campo personalizzati generati dinamicamente.)</span><span class="sxs-lookup"><span data-stu-id="72e9a-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="72e9a-218">Di seguito è riportato uno screenshot da Visual Studio dell'albero degli oggetti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="72e9a-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="72e9a-219">Mostra un'estensione della tabella TSTimesheetLine con il campo TestLineString aggiunto come campo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="72e9a-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Stringa della riga](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="72e9a-221">Utilizzare la catena di comando sul metodo buildCustomFieldList della classe TSTimesheetSettings per mostrare un campo nella sezione di immissione del foglio presenze</span><span class="sxs-lookup"><span data-stu-id="72e9a-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="72e9a-222">Questo codice controlla le impostazioni di visualizzazione per il campo nell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="72e9a-223">Ad esempio, controlla il tipo di campo, l'etichetta, se il campo è obbligatorio e in quale sezione viene visualizzato il campo.</span><span class="sxs-lookup"><span data-stu-id="72e9a-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="72e9a-224">L'esempio seguente mostra un campo stringa sugli inserimenti ore.</span><span class="sxs-lookup"><span data-stu-id="72e9a-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="72e9a-225">Questo campo ha due opzioni, **Prima opzione** e **Seconda opzione**, disponibili tramite pulsanti di opzione (pulsanti di opzione).</span><span class="sxs-lookup"><span data-stu-id="72e9a-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="72e9a-226">Il campo nell'app è associato al campo **TestLineString** aggiunto alla tabella TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="72e9a-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="72e9a-227">Nota l'uso del metodo **TSTimesheetCustomField::newFromMetatdata()** per semplificare l'inizializzazione delle proprietà del campo personalizzato: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** e **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="72e9a-228">Puoi anche impostare questi parametri manualmente, come preferisci.</span><span class="sxs-lookup"><span data-stu-id="72e9a-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="72e9a-229">Utilizzare la catena di comando sul metodo buildCustomFieldListForEntry della classe TSTimesheetEntry per immettere valori in una voce del foglio presenze</span><span class="sxs-lookup"><span data-stu-id="72e9a-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="72e9a-230">Il metodo **buildCustomFieldListForEntry** viene utilizzato per immettere i valori nelle righe del foglio presenze salvate nell'app per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="72e9a-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="72e9a-231">Acquisisce un record TSTimesheetTrans come parametro.</span><span class="sxs-lookup"><span data-stu-id="72e9a-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="72e9a-232">I campi di quel record possono essere utilizzati per compilare il valore del campo personalizzato nell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="72e9a-233">Utilizzare la catena di comando sulla classe TSTimesheetEntryService per salvare una voce del foglio presenze dall'app nel database</span><span class="sxs-lookup"><span data-stu-id="72e9a-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="72e9a-234">Per salvare un campo personalizzato di nuovo nel database nell'utilizzo tipico, è necessario estendere più metodi:</span><span class="sxs-lookup"><span data-stu-id="72e9a-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="72e9a-235">Il metodo **timesheetLineNeedsUpdating** viene utilizzato per determinare se il record di riga è stato modificato dall'utente nell'app e deve essere salvato nel database.</span><span class="sxs-lookup"><span data-stu-id="72e9a-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="72e9a-236">Se le prestazioni non sono un problema, questo metodo può essere semplificato in modo che restituisca sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="72e9a-237">I metodi **populateTimesheetLineFromEntryDuringCreate** e **populateTimesheetLineFromEntryDuringUpdate** possono essere estesi in modo da immettere valori nel record del database TSTimesheetLine database dal record del contratto dati TSTimesheetEntry specificato.</span><span class="sxs-lookup"><span data-stu-id="72e9a-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="72e9a-238">Nell'esempio che segue, nota come il mapping tra il campo del database e il campo di immissione venga eseguito manualmente tramite codice X++.</span><span class="sxs-lookup"><span data-stu-id="72e9a-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="72e9a-239">Il metodo **populateTimesheetWeekFromEntry** può essere esteso anche se il campo personalizzato mappato all'oggetto **TSTimesheetEntry** deve essere scritto nuovamente nella tabella del database TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="72e9a-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="72e9a-240">L'esempio seguente salva il valore **firstOption** o **secondOption** che l'utente seleziona nel database come valore stringa non elaborato.</span><span class="sxs-lookup"><span data-stu-id="72e9a-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="72e9a-241">Se il campo del database è un campo di tipo **Enum**, questi valori possono essere mappati manualmente a un valore enum e quindi salvati in un campo enum nella tabella del database.</span><span class="sxs-lookup"><span data-stu-id="72e9a-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="72e9a-242">Mostra un campo personalizzato nella sezione di intestazione del foglio presenze</span><span class="sxs-lookup"><span data-stu-id="72e9a-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="72e9a-243">Di seguito è riportato uno screenshot dall'app per dispositivi mobili di un utente che visualizza un foglio presenze.</span><span class="sxs-lookup"><span data-stu-id="72e9a-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="72e9a-244">Il pulsante "Altre informazioni" è stato selezionato nell'angolo in alto a destra per mostrare l'opzione "Visualizza altri dettagli".</span><span class="sxs-lookup"><span data-stu-id="72e9a-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Comando Visualizza altri dettagli](media/show-more.png)

<span data-ttu-id="72e9a-246">Di seguito è riportato uno screenshot dall'app per dispositivi mobili che mostra la sezione "Altro" di un foglio presenze.</span><span class="sxs-lookup"><span data-stu-id="72e9a-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="72e9a-247">Un campo personalizzato denominato "Tasso di utilizzo di questo foglio presenze (campo personalizzato calcolato)" è stato aggiunto alla sezione dell'intestazione del foglio presenze.</span><span class="sxs-lookup"><span data-stu-id="72e9a-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="72e9a-248">Un valore di sola lettura di "0,667" è impostato nel campo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="72e9a-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Sezione Altro](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="72e9a-250">Estendere la tabella TSTimesheetTable in modo che abbia un campo personalizzato</span><span class="sxs-lookup"><span data-stu-id="72e9a-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="72e9a-251">In scenari tipici, è probabile che i dati per un campo personalizzato nella sezione di intestazione verranno estratti dalla tabella TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="72e9a-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="72e9a-252">Tuttavia, è possibile utilizzare altre tabelle se i dati possono essere recuperati in base a un record TSTimesheetTable fornito o se non dispone di un contesto di record specifico (ad esempio, se il campo è impostato come di sola lettura nei parametri del progetto) .</span><span class="sxs-lookup"><span data-stu-id="72e9a-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="72e9a-253">Tieni presente che i campi personalizzati non devono avere alcun record del database di supporto.</span><span class="sxs-lookup"><span data-stu-id="72e9a-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="72e9a-254">Possono essere generati dinamicamente in base alla logica X++.</span><span class="sxs-lookup"><span data-stu-id="72e9a-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="72e9a-255">L'esempio che segue mostra questo approccio.</span><span class="sxs-lookup"><span data-stu-id="72e9a-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="72e9a-256">I campi nella sezione dell'intestazione sono sempre di sola lettura nell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="72e9a-257">Utilizzare la catena di comando sul metodo buildCustomFieldList della classe TSTimesheetSettings per mostrare un campo nella sezione di intestazione</span><span class="sxs-lookup"><span data-stu-id="72e9a-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="72e9a-258">Questo codice controlla le impostazioni di visualizzazione per il campo nell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="72e9a-259">Ad esempio, controlla il tipo di campo, l'etichetta, se il campo è obbligatorio e in quale sezione viene visualizzato il campo.</span><span class="sxs-lookup"><span data-stu-id="72e9a-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="72e9a-260">L'esempio seguente mostra un valore calcolato nella sezione dell'intestazione nell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="72e9a-261">Utilizzare la catena di comando sul metodo buildCustomFieldListForHeader della classe TSTimesheetDetails per compilare i dettagli del foglio presenze</span><span class="sxs-lookup"><span data-stu-id="72e9a-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="72e9a-262">Il metodo **buildCustomFieldListForHeader** viene utilizzato per compilare i dettagli dell'intestazione del foglio presenze nell'app per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="72e9a-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="72e9a-263">Acquisisce un record TSTimesheetTable come parametro.</span><span class="sxs-lookup"><span data-stu-id="72e9a-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="72e9a-264">I campi di quel record possono essere utilizzati per compilare il valore del campo personalizzato nell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="72e9a-265">L'esempio seguente non legge alcun valore dal database.</span><span class="sxs-lookup"><span data-stu-id="72e9a-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="72e9a-266">Invece, utilizza la logica X + per generare un valore calcolato che viene quindi mostrato nell'app.</span><span class="sxs-lookup"><span data-stu-id="72e9a-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="72e9a-267">Altre opportunità di configurabilità/estendibilità</span><span class="sxs-lookup"><span data-stu-id="72e9a-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="72e9a-268">Aggiunta di ulteriore convalida per l'app</span><span class="sxs-lookup"><span data-stu-id="72e9a-268">Adding additional validation for the app</span></span>

<span data-ttu-id="72e9a-269">La logica esistente per la funzionalità del foglio presenze a livello di database continuerà a funzionare come previsto.</span><span class="sxs-lookup"><span data-stu-id="72e9a-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="72e9a-270">Per interrompere il completamento delle operazioni di salvataggio o invio e visualizzare un messaggio di errore specifico, puoi aggiungere **throw error("message to user")** al codice tramite una catena di estensione dei comandi.</span><span class="sxs-lookup"><span data-stu-id="72e9a-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="72e9a-271">Ecco tre esempi di utili metodi estensibili:</span><span class="sxs-lookup"><span data-stu-id="72e9a-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="72e9a-272">Se **validateWrite** nella tabella TSTimesheetLine restituisce **false** durante un'operazione di salvataggio per una riga del foglio presenze, viene visualizzato un messaggio di errore app per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="72e9a-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="72e9a-273">Se **validateSubmit** nella tabella TSTimesheetTable restituisce **false** durante un'operazione di invio del foglio presenze nell'app, viene visualizzato un messaggio di errore app all'utente.</span><span class="sxs-lookup"><span data-stu-id="72e9a-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="72e9a-274">La logica che compila i campi (ad esempio, **Proprietà riga**) durante il metodo di **inserimento** nella tabella TSTimesheetLine verrà comunque eseguita.</span><span class="sxs-lookup"><span data-stu-id="72e9a-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="72e9a-275">Nascondere e contrassegnare i campi predefiniti come di sola lettura tramite la configurazione</span><span class="sxs-lookup"><span data-stu-id="72e9a-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="72e9a-276">Dai parametri del progetto, puoi rendere i campi predefiniti di sola lettura o nascosti nell'app per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="72e9a-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="72e9a-277">Imposta le opzioni nella sezione **Fogli presenze per dispositivi mobili** nella scheda **Foglio presenze** della pagina **Parametri Gestione progetti e contabilità**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parametri del progetto](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="72e9a-279">Modifica delle attività disponibili per la selezione tramite estensioni</span><span class="sxs-lookup"><span data-stu-id="72e9a-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="72e9a-280">Le attività disponibili per la selezione per un progetto vengono compilate tramite i metodi **getActivitiesForProject()** e **getActivityQuery()** nella classe **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="72e9a-281">Puoi utilizzare la catena di comando per modificare questo comportamento in modo che corrisponda al tuo scenario aziendale per le attività disponibili per la selezione per un progetto specifico.</span><span class="sxs-lookup"><span data-stu-id="72e9a-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="72e9a-282">Immissione di una categoria di progetto predefinita negli inserimenti del foglio presenze</span><span class="sxs-lookup"><span data-stu-id="72e9a-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="72e9a-283">L'immissione di una categoria di progetto predefinita negli inserimenti del foglio presenze avviene a tre livelli.</span><span class="sxs-lookup"><span data-stu-id="72e9a-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="72e9a-284">Puoi utilizzare la catena di comando per estendere il comportamento a uno o tutti questi livelli per ottenere il comportamento desiderato.</span><span class="sxs-lookup"><span data-stu-id="72e9a-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="72e9a-285">Viene utilizzata la gerarchia seguente:</span><span class="sxs-lookup"><span data-stu-id="72e9a-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="72e9a-286">L'app tenta di inserire la categoria predefinita dalla risorsa del progetto.</span><span class="sxs-lookup"><span data-stu-id="72e9a-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="72e9a-287">Questa categoria predefinita è impostata nei metodi **getCurrentUserResource** e **getDelegatedResourcesForCurrentUser** nella classe **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="72e9a-288">Se la categoria predefinita non viene specificata a livello di risorsa del progetto, l'app tenta di estrarla dall'attività del progetto.</span><span class="sxs-lookup"><span data-stu-id="72e9a-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="72e9a-289">Questa categoria predefinita è impostata nel metodo **getActivitiesForProject** nella classe **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="72e9a-290">Se la categoria predefinita non viene specificata a livello di attività del progetto, la categoria predefinita viene acquisita dai parametri del progetto.</span><span class="sxs-lookup"><span data-stu-id="72e9a-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="72e9a-291">Questa categoria predefinita è impostata nel metodo **getProjectDetailsbyRule** nella classe **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="72e9a-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]