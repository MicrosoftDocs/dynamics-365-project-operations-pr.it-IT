---
title: Gestire i listini prezzi di progetto sulle offerte di progetto
description: Questo argomento fornisce informazioni sull'utilizzo dei listini prezzi di progetto sulle offerte.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3d9c13568921540f4cc2e1e5e58d01803631a339
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598263"
---
# <a name="manage-project-price-lists-on-project-quotes"></a>Gestire i listini prezzi di progetto sulle offerte di progetto 

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le offerte di progetto sono progettate per supportare listini prezzi di vendita con più date di validità. Con Dynamics 365 Project Operations, una nuova entità associata chiamata **Listini prezzi di progetto** è stata aggiunta. Questa entità ha una relazione 1-a-molti con un'offerta di progetto.

I listini prezzi del progetto sono utilizzati per calcolare il prezzo delle transazioni di tempo, materiale e spesa in un progetto. Quando un'offerta include uno o più listini prezzi di progetto, questi listini prezzi vengono utilizzati per determinare il prezzo delle stime di tempo, materiale e spesa e valori effettivi nei progetti associati all'offerta tramite la riga di offerta.

Quando non ci sono listini prezzi di progetto per un'offerta di progetto, riceverai un messaggio di avviso. Il messaggio indica che, poiché non sono presenti listini prezzi di progetto, non verrà assegnato un prezzo al lavoro e alle spese del progetto stimati ed effettivi. Invece, avranno il prezzo zero (0) per i valori di vendita.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Associare o annullare l'associazione di un listino prezzi di un progetto in un'offerta di progetto

Per creare o selezionare un listino prezzi specifico per la stima del lavoro e delle spese in base al progetto, completa i seguenti passaggi.

1. Nell'offerta, seleziona la scheda **Prezzo progetto** e nella griglia secondaria seleziona **+ Aggiungi nuovo listino prezzi di progetto**.
2. Nella pagina Creazione rapida, seleziona un listino prezzi. L'elenco a discesa mostra tutti i listini prezzi che hanno il contesto impostato su **Vendite** e la valuta corrisponde alla valuta dell'offerta.
4. Immetti una descrizione per l'associazione di listini prezzi di progetto e seleziona **Salva e chiudi**.

Viene creata un'associazione di listini prezzi di progetto.

È possibile ripetere questo processo se è necessario associare più di un listino prezzi di progetto all'offerta di progetto. Crea più listini prezzi di progetto solo se sono presenti date di validità diverse su ciascuno dei listini prezzi di progetto associati.

> [!NOTE]
> Project Operations non supporta la sovrapposizione della validità delle date dei listini prezzi di progetto. Se sono presenti più listini prezzi di progetto per una transazione con una determinata data, il prezzo su quella transazione verrà impostato come predefinito su zero (0).
Per rimuovere un'associazione di listini prezzi di progetto, seleziona il listino prezzi di progetto e quindi seleziona **Elimina listino prezzi di progetto di offerta**. Il listino prezzi viene rimosso dai listini prezzi di progetto dell'offerta, ma non viene eliminato. Viene eliminata solo l'associazione all'offerta.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Impostare listini prezzi di progetto predefiniti su un'offerta

I listini prezzi di progetto possono essere impostati come predefiniti su un'offerta di progetto. Questa impostazione garantisce che tutte le offerte nell'organizzazione inizino sempre con un listino prezzi standard per quel periodo di prezzi.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Impostare un valore predefinito organizzativo per i listini prezzi di progetto

1. Vai a **Impostazioni** > **Generali** > **Parametri**.
2. Nella pagina di elenco **Parametri attivi**, individua il record e fai doppio clic per aprirlo. 
3. Nella pagina **Parametri**, seleziona la scheda **Listino prezzi**. Viene visualizzato l'elenco dei listini prezzi predefiniti. Si tratta di un listino prezzi di vendita e costi standard. La disponibilità di un listino prezzi di vendita associato qui per ogni valuta in cui vendi assicurerà che questo listino prezzi di vendita sia utilizzato come predefinito su qualsiasi offerta creata per i clienti che effettuano transazioni in questa valuta.

### <a name="set-up-customer-specific-project-price-lists"></a>Impostare listini prezzi di progetto specifici per il cliente

I listini prezzi di progetto specifici per il cliente possono essere impostati anche dopo aver negoziato un accordo master di determinazione dei prezzi con i clienti.

Per impostare un listino prezzi di progetto specifico per il cliente, completa i seguenti passaggi.

1. Nell'area **Vendite** seleziona **Clienti**.
2. Nell'elenco dei tuoi account attivi, seleziona e apri il record del cliente per il quale disponi di un listino prezzi speciale.
3. Nella scheda **Listini prezzi di progetto**, puoi creare una nuova associazione di listini prezzi per avere il listino prezzi di progetto specifico per questo cliente.

## <a name="create-custom-pricing-on-a-project-quote"></a>Creare una determinazione dei prezzi personalizzata in un'offerta di progetto

Dopo aver impostato i listini prezzi di progetto predefiniti dell'organizzazione e specifici del cliente, le offerte di progetto verranno create automaticamente con queste associazioni di listini prezzi di progetto. Tuttavia, in alcuni casi, potrebbe essere necessario creare una determinazione dei prezzi personalizzata per un'offerta di progetto specifica. 

1. In **Offerta di progetto**, nella scheda **Listino prezzi di progetto**, verifica nella griglia secondaria che non sia selezionato alcun record di listino prezzi specifico.
2. Seleziona **Crea determinazione dei prezzi personalizzata**. Questo effettua delle copie di tutti i listini prezzi standard attualmente associati all'offerta e associa queste copie all'offerta. Le associazioni esistenti ai listini prezzi standard verranno rimosse. Il venditore può quindi iniziare a modificare i prezzi su queste copie. Questi prezzi modificati saranno applicabili solo a questa offerta di progetto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
