---
title: Utilizzare il componente aggiuntivo Project Service per lavorare in Microsoft Project | Microsoft Docs
description: In questo argomento vengono fornite informazioni su come aggiungere, configurare e utilizzare il componente aggiuntivo Microsoft Project per Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: Dynamics 365 Project Service Automation
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: efd589e0-8233-4abf-bf7e-5c1e83c4daea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0ad503ff0c27f1543d15b60714c2be46b8487d18
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752609"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Utilizzare il componente aggiuntivo Project Service Automation di pianificare il lavoro in Microsoft Project

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] semplifica la pianificazione di un progetto, incluse le stime. È possibile definire il lavoro in modo che costi, lavoro e valore delle vendite siano chiari quando la proposta definitiva viene inviata.  

 È ora possibile installare [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ed eseguire le attività di pianificazione nell'ambiente già noto di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Utilizzare le affidabili funzionalità di gestione e pianificazione di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e quindi aggiornare il piano di progetto in piano di progetto in Project Service Automation.  

> [!IMPORTANT]
> - Per utilizzare la funzionalità per la gestione dei documenti di SharePoint per archiviare i file di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] per i progetti di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], l'amministratore di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] deve abilitare la gestione dei documenti. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Abilitare la gestione dei documenti di SharePoint per specifiche entità](../admin/enable-sharepoint-document-management-specific-entities.md)  
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] è compatibile solo con [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Professional Edition 2016.  

## <a name="download-and-install-the-add-in"></a>Scaricare e installare il componente aggiuntivo.  
 Tenere pronte le informazioni sulle credenziali di accesso di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Queste informazioni sono necessarie per connettersi da [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Dall'area download, puoi scaricare il componente aggiuntivo per la versione supportata di Project Service, ovvero [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) o [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Fare clic sul collegamento Scarica.  

3.  Al termine del download, fare clic su **Sì** per installare il componente aggiuntivo.  

## <a name="configure-the-add-in"></a>Configurare il componente aggiuntivo  

1. Aprire [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e fare clic sulla scheda **Project Service**.  

2. Fare clic su **Connetti**.  

3. Immettere le informazioni di accesso e quindi fare clic su **Accedi**.  

   È possibile iniziare a utilizzare il componente aggiuntivo.  

## <a name="read-from-a-template"></a>Lettura da un modello  
 È possibile leggere da un modello creato in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] e copiato in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] per avviare la pianificazione di progetto. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Creare un modello di progetto (Project Service Automation)](../project-service/create-project-template.md)  

1.  Nella scheda **Project Service**, fare clic su **Lettura** > **Modello di progetto di Project Service Automation**.  

2.  Scegliere un modello di progetto dall'elenco e fare clic su **Apri**.  

    > [!NOTE]
    >  Per impostazione predefinita, le attività copiate dal modello nel progetto sono impostate come pianificate manualmente.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Assegnare i ruoli [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] alle risorse di progetto  

1.  Aprire un progetto e fare clic sulla barra multifunzione **Attività**.  

2.  Fare clic sul menu **Diagramma di Gantt** e quindi scegliere **Foglio risorse**.  

3.  Nel foglio delle risorse, fare clic sul menu a discesa **Ruolo di risorsa di Project Service** e selezionare un ruolo di Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Immettere le risorse per il progetto  

1.  Nella scheda Project Service, selezionare una riga e quindi fare clic su **Cerca risorse**.  

2.  Nella schermata **Prenota risorsa**, selezionare la risorsa che si desidera utilizzare per il progetto.  

3.  Fare clic su **Prenota** e quindi su **OK**.  

## <a name="publish-your-project"></a>Pubblicare il progetto  
Quando la pianificazione di progetto è completa, è necessario importare e pubblicare il progetto in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Il progetto verrà importato in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Il processo di creazione del team e dei prezzi viene applicato. Aprire il progetto in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per verificare che team, stime di progetto e struttura di suddivisione del lavoro siano stati creati. La tabella seguente mostra dove trovare i risultati:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Diagramma di Gantt**   | Importare nella schermata **Struttura di suddivisione del lavoro** di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Foglio risorse** |   Esegue l'importazione in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], schermata **Solo membri del team di progetto**   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Utilizzare l'utilizzo**    |    Esegue l'importazione in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], schermata  **Stime di progetto**.     |

**Per importare e pubblicare il progetto**  
1. Nella scheda **Project Service**, fare clic su **Pubblica** > **Nuovo progetto di Project Service Automation**.  

2. Nella finestra di dialogo **Pubblica su un nuovo progetto di Project Service** immettere il **Nome progetto** e selezionare il **Cliente**.  

