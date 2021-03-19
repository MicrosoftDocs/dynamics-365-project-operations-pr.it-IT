---
title: Mappare progetti e attività a una riga dell'offerta basata su progetto
description: Questo argomento fornisce informazioni su come mappare progetti e attività a una riga di attività basata sul progetto.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272753"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Mappare progetti e attività a una riga dell'offerta basata su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Nelle righe di offerta basate sul progetto, è possibile mappare le attività specifiche di un progetto già associato a una riga di offerta.

Quando si mappano attività a una riga di offerta, i seguenti elementi definiti nella riga di offerta verranno applicati solo a tali attività:

- Metodo di fatturazione
- Opzioni di esigibilità
- Limite da non superare
- Clienti

Ad esempio, puoi avere un progetto in cui una fase è a prezzo fisso e tutte le altre fasi sono tempistica e materiali. In questo caso, puoi associare la prima fase e tutte le sue attività figlio alla riga di offerta per quella fase con un metodo di fatturazione a prezzo fisso. È quindi possibile associare tutte le altre fasi alla riga di offerta basata su tempistica e materiali.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Associare le attività alle righe di offerta basate sul progetto

È possibile associare attività a righe di offerta dalle seguenti posizioni:

- Pagina **Progetto** > scheda **Fatturazione attività** (ottimale)
- Pagina **Riga offerta** > scheda **Attività addebitabili** 

### <a name="from-the-project-page"></a>Dalla pagina Progetto

La pagina **Progetto** fornisce l'esperienza ottimale per associare attività a righe di offerta. È possibile utilizzare questa pagina per selezionare più attività e associarle tutte, con le relative attività figlio, alla riga di offerta selezionata.

1. Nella scheda **Generale** di una riga di offerta basata su progetto, controlla che il campo **Progetto** sia compilato.
2. Nel campo **Attività incluse**, seleziona **Solo le attività selezionate**.
3. Salva la riga dell'offerta basata su progetto. Quando il modulo viene aggiornato, viene visualizzata la scheda **Attività addebitabili**.
4. Nella scheda **Generale**, seleziona il collegamento per il progetto dal campo **Progetto**.
5. Nella pagina **Progetto**, seleziona la scheda **Fatturazione attività**.
6. Nella seconda griglia, che si applica all'impostazione della fatturazione specifica per attività, seleziona una o più attività, quindi seleziona **Associa righe di offerta**.
7. Nella finestra di dialogo che appare, seleziona una riga di offerta che visualizza le righe di offerta basate sul progetto nell'offerta.
8. Nel campo **Tipo di fatturazione**, indica se queste attività sono addebitabili o non addebitabili.
9. Seleziona la casella di controllo per indicare se l'associazione deve includere le attività figlio delle attività selezionate. La selezione della casella associa le attività figlio delle attività selezionate alla riga dell'offerta.
10. Selezionate **OK** per chiudere la finestra di dialogo.

### <a name="from-the-quote-line-page"></a>Dalla pagina Riga di offerta

È possibile associare attività di progetto a righe di offerta dalla scheda **Attività addebitabili** nella pagina **Riga di offerta**.

>[!NOTE]
>Il posto ottimale per associare le attività del progetto alle righe di offerta è nella scheda **Fatturazione attività** nella pagina **Progetto**. Se associ attività dalla scheda **Attività addebitabili** nella pagina **Riga di offerta**, devi associare manualmente ogni progetto.

1. Nella scheda **Generale** di una riga di offerta basata su progetto, controlla che vi sia un progetto selezionato nel campo **Progetto**.
2. Nel campo **Attività incluse**, seleziona **Solo le attività selezionate**.
3. Salva la riga dell'offerta basata su progetto. Quando il modulo viene aggiornato, viene visualizzata la scheda **Attività addebitabili**.
4. Nella scheda **Attività addebitabili**, seleziona **Aggiungi attività riga di offerta**.
5. Nella pagina **Attività riga offerta**, nel campo **Attività** seleziona l'attività e nel campo **Tipo di fatturazione** seleziona **Salva**. 
6. Chiudi la pagina. L'attività selezionata è ora associata alla riga di offerta.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Annullare l'associazione di attività alle righe di offerta basate sul progetto

### <a name="from-the-project-page"></a>Dalla pagina Progetto

Questo metodo fornisce l'esperienza ottimale per annullare l'associazione di attività a righe di offerta. Puoi selezionare più attività e annullare l'associazione di tutte, con le relative attività figlio, alla riga di offerta selezionata.

1. Nella scheda **Generale** di una riga di offerta basata su progetto, nel campo **Progetto** seleziona il collegamento per il progetto.
2. Nella pagina **Progetto**, seleziona la scheda **Fatturazione attività**.
3. Nella seconda griglia, che si applica all'impostazione della fatturazione specifica per attività, seleziona una o più attività, quindi seleziona **Annulla associazione righe di offerta**.
4. Nella finestra di dialogo che appare, seleziona una riga di offerta.
5. Seleziona la casella di controllo per indicare se l'associazione deve essere rimossa anche dalle attività figlio delle attività selezionate. La selezione della casella annulla l'associazione anche delle attività figlio delle attività selezionate alla riga dell'offerta.
6. Seleziona **OK**. Un messaggio di avviso informa che se si rimuove questa associazione eventuali valori effettivi registrati in precedenza sull'attività potrebbero essere annullati. 
7. Seleziona **OK** per continuare e rimuovere l'associazione tra l'attività e la riga dell'offerta basata sul progetto.

### <a name="from-the-quote-line-page"></a>Dalla pagina Riga di offerta

È possibile inoltre annullare l'associazione di attività di progetto a righe di offerta dalla scheda **Attività addebitabili** nella pagina **Riga di offerta**.

1. Nella scheda **Attività addebitabili**, seleziona **Elimina attività riga di offerta**.
2. Seleziona **OK**. Un messaggio di avviso informa che se si rimuove questa associazione eventuali valori effettivi registrati in precedenza sull'attività potrebbero essere annullati. 
3. Seleziona **OK** per continuare e rimuovere l'associazione tra l'attività e la riga dell'offerta basata sul progetto.

>[!NOTE]
> Questa procedura non elimina l'attività dal progetto. Rimuove solo l'associazione dell'attività alla riga dell'offerta basata sul progetto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]