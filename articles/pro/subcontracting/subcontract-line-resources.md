---
title: Risorse riga conto lavoro
description: Questo argomento spiega come specificare le risorse dedicate fornite dal fornitore per una specifica riga di conto lavoro per orario.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323376"
---
# <a name="subcontract-line-resources"></a>Risorse riga conto lavoro

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

In Dynamics 365 Project Operations, un fornitore può specificare le risorse che verranno utilizzate per fornire la capacità della risorsa acquistata nella voce di conto lavoro per orario.

## <a name="create-subcontract-line-resources"></a>Creare risorse voce di conto lavoro

Per creare risorse di voci di conto lavoro, completa la seguente procedura.

1. Nel riquadro di spostamento, seleziona **Conti lavoro** e apri il conto lavoro con cui desideri lavorare.
2. Apri la voce del contratto di conto lavoro per l'ora in cui si desidera specificare le risorse del fornitore.
3. Nella scheda **Risorse riga conto lavoro**, nella sottogriglia, seleziona **+ Nuova risorsa riga conto lavoro**.
4. Nella pagina **Nuovo passaggio fondamentale della voce di conto lavoro**, inserisci le informazioni quindi seleziona **Salva e chiudi**.

La tabella seguente illustra i campi nella risorsa della voce di conto lavoro.

| Campo |  Descrizione |
| ----- | ------------ |
| Risorsa prenotabile | Seleziona una risorsa prenotabile di tipo "Lavoratore a contratto" che si desidera utilizzare come risorsa nella voce del conto lavoro. Se non hai ancora creato una risorsa prenotabile per il lavoratore a contratto, lascia vuoto questo campo. Una risorsa prenotabile viene creata quando si salva il record.  |
| Contatto | Se il campo **Risorsa prenotabile** è vuoto, puoi creare la risorsa della voce di conto lavoro da un contatto esistente. Utilizza la ricerca per visualizzare l'elenco dei contatti attivi nel sistema. Seleziona un contatto per il fornitore di questo conto lavoro. Il contatto selezionato viene convalidato quando si salva il record. Se il contatto che hai selezionato non è un contatto valido, il tuo record non verrà salvato. Se non sono presenti risorse prenotabili per il contatto selezionato, il sistema crea una risorsa prenotabile per il contatto selezionato prima di creare la risorsa della voce di conto lavoro. |
| Utente | Se il campo **Risorsa prenotabile** è vuoto, puoi creare una risorsa della voce di conto lavoro selezionando un utente attivo. Utilizza la ricerca per visualizzare l'elenco degli utenti attivi nel sistema. Se non sono presenti risorse prenotabili per l'utente selezionato, il sistema crea una risorsa prenotabile per l'utente selezionato prima di creare la risorsa della voce di conto lavoro venga creata. |
| Data di inizio | La data di inizio dell'assegnazione del lavoratore in conto lavoro. Se questa risorsa viene prenotata per un periodo che cade prima di questo intervallo di date, verrà visualizzato un avviso. |
| Data finali | La data di fine dell'assegnazione del lavoratore in conto lavoro. Se questa risorsa viene prenotata per un periodo posteriore a questo intervallo di date, verrà visualizzato un avviso. |
| Lavoro | Il numero totale di ore di lavoro che il lavoratore in conto lavoro trascorrerà su questa voce di conto lavoro. Se questa risorsa viene prenotata oltre lo sforzo a cui è assegnata in questo conto lavoro, verrà visualizzato un avviso. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
