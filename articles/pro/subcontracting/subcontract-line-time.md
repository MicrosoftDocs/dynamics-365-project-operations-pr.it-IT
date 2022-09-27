---
title: Righe conto lavoro per orario
description: Questo articolo spiega come registrare le righe di conto lavoro per tempo e registrare l'acquisto di tempo dei fornitori.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ba013dd7ad023acc4f0cf077099c8c2c8d5bcd8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522237"
---
# <a name="subcontract-lines-for-time"></a>Righe conto lavoro per orario

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione lite: dalla transazione alla fatturazione proforma_

Un conto lavoro in Dynamics 365 Project Operations può avere una voce di conto lavoro per le ore. Le voci di conto lavoro per il tempo consentono a un responsabile di progetto di acquistare il tempo delle risorse del fornitore per le attività di progetto del personale e i requisiti di risorse.

Per creare una voce di conto lavoro per le ore in Project Operations, completare la seguente procedura.

1. Nel riquadro di spostamento, seleziona **Conti lavoro** e apri un conto lavoro.
2. Nella scheda **Voci di conto lavoro**, seleziona **Nuovo** per creare una nuova riga conto lavoro.
3. Nella pagina **Creazione rapida**, nel campo **Classe di transazione**, seleziona **Ore**.
4. Immetti le altre informazioni nel campo e quindi seleziona **Salva**.

  La seguente tabella fornisce informazioni sui campi nella pagina **Voce conto lavoro** e nella pagina **Creazione rapida**.

| **Campo** | **Descrizione** | **Impatto funzionale** |
| --- | --- | --- |
| Nome | Nome della riga di conto lavoro per facilitare l'identificazione. | Questa verrà mostrata come prima colonna in tutte le ricerche basate sulle righe di conto lavoro. |
| Descrizione | Una breve descrizione dei servizi acquistati nella voce di conto lavoro. |Nessuna |
| Tipo di linea |   Il valore predefinito di questo campo è **Basato su quantità**.| Nessuna |
| Metodo di fatturazione | Questo è un set di opzioni che rappresenta i due principali modelli di contrattazione supportati da Project Operations: **Prezzo fisso** e **Tempistica e materiali**. | In base al metodo di fatturazione selezionato, se è stato selezionato il metodo di fatturazione a prezzo fisso, per le righe del conto di lavoro viene resa disponibile una pianificazione fattura basata su passaggi fondamentali. |
| Classe di transazione | Il valore predefinito è **Ore**. | Ciò indica che la riga del conto lavoro viene utilizzata per registrare un acquisto di ore di lavoro in conto lavoro. |
| Ruolo | Seleziona il ruolo delle risorse in conto lavoro di cui si sta acquistando il tempo. | Il ruolo svolto dalle risorse in conto lavoro determina il costo dell'acquisto. |
| Inizio richiesto | Immetti la data in cui le risorse del subappaltatore devono iniziare a lavorare. | Ciò viene utilizzato per selezionare un listino prezzi dai listini prezzi del progetto allegati al conto lavoro. Il costo del ruolo nella riga del conto lavoro deriva da quel listino prezzi. |
| Fine richiesta | Immetti la data in cui termina l'assegnazione della risorsa del terzista. | Ciò verrà utilizzato per mostrare avvisi quando un responsabile di progetto sta attingendo dalla capacità per i requisiti di risorse che si verificano dopo questa data. |
| Quantità ordinata | Immetti il numero di ore del ruolo acquistato dal fornitore. | Ciò verrà utilizzato per mostrare avvisi quando un responsabile di progetto sta andando oltre questa capacità per i requisiti di risorse. |
| Unità di vendita | Il valore predefinito è **Unità di vendita Ore**, che non può essere modificato. | Nessuna|
| Unità | L'impostazione predefinita per questo campo è l'unità di base delle ore dal **Unità di vendita Ore**. Puoi modificare questo valore per acquistare qualsiasi unità delle **Unità di vendita Ore**, ad esempio giorno o settimana. | La combinazione di **Ruolo** e **Unità** verrà utilizzata come valore predefinito o calcolato per il prezzo unitario per la riga di conto lavoro. |
| Prezzo unitario | Il prezzo unitario predefinito utilizza la combinazione di **Ruolo** e **Unità** dal listino prezzi del progetto applicabile alla data **Inizio richiesto** della riga di conto lavoro. | Quando il listino prezzi del progetto applicabile ha il prezzo impostato in un'unità diversa dall'unità nella voce del conto lavoro, il sistema utilizza la conversione dell'unità per calcolare il prezzo unitario. |
| Subtotale |    Questo è un campo di sola lettura che viene calcolato come Quantità x Prezzo unitario, se vengono immessi sia i valori di quantità che di prezzo unitario. Se il campo Quantità, Prezzo unitario o entrambi sono vuoti, puoi inserire un valore nel campo. | Nessuna|
| IVA |   Immetti l'importo IVA. |Nessuna |
| Totale importo | L'importo totale della voce di conto lavoro incluse le imposte. Questo campo viene calcolato come Subtotale + IVA.|Nessuna |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
