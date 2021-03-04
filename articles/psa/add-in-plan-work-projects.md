---
title: Pianificare il lavoro in Microsoft Project con il componente aggiuntivo Project Service
description: In questo argomento vengono fornite informazioni su come utilizzare il componente aggiuntivo Microsoft Project per Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 87387ff870a7ef3ed0689f4ae38daad8cf220b46
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145948"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Pianificare il lavoro in Microsoft Project con il componente aggiuntivo Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] semplifica la pianificazione di un progetto, incluse le stime. È possibile definire il lavoro in modo che costi, lavoro e valore delle vendite siano chiari quando la proposta definitiva viene inviata.  

Puoi installare [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ed eseguire le attività di pianificazione nell'ambiente già noto di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Utilizzare le affidabili funzionalità di gestione e pianificazione di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e quindi aggiornare il piano di progetto in piano di progetto in Project Service Automation.  

> [!IMPORTANT]
> - Per utilizzare la funzionalità per la gestione dei documenti di SharePoint per archiviare i file di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] per i progetti di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], l'amministratore di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] deve abilitare la gestione dei documenti. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] è compatibile solo con [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Professional Edition 2016.  

## <a name="download-and-install-the-add-in"></a>Scaricare e installare il componente aggiuntivo.  
 Tenere pronte le informazioni sulle credenziali di accesso di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Queste informazioni sono necessarie per connettersi da [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Dall'area download, puoi scaricare il componente aggiuntivo per la versione supportata di Project Service, ovvero [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) o [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Seleziona il collegamento per il download.  

3.  Al termine del download, seleziona **Sì** per installare il componente aggiuntivo.  

## <a name="configure-the-add-in"></a>Configurare il componente aggiuntivo  

1. Apri [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e seleziona la scheda **Project Service**.  

2. Seleziona **Connetti**.  

3. Immetti le informazioni di accesso e quindi seleziona **Accedi**.  

   È possibile iniziare a utilizzare il componente aggiuntivo.  

## <a name="read-from-a-template"></a>Lettura da un modello  
 È possibile leggere da un modello creato in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] e copiato in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] per avviare la pianificazione di progetto. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Creare un modello di progetto (Project Service Automation)](../psa/create-project-template.md)  

1.  Nella scheda **Project Service**, seleziona **Lettura** > **Modello di progetto di Project Service Automation**.  

2.  Scegli un modello di progetto dall'elenco e seleziona **Apri**.  

    > [!NOTE]
    >  Per impostazione predefinita, le attività copiate dal modello nel progetto sono impostate come pianificate manualmente.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Assegnare i ruoli [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] alle risorse di progetto  

1.  Apri un progetto e seleziona la barra multifunzione **Attività**.  

2. Seleziona il menu **Diagramma di Gantt** e quindi scegli **Foglio risorse**.  

3. Nel foglio delle risorse, seleziona il menu a discesa **Ruolo di risorsa di Project Service** e scegli un ruolo di Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Immettere le risorse per il progetto  

1.  Nella scheda Project Service, seleziona una riga e seleziona **Cerca risorse**.  

2.  Nella schermata **Prenota risorsa**, selezionare la risorsa che si desidera utilizzare per il progetto.  

3.  Seleziona **Prenota** e quindi **OK**.  

## <a name="publish-your-project"></a>Pubblicare il progetto  
Quando la pianificazione di progetto è completa, è necessario importare e pubblicare il progetto in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Il progetto verrà importato in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Il processo di creazione del team e dei prezzi viene applicato. Aprire il progetto in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per verificare che il team, le stime di progetto e la struttura di suddivisione del lavoro siano stati creati. La tabella seguente mostra dove trovare i risultati.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Diagramma di Gantt**   | Importare nella schermata **Struttura di suddivisione del lavoro** di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Foglio risorse** |   Esegue l'importazione in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], schermata **Solo membri del team di progetto**   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Utilizzare l'utilizzo**    |    Esegue l'importazione in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], schermata **Stime di progetto**.     |

**Per importare e pubblicare il progetto**  
1. Nella scheda **Project Service**, vai a **Pubblica** > **Nuovo progetto di Project Service Automation**.  

2. Nella finestra di dialogo **Pubblica su un nuovo progetto di Project Service** immetti il **Nome progetto** e seleziona il **Cliente**.  

3. Facoltativamente, seleziona **Collega piano di progetto a Project Service Automation** per collegare il file del piano di progetto a Project Service Automation.  

