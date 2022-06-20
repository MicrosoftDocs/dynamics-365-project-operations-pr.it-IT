---
title: Impostare le tariffe per la fatturazione del lavoro
description: Questo articolo fornisce informazioni su come impostare le tariffe di fatturazione del lavoro in Project Operations.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ad83e899030be480baed95597e1ccfc0e560e24
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924343"
---
# <a name="set-up-labor-bill-rates"></a>Impostare le tariffe per la fatturazione del lavoro

_ **Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati

Ogni listino prezzi ha una serie di prezzi di ruolo, o tariffe di manodopera che sono valide per il contenuto e la data di validità inclusa nell'intestazione del listino prezzi. I tassi di fatturazione per il tempo in Dynamics 365 Project Operations possono essere impostati in una sola valuta, che è la valuta nell'intestazione del listino prezzi.

1. Per impostare le tariffe di fatturazione del lavoro per un listino prezzi di vendita, vai a **Vendita** > **Clienti** > **Listini prezzi** e seleziona **Nuovo** per creare un nuovo listino prezzi. 
2. Nella scheda **Prezzi ruolo**, nella griglia secondaria, seleziona **Nuovo prezzo ruolo**. 
3. Nel riquadro **Creazione rapida** immetti la combinazione di ruolo e unità organizzativa per cui è necessario impostare la tariffa di fatturazione.

   La tabella seguente include i campi della scheda **Generale** e nel riquadro **Creazione rapida** di una riga di prezzo del ruolo che devi tenere a mente quando crei i prezzi del ruolo in un listino prezzi di vendita:

    | Campo | Ufficio | Descrizione | Impatto downstream |
    | --- | --- | --- | --- |
    | Ruolo | Scheda **Generale** e riquadro **Creazione rapida** | Seleziona il ruolo per il quale stai impostando la tariffa di fatturazione. | Il ruolo nella stima in entrata o nel valore effettivo verrà confrontato con questa riga per impostare la tariffa di fatturazione predefinita del ruolo. |
    | Società resourcing | Scheda **Generale** e riquadro **Creazione rapida** | Seleziona la società o la persona giuridica da cui è assegnato il ruolo. Ad esempio, uno sviluppatore di Fabrikam India o uno sviluppatore di Fabrikam USA. | La società di gestione risorse nella stima in entrata o nel valore effettivo verrà confrontato con questa riga per impostare la tariffa di fatturazione predefinita del ruolo. |
    | Unità gestione risorse | Scheda **Generale** e riquadro **Creazione rapida** | Seleziona l'unità organizzativa o la divisione dell'azienda da cui proviene il ruolo. Ad esempio, uno sviluppatore della divisione Robotics di Fabrikam India o uno sviluppatore della divisione Software di Fabrikam USA. | L'unità di gestione risorse nella stima in entrata o nel valore effettivo verrà confrontato con questa riga per impostare la tariffa di fatturazione predefinita del ruolo. |
    | Prezzo | Scheda **Generale** e riquadro **Creazione rapida** | Imposta la tariffa di fatturazione per la combinazione di ruolo, società di gestione risorse e unità di gestione risorse. Ad esempio, uno sviluppatore di Fabrikam India ha una tariffa di fatturazione di 100 USD o uno sviluppatore di Fabrikam USA ha una tariffa di fatturazione di 150 USD. | Il prezzo è la tariffa di fatturazione predefinita sul prezzo unitario della stima in entrata o della riga effettiva per la classe di transazione Tempo. |
    | Valuta | Scheda **Generale** e riquadro **Creazione rapida**| Per impostazione predefinita, il valore della valuta proviene dalla valuta nell'intestazione del listino prezzi di vendita. In un listino prezzi di vendita, la valuta non può essere sovrascritta. | La valuta è la valuta predefinita sul prezzo unitario della riga di vendita effettiva in entrata per la classe di transazione Tempo. |
    | Pianificazione unità | Scheda **Generale** e riquadro **Creazione rapida** | L'impostazione predefinita della pianificazione dell'unità è Tempo e non può essere modificata nell'entità Prezzo ruolo perché vengono utilizzate tariffe espresse per unità di tempo. | Non vi è alcun impatto downstream per questo campo. |
    | Unità | Scheda **Generale** e riquadro **Creazione rapida** | Il valore unitario proviene dal campo **Unità di tempo** nell'intestazione del listino prezzi di vendita. Tuttavia il valore può essere sovrascritto. Ad esempio, uno sviluppatore di Fabrikam India ha una tariffa di fatturazione di 1000 USD per **giorno in India**. Uno sviluppatore di Fabrikam USA ha una tariffa di fatturazione di 1500 USD per **giorno in USA**. | Quando il prezzo unitario predefinito viene utilizzato in una riga di valore effettivo o stima in entrata, il sistema utilizza il sistema di unità e conversione in unità di base per calcolare un costo unitario. Ad esempio, una stima è per il valore del lavoro di 10 **giorni in India** per uno sviluppatore indiano e l'unità, giorno in India è definita come 10 ore. Quando si determina il prezzo di quella riga di stima, l'applicazione calcola il prezzo unitario sulla stima come 1000 USD / 10 ore = 100 USD all'ora. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Trasferire i prezzi o impostare le tariffe di fatturazione per le risorse di altre unità organizzative o divisioni 

Le società basate su progetto spesso utilizzano dipendenti di diverse persone giuridiche e diverse divisioni all'interno della persona giuridica per lavorare sui progetti. I progetti possono essere eseguiti da una persona giuridica e una divisione specifica, mentre i dipendenti o i consulenti che lavorano sui progetti potrebbero provenire dalla stessa persona giuridica o divisione oppure da un'altra. Il progetto potrebbe anche essere costituito da una combinazione di persone provenienti da persone giuridiche e divisioni diverse. In Project Operations, la persona giuridica proprietaria della consegna del progetto è chiamata **società proprietaria** e la divisione proprietaria della consegna è chiamata **unità contraente**. Tutte le altre persone giuridiche che forniscono risorse sono chiamate **società di gestione risorse** e le divisioni che forniscono risorse sono chiamate **unità di gestione risorse**. A causa delle differenze nel costo del lavoro nelle varie aree geografiche e mercati in tutto il mondo, anche le tariffe di fatturazione del lavoro sono impostate in modo diverso per le diverse aree geografiche.

Ad esempio, uno sviluppatore delle divisione v di Fabrikam India che lavora a un progetto negli Stati Uniti viene fatturato alla tariffa di 100 USD all'ora. A uno sviluppatore della divisione Robotics di Fabrikam US che lavora su un progetto US viene fatturato a 150 USD all'ora. 

### <a name="example-set-up-a-bill-rate"></a>Esempio: impostare un tasso di fatturazione 

1. Crea un listino prezzi di vendita chiamato *Tariffe di fatturazione Fabrikam US* e imposta la validità della data.
2. Nel listino prezzi di vendita immetti le seguenti tariffe:

    | Ruolo | Società di gestione risorse | Unità gestione risorse | Tasso di fatturazione |
    | --- | --- | --- | --- |
    | Developer | Fabrikam India | Fabrikam India - Robotics | 100 |
    | Developer | Fabrikam Philippines | Fabrikam Philippines - Robotics | $90 |
    | Developer | Fabrikam US | Fabrikam US - Robotics | $150 |

3. Collega il listino prezzi di vendita, **Tariffe di fatturazione Fabrikam US** al listino prezzi di progetto del contratto di progetto o a un determinato conto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
