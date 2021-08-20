---
title: Spese interaziendali
description: Questo argomento fornisce informazioni su come utilizzare le spese interaziendali per assegnare le spese di un lavoratore alla persona giuridica per la quale è stato eseguito il lavoro.
author: Surya Vaidyanathan
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ef42bf5274ff9a5c50e6dcb93995cfbbda40a66d7471f29ebf056086320640
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001211"
---
# <a name="intercompany-expenses"></a>Spese interaziendali

Un lavoratore dipendente di una persona giuridica in un'organizzazione potrebbe svolgere il lavoro per un'altra persona giuridica nella stessa organizzazione. Puoi utilizzare le spese interaziendali per assegnare le spese di un lavoratore alla persona giuridica per la quale è stato eseguito il lavoro. La persona giuridica che impiega il lavoratore è chiamata persona giuridica che presta la risorsa. La persona giuridica per la quale il lavoratore sostiene le spese è denominata persona giuridica che prende in prestito la risorsa. 

Prima che un lavoratore possa creare e inviare le spese interaziendali, è necessario abilitare le righe spese interaziendali. Nella persona giuridica, nella pagina **Parametri di gestione spese** seleziona **Consenti righe spesa interaziendale**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Registrazione delle imposte per spese interaziendali

[!include [banner](../includes/banner.md)]

Prima di poter utilizzare le fasce IVA associate alla persona giuridica concedente (origine) anziché alla persona giuridica richiedente (destinazione) nella nota spese, devi abilitare la funzionalità nell'impostazione IVA di contabilità generale. Quando il parametro **Persona giuridica per registrazione imposte interaziendali** è impostato su **Origine** e **Applica regole di tassazione vendite** è impostato su **No**, viene utilizzata la combinazione fiscale per la persona giuridica concedente. Quando lo stesso parametro è impostato su **Destinazione**, verrà utilizzata la combinazione fiscale per la persona giuridica che prende in prestito la risorsa. Per le persone giuridiche negli Stati Uniti, quando il parametro è impostato su **Origine**, il campo **Contabilità IVA** deve essere configurato anche nella nuova pagina **Gruppi di registrazione contabile**. Il motore di contabilità utilizzerà le informazioni di questo campo per la registrazione contabile relativa alle imposte.   
Il comportamento è coerente per le righe di spesa registrate con o senza un progetto.  

## <a name="new-expense-expression-builder"></a>Nuovo generatore di espressioni di spesa

Il nuovo generatore di espressioni di spesa risolve i problemi associati agli scenari di spesa interaziendali che utilizzano i progetti. Questa funzionalità garantisce che, quando si crea una spesa interaziendale, i criteri di spesa vengano convalidato correttamente a fronte del progetto selezionato nella riga di spesa e che la nota spese possa essere inviata correttamente.

Affinché la funzionalità di generazione delle espressioni di spesa funzioni, deve essere attivata. Inoltre, è necessario impostare i criteri di spesa con un ID progetto.

Se hai già configurato criteri che convalidano l'ID progetto nella riga di spesa, tali criteri devono essere ritirati. Una volta effettuata questa operazione, potrai attivare la funzionalità e riconfigurare i criteri.

Per attivare la funzionalità, esegui la procedura seguente.

1. Vai ad **Aree di lavoro** \> **Gestione funzionalità**.
2. Nell'elenco, seleziona **Nuovo generatore di espressioni di spesa che risolve i problemi associati agli scenari di spesa interaziendali che utilizzano i progetti**. Quindi, seleziona **Abilita ora**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
