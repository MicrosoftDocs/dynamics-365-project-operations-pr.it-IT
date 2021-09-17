---
title: Righe conto lavoro per orario
description: Questo argomento spiega come registrare le righe di conto lavoro per orario e registrare l'acquisto di ore dai fornitori.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323871"
---
# <a name="subcontract-lines-for-time"></a>Righe conto lavoro per orario

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Un conto lavoro in Dynamics 365 Project Operations può avere una voce di conto lavoro per le ore. Le voci di conto lavoro per il tempo consentono a un responsabile di progetto di acquistare il tempo delle risorse del fornitore per le attività di progetto del personale e i requisiti di risorse.

Per creare una voce di conto lavoro per le ore in Project Operations, completare la seguente procedura.

1. Nel riquadro di spostamento, seleziona **Conti lavoro** e apri un conto lavoro.
2. Nella scheda **Voci di conto lavoro**, seleziona **Nuovo** per creare una nuova riga conto lavoro.
3. Nella pagina **Creazione rapida**, nel campo **Classe di transazione**, seleziona **Ore**.
4. Immetti le altre informazioni nel campo e quindi seleziona **Salva**.

  La seguente tabella fornisce informazioni sui campi nella pagina **Voce conto lavoro** e nella pagina **Creazione rapida**.

| **Campo** | **Descrizione** |
| --- | --- |
| Nome | Il nome della voce di conto lavoro. |
| Descrizione | Una breve descrizione dei servizi acquistati nella voce di conto lavoro. | 
| Tipo di linea | Questo campo è un valore predefinito.  |
| Metodo di fatturazione | Seleziona il metodo di fatturazione. In base al metodo di fatturazione della voce di conto lavoro a cui si fa riferimento, viene reso disponibile un programma di fatturazione basato su passaggi fondamentali per il metodo di fatturazione a prezzo fisso. |
| Classe di transazione | Questo campo è un valore predefinito che indica se la voce di conto lavoro viene utilizzata per registrare un acquisto di ore di lavoro in conto lavoro. |
| Ruolo | Il ruolo delle risorse in conto lavoro il cui tempo viene acquistato. Il ruolo assegnato alle risorse in conto lavoro determina il costo dell'acquisto. |
| Inizio richiesto | La data in cui le risorse del terzista sono necessarie per iniziare a lavorare. La data richiesta viene utilizzata anche per selezionare un listino prezzi per il progetto dai listini allegati al conto lavoro. Il costo del ruolo nella voce del conto lavoro viene quindi predefinito da quel listino prezzi. |
| Fine richiesta | La data in cui termina l'assegnazione delle risorse del terzista. Questa data viene utilizzata per mostrare avvisi quando un responsabile di progetto attinge a questa capacità per i requisiti di risorse che si verificano dopo tale data. |
| Quantità ordinata | Il numero di ore di ruolo acquistate dal fornitore. Questo valore viene utilizzato per mostrare avvisi quando un responsabile di progetto eccede questa capacità per i requisiti di risorse. |
| Unità di vendita | Il valore predefinito di questo campo sono le unità di vendita Ore e non può essere modificato.  |
| Unità | L'impostazione predefinita di questo campo è l'unità di base delle ore delle unità di vendita Ore. Puoi modificare questo valore per acquistare qualsiasi unità delle unità di vendita Ore, ad esempio giorno o settimana. La combinazione di Ruolo e Unità viene utilizzata per calcolare il prezzo unitario predefinito nella voce del conto lavoro. |
| Prezzo unitario | Il prezzo unitario viene predefinito utilizzando la combinazione di Ruolo e Unità dalle voci di listino applicabile per la data di inizio richiesta della voce di conto lavoro. Quando il listino prezzi del progetto applicabile ha il prezzo impostato in un'unità diversa dall'unità nella voce del conto lavoro, il sistema utilizza la conversione dell'unità per calcolare il prezzo unitario. |
| Subtotale | Questo è un campo di sola lettura che viene calcolato automaticamente come **Quantità x Prezzo unitario** se vengono inseriti sia il valore della quantità che del prezzo unitario. Se il campo Quantità, Prezzo unitario o entrambi sono vuoti, puoi inserire un valore nel campo. |
| IVA |  Immetti l'importo IVA. |
| Totale importo | L'importo totale della voce di conto lavoro dopo l'inclusione delle imposte. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
