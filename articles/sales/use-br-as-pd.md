---
title: Utilizzare una risorsa prenotabile come dimensione di determinazione dei prezzi
description: In questo argomento vengono fornite informazioni sull'utilizzo di una risorsa prenotabile come dimensione di determinazione dei prezzi.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d46d4659a5f60226f80b29f3dd8607249cb91ac2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011196"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Utilizzare una risorsa prenotabile come dimensione di determinazione dei prezzi

 _**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_ 

In questo argomento vengono fornite informazioni sull'utilizzo di una risorsa prenotabile come dimensione di determinazione dei prezzi. Se la tua strategia di prezzo è impostata in modo che ogni risorsa prenotabile deve avere un prezzo o una tariffa di costo specifici, utilizza una risorsa prenotabile come dimensione di prezzo.

## <a name="prerequisites"></a>Prerequisiti
Prima di completare le procedure in questo argomento, devi disporre di una nuova soluzione per la dimensione dei prezzi per la tua organizzazione. Se non ne hai già creato uno, vedi [Crea campi ed entità personalizzati](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Aggiungi il campo Risorsa prenotabile ai moduli e alle viste
Per rendere il campo **Risorsa prenotabile** visibile nella soluzione dimensione prezzo, è necessario aggiungere il campo a tutti i moduli e le viste come entità.

La tabella seguente elenca tutti i moduli e le visualizzazioni predefiniti, per entità. Sarà inoltre necessario aggiungere il nuovo campo a eventuali moduli o visualizzazioni aggiuntivi nelle entità personalizzate.

|   Entity        | Form   |Visualizzazioni        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prezzo ruolo| Informazioni | - Prezzi categorie di risorse attivi<br> - Associato a prezzo categoria di risorsa |
|  Ricarico prezzo ruolo| Informazioni| - Ricarico prezzo ruolo attivo<br>- Vista associata ricarichi prezzo ruolo |
|  Dettagli riga di offerta| - Informazioni sul progetto<br>- Creazione rapida progetti| - Dettagli di riga di offerta attiva<br>- Dettagli di riga di offerta combinata<br>- Visualizzazione associata dettagli di riga di offerta |
|  Dettagli di voce di contratto di progetto| - Informazioni sul progetto<br>- Creazione rapida progetti| - Dettagli voce di contratto combinati<br>- Dettagli voce di contratto attivi<br>- Associata a dettaglio voce di contratto |
|  Attività di progetto| - Informazioni<br>- Nuovo modulo| &nbsp; |
|  Membro del team di progetto| - Informazioni<br>- Nuovo modulo| - Membri del team di progetto attivi<br>- Membri del team di progetto<br>- Visualizzazione associata membri del team di progetto |
|  Inserimento ore| - Informazioni<br>- Crea inserimento ore| - Inserimenti ore personali per data<br>- Inserimenti ore personali per questa settimana<br>- Inserimenti ore per l'approvazione|
|  Riga giornale di registrazione| - Informazioni<br>- Creazione rapida| - Righe giornale di registrazione attive<br>- Visualizzazione associata riga giornale di registrazione |
|  Dettagli di riga fattura| - Informazioni<br>- Creazione rapida| - Dettagli di riga fattura attiva<br>- Transazioni fattura addebitabili<br>- Transazioni fattura gratuite<br>- Visualizzazione associata dettagli di riga fattura <br>- Transazione fattura non addebitabile|
|  Effettiva| - Informazioni<br>- Valori effettivi attivi| Associata a valore effettivo |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Impostare una risorsa prenotabile come dimensione di determinazione dei prezzi
Per impostare una risorsa prenotabile come dimensione di determinazione dei prezzi, seguire questa procedura:

1. Vai a **Impostazioni** > **Parametri**. 
2. Nella pagina **Parametro**, nella scheda **Dimensioni di determinazione dei prezzi basate su importo**, verifica che la griglia nella scheda mostra i record nell'entità **Dimensioni di determinazione dei prezzi**. 
2. Aggiungi **Risorsa prenotabile** a questo elenco di dimensioni di determinazione dei prezzi come **msdyn_bookableresource**. 
3. In **Applicabile al costo** e **Applicabile alle vendite**, seleziona un valore.
4. In **Tipo di dimensione**, seleziona **Basata su importo**. 
5. Seleziona la priorità di vendita e costo per la risorsa prenotabile. In genere, una risorsa prenotabile ha la massima priorità quando inclusa come dimensione del prezzo. Imposta la priorità su **1** (o **0** a seconda di come si conta la priorità) per garantire questo comportamento.

## <a name="set-up-pricing-dimension-field-names"></a>Configurare nomi di campo di dimensioni di determinazione dei prezzi

Quando il nome di campo di una dimensione di determinazione dei prezzi nella tabella **Prezzo ruolo** è diverso dal relativo nome di campo in una qualsiasi delle altre entità in cui si deve utilizzare il prezzo predefinito, il record della dimensione di determinazione dei prezzi deve essere notificato in relazione ai differenti nomi.  

Per una risorsa prenotabile, l'entità **Membri del team di progetto** ha un nome di campo leggermente diverso da quello dell'entità **Prezzo ruolo**: 

 - **Membri del team di progetto** entità = **msdyn_bookableresourceid**
 - **Prezzo del ruolo** entità = **msdyn_bookableresource**

È necessario indicare questa differenza nel record della dimensione di determinazione dei prezzi di **msydn_bookableresource**.

1. Fai doppio clic sulla riga nella griglia **Dimensioni di determinazione dei prezzi** per aprire la pagina di **msdyn_bookableresource**.
2. Nella pagina della dimensione, nella scheda **Elementi correlati**, seleziona **Nomi campo dimensioni determinazione dei prezzi**.

  ![Scheda Nomi campo dimensioni determinazione dei prezzi](media/PD-fieldname.png)

3. Nella vista associata che viene aperta, seleziona **Aggiungi nuovo nome campo dimensioni determinazione dei prezzi**.

  ![Aggiungi nuovo nome campo dimensioni determinazione dei prezzi](media/Add-NewPD-fieldname.png)

  Viene aperta la pagina **Nuovo nome campo dimensioni di determinazione dei prezzi** per **msdyn_bookableresource**. 

4. Nella pagina **Nuovo nome campo dimensione determinazione prezzo**, aggiungi **msdyn_projectteam** per **Nome locale dell'entità**.
5. Aggiungi **msdyn_bookableresourceid** a **Nome campo**.

 ![Modulo Nuovo nome campo dimensioni di determinazione dei prezzi](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]