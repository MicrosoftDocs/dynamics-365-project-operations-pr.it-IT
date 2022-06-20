---
title: Configurare l'integrazione della carta di credito
description: Questo articolo descrive come usare le transazioni con carta di credito correlate alle spese.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d32754548af67bdd5b9f7345f6363bd6193b36d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924481"
---
# <a name="set-up-credit-card-integration"></a>Configurare l'integrazione della carta di credito

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le transazioni con carta di credito relative alle spese possono essere impostate in modo che vengano importate automaticamente in base a una pianificazione ricorrente. In alternativa, le transazioni possono essere importate manualmente in base alle necessità. Le transazioni con carta di credito vengono importate tramite l'entità di dati per le transazioni con carta di credito.

## <a name="import-credit-card-transactions"></a>Importare le transazioni con carta di credito

Per importare transazioni con carta di credito, segui questi passaggi:

1. Nella pagina **Transazioni con carta di credito** seleziona **Importa transazioni**. Se si sta aprendo la gestione dei dati per la prima volta, il sistema deve aggiornare l'elenco delle entità dati prima di poter continuare.
2. Nel campo **Nome**, immetti una descrizione univoca per il processo di importazione.
3. Nel campo **Formato dei dati di origine** seleziona il formato del file che contiene le transazioni della carta di credito da importare.
4. Seleziona **Carica**, quindi trova e seleziona il file da importare.
5. Dopo che il file è stato caricato, convalida la mappatura del file di transazione della carta di credito e le colonne dell'entità di dati delle transazioni della carta di credito selezionando il collegamento **Visualizza mappa** nel riquadro. Se sono presenti errori di mappatura o se è necessario modificare la mappatura, apporta le modifiche alla mappatura dalla scheda **Visualizzazione della mappatura** o dalla scheda **Dettagli della mappatura**.
6. Per automatizzare le transazioni con carta di credito, seleziona **Crea processo dati ricorrente**. Quindi puoi impostare la ricorrenza che definisce la frequenza con cui devono essere importate le transazioni con carta di credito. Al termine, selezionare **OK**.
7. Per importare ora il file selezionato, seleziona **Importa**.
8. Se si verificano errori durante l'importazione, puoi visualizzare il registro di esecuzione o i dati di gestione temporanea per vedere gli errori che è necessario correggere per garantire un'importazione corretta.

> [!NOTE]
> Se è necessario importare più di un formato di file, devi creare processi di importazione distinti per ogni tipo di formato.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Riassegnare le transazioni con carta di credito per i dipendenti licenziati

Dopo che un record di dipendente viene terminato, l'account Active Directory Domain Services (AD DS) del dipendente viene disabilitato. Tuttavia, potrebbero essere attive transazioni con carta di credito che devono ancora essere spesate e rimborsate. Nella pagina **Transazioni con carta di credito** puoi riassegnare il dipendente per qualsiasi transazione con carta di credito in cui il dipendente associato è stato terminato.

Seleziona una o più transazioni con carta di credito, quindi seleziona **Riassegna transazioni**. È quindi possibile selezionare un altro dipendente a cui assegnare le transazioni con carta di credito. Dopo che le transazioni con carta di credito sono state riassegnate, possono essere selezionate per una nota spese e pagate attraverso il normale processo di rimborso della nota spese.

## <a name="delete-credit-card-transactions"></a>Eliminare transazioni con carta di credito 

A volte, dopo l'importazione delle transazioni con carta di credito, potrebbe essere necessario eliminare alcune transazioni. Ciò potrebbe essere dovuto al fatto che le transazioni sono duplicate o che i dati non sono accurati. Gli amministratori possono utilizzare la funzionalità **"Elimina transazioni con carta di credito"** per selezionare ed eliminare transazioni con carta di credito che **non sono associate** a una nota spese. 

1. Vai a **Attività periodiche** > **Elimina le transazioni con carta di credito**.
2. Seleziona **Filtro** e fornisci informazioni per identificare i record da includere.
3. Seleziona **OK** per eliminare i record. 

## <a name="storing-credit-card-numbers"></a>Archiviazione dei numeri di carta di credito

Sono disponibili tre opzioni per archiviare i numeri di carta di credito. I numeri di carta di credito vengono archiviate nella pagina **Parametri di gestione spese**.

- **Impedisci immissione del numero di carta**: i numeri di carta di credito non vengono archiviati.
- **Numeri di carta hash (archivia le ultime quattro cifre)**: le ultime quattro cifre dei numeri di carta di credito vengono archiviate in un formato crittografato.
- **Numeri di carta punto vendita**: i numeri delle carte di credito vengono archiviati in un formato non crittografato. Questa opzione non è conforme ai requisiti Payment Card Industry (PCI) Data Security Standard (DSS). Per mantenere la propria organizzazione conforme alle normative PCI DSS, gli amministratori dell'organizzazione dovrebbero scegliere di non archiviare i numeri di carta di credito o di archiviare i numeri di carta hash.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
