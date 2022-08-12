---
title: Impostare i terzisti come risorse prenotabili
description: Questo articolo spiega come impostare e gestire le risorse del terzista create da utenti e contatti nel sistema, in modo che possano essere associate ai terzisti in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f005a05fb874f9e32a0041db5fc8fa1228fc91f1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927522"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Impostare i terzisti come risorse prenotabili

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Segui questi passaggi per configurare i terzisti come risorse prenotabili in Microsoft Dynamics 365 Project Operations.

1. Vai a **Progetto** \> **Risorse**, quindi seleziona **Nuovo**.
2. Nella pagina **Nuova risorsa prenotabile**, nel campo **Tipo di risorsa**, seleziona una delle opzioni seguenti:

    - **Utente** – Seleziona questo tipo di risorsa se il terzista deve accedere a Project Operations per inserire tempi o spese. Se selezioni **Utente**, il terzista richiede una licenza valida per accedere al sistema.
    - **Contatto** o **Account** – Seleziona uno di questi tipi di risorse se il terzista non richiede l'accesso a Project Operations, ma deve essere disponibile per le assegnazioni di attività o le prenotazioni sui progetti. Nessuno di questi tipi di risorse fornisce l'accesso al sistema. Seleziona **Account** per rappresentare l'azienda del fornitore come risorsa prenotabile. Seleziona **Contatto** per rappresentare i singoli dipendenti del fornitore.

3. A seconda del tipo di risorsa selezionato, ti verrà chiesto di selezionare l'utente, l'account o il record del contatto corrispondente.
4. Nel campo **Tipo di lavoratore**, seleziona "Lavoratore a contratto" per impostare il terzista come risorsa prenotabile.

    > [!NOTE]
    > Se lasci vuoto il campo **Tipo di lavoratore**, la risorsa prenotabile verrà considerata come un dipendente.

5. Se hai selezionato **Lavoratore a contratto** come tipo di lavoratore, seleziona il fornitore per cui lavora la risorsa.
6. Seleziona il fuso orario della risorsa, quindi seleziona **Salva**. Per assegnare un modello di orario di lavoro alla risorsa prenotabile, puoi selezionare **Imposta calendario** sulla pagina elenco **Risorsa prenotabile**.

Per essere associata a una riga del conto lavoro, una risorsa prenotabile deve soddisfare le seguenti condizioni:

- La risorsa prenotabile deve essere un lavoratore a contratto.
- Una risorsa prenotabile del tipo di risorsa **Contatto** deve essere associata al conto fornitore come referente. Una risorsa prenotabile del tipo di risorsa **Utente** non deve necessariamente essere associata al conto fornitore come referente.
- Il valore del campo **Fornitore** per la risorsa prenotabile deve corrispondere al valore del campo **Fornitore** per il conto di lavoro.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Aggiornare il tipo di mapping del lavoratore e del fornitore per le risorse prenotabili

Il campo **Tipo di lavoratore** per una risorsa prenotabile determina se la risorsa prenotabile è un lavoratore a contratto o un dipendente. Il campo **Fornitore** definisce il conto fornitore a cui è associata la risorsa prenotabile. Associando una risorsa prenotabile a un fornitore come contatto, si indica che il contatto è un dipendente della società del fornitore.

Se i campi **Tipo di lavoratore** e **Fornitore** per una risorsa prenotabile vengono modificati, le modifiche incidono sulle future convalide dei nuovi record creati dalla risorsa prenotabile, quali gli inserimenti di ore. Tuttavia, le modifiche non invalidano i record esistenti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]