3. Se lo si desidera, selezionare **Collega piano di progetto a Project Service Automation** per collegare il file del piano di progetto a Project Service Automation.  

4. Fare clic su **Pubblica**.  

   Il collegamento del file di progetto a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] imposta il file di Project come master e imposta la struttura di suddivisione del lavoro in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] su sola lettura.  Per apportare modifiche al piano di progetto, è necessario eseguire le modifiche in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e pubblicarle come aggiornamenti in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Modificare un progetto che è stato importato  
 Per apportare modifiche a un piano di progetto importato in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], è possibile procedere in due modi:  

- Aprire il file master principale e modificarlo in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Annullare il collegamento del file master principale e modificarlo direttamente in Project Service. Per impostazione predefinita, un progetto che è stato caricato da [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] è bloccato ed è modificabile solo in Project. Per modificare il file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], il collegamento del file deve essere annullato.  

### <a name="edit-in-pn_microsoft_project"></a>Modificare in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Nel menu principale fare clic su **Project Service** > **Progetti**.  

2. Nell'elenco dei progetti, aprire quello creato in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Fare clic su **Aprire in MS Project** nella barra multifunzione. Verrà aperto il file master collegato in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Annullare il collegamento di un file e modificarlo in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Nel menu principale fare clic su **Project Service** > **Progetti**.  

2. Nell'elenco dei progetti, aprire quello creato in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Fare clic su **Scollega da MS Project** nella barra multifunzione.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Caricare un file di Project in gruppi di Office o SharePoint  
 È possibile caricare il file di Project in SharePoint e trovarlo nei documenti associati per il progetto di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  È necessario chiedere all'amministratore di configurare la gestione dei documenti di SharePoint e abilitarla per l'entità di Project. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configurare l'integrazione di SharePoint](../admin/set-up-sharepoint-integration.md)  

 È inoltre possibile caricare il file di Project in [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] se Gruppi di Office è configurato. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Collaborare con i colleghi utilizzando Gruppi di Office 365](../basics/collaborate-with-colleagues-using-office-365-groups.md)  

### <a name="upload-a-file-for-sharepoint"></a>Caricare un file per SharePoint  

1. Nel menu principale fare clic su **Project Service** > **Carica**.  

2. Selezionare **In documenti di progetto di Project Service Automation**.  

3. Nella finestra di dialogo **Abilita Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selezionare **Sì** o **No**.  

   - Se si fa clic su **Sì** è possibile selezionare il pulsante **Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** in Project Service Automation, avviare [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e caricare il file di Project dalla raccolta documenti di SharePoint.  

   - Se si fa clic su **No** il collegamento per il pulsante **Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** non funzionerà.  

4. Il file di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] può essere trovato in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nella sezione **Documenti** del progetto [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] specifico.  

### <a name="upload-a-file-for-office-groups"></a>Caricare un file per i Gruppi di Office  

1. Nel menu principale fare clic su **Project Service** > **Carica**.  

2. Selezionare **In documenti di progetto di Project Service Automation**.  

3. Nella finestra di dialogo **Abilita Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selezionare **Sì** o **No**.  

   - Se si fa clic su **Sì** è possibile selezionare il pulsante **Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** in Project Service Automation, avviare [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e caricare il file di Project dalla raccolta documenti di SharePoint.  

   - Se si fa clic su **No** il collegamento per il pulsante **Apri in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** non funzionerà.  

4. Il file di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] può essere trovato in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nella sezione **Documenti** del progetto [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] specifico.  

## <a name="publish--your-project-as-a-template"></a>Pubblicare il progetto come modello  
 È possibile salvare il progetto e riutilizzarlo salvandolo come modello di progetto in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  I modelli di progetto sono piani di progetto riutilizzabili in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Creare un modello di progetto (Project Service Automation)](../project-service/create-project-template.md)  

1. Nella scheda **Project Service**, fare clic su **Pubblica** > **Nuovo modello di progetto di Project Service Automation**.  

2. Nella finestra di dialogo **Pubblica in un nuovo progetto in modello di Project Service** immettere il **nome del modello di progetto**.  

3. Se lo si desidera, selezionare **Collega piano di progetto a Project Service Automation** per collegare il file di Project a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Fare clic su **Pubblica**.  

Il collegamento del file di Project a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] imposta il file di Project come master e imposta la struttura di suddivisione del lavoro nel modello di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] su sola lettura.  Per apportare modifiche al piano di progetto, è necessario eseguire le modifiche in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e pubblicarle come aggiornamenti in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

### <a name="see-also"></a>Vedi anche  
 [Guida del responsabile di progetto](../project-service/project-manager-guide.md)