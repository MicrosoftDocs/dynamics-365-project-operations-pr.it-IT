---
title: Considerazioni sull'aggiornamento - Da Microsoft Dynamics 365 Project Service Automation versione 2.x o 1.x alla versione 3
description: In questo argomento vengono fornite informazioni sulle considerazioni che devi eseguire quando esegui l'aggiornamento da Project Service Automation versione 2.x o 1.x alla versione 3.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: e4fae2ea-9013-488e-a666-f7192dd42c0b
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: ba710eb8c07df7dac97e8b911184c00b87b14548
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752680"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Considerazioni sull'aggiornamento - Da PSA versione 2.x o 1.x alla versione 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation e Field Service
Dynamics 365 Project Service Automation e Dynamics 365 Field Service utilizzano la soluzione URS (Universal Resourcing Scheduling) per la pianificazione delle risorse. Se nell'istanza sono presenti sia Project Service Automation che Field Service, è necessario pianificare l'aggiornamento di entrambe le soluzioni all'ultima versione (versione 3.x per Project Service Automation, versione 8.x per Field Service). L'aggiornamento di Project Service Automation o Field Service installerà l'ultima versione di URS, di conseguenza un comportamento incoerente è possibile se entrambe le soluzioni Project Service Automation e Field Service nella stessa istanza non vengono aggiornate all'ultima versione.

## <a name="resource-assignments"></a>Assegnazioni di risorse
In Project Service Automation versione 2 e versione 1, le assegnazioni di attività erano archiviate come attività figlio (dette anche attività riga) nell'**entità Attività** e indirettamente correlate all'entità **Assegnazione risorse**. L'attività riga era visibile nella finestra popup di assegnazione nella Struttura di suddivisione del lavoro.

![Attività riga nella Struttura di suddivisione del lavoro in Project Service Automation versione 2 e versione 1](media/upgrade-line-task-01.png)

Nella versione 3 di Project Service Automation, lo schema sottostante di assegnazione di risorse prenotabili ad attività è stato modificato. L'attività riga è stata deprecata ed esiste una relazione diretta 1:1 tra l'attività nell'**entità Attività** e il membro del team nell'entità **Assegnazione risorse**. Le attività assegnate a un membro del team di progetto ora vengono archiviate direttamente nell'entità Assegnazione risorse.  

Queste modifiche hanno un impatto sull'aggiornamento di qualsiasi progetto esistente che ha assegnazioni di risorse per le risorse prenotabili denominate e le risorse generiche in un team di progetto. In questo argomento vengono fornite informazioni che devono essere prese in considerazione per i progetti durante l'aggiornamento alla versione 3. 

### <a name="tasks-assigned-to-named-resources"></a>Attività assegnate a risorse denominate
Con l'entità attività sottostante, le attività nella versione 2 e nella versione 1 consentivano ai membri del team di creare un ruolo diverso da quello definito predefinito. Ad esempio, a Teresa Fanucci, alla quale veniva assegnato, per impostazione predefinita, il ruolo di Program Manager, poteva essere assegnata un'attività con il ruolo di Sviluppatore. Nella versione 3, il ruolo di un membro del team denominato è sempre predefinito, quindi qualsiasi attività a cui Teresa Fanucci è assegnata utilizza il ruolo predefinito di Program Manager.

Se hai assegnato una risorsa a un'attività al di fuori del relativo ruolo predefinito nella versione 2 e nella versione 1, quando esegui l'aggiornamento, alla risorsa denominata viene assegnato il ruolo predefinito per tutte le assegnazioni di attività, indipendentemente dall'assegnazione di ruolo nella versione 2. Ciò darà luogo a differenze nelle stime calcolate dalla versione 2 o versione 1 alla versione 3 in quanto le stime vengono calcolate in base al ruolo della risorsa e non all'assegnazione di attività riga. Ad esempio, nella versione 2, due attività sono state assegnate a Lucia Cattaneo. Il ruolo nell'attività riga per l'attività 1 è Sviluppatore e per l'attività 2 è Program Manager. Lucia Cattaneo ha il ruolo predefinito di Program Manager.

![Molteplici ruoli assegnati a una risorsa](media/upgrade-multiple-roles-02.png)

Poiché i ruoli Sviluppatore e Program Manager differiscono, le stime di costo e vendite sono come segue:

![Stime di costo per ruoli risorsa](media/upggrade-cost-estimates-03.png)

![Stime di vendite per ruoli risorsa](media/upgrade-sales-estimates-04.png)

Quando esegui l'aggiornamento alla versione 3, le attività riga vengono sostituite con assegnazioni di risorsa nell'attività del membro del team di risorse prenotabili. L'assegnazione utilizzerà il ruolo predefinito della risorsa prenotabile. Nell'illustrazione seguente, Lucia Cattaneo, che ha il ruolo di Program Manager, è la risorsa.

![Assegnazioni di risorse](media/resource-assignment-v2-05.png)

Poiché le stime sono basate sul ruolo predefinito della risorsa, le stime di costi e vendite possono cambiare. Nota che nell'illustrazione seguente, il ruolo **Sviluppatore** non è più visibile in quanto ora il ruolo è quello predefinito della risorsa prenotabile.

![Stime dei costi per ruoli predefiniti](media/resource-assignment-cost-estimate-06.png)
![Stima di vendita per ruoli predefiniti](media/resource-assignment-sales-estimate-07.png)

