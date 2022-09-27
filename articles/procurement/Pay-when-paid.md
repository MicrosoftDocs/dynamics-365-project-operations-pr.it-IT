---
title: Pagamenti del fornitore con pagamento su pagamento
description: Questo argomento descrive come utilizzare lo scenario di pagamento su pagamento.
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525338"
---
# <a name="pay-when-paid-vendor-payments"></a>Pagamenti del fornitore con pagamento su pagamento

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento descrive come utilizzare lo scenario di pagamento su pagamento.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Creare un ordine di acquisto con condizioni di pagamento su pagamento

Quando registri una fattura da un fornitore, se il fornitore è soggetto alle condizioni di pagamento su pagamento, tali condizioni vengono visualizzate nelle righe dell'ordine fornitore. Per creare un ordine di acquisto con condizioni di pagamento su pagamento, segui questi passaggi.

1. In Microsoft Dynamics 365 Finance, segui uno di questi passaggi:

    - Vai a **Approvvigionamento** \> **Ordini di acquisto** \> **Tutti gli ordini di acquisto**. Nel riquadro Azioni seleziona **Nuovo**. Nella finestra di dialogo **Crea ordine di acquisto**, seleziona il fornitore per il quale le condizioni di pagamento su pagamento sono configurate nel progetto, immetti le altre informazioni necessarie, quindi seleziona **OK**.
    - Vai a **Gestione progetti e contabilità** \> **Progetti** \> **Tutti i progetti**. Nella scheda **Gestisci** del riquadro Azioni seleziona **Attività articolo**. Seleziona l'ordine fornitore. Seleziona il fornitore per il quale sono configurate le condizioni di pagamento su pagamento, quindi seleziona **OK**.

2. Nella pagina **Ordine fornitore**, nella Scheda dettaglio **Righe ordine fornitore**, seleziona **Aggiungi riga** per creare una riga di ordine fornitore.
3. Seleziona il numero dell'articolo o la categoria di approvvigionamento e inserisci gli altri dettagli. Esamina i dettagli della riga dell'ordine fornitore per il fornitore.

    L'opzione **Pagamento su pagamento** è selezionata automaticamente e il valore nel campo **Percentuale di soglia pagamento su pagamento** viene automaticamente copiato dal campo **Percentuale di soglia pagamento su pagamento** della pagina **Progetti**.

4. Se non desideri applicare le condizioni di pagamento su pagamento al fornitore per una riga dell'ordine di acquisto, deseleziona l'opzione **Pagamento su pagamento**. In questo caso, il campo **Percentuale di soglia pagamento su pagamento** per la riga dell'ordine fornitore verrà reimpostato su **0** (zero).
5. Nella pagina **Ordine fornitore** del riquadro azioni, nella scheda **Acquisto**, seleziona **Conferma** per confermare l'ordine fornitore.
6. Nella scheda **Fattura** del riquadro Azioni, seleziona **Fattura** per generare la fattura per l'ordine fornitore.

## <a name="create-a-project-invoice-proposal"></a>Creare una proposta di fattura di progetto

Le proposte di fattura di progetto vengono utilizzate per creare fatture di progetto per il cliente. Nello scenario di pagamento su pagamento, i pagamenti del fornitore dipendono dai pagamenti dei clienti in base alle impostazioni relative al pagamento su pagamento. Tuttavia, vi sono opzioni che ti consentono di rilasciare i pagamenti senza i pagamenti dei clienti come richiesto. Per creare una fattura di progetto per il cliente, segui questi passaggi.

1. Nelle app di interazione con i clienti, vai a **Progetto** \> **Progetti** e seleziona il progetto.
2. Nella scheda **Valori effettivi**, seleziona la riga effettiva che viene generata dall'ordine fornitore il cui tipo di transazione è **Vendite non fatturate**. Quindi seleziona **Pronto per fattura**.
3. Vai a **Sales** \> **Vendite** \> **Contratto di progetto** e seleziona il contratto di progetto.
4. Per generare la fattura del cliente, nel riquadro Azioni, seleziona **Fattura**.
5. In Finance, vai a **Gestione progetti e contabilità** \> **Periodico** \> **Importa da tabella di gestione temporanea** e seleziona **OK** per generare il giornale di registrazione di integrazione Project Operations.
6. Vai a **Gestione progetto e contabilità** \> **Fatture di progetto** \> **Proposta di fatturazione di progetto** e seleziona **Registra** per registrare la proposta di fatturazione generata per il progetto.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Aggiornare il pagamento di un cliente e pagare il venditore

Quando un fornitore completa il proprio lavoro su un progetto e ti invia una fattura, devi esaminare lo stato del progetto e le fatture del cliente per determinare se le condizioni di pagamento su pagamento sono state soddisfatte per il progetto. Se le condizioni di pagamento su pagamento per il fornitore sono stati soddisfatte, è possibile determinare quali righe della fattura fornitore pagare, in base ai pagamenti del cliente per il progetto. Se decidi di pagare il fornitore anche se le condizioni di pagamento su pagamento non sono stati rispettate, puoi sovrascrivere le condizioni di pagamento su pagamento nella pagina **Fattura fornitore con condizioni di pagamento su pagamento**.

1. In Finance, vai a **Gestione progetti e contabilità** \> **Progetti** \> **Tutti i progetti** e seleziona il progetto.
2. Nel riquadro Azioni, seleziona **Controllo**, quindi seleziona **Fatture fornitore** per visualizzare tutte le fatture fornitore generate per il progetto.
3. Nella pagina **Fatture fornitore con pagamento su pagamento**, nel campo di ricerca, immetti i valori per trovare la fattura fornitore che desideri esaminare, quindi seleziona **Cerca**.
4. Seleziona l'opzione **Pagamento su pagamento** per visualizzare solo le fatture di pagamento su pagamento.
5. Nella scheda dettaglio **Righe fattura fornitore** seleziona le righe che vuoi rilasciare per il pagamento.
6. Seleziona **Rilascia pagamento fornitore**. L'opzione **Pagamento su pagamento** viene deselezionata e il valore del campo **Pronto per il pagamento** viene modificato in **Sì**.
