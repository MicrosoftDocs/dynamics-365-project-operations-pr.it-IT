---
title: Gestire i listini prezzi di progetto sui contratti di progetto
description: Questo argomento fornisce informazioni sulla gestione dei listini prezzi di progetto sui contratti di progetto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824026d0620de809c0366c86c2d4d13fe83d4d1ddd4c0dc1cc2645ff712705d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996486"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Gestire i listini prezzi di progetto sui contratti di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

I contratti di progetto in Dynamics 365 Project Operations sono progettati per supportare più listini prezzi di vendita con data di validità in un contratto. In Project Operations, è presente una nuova entità associata chiamata **Listini prezzi di progetto**. Questa entità ha una relazione uno-a-molti con un contratto di progetto.

I listini prezzi del progetto sono utilizzati per calcolare il prezzo delle transazioni di tempo, materiale e spesa in un progetto. Quando un contratto include uno o più listini prezzi di progetto, questi listini prezzi vengono utilizzati per determinare il prezzo delle stime di tempo, materiale e spesa e valori effettivi nei progetti associati al contratto tramite la voce di contratto.

Quando non sono presenti listini prezzi di progetto in un contratto di progetto, verrà visualizzato un messaggio di avviso indicante che non sono presenti listini prezzi di progetto e che il prezzo di stime, lavoro effettivo del progetto, materiale e spese registrate non verrà determinato. Non ci sarà un prezzo per i valori di vendita.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Associare o annullare l'associazione di un listino prezzi di progetto in un contratto di progetto

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Creare o associare un listino prezzi specifico per la stima di lavoro, materiali e spese basati sul progetto

1. Nel contratto di progetto, seleziona la scheda **Listini prezzi di progetto**.
2. Nella griglia secondaria seleziona **+ Aggiungi nuovo listino prezzi di progetto**.
3. Nell'indicatore **Creazione rapida** seleziona un listino prezzi. 

  L'elenco a discesa mostra tutti i listini prezzi che hanno il contesto impostato su **Vendite**, dove la valuta del listino prezzi corrisponde alla valuta del contratto.
  
4. Immetti una descrizione per l'associazione del listino prezzi di progetto, seleziona **Salva** e quindi chiudi l'indicatore **Creazione rapida**.

   Viene creata un'associazione di listini prezzi di progetto.
   
5. Ripeti i passaggi 1-4 per associare più di un listino prezzi di progetto al contratto di progetto. Crea più listini prezzi di progetto solo se hai una data di validità diversa per ciascuno dei listini prezzi di progetto associati.

> [!NOTE]
> Project Operations non supporta la sovrapposizione delle date di validità dei listini prezzi di progetto. Se sono presenti più listini prezzi di progetto per una transazione con una determinata data, il prezzo di tale transazione verrà impostato su zero.

### <a name="remove-a-project-price-list-association"></a>Rimuovere un'associazione di listino prezzi di progetto

- Seleziona il listino prezzi di progetto, quindi seleziona **Elimina listino prezzi di progetto del contratto** sulla griglia secondaria. 

  Il listino prezzi viene rimosso dai listini prezzi di progetto nel contratto. Il listino prezzi non verrà cancellato. Verrà eliminata solo l'associazione al contratto.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Impostare automaticamente il listino prezzi predefinito di progetto su un contratto

Un listino prezzi di progetto può essere impostato come listino prezzi di progetto predefinito. Questa configurazione garantisce che tutti i contratti nell'organizzazione inizino sempre con un listino prezzi di progetto standard per quel periodo di prezzo.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Impostare l'impostazione predefinita dell'organizzazione per i listini prezzi di progetto

1. Vai a **Impostazioni** > **Generale** e quindi seleziona **Parametri**.
2. Nella pagina elenco **Parametri attivi**, seleziona e fai doppio clic sul record per aprirlo. Durante il doppio clic, assicurati di non fare clic su un valore di campo che è un collegamento ipertestuale. 
3. Nella pagina **Parametri attivi** seleziona la scheda **Listino prezzi**. Una griglia secondaria mostra un elenco di listini prezzi predefiniti. Questo è un elenco di listini prezzi di vendita e costi standard. Avere un listino prezzi di **vendita** associato per ogni valuta in cui vendi garantisce che il listino prezzi di vendita sia l'impostazione predefinita per qualsiasi contratto creato per i clienti che effettuano transazioni in questa valuta.

### <a name="set-up-a-customer-specific-project-price-list"></a>Impostare un listino prezzi di progetto specifico per il cliente

Puoi inoltre impostare listini prezzi di progetto specifici per il cliente dopo aver negoziato un contratto master sui prezzi con i clienti.

1. Vai a **Vendite** > **Clienti**.
2. Dall'elenco dei conti attivi, seleziona il cliente per il quale hai un listino prezzi speciale.
3. Seleziona il record del cliente per aprirlo, quindi seleziona la scheda **Listini prezzi di progetto**. Una griglia secondaria mostra un elenco di listini prezzi di progetto specifici per questo cliente. 
4. Crea qui una nuova associazione di listino prezzi per avere un listino prezzi di progetto specifico per questo cliente.

## <a name="custom-pricing-on-a-project-contract"></a>Prezzi personalizzati su un contratto di progetto

Dopo aver ottenuto i listini prezzi di progetto predefiniti dell'organizzazione e specifici del cliente, i contratti di progetto verranno creati automaticamente con queste associazioni di listini prezzi di progetto. Tuttavia, i listini prezzi di progetto su un contratto di progetto vengono sempre copiati con la data e il nome del contratto aggiunti alla fine del nome. Il conto e i responsabili di progetto possono quindi iniziare a modificare i prezzi su queste copie. Questi prezzi modificati saranno applicabili solo a questo contratto di progetto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
