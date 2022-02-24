---
title: Impostare le tariffe del costo del lavoro
description: Questo argomento fornisce informazioni su come impostare le tariffe del costo del lavoro in Project Operations
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 697129b65f53359615ea537fe135d657748dd909
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180602"
---
# <a name="set-up-labor-cost-rates"></a>Impostare le tariffe del costo del lavoro

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_


Ogni listino prezzi ha una serie di tariffe di manodopera (prezzi di ruolo) che si allineano con il contenuto e la data di validità del listino prezzi.

1. Crea un listino prezzi e nella scheda **Prezzo ruolo** della griglia secondaria, seleziona **Nuovo ruolo**.
2. Nella pagina **Creazione rapida** seleziona il ruolo e l'unità organizzativa.
3. Immetti le informazioni richieste nei campi.

La tabella seguente include alcuni dei campi importanti quando si creano le tariffe di manodopera in un listino prezzi di costo.

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| Ruolo | Scheda **Generale** e pagine **Creazione rapida** | Seleziona il ruolo a cui si applicata la tariffa di costo. | Il ruolo nella stima in entrata o nel valore effettivo verrà confrontato con questa riga per impostare il costo predefinito del ruolo. |
| Società resourcing | Scheda **Generale** e pagine **Creazione rapida** | Seleziona la persona giuridica a cui è assegnato il ruolo. Ad esempio, uno sviluppatore di Fabrikam India o uno sviluppatore di Fabrikam USA. | La società di gestione risorse nella stima in entrata o nel valore effettivo verrà confrontato con questa riga per impostare la tariffa di costo predefinita del ruolo. |
| Unità gestione risorse | Scheda **Generale** e pagine **Creazione rapida** | Seleziona l'unità organizzativa o la divisione dell'azienda da cui verrà utilizzato questo ruolo. Ad esempio, uno sviluppatore della divisione Robotics di Fabrikam India o uno sviluppatore della divisione Software di Fabrikam USA. | L'unità di gestione risorse nella stima in entrata o nel valore effettivo verrà confrontato con questa riga per impostare il costo predefinito del ruolo. |
| Prezzo | Scheda **Generale** e pagine **Creazione rapida** | Imposta la tariffa di costo per la combinazione di ruolo, società di gestione risorse e unità di gestione risorse. Ad esempio, uno sviluppatore di Fabrikam India costa 1000 INR o uno sviluppatore di Fabrikam USA costa 150 UDS. | Il prezzo è la tariffa di costo predefinita sul costo unitario della stima in entrata o della riga effettiva per la classe di transazione **Tempo**. |
| Valuta | Scheda **Generale** e pagine **Creazione rapida** | Per impostazione predefinita, il valore della valuta proviene dalla valuta nell'intestazione del listino prezzi di costo ma può essere sovrascritta. Ad esempio, uno sviluppatore di Fabrikam India costa 1000 INR. Uno sviluppatore di Fabrikam USA costa 150 USD. | La valuta predefinita sul costo unitario della riga di costo effettiva in entrata per la classe di transazione **Tempo**. In una stima di progetto, il valore della valuta viene convertito nella valuta di progetto e mostrato nella vista su scala cronologica della stima. |
| Pianificazione unità | Scheda **Generale** e pagine **Creazione rapida** | L'impostazione predefinita della pianificazione dell'unità è Tempo e non può essere modificata nell'entità Prezzo ruolo perché vengono utilizzate tariffe espresse per unità di tempo. | Non c'è alcun impatto downstream. |
| Unità | Scheda **Generale** e pagine **Creazione rapida** | Per impostazione predefinita, il valore proviene dal campo **Unità di tempo** nell'intestazione del listino prezzi di costo. Il valore può essere sovrascritto. Ad esempio, uno sviluppatore di Fabrikam India costa 1000 INR per **giorno in India**. Uno sviluppatore di Fabrikam USA costa 150 USD per **giorno in USA**. | Il sistema utilizza il sistema di unità e conversione in unità di base per calcolare un costo unitario per calcolare il prezzo predefinito per unità su una stima in entrata o una riga effettiva. Ad esempio, una stima è per il valore del lavoro di 10 **giorni in India** per uno sviluppatore indiano e l'unità, **giorno in India** è definita come 10 ore. Quando si calcola il costo della riga di stima, l'applicazione calcola il costo unitario sulla stima come: 1000 INR/ 10 ore = 100 INR all'ora, che viene convertito in USD e mostrato come costo unitario nella pagina **Stime di progetto**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Trasferire prezzi e costi per risorse esterne alla divisione o alla persona giuridica

