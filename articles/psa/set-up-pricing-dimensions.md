---
title: Configurare campi personalizzati come dimensioni di determinazione dei prezzi
description: In questo articolo vengono fornite informazioni sull'impostazione di dimensioni di determinazione dei prezzi.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 14d27b53b42744d47e298bf5a926c1262dbf44d4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922602"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Configurare campi personalizzati come dimensioni di determinazione dei prezzi 

[!include [banner](../includes/psa-now-project-operations.md)]

Questo articolo presuppone che tu abbia completato le procedure negli articoli [Creare campi ed entità personalizzati](create-custom-fields-entities.md) e [Aggiungere campi personalizzati alla configurazione dei prezzi e ad entità transazionali](field-references.md). Se non hai completato queste procedure, completale prima di leggere questo articolo. 

In questo articolo vengono fornite informazioni sull'impostazione di dimensioni di determinazione dei prezzi. Nell'interfaccia Web di Project Service, nella pagina **Parametri**, la scheda **Dimensioni di determinazione dei prezzi basate su importo** mostra i record nelle entità Dimensione di determinazione dei prezzi. Per impostazione predefinita, l'installazione di Project Service crea 2 righe nella griglia d questa scheda:

- **msdyn_resourcecategory** (Ruolo)
- **msdyn_OrganizationalUnit** (Unità organizzativa)

> [!IMPORTANT]
> Non eliminare queste righe. Tuttavia, se non sono necessarie, puoi renderle non applicabili in uno specifico contesto impostando **Costo applicabile a**, **Vendite applicabili a** e **Acquisto applicabile a** su **No**. L'impostazione di questi valori di attributo su **No** ha lo stesso effetto di non avere il campo come dimensione di determinazione dei costi.

Affinché un campo diventi una dimensione di determinazione dei costi, deve essere:

- Creato come campo nelle entità **Prezzo ruolo** e **Ricarichi prezzo ruolo**. Per ulteriori informazioni su come eseguire questa operazione, vedi [Aggiungere campi personalizzati alla configurazione dei prezzi e ad entità transazionali](field-references.md).
- Creato come riga nella tabella **Dimensione di determinazione dei prezzi**. Ad esempio, aggiungi righe come dimensioni di determinazione dei prezzi come mostrato nell'illustrazione seguente. 

![Righe di dimensioni di determinazione dei prezzi basate su importo.](media/Amt-based-PD.png)

Nota che il campo Ore lavorative della risorsa (**msdyn_resourceworkhours**) è stato aggiunto come dimensione basata su ricarico e alla griglia nella scheda **Dimensione di determinazione dei prezzi basata su ricarico**.

![Righe di dimensioni di determinazione dei prezzi basate su ricarico.](media/Markup-based-PD.png)

> [!IMPORTANT]
> Tutte le modifiche ai dati nuovi o esistenti delle dimensioni di determinazione dei prezzi in questa tabella vengono propagate alla regole di business per la determinazione dei prezzi di Project Service solo dopo l'aggiornamento della cache. L'aggiornamento della cache può durare fino a 10 minuti. Utilizza questo tempo per dare un'occhiata alle modifiche alla logica di impostazione predefinita dei prezzi che deve risultare dalle modifiche ai dati di Dimensione di determinazione dei prezzi.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Attributi della tabella Dimensioni di determinazione dei prezzi
Le sezioni seguenti forniscono informazioni sui differenti attributi nella tabella **Dimensioni di determinazione dei prezzi**.

### <a name="pricing-dimension-name"></a>Nome della dimensione di determinazione dei prezzi
Questo valore deve essere esattamente uguale al nome di schema del campo aggiunto alla tabella **Prezzo ruolo** per le dimensioni di determinazione dei prezzi personalizzate. Per ulteriori informazioni sull'aggiunta di campi alla tabella **Prezzo ruolo**, vedi [Aggiungere campi personalizzati alla configurazione dei prezzi e ad entità transazionali](field-references.md).

