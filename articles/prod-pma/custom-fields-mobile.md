---
title: Implementare campi personalizzati per l'app per dispositivi mobili Microsoft Dynamics 365 Project Timesheet  su iOS e Android
description: Questo argomento fornisce modelli comuni per l'utilizzo delle estensioni per implementare i campi personalizzati.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003042"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementare campi personalizzati per l'app per dispositivi mobili Microsoft Dynamics 365 Project Timesheet  su iOS e Android

[!include [banner](../includes/banner.md)]

Questo argomento fornisce modelli comuni per l'utilizzo delle estensioni per implementare i campi personalizzati. Vengono trattati i seguenti argomenti:

- I vari tipi di dati supportati dal framework del campo personalizzato
- Come mostrare i campi di sola lettura o modificabili negli inserimenti del foglio presenze e salvare i valori forniti dall'utente nel database
- Come mostrare i campi di sola lettura nell'intestazione del foglio presenze
- Come integrare altra logica aziendale personalizzata per inserire valori predefiniti nei campi ed eseguire ulteriori convalide

## <a name="audience"></a>Destinatari

Questo argomento è destinato agli sviluppatori che stanno integrando i propri campi personalizzati nell'applicazione per dispositivi mobili Microsoft Dynamics 365 Project Timesheet per Apple iOS e Google Android. Il presupposto è che i lettori abbiano familiarità con le funzionalità di sviluppo X++ e del foglio presenze del progetto.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Contratto dati: classe TSTimesheetCustomField X++

La classe **TSTimesheetCustomField** è la classe del contratto dati X++ che rappresenta le informazioni su un campo personalizzato per la funzionalità del foglio presenze. Gli elenchi degli oggetti campo personalizzati vengono passati sia al contratto dati TSTimesheetDetails che al contratto dati TSTimesheetEntry per mostrare i campi personalizzati nell'app per dispositivi mobili.

- **TSTimesheetDetails**: il contratto dell'intestazione del foglio presenze.
- **TSTimesheetEntry**: il contratto di transazione del foglio presenze. I gruppi di questi oggetti che hanno le stesse informazioni sul progetto e il valore **timesheetLineRecId** costituiscono una riga.

### <a name="fieldbasetype-types"></a>fieldBaseType (Tipi)

La proprietà **FieldBaseType** sull'oggetto **TsTimesheetCustom** determina il tipo di campo che appare nell'app. I valori **Tipi** seguenti supportati.

| Valore Tipi | Tipo              | Note |
|-------------|-------------------|-------|
| 0           | Stringa (ed Enum) | Il campo appare come un campo di testo. |
| 1           | Intero           | Il valore viene visualizzato come un numero senza posizioni decimali. |
| 2           | Reale              | Il valore viene visualizzato come un numero che include posizioni decimali.<p>Per mostrare il valore reale come valuta nell'app, utilizza la proprietà **fieldExtenededType**. Puoi utilizzare la proprietà **numberOfDecimals** per impostare il numero di posizioni decimali visualizzate.</p> |
| 3           | Date              | I formati della data sono determinati dall'impostazione di **Formato di data, ora e numeri** dell'utente specificata in **Preferenza di lingua e paese/area geografica** in **Opzioni utente**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Se la proprietà **stringOptions** non è specificata nell'oggetto **TSTimesheetCustomField**, all'utente viene fornito un campo di testo libero.

    La proprietà **stringLength** può essere utilizzata per impostare la lunghezza massima della stringa che gli utenti possono immettere.

- Se la proprietà **stringOptions** viene specificata sull'oggetto **TSTimesheetCustomField**, quegli elementi dell'elenco sono gli unici valori che gli utenti possono selezionare utilizzando i pulsanti di opzione (pulsanti di opzione).

    In questo caso, il campo stringa può fungere da valore enum ai fini dell'immissione dell'utente. Per salvare il valore nel database come enum, mappa manualmente il valore della stringa di nuovo al valore enum prima di salvare nel database utilizzando la catena di comando (vedi la sezione "Utilizzare la catena di comando sulla classe TSTimesheetEntryService per salvare un inserimento del foglio presenze dall'app al database" più avanti in questo argomento per un esempio).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Puoi utilizzare questa proprietà per formattare i valori reali come valuta. Questo approccio è applicabile solo quando il valore **fieldBaseType** è **Reale**.

- **TSCustomFieldExtendedType:None**: nessuna formattazione applicata.
- **TSCustomFieldExtendedType::Currency**: il valore viene formattato come valuta.

    Quando la formattazione della valuta è attiva, il campo **stringValue** può essere utilizzato per passare il codice valuta che dovrebbe essere mostrato nell'app. Il valore è un valore di sola lettura.

    Il campo **realValue** contiene l'importo in denaro che deve essere salvato nel database.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Puoi utilizzare questa proprietà per specificare dove deve essere visualizzato il campo personalizzato nell'app.