Dopo aver completato l'aggiornamento, puoi modificare il ruolo di un membro del team affinché sia diverso da quello predefinito assegnato. Tuttavia, se modifichi il ruolo di un membro del team, verrà modificato in tutte le relative attività assegnate in quanto ai membri del team non è più consentito assegnare più ruoli nella versione 3.

![Aggiornare un ruolo risorsa](media/resource-role-assignment-08.png)

Ciò è vero anche per le attività riga che erano assegnate a risorse denominate quando si modificava l'unità organizzativa della risorsa da quella predefinita a un'altra unità organizzativa. Dopo l'aggiornamento alla versione 3, l'assegnazione utilizza l'unità organizzativa predefinita della risorsa anziché quella impostata nell'attività riga.

### <a name="tasks-assigned-to-generic-resources"></a>Attività assegnate a risorse generiche
Nella versione 2 e nella versione 1, puoi impostare il ruolo e l'unità organizzativa in un'attività e quindi utilizzare la funzionalità **Genera team** per generare risorse generiche in base agli attributi impostati per l'attività. Nella versione 3, crei i membri del team generici con il ruolo e l'unità organizzativa e quindi assegni i membri del team ad attività.

Nella versione 2 e nella versione 1, i progetti con risorse generiche possono avere due stati oppure una combinazione di entrambi a livello di attività. Ad esempio, sono possibili i seguenti scenari:

- Attività con ruoli e unità organizzative impostati, ma nessuna assegnazione di risorsa associata generata.
- Attività con assegnazioni di risorsa dei membri del team generici assegnate creando una risorsa generica con la funzionalità **Genera team**.

Prima di iniziare l'aggiornamento, è consigliabile rigenerare il team per ogni progetto con attività assegnate a risorse generiche o per il quale non è ancora stato eseguita la procedura di generazione di team.

Per le attività assegnate a membri del team generici generati con **Genera team**, l'aggiornamento manterrà la risorsa generica nel team e lascerà l'assegnazione a quel membro del team generico. È consigliabile generare il requisito di risorsa per il membro del team generico dopo l'aggiornamento ma prima di prenotare o inviare una richiesta di risorsa. Ciò preserverà qualsiasi assegnazione di unità organizzativa per i membri del team generici che è differente dall'unità organizzativa di contratto del progetto.

Ad esempio, nel progetto Progetto Z, l'unità organizzativa di contratto è Contoso US. Nel piano di progetto, alle attività di test nella fase di implementazione è stato assegnato il ruolo Consulente Tecnico e l'unità organizzativa assegnata è Contoso India.

![Assegnazione dell'organizzazione nella fase di implementazione](media/org-unit-assignment-09.png)

Dopo la fase di implementazione, l'attività di test di integrazione viene assegnata al ruolo Consulente Tecnico, ma l'organizzazione è impostata su Contoso US.  

![Assegnazione dell'attività di test di integrazione](media/org-unit-generate-team-10.png)

Quando generi un team per il progetto, due membri del team generici vengono creati a seguito delle unità organizzative differenti per le attività. Al consulente tecnico 1 vengono assegnate le attività di Contoso India e al consulente tecnico 2 le attività di Contoso US.  

![Membri del team generici generati](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> Nelle versioni 2 e 1 di Project Service Automation, l'unità organizzativa non viene aggiunta al membro del team ma rimane nell'attività riga.

![Attività riga in Project Service Automation versione 2 e versione 1](media/line-tasks-12.png)

L'unità organizzativa è visualizzata nella vista Stime. 

![Stime dell'unità organizzativa](media/org-unit-estimates-view-13.png)
 
Al termine dell'aggiornamento, l'unità organizzativa dell'attività riga che corrisponde al membro del team generico viene aggiunta al membro del team generico e l'attività riga viene rimossa. Per questo motivo, è consigliabile, prima di eseguire l'aggiornamento, di generare o rigenerare il team per ogni progetto contenente risorse generiche.

Per le attività assegnate a un ruolo con un'unità organizzativa differente dall'unità organizzativa del progetto di contratto e se un team non è stato generato, l'aggiornamento creerà un membro del team generico per il ruolo, ma utilizzerà l'unità contratto del progetto per l'unità organizzativa del membro del team. Se consideriamo l'esempio con il Progetto Z, ciò significa che all'unità organizzativa di contratto Contoso US e alle attività di test del piano di progetto nella fase di implementazione è stato assegnato il ruolo Consulente Tecnico con l'unità organizzativa assegnata a Contoso India. L'attività di test di integrazione completata dopo la fase di implementazione è stata assegnata al ruolo Consulente Tecnico. L'unità organizzativa è Contoso US e un team non è stato generato. L'aggiornamento crea un membro del team generico, un Consulente Tecnico con le ore assegnate di tutte e tre le attività e un'unità organizzativa Contoso US, ovvero l'unità organizzativa di contratto del progetto.   
 
La modifica dell'impostazione predefinita delle differenti unità organizzative di gestione risorse per i membri del team non generati è il motivo per cui consigliamo di generare o rigenerare il team per ogni progetto contenente risorse generiche prima di eseguire l'aggiornamento. In questo, non si perderanno le assegnazioni delle unità organizzative.