4. Seleziona **Pubblica**.  

   Il collegamento del file di progetto a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] imposta il file di Project come master e imposta la struttura di suddivisione del lavoro in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] su sola lettura.  Per apportare modifiche al piano di progetto, è necessario eseguire le modifiche in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e pubblicarle come aggiornamenti in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Modificare un progetto che è stato importato  
 Per apportare modifiche a un piano di progetto importato in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], è possibile procedere in due modi:  

- Aprire il file master principale e modificarlo in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Annullare il collegamento del file master principale e modificarlo direttamente in Project Service. Per impostazione predefinita, un progetto che è stato caricato da [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] è bloccato ed è modificabile solo in Project. Per modificare il file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], il collegamento del file deve essere annullato.  

### <a name="edit-in-pn_microsoft_project"></a>Modifica in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Nel menu principale vai a **Project Service** > **Progetti**.  

2. Nell'elenco dei progetti, apri quello che hai creato in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Seleziona **Apri in MS Project** nella barra multifunzione. Verrà aperto il file master collegato in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Annullare il collegamento di un file e modificarlo in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Nel menu principale vai a **Project Service** > **Progetti**.  

2. Nell'elenco dei progetti, apri quello che hai creato in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Seleziona **Scollega da MS Project** nella barra multifunzione.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Caricare un file di Project in gruppi di Office o SharePoint  
 È possibile caricare il file di Project in SharePoint e trovarlo nei documenti associati per il progetto di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  È necessario chiedere all'amministratore di configurare la gestione dei documenti di SharePoint e abilitarla per l'entità di Project. 

 È inoltre possibile caricare il file di Project in [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] se Gruppi di Office è configurato.

### <a name="upload-a-file-for-sharepoint"></a>Caricare un file per SharePoint  

1. Nel menu principale vai a **Project Service** > **Carica**.  

2. Selezionare **In documenti di progetto di Project Service Automation**.  

3. Nella finestra di dialogo **Abilita Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** seleziona **Sì** o **No**.  

   - Se selezioni **Sì** potrai selezionare il pulsante **Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** in Project Service Automation, avviare [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e caricare il file di Project dalla raccolta documenti di SharePoint.  

   - Se selezioni **No**, il collegamento per **Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** non funzionerà.  

4. Il file di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] può essere trovato in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nella sezione **Documenti** del progetto [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] specifico.  

### <a name="upload-a-file-for-office-groups"></a>Caricare un file per i Gruppi di Office  

1. Nel menu principale vai a **Project Service** > **Carica**.  

2. Selezionare **In documenti di progetto di Project Service Automation**.  

3. Nella finestra di dialogo **Abilita Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** seleziona **Sì** o **No**.  

   - Se selezioni **Sì** potrai selezionare il pulsante **Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** in Project Service Automation, avviare [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e caricare il file di Project dalla raccolta documenti di SharePoint.  

   - Se selezioni **No**, il collegamento per **Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** non funzionerà.  

4. Il file di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] può essere trovato in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nella sezione **Documenti** del progetto [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] specifico.  

## <a name="publish--your-project-as-a-template"></a>Pubblicare il progetto come modello  
 È possibile salvare il progetto e riutilizzarlo salvandolo come modello di progetto in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. I modelli di progetto sono piani di progetto riutilizzabili in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Per ulteriori informazioni, vedi [Creare un modello di progetto (Project Service Automation)](../psa/create-project-template.md). 

1. Nella scheda **Project Service**, vai a **Pubblica** > **Nuovo modello di progetto di Project Service Automation**.  

2. Nella finestra di dialogo **Pubblica in un nuovo progetto in modello di Project Service** immetti il **nome del modello di progetto**.  

3. Facoltativamente, seleziona **Collega piano di progetto a Project Service Automation** per collegare il file del piano di Project a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Seleziona **Pubblica**.  

Il collegamento del file di Project a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] imposta il file di Project come master e imposta la struttura di suddivisione del lavoro nel modello di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] su sola lettura.  Per apportare modifiche al piano di progetto, è necessario eseguire le modifiche in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e pubblicarle come aggiornamenti in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Leggere una pianificazione caricata di risorse

Durante la lettura di un progetto da Project Service Automation, il calendario della risorsa non viene sincronizzato con il client desktop. Se sono presenti differenze nella durata, nello svolgimento o nella fine delle attività, è probabile che le risorse e il client desktop non abbiano lo stesso calendario del modello delle ore di lavoro applicato al progetto.


