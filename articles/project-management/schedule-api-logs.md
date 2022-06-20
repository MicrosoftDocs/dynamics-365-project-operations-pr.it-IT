---
title: Log di pianificazione del progetto
description: Questo articolo fornisce informazioni ed esempi utili per usare i log di pianificazione del progetto per tenere traccia degli errori correlati al servizio di pianificazione del progetto e alle API di pianificazione del progetto.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923700"
---
# <a name="project-scheduling-logs"></a>Log di pianificazione del progetto

_**Si applica a**: Project Operations per scenari basati su articoli non stoccati/risorse e Distribuzione semplice: dalla transazione alla fatturazione proforma_, _Project for the Web_

Microsoft Dynamics 365 Project Operations usa [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) come principale motore di pianificazione. Invece di usare le interfacce API Web standard di Microsoft Dataverse, Project Operations usa le nuove API di pianificazione del progetto per creare, aggiornare ed eliminare attività di progetto, assegnazioni di risorse, dipendenze di attività, bucket di progetto e membri dei team di progetto. Quando le operazioni di creazione, aggiornamento o eliminazione vengono eseguite a livello di codice sulle entità della struttura di suddivisione del lavoro, potrebbero tuttavia verificarsi degli errori. Per tenere traccia di questi errori e della cronologia delle operazioni, sono stati implementati due nuovi log amministrativi: **Set di operazioni** e **Servizio di pianificazione del progetto (PSS)**. Per accedere a questi log, vai a **Impostazioni** \> **Integrazione di pianificazione**.

Nella figura seguente è illustrato il modello di dati per i log di pianificazione del progetto.

![Modello di dati per i log di pianificazione del progetto.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Log Set di operazioni

Il log Set di operazioni tiene traccia dell'esecuzione di un set di operazioni usato per eseguire una o più operazioni di creazione, aggiornamento o eliminazione in un batch su progetti, attività di progetto, assegnazioni di risorse, dipendenze di attività, bucket di progetto e membri dei team di progetto. Il campo **Operazione in stato** mostra lo stato generale del set di operazioni. I dettagli del payload del set di operazioni vengono acquisiti nei record Dettagli set di operazioni correlati.

### <a name="operation-set"></a>Set di operazioni

La tabella seguente mostra i campi relativi all'entità **Set di operazioni**.

| SchemaName            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Data/ora in cui il set di operazioni è stato completato o non è riuscito.                                                | CompletedOn            |
| msdyn_correlationid   | Valore **correlationId** della richiesta.                                                                  | CorrelationId          |
| msdyn_description     | Descrizione del set di operazioni.                                                                        | Description            |
| msdyn_executedon      | Data/ora in cui è stato eseguito il record.                                                                       | Data esecuzione            |
| msdyn_operationsetId  | Identificatore univoco delle istanze di entità.                                                                   | OperationSet           |
| msdyn_Project         | Progetto correlato al set di operazioni.                                                            | Project                |
| msdyn_projectid       | Valore **projectId** della richiesta.                                                                      | ProjectId (deprecato) |
| msdyn_projectName     | Non applicabile.                                                                                              | Non applicabile         |
| msdyn_PSSErrorLog     | Identificatore univoco del log degli errori del servizio di pianificazione del progetto associato al set di operazioni. | Registro errori PSS          |
| msdyn_PSSErrorLogName | Non applicabile.                                                                                              | Non applicabile         |
| msdyn_status          | Stato del set di operazioni.                                                                             | Status                 |
| msdyn_statusName      | Non applicabile.                                                                                              | Non applicabile         |
| msdyn_useraadid       | ID oggetto Azure Active Directory (Azure AD) dell'utente a cui appartiene la richiesta.                     | UserAADID              |

### <a name="operation-set-detail"></a>Dettagli set di operazioni

La tabella seguente mostra i campi relativi all'entità **Dettagli set di operazioni**.

| SchemaName                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Campi Dataverse serializzati per la richiesta.                                            | CdsPayload            |
| msdyn_entityname           | Nome dell'entità per la richiesta.                                                     | EntityName            |
| msdyn_httpverb             | Metodo di richiesta.                                                                         | Verbo HTTP (deprecato) |
| msdyn_httpverbName         | Non applicabile.                                                                             | Non applicabile        |
| msdyn_operationset         | Identificatore univoco del set di operazioni a cui appartiene questo record.                      | OperationSet          |
| msdyn_operationsetdetailId | Identificatore univoco delle istanze di entità.                                                  | Dettagli OperationSet   |
| msdyn_operationsetName     | Non applicabile.                                                                             | Non applicabile        |
| msdyn_operationtype        | Tipo di operazione dei dettagli del set di operazioni.                                             | OperationType         |
| msdyn_operationtypeName    | Non applicabile.                                                                             | Non applicabile        |
| msdyn_psspayload           | Campi serializzati del servizio di pianificazione del progetto (PSS) per la richiesta.                           | PssPayload            |
| msdyn_recordid             | Identificatore del record della richiesta.                                                       | ID record             |
| msdyn_requestnumber        | Numero generato automaticamente che identifica l'ordine in cui sono state ricevute le richieste. | Numero richiesta        |

## <a name="project-scheduling-service-error-logs"></a>Log degli errori del servizio di pianificazione del progetto

I log degli errori del servizio di pianificazione del progetto acquisiscono gli errori che si verificano quando il servizio di pianificazione del progetto tenta di eseguire un'operazione **Salva** o **Apri**. Esistono tre scenari supportati in cui vengono generati questi log:

- Le azioni avviate dall'utente restituiscono errori critici (ad esempio, non è possibile creare un'assegnazione a causa di privilegi mancanti).
- Il servizio di pianificazione del progetto non è in grado di creare, aggiornare, eliminare o eseguire altre operazioni a catena a livello di codice su un'entità.
- L'utente riscontra errori quando un record non si apre (ad esempio, quando viene aperto un progetto o vengono aggiornate le informazioni di un membro del team).

