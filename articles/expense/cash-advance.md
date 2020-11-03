---
title: Anticipo in contanti
description: In questo argomento vengono fornite informazioni sugli anticipi di contanti.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078759"
---
# <a name="cash-advance"></a>Anticipo in contanti

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Un anticipo in contanti consente ai dipendenti di prendere in prestito denaro dalla propria azienda prima di sostenere eventuali spese. Quando un anticipo in contanti richiesto viene approvato e pagato, il dipendente può utilizzare il denaro per le spese aziendali che potrebbero essere in procinto di sostenere. 

## <a name="create-and-submit-a-cash-advance-request"></a>Creare e inviare una richiesta di anticipo contanti

1. In **Le mie spese** , seleziona **Anticipi contanti** > **Nuovo** per creare un nuovo anticipo contanti. 
2. Nella pagina **Nuova richiesta di anticipo contanti** , inserisci lo scopo della spesa e seleziona la posizione in cui verrà sostenuta la spesa.
3. Immetti l'importo e la valuta richiesti, quindi seleziona **Salva**. 
4. Quando sei pronto per inviare la richiesta di anticipo contanti, nella pagina **Richiesta di anticipo contanti** , seleziona **Flusso di lavoro** > **Invia**.

## <a name="modify-a-cash-advance-request"></a>Modificare una richiesta di anticipo contanti

È possibile modificare una richiesta di anticipo contanti se non è stata inviata per l'approvazione.

1. In **Le mie spese: anticipi in contanti** individua e seleziona l'anticipo in contanti che si desidera modificare.
2. Seleziona **Modifica** e apporta le modifiche necessarie alla richiesta di anticipo in contanti. 
3. Seleziona **Salva e chiudi**.


## <a name="view-cash-advance-requests"></a>Visualizzare le richiesta di anticipo contanti
È possibile rivedere l'elenco di tutti gli anticipi contanti che sono in bozza, inviati, in revisione o pagati in **Le mie spese: anticipi in contanti**. 

## <a name="approve-cash-advance-requests"></a>Approvare le richiesta di anticipo contanti

I responsabili o gli utenti configurati come responsabile approvazione nel flusso di lavoro potranno approvare gli anticipi contanti inviati loro per la revisione. 

1. Per approvare un anticipo contanti, in **Elabora anticipi contanti** , seleziona **Anticipi contanti per revisione personale**.
2. Seleziona l'anticipo contanti che devi rivedere e seleziona **Approva**.  

## <a name="pay-cash-advances"></a>Pagare gli anticipi in contanti 
La procedura seguente viene in genere completata da un contabile o un utente con autorizzazioni di contabilità.

1. Per registrare anticipi in contanti approvati, seleziona **Anticipi contanti approvati** e quindi seleziona **Paga e trasferisci**.  
2. Fornisci i dettagli del giornale di registrazione per gli anticipi contanti, quindi seleziona **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Inviare una nota spese a fronte di un anticipo contanti pagato 

Quando crei e invii una nota spese per l'anticipo contanti che hai già ricevuto, le spese verranno automaticamente adeguate a tale anticipo. Se il tuo anticipo in contanti è maggiore dell'importo speso, devi restituire il saldo alla società utilizzando la categoria di spesa **Restituisci anticipi contanti**. Se l'anticipo contanti pagato dall'azienda è inferiore all'importo che hai speso, l'azienda deve rimborsarti il saldo. 

### <a name="example"></a>Esempio
Stai pianificando di viaggiare per una conferenza da Seattle a New York City. Crei una richiesta di anticipo contanti per 3000,00 USD poiché hai stimato che il costo del biglietto della conferenza, dei voli, dell'hotel, del vitto e del taxi sia approssimativamente questo importo. Non verrai pagato a meno che il tuo responsabile non abbia approvato questa richiesta. Dopo che il tuo responsabile ha approvato, l'anticipo in contanti richiesto viene pagato come 3000,00 USD sul tuo conto bancario. Quindi partecipi alla conferenza. Dopo aver completato il tuo viaggio, scopri che la spesa totale era solo 2790,00 USD. Seleziona **Contanti** nel campo **Metodo di pagamento** e invia la tua spesa per 2790,00 USD. L'importo della spesa inviato viene rettificato automaticamente in base all'anticipo in contanti di 3000,00 USD che ti è stato prestato. Ora devi un saldo di 210,00 USD (3000,00-2790,00) all'azienda, che puoi restituire utilizzando la categoria di spesa **Restituisci anticipi contanti**. 
