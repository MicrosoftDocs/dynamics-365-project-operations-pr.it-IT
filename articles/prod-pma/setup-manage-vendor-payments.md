---
title: Impostare e utilizzare i pagamenti del fornitore con pagamento su pagamento
description: Questo argomento spiega come creare le condizioni di pagamento su pagamento in modo da poter rilasciare pagamenti parziali al fornitore, in base ai pagamenti dei clienti.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078855"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Impostare e utilizzare i pagamenti del fornitore con pagamento su pagamento

[!include [banner](../includes/banner.md)]

Quando autorizzi un fornitore a lavorare come terzista, potresti voler trattenere il pagamento al fornitore fino a quando il cliente non paga per il progetto. Per supportare questo scenario, puoi impostare le condizioni di pagamento su pagamento quando imposti l'ordine di acquisto con il fornitore.

Ad esempio, quando un cliente paga un importo su una fattura di progetto, è possibile rilasciare parte o tutto l'importo della fattura al fornitore. Basta impostare le condizioni di pagamento su pagamento che specificano che il venditore verrà pagato dopo aver ricevuto una percentuale del relativo pagamento dal cliente. Se ricevi un pagamento parziale da un cliente, puoi rilasciare manualmente alcune delle fatture del fornitore correlate per il pagamento.

L'esempio seguente delinea il processo quando vengono utilizzate le condizioni di pagamento su pagamento.

## <a name="example"></a>Esempio

La tua organizzazione accetta di fornire a un cliente 100 computer su cui è installato software, al prezzo di 150,00 dollari USA (USD) per computer. Quindi contatti un fornitore che ti fornisca i computer su cui è installato il software. Secondo il contratto, il cliente deve approvare la qualità dei computer prima di pagare la tua organizzazione. I criteri della tua organizzazione consentono di trattenere il pagamento ai fornitori fino a quando il cliente non ti ha pagato. Pertanto, imposti il progetto in modo che abbia una percentuale di pagamento su pagamento del 100 percento.

Il venditore ti invia i 100 computer su cui è installato il software, insieme a una fattura per 10,000,00 USD. Poiché le condizioni di pagamento su pagamento sono impostate per il tuo progetto, non paghi il fornitore al ricevimento dei computer. Invece, invii i computer al cliente, insieme a una fattura per 15.000,00 USD. Il cliente ispeziona i computer e approva l'intero importo della fattura del progetto.

Dopo aver ricevuto il pagamento completo dal cliente, paghi al fornitore 10,000,00, l'intero importo della fattura del fornitore.

## <a name="set-up-pwp-terms-for-a-project"></a>Impostare le condizioni di pagamento su pagamento per un progetto

Quando imposti le condizioni di pagamento su pagamento per un progetto, devi specificare, in percentuale, l'importo minimo che un cliente deve pagare per il progetto prima che tu paghi il fornitore. L'importo di soglia viene calcolato automaticamente sulle fatture del cliente per il progetto. Segui questi passaggi per impostare la percentuale di soglia per le condizioni di pagamento su pagamento.

1. Vai a **Gestione progetti e contabilità** \> **Progetti** \> **Tutti i progetti**.
2. Trova e apri il progetto per il quale desideri impostare le condizioni di pagamento su pagamento.
3. Nella scheda dettaglio **Contratti fornitori** seleziona **Aggiungi riga**.
3. Nel campo **Codice conto** , seleziona una delle seguenti opzioni:

    - **Tabella** : le condizioni di pagamento su pagamento si applicano a un singolo fornitore.
    - **Gruppo** : le condizioni di pagamento su pagamento si applicano a tutti i fornitori in un gruppo di fornitori.
    - **Tutto** : le condizioni di pagamento su pagamento si applicano a tutti i fornitori.

4. Se hai selezionato **Tabella** o **Gruppo** nel passaggio precedente, in **Fornitore/Gruppo di fornitori** seleziona il fornitore o il gruppo di fornitori a cui si applicano le condizioni di pagamento su pagamento. Se hai selezionato **Tutti** nel passaggio precedente, il campo **Fornitore/Gruppo di fornitori** non può essere modificato.
5. Se le condizioni di conservazione del fornitore sono impostate per il fornitore nel progetto, nel campo **Condizioni di conservazione fornitore** seleziona l'ID regola per le condizioni di conservazione.
6. Nel campo **Percentuale di soglia pagamento su pagamento** immetti la percentuale di soglia per il progetto. La percentuale immessa per il progetto definisce l'importo minimo che il cliente deve pagare prima che tu paghi il fornitore.

## <a name="create-a-po-that-has-pwp-terms"></a>Crea un ordine di acquisto con condizioni di pagamento su pagamento

Quando registri una fattura da un fornitore, se il fornitore è soggetto alle condizioni di pagamento su pagamento tali condizioni vengono visualizzate nelle righe dell'ordine d'acquisto. Per creare un ordine di acquisto con condizioni di pagamento su pagamento, segui questi passaggi.

1. Vai a **Approvvigionamento** \> **Ordini di acquisto** \> **Tutti gli ordini di acquisto**.
2. Nel riquadro Azioni seleziona **Nuovo**. Quindi, nella finestra di dialogo **Crea ordine di acquisto** immetti le informazioni richieste e seleziona **OK**.

    In alternativa, apri un ordine di acquisto esistente nella pagina elenco **Tutti gli ordini di acquisto**.

4. Nella pagina **Ordine di acquisto** nella scheda dettaglio **Righe ordine di acquisto** esamina i dettagli della riga dell'ordine di acquisto per il fornitore. L'opzione **Pagamento su pagamento** è selezionata automaticamente e il valore nel campo **Percentuale di soglia pagamento su pagamento** viene automaticamente copiato dal campo **Percentuale di soglia pagamento su pagamento** della pagina **Progetti**.
6. Se non desideri applicare le condizioni di pagamento su pagamento al fornitore per una riga dell'ordine di acquisto, deseleziona l'opzione **Pagamento su pagamento**. In questo caso, il campo **Percentuale di soglia pagamento su pagamento** per la riga dell'ordine di acquisto verrà reimpostato su 0 (zero).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Aggiornare il pagamento di un cliente e pagare il venditore

Quando un fornitore completa il suo lavoro su un progetto e ti invia una fattura, devi rivedere lo stato del progetto e le fatture del cliente per determinare se le condizioni di pagamento su pagamento sono stati rispettati per il progetto. Se le condizioni di pagamento su pagamento per il fornitore sono stati soddisfatte, è possibile determinare quali righe della fattura fornitore pagare, in base ai pagamenti del cliente per il progetto. Se decidi di pagare il fornitore anche se le condizioni di pagamento su pagamento non sono stati rispettate, puoi sovrascrivere le condizioni di pagamento su pagamento nella pagina **Fattura fornitore con condizioni di pagamento su pagamento**.

1. Vai a **Gestione progetti e contabilità** \> **Richieste e report** \> **Richieste di conservazione** \> **Fattura fornitore con pagamento su pagamento**.
2. Nella pagina **Fatture fornitore con pagamento su pagamento** , nel campo di ricerca, immetti i valori per trovare la fattura fornitore che desideri esaminare, quindi seleziona **Cerca**.
3. Nella scheda dettaglio **Righe fattura fornitore** seleziona le righe che vuoi modificare.
4. Se le condizioni di **pagamento su pagamento** sono soddisfatte per la riga della fattura, seleziona **Rilascia pagamento fornitore**. L'opzione **Pagamento su pagamento** viene deselezionata e il valore del campo **Pronto per il pagamento** viene modificato in **Sì**.