### <a name="type-of-dimension"></a>Tipo di dimensione
Esistono due tipi di dimensioni di determinazione dei prezzi
  
  - **Dimensioni basate su importo**: i valori delle dimensioni nel contesto di input sono allineati ai valori delle dimensioni nella riga **Prezzo ruolo** e il prezzo/costo viene definito per impostazione predefinita direttamente dalla tabella **Prezzo di ruolo**.
  - **Dimensioni basate su ricarico**: queste sono le dimensioni in cui Project Service utilizza i seguenti 3 passaggi per ottenere il prezzo/costo
 
    1. Project Service allinea i valori delle dimensioni non basate su ricarico nel contesto di input alla riga Prezzi ruolo per ottenere il tasso di base.
    2. Project Service allinea tutti i valori delle dimensioni nel contesto di input alla riga **Prezzi ruolo** per ottenere una percentuale di ricarico.
    3. Project Service applica la percentuale di ricarico del secondo passaggio al tasso di base ottenuto dalla tabella **Prezzo ruolo** nel primo passaggio per arrivare al prezzo/costo finale.
   
   Nella tabella seguente viene illustrato il calcolo dei ricarichi del prezzo.
  
| Ruolo        | Unità organizzativa    |Ubicazione lavoro      |Titolo standard      |Ore lavorative risorsa      |  Ricarico|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|In loco            |                    |Straordinario                 |15     |
|             | Contoso India|Locale             |                    |Straordinario                 |10     |
|             | Contoso US   |Locale             |                    |Straordinario                 |20     |


Se una risorsa di Contoso India il cui tasso di base è 100 USD lavora in loco e registra 8 ore di lavoro normale e 2 ore di straordinario nell'inserimento ore, il motore di determinazione dei prezzi di Project Service utilizza il tasso base 100 per 8 ore per registrare 800 USD. Per le 2 ore di straordinario, viene applicato un ricarico del 15% al tasso di base 100 per ottenere un prezzo unitario di 115 USD e un costo totale di 230 USD.

### <a name="applicable-to-cost"></a>Costo applicabile a 
Se questo campo è impostato su **Sì**, indica che il valore della dimensione nel contesto di input deve essere utilizzato per l'allineamento al **prezzo ruolo** e al **ricarico prezzo ruolo** quando si recuperano i tassi di costo e di ricarico.

### <a name="applicable-to-sales"></a>Vendite applicabili a
Se questo campo è impostato su **Sì**, indica che il valore della dimensione nel contesto di input deve essere utilizzato per l'allineamento al **prezzo ruolo** e al **ricarico prezzo ruolo** quando si recuperano i tassi di fatturazione e di ricarico.

### <a name="applicable-to-purchase"></a>Acquisto applicabile a
Se questo campo è impostato su **Sì**, indica che il valore della dimensione nel contesto di input deve essere utilizzato per l'allineamento al **prezzo ruolo** e al **ricarico prezzo ruolo** quando si recupera il prezzo di acquisto. Attualmente Project Service non supporta scenari di subappalto, quindi questo campo non è utilizzato. 

### <a name="priority"></a>Priorità
L'impostazione della priorità delle dimensioni consente a Project Service di generare un prezzo anche quando non è possibile trovare una corrispondenza esatta tra i valori di dimensione di input e i valori della tabella **Ricarico prezzo ruolo** o **Prezzo ruolo**. In questo scenario, Project Service utilizza valori null per i valori di dimensione non corrispondenti valutando le dimensioni in ordine di priorità.

- **Priorità costo**: il valore della priorità costo di una dimensione indica il peso di quella dimensione durante l'allineamento alla configurazione dei prezzi di costo. Il valore di **Priorità costo** deve essere univoco nelle dimensioni **applicabili al costo**.
- **Priorità vendite**: il valore della priorità vendite di una dimensione indica il peso di quella dimensione durante l'allineamento alla configurazione dei prezzi di vendita o dei tassi di fatturazione. Il valore di **Priorità vendite** deve essere univoco nelle dimensioni **applicabili alle vendite**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
