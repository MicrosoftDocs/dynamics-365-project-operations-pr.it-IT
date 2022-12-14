---
title: Applicare i dati di configurazione e la configurazione dimostrativa - semplice
description: In questo articolo vengono fornite informazioni su come applicare i dati di configurazione e installazione dimostrativi per Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811030"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Applicare i dati di configurazione e la configurazione dimostrativa per Project Operations - semplice 

_**Distribuzione semplice: accordo per la fatturazione proforma_



## <a name="prerequisites"></a>Prerequisiti

Prima di iniziare la configurazione, è necessario disporre di un ambiente Dataverse con provisioning per Dynamics 365 Project Operations.


## <a name="instructions"></a>Istruzioni

1. Scarica il [Pacchetto dati di installazione](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Vai alla cartella *ProjOpsSampleSetupData - solo CE CMT* ed esegui il file eseguibile, *DataMigrationUtility*.
1. A pagina 1 del Configurazione guidata della migrazione (CMT) di Common Data Service, seleziona **Importa dati** e poi seleziona **Continua**.

    ![Migrazione della configurazione.](./media/1ConfigurationMigration.png)

1. A pagina 2 della procedura guidata CMT, seleziona **Microsoft 365** come **Tipo di distribuzione**.
1. Seleziona le caselle di controllo **Visualizza l'elenco delle organizzazioni disponibili** e **Mostra avanzate**.
1. Seleziona l'area del tenant, inserisci le tue credenziali e seleziona **Accedi**.

   ![Accesso alla configurazione.](./media/2ConfigurationSignin.png)

1. A pagina 3, dall'elenco delle organizzazioni nel tenant, seleziona l'organizzazione in cui vuoi importare i dati dimostrativi e seleziona **Accedi**.
1. A pagina 4, seleziona il file zip, *SampleSetupAndConfigData* dalla cartella scompattata, *ProjOpsSampleSetupData - Solo CE CMT*.

   ![File ZIP.](./media/3ZipFile.png)

   ![Seleziona un file.](./media/4SelectAFile.png)

1. Dopo aver selezionato il file zip, seleziona **Importa dati**.

   ![Importa dati.](./media/5ImportData.png)

1. L'importazione verrà eseguita per circa due-dieci minuti a seconda della velocità della rete. Al termine dell'operazione, esci dalla procedura guidata CMT. 
1. Nella tua organizzazione controlla i dati nelle seguenti 18 entità:

    -   Valuta
    -   Conto
    -   Unità organizzativa
    -   Contatto
    -   Unità
    -   Unità di vendita
    -   Listino prezzi
    -   Listino prezzi di parametro progetto 
    -   Frequenza di fatturazione
    -   Categoria di risorsa prenotabile
    -   Categoria di transazione
    -   Categoria di spesa
    -   Prezzo ruolo
    -   Prezzo categoria di transazione
    -   Caratteristica
    -   Risorsa prenotabile
    -   Associazione categoria di risorsa prenotabile
    -   Caratteristica di risorsa prenotabile

    ![Completa l'importazione.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