- **TSCustomFieldSection::Header**: il campo verrà visualizzato nella sezione **Visualizza altri dettagli** dell'app. Questi campi sono sempre di sola lettura.
- **TSCustomFieldSection::Line**: il campo verrà visualizzato dopo i campi riga predefiniti tra le voci del foglio presenze. Questi campi possono essere modificabili o di sola lettura.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Questa proprietà identifica il campo quando i valori forniti dall'app vengono salvati di nuovo nel database.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Questa proprietà identifica il campo quando i valori forniti dall'app vengono salvati di nuovo nel database.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Imposta questa proprietà su **Sì** per specificare che il campo nella sezione di immissione del foglio presenze deve essere modificabile dagli utenti. Imposta la proprietà su **No** per impostare il campo di sola lettura.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Imposta questa proprietà su **Sì** per specificare che il campo nella sezione di immissione del foglio presenze deve essere obbligatorio.

### <a name="label-str"></a>label (str)

Questa proprietà specifica l'etichetta che viene mostrata accanto al campo nell'app.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

Questa proprietà è applicabile solo quando **fieldBaseType** è impostata su **Stringa**. Se **stringOptions** è impostata, i valori di stringa disponibili per la selezione tramite i pulsanti di opzione (pulsanti di opzione) sono specificati dalle stringhe nell'elenco. Se non vengono specificate stringhe, è consentita l'immissione di testo libero nel campo della stringa (vedi la sezione "Utilizzare la catena di comando sulla classe TSTimesheetEntryService per salvare una voce del foglio presenze dall'app nel database" più avanti in questo argomento per un esempio ).

### <a name="stringlength-int"></a>stringLength (int)

Questa proprietà specifica la lunghezza massima per un campo stringa. Questa proprietà è applicabile solo quando **fieldBaseType** è impostata su **Stringa**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Questa proprietà specifica il numero di posizioni decimali visualizzate per un campo reale. Questa proprietà è applicabile solo quando **fieldBaseType** è impostata su **Reale**.

### <a name="ordersequence-int"></a>orderSequence (int)

Questa proprietà controlla l'ordine in cui i campi personalizzati vengono visualizzati nell'app quando viene specificato più di un campo personalizzato. I campi con numeri inferiori vengono visualizzati per primi.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Per i campi di tipo **Booleano**, questa proprietà passa il valore booleano del campo tra il server e l'app.

### <a name="guidvalue-guid"></a>guidValue (guid)

Per i campi di tipo **GUID**, questa proprietà passa il valore dell'identificatore univoco globale (GUID) del campo tra il server e l'app.

### <a name="int64value-int64"></a>int64Value (int64)

Per i campi di tipo **Int64**, questa proprietà passa il valore int64 del campo tra il server e l'app.

### <a name="intvalue-int"></a>intValue (int)

Per i campi di tipo **Int**, questa proprietà passa il valore int del campo tra il server e l'app.

### <a name="realvalue-real"></a>realValue (real)

Per i campi di tipo **Reale**, questa proprietà passa il valore reale del campo tra il server e l'app.

### <a name="stringvalue-str"></a>stringValue (str)

Per i campi di tipo **Stringa**, questa proprietà passa il valore stringa del campo tra il server e l'app. Viene utilizzato anche per i campi di tipo **Reale** formattati come valuta. Per questi campi, la proprietà viene utilizzata per passare il codice della valuta all'app.

### <a name="datevalue-date"></a>dateValue (date)

Per i campi di tipo **Data**, questa proprietà passa il valore data del campo tra il server e l'app.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Mostra e salva un campo personalizzato nella sezione di immissione del foglio presenze

Di seguito è riportato uno screenshot dall'app per dispositivi mobili della creazione di una voce del foglio presenze. Mostra i campi predefiniti e un campo personalizzato nella sezione "Inserimento ora" chiamato "Stringa di prova" con un valore di enum di "Seconda opzione" già impostato.

