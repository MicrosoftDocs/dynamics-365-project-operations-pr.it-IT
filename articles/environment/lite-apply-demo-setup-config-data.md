---
title: Applicare i dati di configurazione e la configurazione dimostrativa - semplice
description: Questo argomento fornisce informazioni su come applicare la configurazione dimostrativa i dati di configurazione in Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997156"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Applicare i dati di configurazione e la configurazione dimostrativa per Project Operations - semplice 

_**Distribuzione semplice: accordo per la fatturazione proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Prerequisiti

Prima di iniziare la configurazione, è necessario disporre di un ambiente Common Data Service (CDS) con provisioning per Dynamics 365 Project Operations.


## <a name="instructions"></a>Istruzioni

1. Scarica il [Pacchetto dati master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Vai alla cartella *ProjOpsSampleSetupData - solo CE CMT* ed esegui il file eseguibile, *DataMigrationUtility*.
3. A pagina 1 del Configurazione guidata della migrazione (CMT) di Common Data Service, seleziona **Importa dati** e poi seleziona **Continua**.

    ![Migrazione della configurazione](./media/1ConfigurationMigration.png)

4. A pagina 2 della procedura guidata CMT, seleziona **Microsoft 365** come **Tipo di distribuzione**.
5. Seleziona le caselle di controllo **Visualizza l'elenco delle organizzazioni disponibili** e **Mostra avanzate**.
6. Seleziona l'area del tenant, inserisci le tue credenziali e seleziona **Accedi**.

   ![Accesso alla configurazione](./media/2ConfigurationSignin.png)

7. A pagina 3, dall'elenco delle organizzazioni nel tenant, seleziona l'organizzazione in cui vuoi importare i dati dimostrativi e seleziona **Accedi**.
8. A pagina 4, seleziona il file zip, *SampleSetupAndConfigData* dalla cartella scompattata, *ProjOpsSampleSetupData - Solo CE CMT*.

   ![File ZIP](./media/3ZipFile.png)

   ![Seleziona un file](./media/4SelectAFile.png)

9. Dopo aver selezionato il file zip, seleziona **Importa dati**.

   ![Importa dati](./media/5ImportData.png)

10. L'importazione verrà eseguita per circa due-dieci minuti a seconda della velocità della rete. Al termine dell'operazione, esci dalla procedura guidata CMT. 
11. Nella tua organizzazione controlla i dati nelle seguenti 18 entità:

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
