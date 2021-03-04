---
title: Spostamento nell'interfaccia utente
description: Questo argomento fornisce informazioni sulla gestione dei progetti in Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: deedfe0c6601fd09e09460034c9a0db936b6566e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127523"
---
# <a name="navigating-the-user-interface"></a>Spostamento nell'interfaccia utente

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

## <a name="overview"></a>Panoramica

Il modulo principale del progetto è suddiviso in diverse schede. Ciascuna scheda rappresenta un diverso livello di dettaglio all'interno del progetto.

- **Riepilogo**: fornisce una descrizione del progetto e aggrega le prestazioni del progetto pianificate ed effettive.

    ![Scheda Riepilogo e campi](media/navigation7.png)

- **Attività**: fornisce i dettagli relativi alla struttura di suddivisione del lavoro rappresentata da una vista griglia, una vista scheda e un diagramma di Gantt.

    ![Scheda Attività e campi](media/navigation8.png)

- **Team**: fornisce dettagli sui partecipanti al progetto. Anche il lavoro richiesto assegnato a ciascun membro del team è riepilogato in questa vista.

    ![Scheda Team e campi](media/navigation9.png)

- **Assegnazioni risorse**: fornisce una visualizzazione cronologica del lavoro richiesto per ciascuna risorsa in un progetto.

    ![Scheda Assegnazioni risorse e campi](media/navigation10.png)

- **Riconciliazione risorse**: fornisce una visualizzazione cronologica delle differenze tra le assegnazioni di ciascuna risorsa denominata e le relative prenotazioni.

    ![Scheda Riconciliazione risorse e campi](media/navigation11.png)

- **Stime**: fornisce una visualizzazione cronologica delle stime di vendita e costi di un progetto.

    ![Scheda Stime e campi](media/navigation12.png)

- **Registrazione**: fornisce una visualizzazione che mostra lo stato di avanzamento delle attività nella struttura di suddivisione del lavoro per lavoro richiesto, costo e vendite.

    ![Scheda Registrazione e campi](media/navigation13.png)

- **Vendite**: fornisce collegamenti diretti a offerte e contratti associati al progetto.

- **Stime di spesa**: fornisce una griglia che definisce le spese del progetto in base alle categorie di spesa dell'organizzazione.

    ![Scheda Stime di spesa e campi](media/navigation14.png)

## <a name="grid-controls"></a>Controlli della griglia

Di seguito è riportata una breve panoramica dei controlli tipici presenti nelle varie schede di pianificazione del progetto.

### <a name="refresh"></a>Refresh

**Aggiorna**: recupera i dati più recenti dal server se sono state apportate modifiche dopo il caricamento della griglia.

![Pulsante Aggiorna](media/navigation7.png)

### <a name="group-by"></a>Raggruppa per

**Raggruppa per**: aggiorna il raggruppamento delle righe nella griglia per riflettere risorse, ruoli o categorie in base alle esigenze dell'utente.

![Pulsante Raggruppa per](media/navigation6.png)

### <a name="previousnext"></a>Precedente/Successivo

**Precedente**/**Successivo**: aggiorna i periodi di tempo visibili sulle griglie temporali.

![Pulsanti Precedente e Successivo](media/navigation2.png)

### <a name="timescale"></a>Scala cronologica

**Scala cronologica**: modifica l'aggregazione dei dati cronologici tra giorni, settimane, mesi e anni.

![Pulsante Scala cronologica](media/navigation3.png)

### <a name="expand"></a>Espansione

**Espandi**: esegue il rendering della griglia visibile a schermo intero consentendo di vedere ruoli aggiuntivi.

![Pulsante Espandi](media/navigation4.png)

### <a name="time-phase-by"></a>Scala cronologica per

**Scala cronologica per**: aggiorna il raggruppamento delle righe nella griglia per riflettere le stime dei costi per le stime di vendita. Questo controllo si applica anche allo script di stima e alla griglia di registrazione.

![Pulsante Scala cronologica per](media/navigation0.png)

### <a name="add-column"></a>Aggiungi colonna

**Aggiungi colonna**: consente all'utente di definire le colonne visibili nella griglia. È possibile aggiungere solo colonne predefinite alle griglie nel modulo **Pianificazione progetto**.

![Pulsante Aggiungi colonna](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]