![Campo personalizzato della stringa di prova nell'app](media/timesheet-entry.jpg)



Di seguito è riportato uno screenshot dall'app per dispositivi mobili dell'utente che seleziona una delle opzioni di enumerazione disponibili per il campo personalizzato "Stringa di prova".  Le due opzioni sono "Prima opzione" e "Seconda opzione" mostrate come pulsanti di opzione. La seconda opzione è attualmente selezionata.

![Pulsanti di opzione (pulsanti di opzione) per il campo personalizzato Stringa di prova](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Estendi la tabella TSTimesheetLine in modo che abbia un campo personalizzato

In scenari tipici, è probabile che i dati per un campo personalizzato nella sezione di immissione del foglio presenze vengano salvati nella tabella TSTimesheetLine. Tuttavia, è possibile utilizzare altre tabelle se i dati possono essere recuperati in base a un record TSTimesheetTrans fornito o se non dispone di un contesto di record specifico (ad esempio, se il campo è impostato come di sola lettura nei parametri del progetto) .

Tieni presente che i campi personalizzati non devono avere alcun record del database di supporto. Possono essere generati dinamicamente in base alla logica X++. Questo approccio può essere utile in scenari di sola lettura (vedi la sezione "Utilizzare la catena di comando sulla classe TSTimesheetDetails, metodo buildCustomFieldListForHeader per compilare i dettagli del foglio presenze" per un esempio di valori di campo personalizzati generati dinamicamente.)

Di seguito è riportato uno screenshot da Visual Studio dell'albero degli oggetti dell'applicazione. Mostra un'estensione della tabella TSTimesheetLine con il campo TestLineString aggiunto come campo personalizzato.

![Stringa della riga](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Utilizzare la catena di comando sul metodo buildCustomFieldList della classe TSTimesheetSettings per mostrare un campo nella sezione di immissione del foglio presenze

Questo codice controlla le impostazioni di visualizzazione per il campo nell'app. Ad esempio, controlla il tipo di campo, l'etichetta, se il campo è obbligatorio e in quale sezione viene visualizzato il campo.

L'esempio seguente mostra un campo stringa sugli inserimenti ore. Questo campo ha due opzioni, **Prima opzione** e **Seconda opzione**, disponibili tramite pulsanti di opzione (pulsanti di opzione). Il campo nell'app è associato al campo **TestLineString** aggiunto alla tabella TSTimesheetLine.

Nota l'uso del metodo **TSTimesheetCustomField::newFromMetatdata()** per semplificare l'inizializzazione delle proprietà del campo personalizzato: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** e **numberOfDecimals**. Puoi anche impostare questi parametri manualmente, come preferisci.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Utilizzare la catena di comando sul metodo buildCustomFieldListForEntry della classe TSTimesheetEntry per immettere valori in una voce del foglio presenze

Il metodo **buildCustomFieldListForEntry** viene utilizzato per immettere i valori nelle righe del foglio presenze salvate nell'app per dispositivi mobili. Acquisisce un record TSTimesheetTrans come parametro. I campi di quel record possono essere utilizzati per compilare il valore del campo personalizzato nell'app.

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Utilizzare la catena di comando sulla classe TSTimesheetEntryService per salvare una voce del foglio presenze dall'app nel database

Per salvare un campo personalizzato di nuovo nel database nell'utilizzo tipico, è necessario estendere più metodi:

- Il metodo **timesheetLineNeedsUpdating** viene utilizzato per determinare se il record di riga è stato modificato dall'utente nell'app e deve essere salvato nel database. Se le prestazioni non sono un problema, questo metodo può essere semplificato in modo che restituisca sempre **true**.
- I metodi **populateTimesheetLineFromEntryDuringCreate** e **populateTimesheetLineFromEntryDuringUpdate** possono essere estesi in modo da immettere valori nel record del database TSTimesheetLine database dal record del contratto dati TSTimesheetEntry specificato. Nell'esempio che segue, nota come il mapping tra il campo del database e il campo di immissione venga eseguito manualmente tramite codice X++.
- Il metodo **populateTimesheetWeekFromEntry** può essere esteso anche se il campo personalizzato mappato all'oggetto **TSTimesheetEntry** deve essere scritto nuovamente nella tabella del database TSTimesheetLineweek.

> [!NOTE]
> L'esempio seguente salva il valore **firstOption** o **secondOption** che l'utente seleziona nel database come valore stringa non elaborato. Se il campo del database è un campo di tipo **Enum**, questi valori possono essere mappati manualmente a un valore enum e quindi salvati in un campo enum nella tabella del database.

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Mostra un campo personalizzato nella sezione di intestazione del foglio presenze

Di seguito è riportato uno screenshot dall'app per dispositivi mobili di un utente che visualizza un foglio presenze. Il pulsante "Altre informazioni" è stato selezionato nell'angolo in alto a destra per mostrare l'opzione "Visualizza altri dettagli".  

![Comando Visualizza altri dettagli](media/show-more.png)

Di seguito è riportato uno screenshot dall'app per dispositivi mobili che mostra la sezione "Altro" di un foglio presenze. Un campo personalizzato denominato "Tasso di utilizzo di questo foglio presenze (campo personalizzato calcolato)" è stato aggiunto alla sezione dell'intestazione del foglio presenze. Un valore di sola lettura di "0,667" è impostato nel campo personalizzato.

![Sezione Altro](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Estendere la tabella TSTimesheetTable in modo che abbia un campo personalizzato

In scenari tipici, è probabile che i dati per un campo personalizzato nella sezione di intestazione verranno estratti dalla tabella TSTimesheetHeader. Tuttavia, è possibile utilizzare altre tabelle se i dati possono essere recuperati in base a un record TSTimesheetTable fornito o se non dispone di un contesto di record specifico (ad esempio, se il campo è impostato come di sola lettura nei parametri del progetto) .

Tieni presente che i campi personalizzati non devono avere alcun record del database di supporto. Possono essere generati dinamicamente in base alla logica X++. L'esempio che segue mostra questo approccio.

I campi nella sezione dell'intestazione sono sempre di sola lettura nell'app.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Utilizzare la catena di comando sul metodo buildCustomFieldList della classe TSTimesheetSettings per mostrare un campo nella sezione di intestazione

Questo codice controlla le impostazioni di visualizzazione per il campo nell'app. Ad esempio, controlla il tipo di campo, l'etichetta, se il campo è obbligatorio e in quale sezione viene visualizzato il campo.

L'esempio seguente mostra un valore calcolato nella sezione dell'intestazione nell'app.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Utilizzare la catena di comando sul metodo buildCustomFieldListForHeader della classe TSTimesheetDetails per compilare i dettagli del foglio presenze

Il metodo **buildCustomFieldListForHeader** viene utilizzato per compilare i dettagli dell'intestazione del foglio presenze nell'app per dispositivi mobili. Acquisisce un record TSTimesheetTable come parametro. I campi di quel record possono essere utilizzati per compilare il valore del campo personalizzato nell'app. L'esempio seguente non legge alcun valore dal database. Invece, utilizza la logica X + per generare un valore calcolato che viene quindi mostrato nell'app.


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

## <a name="other-configurabilityextensibility-opportunities"></a>Altre opportunità di configurabilità/estendibilità

### <a name="adding-additional-validation-for-the-app"></a>Aggiunta di ulteriore convalida per l'app

La logica esistente per la funzionalità del foglio presenze a livello di database continuerà a funzionare come previsto. Per interrompere il completamento delle operazioni di salvataggio o invio e visualizzare un messaggio di errore specifico, puoi aggiungere **throw error("message to user")** al codice tramite una catena di estensione dei comandi. Ecco tre esempi di utili metodi estensibili:

- Se **validateWrite** nella tabella TSTimesheetLine restituisce **false** durante un'operazione di salvataggio per una riga del foglio presenze, viene visualizzato un messaggio di errore app per dispositivi mobili.
- Se **validateSubmit** nella tabella TSTimesheetTable restituisce **false** durante un'operazione di invio del foglio presenze nell'app, viene visualizzato un messaggio di errore app all'utente.
- La logica che compila i campi (ad esempio, **Proprietà riga**) durante il metodo di **inserimento** nella tabella TSTimesheetLine verrà comunque eseguita.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Nascondere e contrassegnare i campi predefiniti come di sola lettura tramite la configurazione

Dai parametri del progetto, puoi rendere i campi predefiniti di sola lettura o nascosti nell'app per dispositivi mobili. Imposta le opzioni nella sezione **Fogli presenze per dispositivi mobili** nella scheda **Foglio presenze** della pagina **Parametri Gestione progetti e contabilità**.

![Parametri del progetto](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Modifica delle attività disponibili per la selezione tramite estensioni

Le attività disponibili per la selezione per un progetto vengono compilate tramite i metodi **getActivitiesForProject()** e **getActivityQuery()** nella classe **TsTimesheetProjectService**. Puoi utilizzare la catena di comando per modificare questo comportamento in modo che corrisponda al tuo scenario aziendale per le attività disponibili per la selezione per un progetto specifico.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Immissione di una categoria di progetto predefinita negli inserimenti del foglio presenze

L'immissione di una categoria di progetto predefinita negli inserimenti del foglio presenze avviene a tre livelli. Puoi utilizzare la catena di comando per estendere il comportamento a uno o tutti questi livelli per ottenere il comportamento desiderato. Viene utilizzata la gerarchia seguente:

1. L'app tenta di inserire la categoria predefinita dalla risorsa del progetto. Questa categoria predefinita è impostata nei metodi **getCurrentUserResource** e **getDelegatedResourcesForCurrentUser** nella classe **TSTimesheetSettingsService**.
2. Se la categoria predefinita non viene specificata a livello di risorsa del progetto, l'app tenta di estrarla dall'attività del progetto. Questa categoria predefinita è impostata nel metodo **getActivitiesForProject** nella classe **TSTimesheetProjectService**.
3. Se la categoria predefinita non viene specificata a livello di attività del progetto, la categoria predefinita viene acquisita dai parametri del progetto. Questa categoria predefinita è impostata nel metodo **getProjectDetailsbyRule** nella classe **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]