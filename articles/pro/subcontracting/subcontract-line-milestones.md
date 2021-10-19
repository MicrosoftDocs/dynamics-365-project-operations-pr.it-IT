---
title: Passaggi fondamentali voci di conto lavoro
description: Questo argomento spiega come creare e gestire una pianificazione delle fatture basata su passaggi fondamentali per un conto lavoro con un fornitore.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7f99853f5f649f96225b7d72580db97bb92de7c5
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558507"
---
# <a name="subcontract-line-milestones"></a>Passaggi fondamentali voci di conto lavoro

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

In Dynamics 365 Project Operations, una voce di conto lavoro con un metodo di fatturazione a prezzo fisso può specificare una pianificazione della fattura basata su passaggi fondamentali con il fornitore.

I passaggi fondamentali per la fatturazione dei fornitori possono essere generati automaticamente utilizzando una frequenza impostata oppure è possibile crearli manualmente.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Crea automaticamente una pianificazione fattura basata su passaggi fondamentali per una voce di conto lavoro

Completa i seguenti passaggi per generare automaticamente una pianificazione delle fatture basata su passaggi fondamentali per un insieme fisso di passaggi fondamentali equamente distribuiti.

1. Vai a **Impostazioni** > **Frequenze di fatturazione** e imposta la frequenza della fattura per le voci del conto lavoro.
2. Apri la pagina **Conti lavoro**, apri il conto lavoro con cui desideri lavorare, quindi apri la riga di contratto di conto lavoro a prezzo fisso per la quale intendi creare una pianificazione di passaggi fondamentali.
3. Nella scheda **Passaggi fondamentali di riga conto lavoro**, seleziona **Genera passaggi fondamentali periodici**.
4. Nella finestra di dialogo, inserisci o seleziona un intervallo di date, il numero di passaggi fondamentali e la frequenza di fatturazione. Puoi selezionare una data di inizio oppure puoi selezionare il numero di tappe e la frequenza di fatturazione o la data di inizio, oppure puoi selezionare la data di fine e la frequenza di fatturazione. Non è possibile selezionare la data di fine e il numero di passaggi fondamentali.
Utilizzando queste informazioni, il sistema genera passaggi fondamentali e record che vengono mostrati nella griglia **Passaggi fondamentali**.

   - **Nome passaggio fondamentale**: il nome del passaggio fondamentale è impostato sulla data del passaggio fondamentale in base alla frequenza di fatturazione.
   - **Data passaggio fondamentale**: la data in base alla frequenza di fatturazione.
   - **Importo passaggio fondamentale**: calcolato dividendo l'importo del subtotale sulla riga del subappalto per il numero di passaggi fondamentali.

Se la voce di conto lavoro ha un valore nel campo **Importo stimato dell'imposta**, questo valore viene aggiunto equamente a ciascun passaggio fondamentale quando si generano passaggi fondamentali periodici.

La somma degli importi dei passaggi fondamentali di voci conto lavoro deve essere uguale al valore della riga conto lavoro. Se non sono uguali, si verifica un errore. Puoi correggere l'errore e verificare che il totale del passaggio fondamentale sia uguale al valore della voce del conto lavoro creando, modificando o eliminando il passaggio fondamentale e gli importi delle imposte. Dopo aver apportato le modifiche, salva e aggiorna la pagina per assicurarti che non ci siano più errori.

## <a name="manually-create-subcontract-line-milestones"></a>Creare manualmente i passaggi fondamentali delle righe di conto lavoro

I passaggi fondamentali a prezzo fisso su una voce di conto lavoro possono essere generati manualmente quando non vengono suddivisi periodicamente. Per creare manualmente un passaggio fondamentale della voce di conto lavoro, completa i seguenti passaggi.

1. Nel riquadro di spostamento, seleziona **Conti lavoro** e apri il conto lavoro con cui desideri lavorare.
2. Apri la riga di conto lavoro a prezzo fisso per la quale desideri creare un passaggio fondamentale.
3. Nella scheda **Punti cardine righe conto lavoro**, nella sottogriglia, seleziona **+ Nuovo passaggio fondamentale della voce di conto lavoro**.
4. Nella pagina **Nuovo passaggio fondamentale della voce di conto lavoro**, inserisci le informazioni richieste in base alla tabella seguente.

    | Campo | Descrizione |Impatto funzionale|
    | --- | --- |----------------------|
    | Nome passaggio fondamentale | Il nome del passaggio fondamentale. |Questa verrà mostrata come prima colonna in tutte le ricerche basate sui passaggi fondamentali della riga di conto lavoro. La riga della fattura fornitore creata in base a questo passaggio fondamentale utilizzerà anche il nome del passaggio fondamentale della riga di conto lavoro come nome predefinito della riga della fattura fornitore.|
    | Descrizione | Una descrizione del passaggio fondamentale. |La riga della fattura fornitore creata in base a questo passaggio fondamentale utilizzerà anche la descrizione del passaggio fondamentale della riga di conto lavoro come descrizione predefinita della riga della fattura fornitore.|
    | Data di passaggio fondamentale | La data in cui il processo di creazione automatica della fattura dovrebbe cercare lo stato di questo passaggio fondamentale per considerarlo per la fatturazione.| Questo valore verrà utilizzato come data predefinita della riga della fattura fornitore durante la fatturazione per questa riga del contratto di conto lavoro. |
    | Numero | L'importo o il valore del passaggio fondamentale che verrà fatturato al cliente. |Questo valore è utilizzato come importo predefinito della riga della fattura fornitore durante la fatturazione per questa riga del contratto di conto lavoro. |
    | Imposta | L'importo delle imposte applicato al passaggio fondamentale.| Questo valore è utilizzato come imposta predefinita della riga della fattura fornitore durante la fatturazione per questa riga del contratto di conto lavoro. |
    | Importo al netto delle imposte | Questo campo è di sola lettura e viene calcolato come Importo + IVA.|Questo valore è utilizzato come predefinito della riga della fattura fornitore durante la fatturazione per questa riga del contratto di conto lavoro. |
    | Stato fattura | Quando viene creato il traguardo, questo stato è sempre impostato su **Non pronto per la fatturazione**.|  Quando lo stato è **Pronto per la fatturazione**, la creazione della fattura fornitore include questo passaggio fondamentale nella fattura fornitore. |

5. Seleziona **Salva e chiudi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
