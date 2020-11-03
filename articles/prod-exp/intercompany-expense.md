---
title: Spese interaziendali
description: Un lavoratore dipendente di una persona giuridica in un'organizzazione potrebbe svolgere il lavoro per un'altra persona giuridica nella stessa organizzazione. In questa situazione puoi utilizzare la funzione Spese interaziendali per attribuire le spese del lavoratore alla persona giuridica per la quale ha eseguito il lavoro.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079027"
---
# <a name="intercompany-expenses"></a>Spese interaziendali

[!include [banner](../includes/banner.md)]

Un lavoratore dipendente di una persona giuridica in un'organizzazione potrebbe svolgere il lavoro per un'altra persona giuridica nella stessa organizzazione. In questa situazione puoi utilizzare la funzione Spese interaziendali per attribuire le spese del lavoratore alla persona giuridica per la quale ha eseguito il lavoro. La persona giuridica che impiega il lavoratore è chiamata persona giuridica che presta la risorsa. La persona giuridica per la quale il lavoratore sostiene le spese è denominata persona giuridica che prende in prestito la risorsa. 

Prima che un lavoratore possa creare e inviare le spese per il lavoro svolto per una persona giuridica diversa, nella persona giuridica che presta la risorsa, nella pagina **Parametri di gestione spese** seleziona l'opzione **Consenti righe spese interaziendali**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Registrazione delle imposte per spese interaziendali

[!include [banner](../includes/banner.md)]

Se vuoi utilizzare i gruppi di imposte associati alla persona giuridica che presta la risorsa (origine) invece della persona giuridica che prende in prestito la risorsa (destinazione) nella tua nota spese, è necessario configurarla nell'impostazione IVA di contabilità generale. Quando il parametro di contabilità generale **Persona giuridica per registrazione imposte interaziendali** è impostato su **Origine** e **Applica regole tassazione IVA** è impostato su **No** , verrà utilizzata la combinazione fiscale della persona giuridica che presta la risorsa. Quando lo stesso parametro è impostato su **Destinazione** , verrà utilizzata la combinazione fiscale per la persona giuridica che prende in prestito la risorsa. Per le persone giuridiche negli Stati Uniti, quando il parametro è impostato su **Origine** , il campo **Contabilità IVA** deve essere configurato anche nella nuova pagina **Gruppi di registrazione contabile**. Il motore di contabilità utilizzerà le informazioni di questo campo per la registrazione contabile relativa alle imposte.   
Il comportamento è coerente per le righe di spesa registrate con o senza un progetto.  
