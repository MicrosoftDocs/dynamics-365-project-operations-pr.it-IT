---
title: Risorse riga conto lavoro
description: In questo articolo viene spiegato come specificare le risorse dedicate fornite dal fornitore per una riga di conto lavoro specifica per il tempo.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 84fbbd6e1a82db2b2d998b5f41579396df884ec3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924159"
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
4. Nella pagina **Nuova risorsa riga conto lavoro**, immetti le informazioni sulla spesa richieste, quindi seleziona **Salva e chiudi**.

La tabella seguente illustra i campi nella risorsa della voce di conto lavoro.

| Campo | Descrizione | Impatto funzionale |
| ----- | ----------- | ----------------- |
| Risorsa prenotabile | Seleziona una risorsa prenotabile di tipo **Lavoratore a contratto** che desideri utilizzare come risorsa nella voce del conto lavoro.| Se non hai creato una risorsa prenotabile per il lavoratore a contratto, lascia vuoto questo campo. Quando salvi il record, verrà creata una risorsa prenotabile.  |
| Contatto | È possibile creare la risorsa della riga di conto lavoro da un contatto esistente. Utilizza la ricerca per visualizzare l'elenco dei contatti attivi nel sistema. Seleziona un contatto per il fornitore di questo conto lavoro. Se il contatto selezionato non è un contatto valido per il fornitore in conto lavoro, il record di risorse della riga di conto lavoro non verrà salvato.| Se non sono presenti risorse prenotabili per il contatto selezionato, il sistema crea una risorsa prenotabile per il contatto selezionato prima di creare la risorsa della voce di conto lavoro. |
| Utente | Puoi creare una risorsa riga conto lavoro selezionando un utente attivo. Utilizza la ricerca per visualizzare l'elenco degli utenti attivi nel sistema.| Se non sono presenti risorse prenotabili per l'utente selezionato, il sistema crea una risorsa prenotabile per l'utente selezionato prima di creare la risorsa della voce di conto lavoro venga creata. |
| Data di inizio | La data di inizio dell'assegnazione del lavoratore in conto lavoro.| Se questa risorsa viene prenotata per un periodo che cade prima di questo intervallo di date, verrà visualizzato un avviso. |
| Data finali | La data di fine dell'assegnazione del lavoratore in conto lavoro.| Se questa risorsa viene prenotata per un periodo posteriore a questo intervallo di date, verrà visualizzato un avviso. |
| Lavoro | Il numero totale di ore di lavoro che il lavoratore a contratto trascorrerà su questa riga di subappalto.| Se questa risorsa viene prenotata oltre il lavoro allocato su questo subappalto, verrà visualizzato un avviso. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
