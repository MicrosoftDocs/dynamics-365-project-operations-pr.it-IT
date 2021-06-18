---
title: Integrazione con Microsoft Project Client
description: La pianificazione e la gestione di una pianificazione del progetto possono essere complesse, quindi i project manager devono utilizzare strumenti che li aiutino a gestire questa attività. L'integrazione con Microsoft Project Client fornisce supporto per aprire e gestire una struttura di suddivisione del lavoro di progetto.
author: Yowelle
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 032d726bb6206c563b573f30d13fe2697a13c949
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999451"
---
# <a name="microsoft-project-client-integration"></a>Integrazione con Microsoft Project Client

[!include [banner](../includes/banner.md)]

La pianificazione e la gestione di una pianificazione del progetto possono essere complesse, quindi i project manager devono utilizzare strumenti che li aiutino a gestire questa attività. L'integrazione con Microsoft Project Client fornisce supporto per aprire e gestire una struttura di suddivisione del lavoro di progetto. Il project manager può pubblicare eventuali modifiche nella struttura di suddivisione del lavoro del progetto Dynamics 365 Finance.

> [!NOTE]
> Se stai usando l'aggiornamento di luglio (versione 10.0.4), devi installare KB 4054797 e 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Configurare il componente aggiuntivo di Microsoft Project Client
Per abilitare l'integrazione con Microsoft Project Client, è necessario installare un componente aggiuntivo di Microsoft Dynamics 365 nell'applicazione client Microsoft Project dell'utente. Questo viene fatto aprendo l'**area di lavoro per la gestione dei progetti**.

•   Fai clic su **Configura componente aggiuntivo client di progetto** dalla sezione **Collegamenti** > **Imposta** dell'area di lavoro.

•   Fai clic su **Apri**, quindi fai clic su **Esegui** quando richiesto.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Aprire e modificare una bozza di struttura di suddivisione del lavoro esistente in Microsoft Project Client
Se un progetto in Dynamics 365 Finance ha già una struttura di suddivisione del lavoro creata, la struttura di suddivisione del lavoro può essere aperta nell'applicazione Microsoft Project Client se la struttura di suddivisione del lavoro è in uno stato di bozza. Per aprire dalla pagina **Progetto**, fai clic sul collegamento **Apri in Microsoft Project** dalla scheda **Piano**. Questa pagina può essere aperta anche dall'interno dell'applicazione Microsoft Project Client facendo clic su **Apri** nella scheda **Microsoft Dynamics 365**. Seleziona **Persona giuridica** e **Progetto** dall'elenco.

> [!NOTE]
> Se stai usando Internet Explorer come browser, dovrai fare clic su **Salva** per aprire manualmente dalla posizione in cui viene scaricato il file. Oppure fai clic su **Salva e apri** per aprire il file in Microsoft Project Client. Non rinominare il nome del file durante il salvataggio.

Prima di apportare modifiche al file utilizzando Microsoft Project Client, devi verificarlo. Fai clic su **Estrai** nella scheda **Microsoft Dynamics 365**. Ciò impedirà ad altri utenti di modificare contemporaneamente la struttura di suddivisione del lavoro da Finance. Per pubblicare la struttura di suddivisione del lavoro dopo aver completato le modifiche, fai clic su **Registra** nella scheda **Microsoft Dynamics 365**.

Se un team di progetto è già stato aggiunto al progetto in Finance, l'elenco delle risorse verrà popolato con i membri del team. Se un team di progetto non è stato ancora aggiunto al progetto, è possibile selezionare le risorse e creare il team all'interno di Microsoft Project Client facendo clic sul pulsante **Risorse** della scheda **Microsoft Dynamics 365**. 

I seguenti dati verranno sincronizzati di nuovo con Finance come parte del processo di check-in:

•   Nome attività

•   Data di inizio

•   Data di fine

•   Attività precedenti

•   Nomi risorse

•   Categoria

•   Categoria di risorsa

•   Orario di lavoro

•   Note

•   Priorità

> [!NOTE]
> Se aggiungi altre colonne al file di Microsoft Project Client, non verranno salvate nel file e non verranno visualizzate quando il file viene aperto di nuovo.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Creare la struttura di suddivisione del lavoro per un progetto esistente utilizzando Microsoft Project Client
Per creare una nuova struttura di suddivisione del lavoro utilizzando Microsoft Project Client, segui questi passaggi:


1.  Apri Microsoft Project Client.

2.  Nella scheda **Microsoft Dynamics 365** fai clic su **Apri**.

3.  Selezionare la **persona giuridica** per il progetto.

4.  Seleziona il **progetto**.

5.  Fai clic su **Estrai** nella scheda **Microsoft Dynamics 365**.

6.  Quando sei pronto per pubblicare su Finance, fai clic su **Registra** nella scheda **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Sostituisci la struttura di suddivisione del lavoro per un progetto esistente utilizzando Microsoft Project Client
Per creare una nuova struttura di suddivisione del lavoro utilizzando Microsoft Project Client e sostituire una struttura di suddivisione del lavoro esistente per un progetto esistente, attieniti alla seguente procedura:

1.  Apri Microsoft Project Client.

2.  Crea la pianificazione in Microsoft Project Client.

3.  Nella scheda **Microsoft Dynamics 365**, fai clic su **Salva modifiche** > **Sostituisci progetto esistente**.

4.  Selezionare la **persona giuridica** per il progetto.

5.  Seleziona il **progetto**.

6.  Fare clic su **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Creare un nuovo progetto dall'interno di Microsoft Project Client


1.  Apri Microsoft Project Client.

2.  Crea la pianificazione in Microsoft Project Client.

3.  Nella scheda **Microsoft Dynamics 365**, fai clic su **Salva modifiche** > **Salva su nuovo progetto**.

4.  Selezionare la **persona giuridica** per il progetto.

5.  Immetti l'**ID progetto**, se necessario.

6.  Immetti il **Nome progetto**.

7.  Seleziona un valore per **Tipo di progetto**, **Gruppo di progetto** e **ID contratto di progetto**. In alternativa, puoi creare un nuovo contratto di progetto facendo clic su **Nuovo**.

8.  Seleziona il **Calendario** da utilizzare per le risorse.

11. Fare clic su **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]