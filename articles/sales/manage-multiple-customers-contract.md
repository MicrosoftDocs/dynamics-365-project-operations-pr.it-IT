---
title: Gestire più clienti nei contratti di progetto
description: Questo argomento fornisce informazioni sulla gestione di più clienti su un contratto di progetto.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1adb786c36d43a148e8c5a8b25ded5a997557119f7e6e9e2248935ad4ed211d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992076"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Gestire più clienti nei contratti di progetto

Questo argomento fornisce informazioni sulla gestione di più clienti su un contratto di progetto. È possibile utilizzare un contratto di progetto quando è necessario un accordo contrattuale per più clienti per finanziare un affare. Nella pagina **Contratto di progetto**, la scheda **Riepilogo** include informazioni sul cliente principale per un'offerta. Altri clienti che partecipano all'offerta possono essere aggiunti alla schea **Clienti**.

Tutti i clienti di contratto nella scheda **Clienti** del contratto di progetto vengono impostati come clienti delle voci di contratto basate sui progetti su qualsiasi nuova voce di contratto creata per il contratto di progetto. Le voci di contratto esistenti basate su progetto non ereditano i nuovi clienti di contratto quando vengono creati record in un secondo momento.

Puoi aggiungere, aggiornare o eliminare clienti delle voci di contratto e contratti in qualsiasi momento prima che il contratto venga acquisito. Un cliente nel contratto di progetto deve essere configurato come cliente nella società proprietaria o persona giuridica nella pagina **Clienti**. Le persone giuridiche sono costituite nel modulo **Contabilità e gestione di progetti** di Dynamics 365 Project Operations e sono disponibili come società nei moduli **Vendite di progetto** e **Consegna** di Project Operations.

## <a name="primary-customers"></a>Clienti primari

Il cliente potenziale nella scheda **Riepilogo** del contratto di progetto è il cliente primario del contratto. Il cliente primario non può essere aggiornato dall'elenco dei clienti di contratto. Se tenti di eliminare il cliente primario da un elenco dei clienti nel contratto, verrà visualizzato un messaggio di errore indicante che un record del cliente primario in un contratto non può essere eliminato. Modificare, invece, il cliente nel campo **Cliente potenziale** nella scheda **Riepilogo** del contratto di progetto. Quando aggiorni questo campo il cliente selezionato di recente viene aggiunto come nuovo cliente del contratto con il flag **Primario** impostato su **Sì**. Il cliente principale precedente è ancora un cliente del contratto, tuttavia non è più il cliente principale.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Creare, aggiornare o eliminare un record cliente di contratto

Puoi creare, aggiornare o eliminare un cliente di contratto dalla scheda **Clienti contratto** nella pagina **Contratto**. I seguenti campi sono inclusi nel record del cliente di contratto di un contratto di progetto.