### <a name="project-scheduling-service-log"></a>Log del servizio di pianificazione del progetto

La tabella seguente mostra i campi inclusi nel log del servizio di pianificazione del progetto.

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Stack di chiamate dell'eccezione.                                               | Stack di chiamate     |
| msdyn_correlationid | ID di correlazione dell'errore.                                               | CorrelationId  |
| msdyn_errorcode     | Campo che viene usato per archiviare il codice di errore Dataverse o il codice di errore HTTP. | Codice di errore     |
| msdyn_HelpLink      | Collegamento alla documentazione della Guida pubblica.                                       | Collegamento della Guida      |
| msdyn_log           | Log del servizio di pianificazione del progetto.                                   | Log            |
| msdyn_project       | Progetto associato al log degli errori.                             | Project        |
| msdyn_projectName   | Nome del progetto se il payload del set di operazioni verrà mantenuto. | Non applicabile |
| msdyn_psserrorlogId | Identificatore univoco delle istanze di entità.                                     | Registro errori PSS  |
| msdyn_SessionId     | ID sessione del progetto.                                                        | ID sessione     |

## <a name="error-log-cleanup"></a>Pulizia del log degli errori

Per impostazione predefinita, sia i log degli errori del servizio di pianificazione del progetto sia il log del set di operazioni possono essere eliminati ogni 90 giorni. Tutti i record più vecchi di 90 giorni verranno eliminati. Modificando il valore del campo **msdyn_StateOperationSetAge** nella pagina **Parametri progetto**, gli amministratori possono tuttavia rettificare l'intervallo di pulizia in modo che sia compreso tra 1 e 120 giorni. Sono disponibili diversi metodi per modificare questo valore:

- Personalizza l'entità **Parametro progetto** creando una pagina personalizzata e aggiungendo il campo **Durata set di operazioni non aggiornate**.
- Usa il codice client basato su [WebApi Software Development Kit (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Usa il codice Service SDK basato sul metodo **updateRecord** di Xrm SDK (riferimento API client) nelle app basate su modello. Power Apps include una descrizione e i parametri supportati per il metodo **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
