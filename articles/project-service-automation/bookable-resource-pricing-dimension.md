---
title: Utilizzare una risorsa prenotabile come dimensione di determinazione dei prezzi
description: In questo argomento vengono fornite informazioni sull'utilizzo di una risorsa prenotabile come dimensione di determinazione dei prezzi.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 1d147827-dc55-48a5-b3f6-d8b00bd1c7f7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 999f7575d1777077376ba74933654b90fcc504c3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752655"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Utilizzare una risorsa prenotabile come dimensione di determinazione dei prezzi
In questo argomento vengono fornite informazioni sull'utilizzo di una risorsa prenotabile come dimensione di determinazione dei prezzi. Prima di iniziare, crea una soluzione per le dimensioni di determinazione dei prezzi se non lo hai già fatto. Se disponi già di tale soluzione, puoi apportare le modifiche in quella soluzione. Se non hai ancora creato questa soluzione per l'organizzazione, completa le procedure nell'argomento [Creare campi ed entità personalizzati](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Aggiungere una risorsa prenotabile a moduli e viste
Per rendere i campi visibili nell'interfaccia utente nella soluzione Dimensione di determinazione dei prezzi, devi esaminare tutti i moduli e viste delle entità Project Service principali e aggiungere tali campi a moduli e viste di queste entità.
La tabella seguente è un elenco completo di moduli e viste predefinite, elencati per entità, che devono essere aggiornati. Se sono presenti ulteriori viste o moduli nelle personalizzazioni di queste entità, aggiungi i nuovi campi anche a questi.
Aprire Esplora soluzioni per la soluzione Dimensione di determinazione dei prezzi e quindi fai clic su **Pubblica tutte le personalizzazioni**.


|   Entità        | Moduli   |Visualizzazioni        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prezzo ruolo|• Informazioni |• Prezzi categorie di risorse attivi<br> • Vista Prezzo categoria di risorsa associata|
|  Ricarico prezzo ruolo|• Informazioni|• Ricarico prezzo ruolo attivo<br>• Vista Ricarico prezzo ruolo associata|
|  Dettagli riga di offerta|• Informazioni sul progetto<br>• Creazione rapida progetti|• Dettagli di riga di offerta attiva<br>• Dettagli di riga di offerta combinata<br>• Vista Dettagli riga di offerta associata|
|  Dettagli di voce di contratto di progetto|• Informazioni sul progetto<br>• Creazione rapida progetti|• Dettagli voce di contratto combinati<br>• Dettagli voce di contratto attivi<br>• Vista Dettaglio riga di contratto associata|
|  Membro del team di progetto|• Informazioni<br>• Nuovo modulo|• Membri del team di progetto attivi<br>• Membri del team di progetto<br>• Vista Membri del team di progetto associata|
|  Inserimento ore|• Informazioni<br>• Crea inserimento ore|• Inserimenti ore personali per data<br>• Inserimenti ore personali per questa settimana<br>• Inserimenti ore per l'approvazione.|
|  Riga giornale di registrazione|• Informazioni<br>• Creazione rapida|• Righe giornale di registrazione attive<br>• Vista Riga giornale di registrazione associata|
|  Dettagli di riga fattura|• Informazioni<br>• Creazione rapida|• Dettagli di riga fattura attiva<br>• Transazioni fattura addebitabili<br>• Transazioni fattura gratuite<br>• Vista Dettagli di riga fattura associata<br>• Transazione fattura non addebitabile|
|  Valore effettivo|• Informazioni<br>• Valori effettivi attivi|• Vista Valore effettivo associata|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Impostare una risorsa prenotabile come dimensione di determinazione dei prezzi

1. Nell'interfaccia Web, seleziona **Project Service** > **Impostazioni** > **Parametri**. Nella pagina **Parametro**, nella scheda **Dimensioni di determinazione dei prezzi basate su importo**, nota che la griglia nella scheda mostra i record nell'entità Dimensioni di determinazione dei prezzi. 
2. Aggiungi **Risorsa prenotabile** a questo elenco di dimensioni di determinazione dei prezzi come **msdyn_bookableresource**. 
3. Indica il contesto in cui la risorsa prenotabile viene utilizzata come dimensione di determinazione dei prezzi e imposta i valori **Costo applicabile a** e **Vendite applicabili a**.
4. Nel campo **Tipo di dimensione**, seleziona **Basata su importo**. 
5. Seleziona la priorità di vendita e costo per la risorsa prenotabile. In genere, quando inclusa come dimensione di determinazione dei prezzi, una risorsa prenotabile ha la priorità più alta di conseguenza se si imposta **1** (o **0** a seconda di come si conta la priorità) si assicura tale comportamento.

## <a name="set-up-pricing-dimension-field-names"></a>Configurare nomi di campo di dimensioni di determinazione dei prezzi

Quando il nome di campo di una dimensione di determinazione dei prezzi nella tabella **Prezzo ruolo** è diverso dal relativo nome di campo in una qualsiasi delle altre entità in cui si deve utilizzare la determinazione dei prezzi predefinita, è necessario indicare l'esistenza di nomi differenti nel record della dimensione di determinazione dei prezzi.    
Per la risorsa prenotabile, l'entità **Membri del team di progetto** ha un nome di campo leggermente diverso (**msdyn_bookableresourceid**) da quello dell'entità **Prezzo ruolo** (**msdyn_bookableresource**). È necessario indicare questa differenza nel record della dimensione di determinazione dei prezzi di **msydn_bookableresource**. 
1. A tale scopo, fai doppio clic sulla riga nella griglia **Dimensioni di determinazione dei prezzi** per aprire la pagina di **msdyn_bookableresource**
2. Nella pagina della dimensione, nella scheda **Elementi correlati**, fai clic su **Nomi campo dimensioni determinazione dei prezzi**.

 ![Scheda Nomi campo dimensioni determinazione dei prezzi](media/PD-fieldname.png)

4. Nella vista associata che viene aperta, fai clic su **Aggiungi nuovo nome campo dimensioni determinazione dei prezzi**.

 ![Aggiungi nuovo nome campo dimensioni determinazione dei prezzi](media/Add-NewPD-fieldname.png)


Viene aperta la pagina **Nuovo nome campo dimensioni di determinazione dei prezzi** per **msdyn_bookableresource**. 

5. Aggiungi **msdyn_projectteam** al campo **Nome logico entità** e **msdyn_bookableresourceid** al campo **Nome campo**. Salvare il record.

 ![Modulo Nuovo nome campo dimensioni di determinazione dei prezzi](media/PD-fieldname-Added.png)