## <a name="data-synchronization"></a>Sincronizzazione dati
Le tabelle in questa sezione forniscono informazioni sulla sincronizzazione dei dati di entità tra Project Service Automation e il componente aggiuntivo desktop di Microsoft Project.

### <a name="project-task-entity-table"></a>Tabella entità Attività di progetto
La tabella seguente illustra come i dati dell'entità Attività di progetto vengono sincronizzati tra Project Service Automation e il componente aggiuntivo desktop di Microsoft Project.

| **Entità** | **Campo** | **Da Microsoft Project a Project Service Automation** | **Da Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Attività di progetto | Data di scadenza | Synchronized | Non sincronizzato |
| Attività di progetto | Lavoro richiesto stimato | Synchronized | Non sincronizzato |
| Attività di progetto | ID client di MS Project | Synchronized | Non sincronizzato |
| Attività di progetto | Attività padre | Synchronized | Non sincronizzato |
| Attività di progetto | Project | Synchronized | Non sincronizzato |
| Attività di progetto | Attività di progetto | Synchronized | Non sincronizzato |
| Attività di progetto | Nome attività di progetto | Synchronized | Non sincronizzato |
| Attività di progetto | Unità gestione risorse (deprecata nella v3.0) | Synchronized | Non sincronizzato |
| Attività di progetto | Durata pianificata | Synchronized | Non sincronizzato |
| Attività di progetto | Data di inizio | Synchronized | Non sincronizzato |
| Attività di progetto | ID struttura di suddivisione del lavoro | Synchronized | Non sincronizzato |

### <a name="team-member-entity-table"></a>Tabella entità Membro del team
La tabella seguente illustra come i dati dell'entità Membro del team vengono sincronizzati tra Project Service Automation e il componente aggiuntivo desktop di Microsoft Project.

| **Entità** | **Campo** | **Da Microsoft Project a Project Service Automation** | **Da Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Membro del team | ID client di MS Project | Synchronized | Non sincronizzato |
| Membro del team | Nome posizione | Synchronized | Non sincronizzato |
| Membro del team | progetto | Synchronized | Synchronized |
| Membro del team | Team di progetto | Synchronized | Synchronized |
| Membro del team | Unità gestione risorse | Non sincronizzato | Synchronized |
| Membro del team | Ruolo | Non sincronizzato | Synchronized |
| Membro del team | Ore lavorative | Non sincronizzato | Non sincronizzato |

### <a name="resource-assignment-entity-table"></a>Tabella entità Assegnazione risorse
La tabella seguente illustra come i dati dell'entità Assegnazione risorse vengono sincronizzati tra Project Service Automation e il componente aggiuntivo desktop di Microsoft Project.

| **Entità** | **Campo** | **Da Microsoft Project a Project Service Automation** | **Da Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Assegnazione risorse | Dal | Synchronized | Non sincronizzato |
| Assegnazione risorse | Ore | Synchronized | Non sincronizzato |
| Assegnazione risorse | ID client di MS Project | Synchronized | Non sincronizzato |
| Assegnazione risorse | Lavoro pianificato | Synchronized | Non sincronizzato |
| Assegnazione risorse | Project | Synchronized | Non sincronizzato |
| Assegnazione risorse | Team di progetto | Synchronized | Non sincronizzato |
| Assegnazione risorse | Assegnazione risorse | Synchronized | Non sincronizzato |
| Assegnazione risorse | Attività | Synchronized | Non sincronizzato |
| Assegnazione risorse | Fino al | Synchronized | Non sincronizzato |

### <a name="project-task-dependencies-entity-table"></a>Tabella entità Dipendenze attività di progetto
La tabella seguente illustra come i dati dell'entità Dipendenze attività di progetto vengono sincronizzati tra Project Service Automation e il componente aggiuntivo desktop di Microsoft Project.

| **Entità** | **Campo** | **Da Microsoft Project a Project Service Automation** | **Da Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Dipendenze attività di progetto | Dipendenza attività di progetto | Synchronized | Non sincronizzato |
| Dipendenze attività di progetto | Tipo di collegamento | Synchronized | Non sincronizzato |
| Dipendenze attività di progetto | Attività precedente | Synchronized | Non sincronizzato |
| Dipendenze attività di progetto | Project | Synchronized | Non sincronizzato |
| Dipendenze attività di progetto | Attività successiva | Synchronized | Non sincronizzato |

### <a name="additional-resources"></a>Risorse aggiuntive
 [Guida del responsabile di progetto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]