Nelle aziende basate su progetti, è comune utilizzare dipendenti di diverse entità legali o divisioni sui progetti. Un progetto può essere eseguito da una persona giuridica, ma i dipendenti o i consulenti che lavorano al progetto potrebbero provenire dalla stessa persona giuridica o da un'altra, oppure potrebbe esserci una combinazione di entrambi. In Dynamics 365 Project Operations, la persona giuridica proprietaria della consegna del progetto è la **società proprietaria** e la divisione proprietaria della consegna è l'**unità contraente**. Altre persone giuridiche che forniscono risorse sono le **società di gestione risorse** e le divisioni che forniscono risorse sono le **unità di gestione risorse**. Nella maggior parte dei paesi, le società sono tenute a garantire che la persona giuridica o la divisione che fornisce le risorse addebiti alla società proprietaria e all'unità contraente l'utilizzo delle risorse.

Ad esempio, la società Fabrikam deve garantire che Fabrikam India-Robotics abbia negoziato un tariffario dei costi con Fabrikam US-Robotics o Fabrikam UK-Robotics.

Uno sviluppatore di Fabrikam India-Robotic addebita $100 se viene prestato a Fabrikam US-Robotics e $150 se viene prestato a Fabrikam U-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Impostare i costi per le risorse esterne

1. Crea un listino prezzi di costo chiamato *Tariffe di costo Fabrikam US-Robotics* e imposta un intervallo di date di validità.
2. Nel listino prezzi di costo, imposta le tariffe utilizzando le informazioni dalla tabella seguente. 

| Ruolo | Società resourcing | Unità gestione risorse | Tasso di costo |
| --- | --- | --- | --- |
| Developer | Fabrikam India | Fabrikam India-Robotics | 100 |
| Developer | Fabrikam Philippines | Fabrikam Philippines-Robotics | $90 |
| Developer | Fabrikam US | Fabrikam US-Robotics | $150 |

3. Collega questo listino prezzi di costo all'unità organizzativa Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Impostare i prezzi di trasferimento per una risorsa nella valuta appropriata 

In Project Operations, il prezzo delle risorse può essere impostato in qualsiasi valuta. La valuta è quella che si trova nell'intestazione del listino prezzi per impostazione predefinita, ma può essere modificata.

Utilizzando l'esempio per l'impostazione del prezzo di trasferimento, le informazioni potrebbero essere modificate in:

La società Fabrikam deve garantire che Fabrikam India-Robotics abbia negoziato un tariffario dei costi con Fabrikam US-Robotics o Fabrikam UK-Robotics.

Uno sviluppatore di Fabrikam India-Robotics costa 5000 INR se viene prestato a Fabrikam US-Robotics e 5500 INR se viene prestato a Fabrikam UK-Robotics.

Nel listino prezzi di Fabrikam US-Robotics, le tariffe possono essere espresse come:

| Ruolo | Società resourcing | Costo |
| --- | --- | --- |
| Developer | Fabrikam India | 5000 INR |
| Developer | Fabrikam US | 115 USD |

Nel listino prezzi di Fabrikam UK-Robotics, le tariffe possono essere espresse come:

| Ruolo | Società di gestione risorse | Costo |
| --- | --- | --- |
| Developer | Fabrikam India | 5500 INR |
| Developer | Fabrikam UK | 115 GBP |

Il listino prezzi di costo può fornire tariffe di manodopera in più valute. Quando si genera una stima dei costi sul progetto, Project Operations convertirà queste tariffe di costo nella valuta del progetto e li mostrerà all'utente. Quando una'immissione ore viene approvata e viene creato un costo effettivo, il costo effettivo viene prezzato nella valuta della riga di prezzo del ruolo corrispondente nel listino prezzi di costo. I costi effettivi per il tempo su un singolo progetto possono essere registrati in più valute. Tuttavia, durante il roll-up o il riepilogo dei costi di manodopera effettivi a livello di progetto, Project Operations convertirà tutti gli importi dei costi di manodopera nella valuta di progetto che l'utente può visualizzare.
