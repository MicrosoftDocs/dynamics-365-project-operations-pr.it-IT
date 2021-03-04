---
title: Impostare e applicare i dati di configurazione in Common Data Service
description: Questo argomento fornisce informazioni sull'impostazione e l'applicazione dei dati di configurazione in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642233"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Impostare e applicare i dati di configurazione in Common Data Service 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Prerequisiti

Prima di iniziare a configurare i dati in Common Data Service (CDS), devono essere soddisfatti i seguenti prerequisiti:

1.  Provisioning di un ambiente CDS e un ambiente Dynamics 365 Finance per Project Operations.
2.  Informazioni sulla persona giuridica di Dynamics 365 Finance condivise nell'ambiente CDS. Ciò significa che l'entità **Società** in CDS ha i seguenti record aziendali:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Installare i dati di impostazione e configurazione

1. Scarica, sblocca e decomprimi il [pacchetto dati di impostazione e configurazione](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Vai alla cartella decompressa ed esegui il file eseguibile *DataMigrationUtility*.
3. A pagina 1 del Configurazione guidata della migrazione (CMT) di Common Data Service, seleziona **Importa dati** e poi seleziona **Continua**.

![Migrazione della configurazione](./media/1ConfigurationMigration.png)

4. A pagina 2 della procedura guidata CMT, seleziona **Microsoft 365** come **Tipo di distribuzione**.
5. Seleziona le caselle di controllo **Visualizza l'elenco delle organizzazioni disponibili** e **Mostra avanzate**.
6. Seleziona l'area del tenant, inserisci le tue credenziali e seleziona **Accedi**.

![Accesso alla configurazione](./media/2ConfigurationSignin.png)

7. A pagina 3, dall'elenco delle organizzazioni nel tenant, seleziona l'organizzazione in cui vuoi importare i dati dimostrativi e seleziona **Accedi**.
8. A pagina 4, seleziona il file zip *SampleSetupAndConfigData* dalla cartella decompressa.

![Selezione del file zip](./media/3ZipFile.png)

![Selezionare un file](./media/4SelectAFile.png)

9. Dopo aver selezionato il file zip, seleziona **Importa dati**.

![Importa dati](./media/5ImportData.png)

10. L'importazione verrà eseguita per circa due-dieci minuti a seconda della velocità della rete. Al termine dell'importazione, esci dalla procedura guidata CMT. 
11. Nella tua organizzazione controlla i dati nelle seguenti 19 entità:

  - Valuta
  - Unità organizzativa
  - Contatto
  - Gruppo imposte
  - Gruppo clienti
  - Unità
  - Unità di vendita
  - Listino prezzi
  - Listino prezzi di parametro progetto
  - Frequenza di fatturazione
  - Categoria di risorsa prenotabile
  - Categoria di transazione
  - Categoria di spesa
  - Prezzo ruolo
  - Prezzo categoria di transazione
  - Caratteristica
  - Risorsa prenotabile
  - Associazione categoria di risorsa prenotabile
  - Caratteristica di risorsa prenotabile

![Completare l'importazione](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Aggiornare le configurazioni di Project Operations

1. Passa all‘ambiente CE. Puoi trovarlo aprendo l'[interfaccia di amministrazione di Power Platform](https://admin.powerplatform.microsoft.com/environments), selezionando l'ambiente e quindi selezionando **Apri ambiente**. 

![Aprire l'ambiente](./media/7OpenEnvironment.png)

2. Vai a **Progetti** > **Risorse** e seleziona **Nuovo** per creare una risorsa prenotabile per il tuo utente.

![Risorse prenotabili](./media/8BookableResources.png)

3. Nella scheda **Generale**, seleziona l'utente amministratore. Verifica che il fuso orario corrisponda a quello in cui ti trovi. 

![Nuova risorsa prenotabile](./media/9NewBookableResource.png)

4. Nella scheda **Pianificazione**, nel campo **Società**, seleziona la società **USPM**, quindi seleziona **Salva**. 

![Scheda Pianificazione](./media/10SchedulingTab.png)

5. Seleziona la scheda **Orario di lavoro**.  

![Orario di lavoro](./media/11WorkHours.png)

6. Fai doppio clic su qualsiasi valore nel calendario e seleziona **Modifica** > **Tutti gli eventi della serie**. 

![Calendario lavorativo](./media/12WorkCalendar.png)

7. Cambia l'orario di lavoro in un giorno lavorativo di otto (8) ore, contrassegna i fine settimana come giorni non lavorativi e assicurati che il fuso orario corrisponda al tuo. 
8. Seleziona **Salva e chiudi**.

![Aggiornare il calendario](./media/13UpdateCalendar.png)

9. Vai a **Impostazioni** > **Modelli calendario** e seleziona **Nuovo**.
 
 ![Modelli calendario](./media/14CalendarTemplates.png)
 
 10. Immetti un nome, seleziona la risorsa del modello creata e quindi seleziona **Salva**. 
 
 ![Salvare il modello calendario](./media/15SaveCalendarTemplate.png)
 
 11. Vai a **Parametri** e fai doppio clic sul record. 
 
 ![Parametri progetto](./media/16ProjectParameters.png)
 
12. Aggiorna i seguenti campi:

 - **Società predefinita**: USPM
 - **Unità organizzativa predefinita**: Contoso Robotics Global
 - **Frequenza di fatturazione**: settimo e ultimo giorno
 - **Modello di ore lavorative**: cambia nel modello che hai creato.

13. Seleziona **Salva**. 

![Parametri progetto aggiornati](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]