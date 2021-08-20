---
title: Mappare progetti e attività a una voce di contratto basata su progetto - semplice
description: Questo argomento fornisce informazioni sull'aggiunta e la rimozione di progetti e attività da una voce di contratto.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ce99e6f770c5eb39e5f2740a861721cf3d210ac9743bbd9d2a1e1a7236f368c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989736"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Mappare progetti e attività a una riga di offerta basata su progetto 

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma, Project Operations per scenari basati su risorse/materiali non stoccati_

Nelle voci di contratto basate su progetto, è possibile mappare attività specifiche in un progetto alla voce di contratto.

Quando mappi attività specifiche a una voce di contratto, il metodo di fatturazione, le opzioni di addebito, i limiti da non superare e i clienti definiti nella voce di contratto saranno applicabili solo a quelle attività specifiche.

Se hai uno scenario in cui una fase di un progetto, ad esempio la fase prototipo, è a prezzo fisso e tutte le altre fasi sono per tempo e materiale, potrai associare la fase prototipo e tutte le attività figlio associate alla voce di contratto per quella fase con un metodo di fatturazione a prezzo fisso.

Tutte le altre fasi nella struttura di suddivisione del lavoro del progetto possono essere associate alla voce di contratto basata su tempo e materiale.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Associare attività a voci di contratto basate su progetto

Le attività possono essere associate a voci di contratto dalla scheda **Attività addebitabili** nella pagina **Voce di contratto** o dalla scheda **Fatturazione attività** della pagina **Progetto**.

### <a name="from-the-contract-line-page"></a>Dalla pagina Voce di contratto

Completa i seguenti passaggi per associare le attività di progetto alla voce di contratto dalla scheda **Attività addebitabili** della pagina **Voce di contratto**.

1. Nella scheda **Generale** di una voce di contratto basata su progetto, verifica che il campo **Progetto** sia compilato.
2. Nel campo **Attività incluse** seleziona **Solo attività selezionate**.
3. Salva le modifiche. Il modulo viene aggiornato e la scheda **Attività addebitabili** diventa visibile.
4. Seleziona la scheda **Attività addebitabili** e nella griglia secondaria seleziona **Aggiungi un'attività voce di contratto**.
5. Nella pagina **Attività voce di contratto** nel menu a discesa **Attività** seleziona l'attività. 
6. Immetti le informazioni nel campo **Tipo di fatturazione** e seleziona **Salva e chiudi**. L'attività selezionata viene associata alla voce di contratto.

> [!NOTE]
> Questa non è l'esperienza ottimale per associare attività di progetto a voci di contratto. Ogni progetto dovrà essere associato manualmente in questa esperienza. Il modo preferito è dalla scheda **Fatturazione attività** della pagina **Progetto**.

### <a name="from-the-project-page"></a>Dalla pagina Progetto

Questo è il metodo ottimale per associare le attività alle voci di contratto. È possibile selezionare più attività e associarle tutte e le relative attività secondarie alla voce di contratto selezionata. Completa i seguenti passaggi per associare le attività alla voce di contratto dalla pagina **Progetto**.

1. Nella scheda **Generale** di una voce di contratto basata su progetto, verifica che il campo **Progetto** sia compilato.
2. Nel campo **Attività incluse** seleziona **Solo attività selezionate**.
3. Salva la voce di contratto basata su progetto. Il modulo viene aggiornato e la scheda **Attività addebitabili** diventa visibile. È solo a scopo di verifica.
4. Nella scheda **Generale** di una voce di contratto basata su progetto, nel campo **Progetto** seleziona il collegamento del progetto.
5. Nella pagina **Progetto** seleziona la scheda **Configurazione fatturazione attività**.
6. Sono disponibili due griglie. Una griglia è per le voci di contratto che si applicano all'intero progetto. La seconda griglia si applica alla configurazione della fatturazione specifica per l'attività. Nella seconda griglia, seleziona una o più attività, quindi seleziona **Associa voci di contratto**.
7. Nella pagina di dialogo che si apre, seleziona una voce di contratto dal menu a discesa.
8. Utilizza il menu a discesa **Tipo di fatturazione** per contrassegnare le attività come addebitabili o non addebitabili.
9. Seleziona la casella di controllo per indicare se l'associazione deve includere anche le attività figlio delle attività selezionate. Selezionando la casella si assoceranno anche le attività figlio delle attività selezionate alla voce di contratto.
10. Selezionate **OK** per chiudere la finestra di dialogo.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Annullare l'associazione di attività da voci di contratto basate su progetto

### <a name="from-the-contract-line-page"></a>Dalla pagina Voce di contratto

Completa i seguenti passaggi per annullare l'associazione delle attività di progetto dalla voce di contratto nella scheda **Attività addebitabili** della pagina **Voce di contratto**.

1. Nella scheda **Attività addebitabili** seleziona **Elimina un'attività voce di contratto**.
2. Un messaggio di avviso indica che la rimozione di questa associazione potrebbe comportare l'annullamento di tutti i valori effettivi precedentemente registrati nell'attività. Seleziona **OK** nella finestra di dialogo per rimuovere l'associazione tra l'attività e la voce di contratto basata su progetto. 

> [!NOTE]
> Ciò non elimina l'attività dal progetto. Rimuove solo l'associazione dell'attività dalla voce di contratto basata su progetto.

### <a name="from-the-project-page"></a>Dalla pagina Progetto

Questa è l'esperienza ottimale per annullare l'associazione di attività da voci di contratto. È possibile selezionare più attività e annullare l'associazione di tutte e delle relative attività secondarie dalla voce di contratto selezionata. Completa i seguenti passaggi per annullare l'associazione di attività dalla voce di contratto.

1. Nella scheda **Generale** di una voce di contratto basata su progetto, nel campo **Progetto** fai clic sul collegamento del progetto.
2. Nella pagina **Progetto** seleziona la scheda **Configurazione fatturazione attività**.
3. Ci sono due griglie nella pagina. Una griglia è per le voci di contratto che si applicano all'intero progetto e la seconda si applica all'impostazione della fatturazione specifica dell'attività. Nella seconda griglia, seleziona una o più attività, quindi seleziona **Annulla associazione voci di contratto**.
4. Nella pagina di dialogo che si apre, seleziona una voce di contratto dal menu a discesa.
5. Seleziona la casella di controllo per indicare se l'associazione deve essere rimossa anche dalle attività figlio delle attività selezionate. Selezionando la casella si annullerà l'associazione anche delle attività figlio delle attività selezionate dalla voce di contratto.
6. Seleziona **OK**. Un messaggio di avviso indica che la rimozione di questa associazione potrebbe comportare l'annullamento di tutti i valori effettivi precedentemente registrati nell'attività. Seleziona **OK** nella finestra di dialogo di avviso per rimuovere l'associazione tra l'attività e la voce di contratto basata su progetto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