| **Campo** | **Luogo** | **Descrizione** | 
| --- | --- | --- | 
| Conto | Griglia modificabile nella scheda **Clienti di contratto** e le pagine di creazione rapida e principale per un cliente di contratto. | Elenca tutti gli account attivi. Questo campo è bloccato dopo la creazione del record. Per aggiornare il record, devi eliminarlo e ricrearlo. Se sono stati registrati valori effettivi o se il record cliente di contratto è un cliente principale, non è possibile eliminare il record. Quando viene creata una voce di contratto, i clienti del contratto vengono copiati come clienti della voce di contratto. |
| Percentuale di separazione fatturazione | Griglia modificabile nella scheda **Clienti di contratto** e le pagine di creazione rapida e principale per un cliente di contratto. | Rappresenta la percentuale di ciascuna transazione di vendita non fatturata attribuita al cliente di contratto. Quando vengono create nuove righe di contratto di progetto, la percentuale di suddivisione della fatturazione viene copiata nelle nuove righe di contratto create e ai clienti delle righe di contratto di progetto. |
| Nome contatto fatturazione | Griglia modificabile nella scheda **Clienti di contratto** e le pagine di creazione rapida e principale per un cliente di contratto. | Questo campo di testo deve essere utilizzato per identificare la persona di contatto per la fatturazione del cliente. I valori predefiniti vengono impostati dal record del conto correlato. Il nome del contatto viene copiato in **Fattura a nome contratto** sulla fattura generata per il cliente. |
| Nome fatturazione | Griglia modificabile nella scheda **Clienti di contratto** e le pagine di creazione rapida e principale per un cliente di contratto. | Utilizzare questo campo per identificare la persona di contatto per la fatturazione per il cliente. I valori predefiniti vengono impostati dal record del conto correlato. Il nome viene copiato nel campo **Fattura a nome contratto** sulla fattura generata per il cliente. |
| Condizioni di pagamento | Griglia modificabile nella scheda **Clienti di contratto** e le pagine di creazione rapida e principale per un cliente di contratto. | I valori predefiniti vengono impostati dal record del conto correlato. I termini vengono copiati in **Fattura a nome contratto** sulla fattura generata per il cliente. |
| Società proprietaria | Griglia modificabile nella scheda **Clienti di contratto di progetto** e le pagine di creazione rapida e principale per un cliente di contratto di progetto. | La persona giuridica in cui il cliente è impostato nel modulo **Contabilità e gestione di progetto**. Questo campo è di sola lettura ed è impostato sulla società proprietaria del contratto di progetto.</br>L'elenco dei clienti da aggiungere nel campo **Conto** è già filtrato in base all'elenco dalla società proprietaria nel modulo **Gestione progetto e contabilità** di Project Operations. La società proprietaria è uguale alla persona giuridica nel modulo **Contabilità e gestione del progetto** di Project Operations. Tutti i costi e i ricavi derivanti da questo progetto sono contabilizzati nella contabilità generale della società proprietaria. |
| Arrotondamento | Griglia modificabile nella scheda **Clienti di contratto** e le pagine di creazione rapida e principale per un cliente di contratto. | Indica se il cliente è un cliente con costi di arrotondamento predefinito per l'offerta. Può esserci un solo cliente con arrotondamento su un contratto di progetto. Quando le suddivisioni dei costi e delle vendite non fatturate in base alla quantità determinano una differenza di arrotondamento, tale differenza viene applicata al valore effettivo associato al cliente. |
| Limite da non superare | Griglia modificabile nella scheda **Clienti di contratto** e le pagine di creazione rapida e principale per un cliente di contratto. | Indica se esiste un limite negoziato o un limite all'importo complessivo che verrà fatturato al cliente per l'impegno. La configurazione del limite da non superare a livello di cliente di contratto viene valutata in base ai valori effettivi delle vendite non fatturate che fanno riferimento al cliente di contratto. |

## <a name="edit-billing-split-percentages"></a>Modifica delle percentuali di separazione della fatturazione

Puio modificare le percentuali di suddivisione della fatturazione modificandole nella griglia. Quando le percentuali di suddivisione della fatturazione non raggiungono il 100 percento viene visualizzato un errore. Dopo aver modificato una percentuale di suddivisione della fatturazione, aggiorna la pagina **Contratto di progetto** per rimuovere l'errore.

Puoi anche selezionare **Distribuzione uniforme** sulla griglia secondaria dei clienti del contratto di progetto. Le suddivisioni di fatturazione vengono allocate uniformemente a tutti i clienti nel contratto di progetto. Se è presente un fattore di arrotondamento, il fattore verrà aggiunto al cliente con arrotondamento. Uno dei clienti di contratto ha sempre il flag **Arrotondamento** impostato su **Sì**. Quel cliente è il cliente con costi di arrotondamento. In genere, il cliente con costi di arrotondamento è anche il cliente principale del contratto, ma non è necessario.


[!INCLUDE[footer-include](../includes/footer-banner.md)]