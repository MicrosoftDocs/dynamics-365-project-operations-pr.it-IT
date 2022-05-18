---
title: Righe di fattura fornitore per passaggi fondamentali
description: Questo argomento spiega come creare righe di fattura fornitore per i passaggi fondamentali di un conto lavoro.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590627"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Righe di fattura fornitore per passaggi fondamentali

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Una fattura fornitore in Microsoft Dynamics 365 Project Operations può avere righe di fattura fornitore per passaggi fondamentali definiti in una riga di conto lavoro. I project manager possono utilizzare le righe di fattura fornitore per i passaggi fondamentali per registrare i costi dei servizi acquistati come costi basati sui passaggi fondamentali sostenuti per servizi o prodotti acquistati per il progetto.

Le righe di fattura fornitore per i passaggi fondamentali devono sempre fare riferimento a una riga di conto lavoro con un metodo di fatturazione a prezzo fisso. Quando una riga di fattura fornitore per passaggi fondamentali fa riferimento a una riga di conto lavoro, i project manager saranno in grado di confrontare e verificare i costi sottostanti di tempo, spese o materiali che fanno riferimento a tale riga di conto lavoro rispetto al passaggio fondamentale fatturato dal fornitore.

La tabella seguente fornisce informazioni sui campi delle righe di fattura fornitore per i passaggi fondamentali.

| Campo | Description | Impatto funzionale |
| --- | --- | --- |
| Name | Nome della riga di fattura fornitore per facilitare l'identificazione. | Questo nome verrà mostrato come prima colonna in tutte le ricerche basate sulle righe di fattura fornitore. |
| Description | Una breve descrizione dei servizi fatturati dal fornitore nella riga di fattura fornitore. | None |
| Conto lavoro | Il conto lavoro in base al quale i servizi sono stati originariamente ordinati. | Quando viene selezionato un conto lavoro per la fattura fornitore, tutte le righe di fattura fornitore erediteranno tale selezione. Una fattura fornitore non può avere righe di fattura fornitore che fanno riferimento a diversi conti lavoro. |
| Riga conto lavoro | La riga conto lavoro in base al quale i servizi sono stati ordinati. L'elenco delle righe di conto lavoro selezionabili è limitato alle righe del conto lavoro selezionato. | Quando viene selezionata una riga di conto lavoro in una riga di fattura fornitore per i passaggi fondamentali, i campi **Ruolo** e **Categoria di transazione** e i campi relativi al prodotto sono irrilevanti e non disponibili. Anche i campi **Quantità**, **Unità**, e **Gruppo di unità** non sono rilevanti per le righe di fattura fornitore basate su passaggi fondamentali. |
| Data transazione | La data in cui il costo effettivo della riga di fattura fornitore verrà registrato nel progetto. | None |
| Classe di transazione | Seleziona **Passaggio fondamentale** per registrare una fattura fornitore per un passaggio fondamentale completato che è stato definito in una riga di conto lavoro. | None |
| Passaggio fondamentale | Seleziona il passaggio fondamentale definito nella riga di conto lavoro correlata contrassegnata come **Pronto per la fatturazione**. | I passaggi fondamentali della riga di conto lavoro con stato **Pronto per la fatturazione** possono essere selezionati in una riga di fattura fornitore. |
| Project | Il nome del progetto su cui sono stati utilizzati i servizi fatturati. | Campo obbligatorio che non può essere lasciato vuoto. |
| Attività | Il nome dell'attività di progetto su cui sono stati utilizzati i servizi fatturati. Questo campo è disponibile solo se è selezionato un progetto. La selezione di un'attività di progetto è facoltativa. | Se questo campo viene lasciato vuoto, il project manager può abbinare la riga di fattura fornitore alla classe di transazioni della riga di conto lavoro correlata registrata su qualsiasi attività del progetto. Se la riga di fattura fornitore non fa riferimento a una riga di conto lavoro e questo campo viene lasciato vuoto, il costo effettivo creato dalla riga di fattura fornitore non sarà collegato ad alcuna vendita effettiva non fatturata. In questo caso, se è impostata la fatturazione basata su attività, i costi possono non essere fatturabili al cliente finale. |
| Importo passaggio fondamentale | Immetti il valore del passaggio fondamentale definito nella riga di conto lavoro pronta per la fatturazione. | None |
| IVA | Immetti l'importo IVA. | None |
| Importo totale | L'importo totale della riga di fattura fornitore, tasse incluse. Questo campo viene calcolato come *Importo passaggio fondamentale* + *IVA*. | None |

> [!NOTE]
> Quando viene creata una riga di fattura fornitore che fa riferimento a un passaggio fondamentale di una riga di conto lavoro, lo stato del passaggio fondamentale di conto lavoro viene aggiornato su **Fattura fornitore creata**. Quindi, quando la fattura fornitore viene confermata, lo stato del passaggio fondamentale della riga di conto lavoro viene aggiornato su **Fattura fornitore confermata**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
