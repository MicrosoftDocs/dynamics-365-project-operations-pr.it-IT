---
title: Anticipo in contanti
description: In questo articolo vengono fornite informazioni sugli anticipi di contante.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: bc270944faa7c16d2e97a988495a2a16380ba879
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931519"
---
# <a name="cash-advance"></a>Anticipo in contanti

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Un anticipo in contanti consente ai dipendenti di prendere in prestito denaro dalla propria azienda prima di sostenere eventuali spese. Quando un anticipo in contanti richiesto viene approvato e pagato, il dipendente può utilizzare il denaro per le spese aziendali che potrebbero essere in procinto di sostenere. 

## <a name="create-and-submit-a-cash-advance-request"></a>Creare e inviare una richiesta di anticipo contanti
Per creare un nuovo anticipo in contanti e inviare una richiesta di anticipo in contanti, procedi come segue: 

1. Sotto **Spese personali**, seleziona **Anticipi in contati** > **Nuovo**. 
2. Nella pagina **Nuova richiesta di anticipo contanti**, inserisci lo scopo della spesa e seleziona la posizione in cui verrà sostenuta la spesa.
3. Immetti l'importo e la valuta richiesti, quindi seleziona **Salva**. 
4. Quando sei pronto per inviare la richiesta di anticipo contanti, nella pagina **Richiesta di anticipo contanti**, seleziona **Flusso di lavoro** > **Invia**.

## <a name="modify-a-cash-advance-request"></a>Modificare una richiesta di anticipo contanti

È possibile modificare una richiesta di anticipo contanti se non è stata inviata per l'approvazione.

1. Sotto **Spese personali: Anticipi in contanti** individua e selezion l'anticipo in contanti che vuoi modificare.
2. Seleziona **Modifica** e apporta le modifiche necessarie alla richiesta di anticipo in contanti. 
3. Seleziona **Salva e chiudi**.


## <a name="view-cash-advance-requests"></a>Visualizzare le richiesta di anticipo contanti
È possibile rivedere l'elenco di tutti gli anticipi contanti che sono in bozza, inviati, in revisione o pagati in **Le mie spese: anticipi in contanti**. 

## <a name="approve-cash-advance-requests"></a>Approvare le richiesta di anticipo contanti

I responsabili o gli utenti configurati come responsabile approvazione nel flusso di lavoro potranno approvare gli anticipi contanti inviati loro per la revisione. 

1. Per approvare un anticipo contanti, in **Elabora anticipi contanti**, seleziona **Anticipi contanti per revisione personale**.
2. Seleziona l'anticipo contanti che devi rivedere e seleziona **Approva**.  

## <a name="pay-cash-advances"></a>Pagare gli anticipi in contanti 
La procedura seguente viene in genere completata da un contabile o un utente con autorizzazioni di contabilità.

1. Per registrare anticipi in contanti approvati, seleziona **Anticipi contanti approvati** e quindi seleziona **Paga e trasferisci**.  
2. Fornisci i dettagli del giornale di registrazione per gli anticipi contanti, quindi seleziona **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Inviare una nota spese a fronte di un anticipo contanti pagato 

Quando crei e invii una nota spese per l'anticipo in contanti che hai già ricevuto, le spese verranno automaticamente adeguate all'anticipo. Se il tuo anticipo in contanti è maggiore dell'importo speso, devi restituire il saldo alla società utilizzando la categoria di spesa **Restituisci anticipi contanti**. Se l'anticipo in contanti pagato dall'azienda è inferiore all'importo che hai speso, l'azienda deve rimborsarti il saldo. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Selezionare anticipi in contanti che si applicano alle spese
Prima di inviare una nota spese, puoi selezionare l'anticipo in contanti che si allinea alle transazioni di spesa nel report. Per utilizzare questa funzionalità, le seguenti due funzionalità devono essere abilitate dall'area di lavoro **Gestione funzionalità**:

  - Note spese riprogettate
  - Possibilità di mappare anticipi in contanti a righe di spesa
 
 Quando queste funzionalità sono abilitate:
 
  - È possibile aggiungere uno o più anticipi di cassa per ciascuna riga di spesa.
  - Il saldo disponibile di un anticipo in contanti è visibile in tempo reale quando viene salvata una nota spese. Ciò ti consente di elaborare le transazioni di spesa e di restituire la transazione in contanti allo stesso tempo.
  - Puoi selezionare più anticipi in contanti per una transazione di spesa.
  - I dati di riconciliazione dell'anticipo in contanti sono disponibili utilizzando una query. 
 
Se non utilizzi queste funzionalità, la funzionalità rimarrà la stessa, con gli anticipi in contanti esistenti ridotti automaticamente dopo l'invio di una spesa.

### <a name="example"></a>Esempio 
Hai intenzione di viaggiare da Seattle a New York City per una conferenza. Crei una richiesta di anticipo in contanti per 3000,00 USD in base al costo stimato del biglietto della conferenza, dei voli, dell'hotel, dei pasti e del taxi. Non verrai pagato a meno che il tuo manager non approvi questa richiesta. Dopo che il tuo responsabile ha approvato, l'anticipo in contanti richiesto viene pagato come 3000,00 USD sul tuo conto bancario. Quindi partecipi alla conferenza. Dopo aver completato il tuo viaggio, scopri che la spesa totale era solo 2790,00 USD. Seleziona **Contante** nel campo **Metodo di pagamento** e invia la tua spesa per 2790,00 USD. L'importo della spesa inviato viene rettificato automaticamente in base all'anticipo in contanti di 3000,00 USD che ti è stato prestato. Ora devi un saldo di 210,00 USD (3000,00 - 2790,00), che puoi restituire all'azienda utilizzando la categoria di spesa **Restituisci contante**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
