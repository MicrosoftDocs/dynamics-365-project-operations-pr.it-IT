---
title: Valuta
description: Questo argomento fornisce informazioni su come aggiungere e rimuovere i tipi di valuta in Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1db7e76dbb220954b9f9088b2168eed1a1902abc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078908"
---
# <a name="currency"></a>Valuta

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le valute determinano i prezzi dei prodotti nel catalogo prodotti e il costo delle transazioni, ad esempio gli ordini di vendita. Se i tuoi clienti sono sparsi tra più aree geografiche, aggiungi le loro valute per gestire le transazioni. Aggiungere le valute più appropriate per le esigenze aziendali correnti e future.  

> [!NOTE]
> Se il tuo ambiente è un ambiente Common Data Service sei nell'interfaccia di amministrazione di Power Platform e selezioni la pagina **Valute** ( **Ambienti** > [seleziona ambiente] > **Impostazioni** > **Azienda** > **Valute** ), la pagina sarà vuota. Questo perché impostare una valuta non  è supportato negli ambienti Common Data Service.

## <a name="add-a-currency"></a>Aggiungere una valuta  
Prima di iniziare questa procedura, verifica che il tuo ruolo di sicurezza includa le autorizzazioni di amministratore di sistema. 

1. Nell'interfaccia di amministrazione di Power Platform seleziona un ambiente. 
2. Seleziona **Impostazioni** > **Business Unit**.
3. Seleziona **Valute**.  
4. Seleziona **Nuovo**.  
5. Compila le informazioni come richiesto.  


   |          Campo          |                                                                                                                                                                                                                                                                                                                                                                            Descrizione                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Tipo di valuta**    | - **Sistema** - Seleziona questa opzione se vuoi utilizzare le valute disponibili nelle app basate su modello in Dynamics 365. Seleziona **Ricerca** per cercare una valuta. Quando selezioni un codice valuta, **Nome valuta** e **Simbolo di valuta** vengono aggiunti automaticamente per la valuta selezionata.<br />- **Personalizzato** - Seleziona questa opzione se vuoi aggiungere una valuta non disponibile nelle app basate su modello in Dynamics 365. In questo caso, devi immettere manualmente i valori per **Codice valuta** , **Precisione valuta** , **Nome valuta** , **Simbolo di valuta** e **Conversione valuta**. |
   |    **Codice valuta**    |                                                                                                                                                                                                                                                                                                                                            Abbreviazione della valuta. Ad esempio, **USD** per il dollaro USA.                                                                                                                                                                                                                                                                                                                                            |
   | **Precisione valuta**  |                                                                                                                                                                                  Digita il numero di decimali che vuoi usare per la valuta.  Puoi aggiungere un valore compreso tra 0 e 4. **Nota:** se hai impostato un valore di precisione nella finestra di dialogo **Impostazioni di sistema** , il valore viene visualizzato qui.                                                                                                                                                                                  |
   |    **Nome valuta**    |                                                                                                                                                                                                                                         Se hai selezionato un codice valuta nell'elenco delle valute disponibili nelle app basate su modello in Dynamics 365, il nome della valuta per il codice selezionato viene visualizzato qui. Se hai selezionato **Personalizzata** come tipo di valuta, digita il nome della valuta.                                                                                                                                                                                                                                          |
   |   **Simbolo di valuta**   |                                                                                                                                                                                                                                                                      Se hai selezionato un codice valuta nell'elenco delle valute disponibili in , il simbolo per la valuta selezionata viene visualizzato qui. Se hai selezionato **Personalizzata** come tipo di valuta, immetti il simbolo per la nuova valuta.                                                                                                                                                                                                                                                                       |
   | **Conversione valuta** |                                                                                                                                                                                                                                     Digita il valore della valuta selezionata in termini di un dollaro USA. Questo è il tasso a cui la valuta selezionata viene convertita nella valuta di base. **Importante:** Aggiorna il valore con la frequenza necessaria per evitare calcoli inesatti nelle transazioni.                                                                                                                                                                                                                                      |


6. Una volta completata l'operazione, seleziona **Salva** o **Salva e chiudi** nella barra dei comandi.  

   > [!TIP]
   >  Per modificare una valuta, seleziona la valuta e quindi immetti o seleziona i nuovi valori.  

## <a name="delete-a-currency"></a>Eliminare una valuta  

1. Nell'interfaccia di amministrazione di Power Platform seleziona un ambiente. 
2. Seleziona **Impostazioni** > **Business Unit**.
3. Seleziona **Valute**.  
4. Nell'elenco delle valute, seleziona la valuta da eliminare.  
5. Seleziona **Elimina.**  
6. Conferma l'eliminazione.  

> [!IMPORTANT]
>  Non puoi eliminare le valute in uso in altri record, ma puoi disattivarle. La disattivazione di record di valuta non comporta la rimozione delle informazioni sulla valuta archiviate nei record esistenti, ad esempio opportunità o ordini. Tuttavia, non ti sarà possibile selezionare la valuta disattivata per le nuove transazioni.  
