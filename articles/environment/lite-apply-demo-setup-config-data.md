---
title: Applicare i dati di configurazione e la configurazione dimostrativa
description: Questo argomento fornisce informazioni su come applicare la configurazione dimostrativa i dati di configurazione in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948927"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Applica la configurazione demo e i dati di configurazione per la distribuzione semplice di Project Operations: accordo per la fatturazione proforma

_**Distribuzione semplice: accordo per la fatturazione proforma_

1. Scarica il [Pacchetto dati master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Vai alla cartella *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ed esegui il file eseguibile *DataMigrationUtility*.
3. A pagina 1 del Configurazione guidata della migrazione (CMT) di Common Data Service, seleziona **Importa dati** e poi seleziona **Continua**.

![Migrazione della configurazione](./media/1ConfigurationMigration.png)

4. A pagina 2 della procedura guidata CMT, seleziona **Office 365** come **Tipo di distribuzione**.
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
- Dettagli di frequenza di fatturazione
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
