---
title: Applicare i dati di configurazione e la configurazione dimostrativa - semplice
description: Questo argomento fornisce informazioni su come applicare la configurazione dimostrativa i dati di configurazione in Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089124"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Applicare i dati di configurazione e la configurazione dimostrativa per Project Operations - semplice 

_**Distribuzione semplice: accordo per la fatturazione proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Prerequisiti

Prima di iniziare la configurazione, è necessario disporre di un ambiente Common Data Service (CDS) con provisioning per Dynamics 365 Project Operations.


## <a name="instructions"></a>Istruzioni

1. Scarica il [Pacchetto dati master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Vai alla cartella *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ed esegui il file eseguibile *DataMigrationUtility*.
3. A pagina 1 del Configurazione guidata della migrazione (CMT) di Common Data Service, seleziona **Importa dati** e poi seleziona **Continua**.

    ![Migrazione della configurazione](./media/1ConfigurationMigration.png)

4. A pagina 2 della procedura guidata CMT, seleziona **Microsoft 365** come **Tipo di distribuzione**.
5. Seleziona le caselle di controllo **Visualizza l'elenco delle organizzazioni disponibili** e **Mostra avanzate**.
6. Seleziona l'area del tenant, inserisci le tue credenziali e seleziona **Accedi**.

   ![Accesso alla configurazione](./media/2ConfigurationSignin.png)

7. A pagina 3, dall'elenco delle organizzazioni nel tenant, seleziona l'organizzazione in cui vuoi importare i dati dimostrativi e seleziona **Accedi**.
8. A pagina 4, seleziona il file zip, *MasterAndSetupData* dalla cartella decompressa, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

   ![File ZIP](./media/3ZipFile.png)

   ![Selezionare un file](./media/4SelectAFile.png)

9. Dopo aver selezionato il file zip, seleziona **Importa dati**.

   ![Importa dati](./media/5ImportData.png)

10. L'importazione verrà eseguita per circa due-dieci minuti a seconda della velocità della rete. Al termine dell'operazione, esci dalla procedura guidata CMT. 
11. Nella tua organizzazione controlla i dati nelle seguenti 20 entità:

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

    ![Completare l'importazione](./media/6CompleteImport.png)
