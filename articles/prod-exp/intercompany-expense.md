---
title: Spese interaziendali
description: Questo argomento fornisce informazioni su come utilizzare le spese interaziendali per assegnare le spese di un lavoratore alla persona giuridica per la quale è stato eseguito il lavoro.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960837"
---
# <a name="intercompany-expenses"></a>Spese interaziendali

Un lavoratore dipendente di una persona giuridica in un'organizzazione potrebbe svolgere il lavoro per un'altra persona giuridica nella stessa organizzazione. Puoi utilizzare le spese interaziendali per assegnare le spese di un lavoratore alla persona giuridica per la quale è stato eseguito il lavoro. La persona giuridica che impiega il lavoratore è chiamata persona giuridica che presta la risorsa. La persona giuridica per la quale il lavoratore sostiene le spese è denominata persona giuridica che prende in prestito la risorsa. 

Prima che un lavoratore possa creare e inviare le spese interaziendali, è necessario abilitare le righe spese interaziendali. Nella persona giuridica, nella pagina **Parametri di gestione spese** seleziona **Consenti righe spesa interaziendale**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Registrazione delle imposte per spese interaziendali

[!include [banner](../includes/banner.md)]

Prima di poter utilizzare le fasce IVA associate alla persona giuridica concedente (origine) anziché alla persona giuridica richiedente (destinazione) nella nota spese, devi abilitare la funzionalità nell'impostazione IVA di contabilità generale. Quando il parametro **Persona giuridica per registrazione imposte interaziendali** è impostato su **Origine** e **Applica regole di tassazione vendite** è impostato su **No**, viene utilizzata la combinazione fiscale per la persona giuridica concedente. Quando lo stesso parametro è impostato su **Destinazione**, verrà utilizzata la combinazione fiscale per la persona giuridica che prende in prestito la risorsa. Per le persone giuridiche negli Stati Uniti, quando il parametro è impostato su **Origine**, il campo **Contabilità IVA** deve essere configurato anche nella nuova pagina **Gruppi di registrazione contabile**. Il motore di contabilità utilizzerà le informazioni di questo campo per la registrazione contabile relativa alle imposte.   
Il comportamento è coerente per le righe di spesa registrate con o senza un progetto.  
