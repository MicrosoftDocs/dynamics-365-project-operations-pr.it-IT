---
title: Utilizzare le voce di contratto basate su progetto
description: Questo argomento fornisce informazioni sulle voci di contratto basate su progetto.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2b856e280ac56c1cedd7d4966aca7e7f234bc520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278108"
---
# <a name="work-with-projectbased-contract-lines"></a>Utilizzare le voce di contratto basate su progetto

Le voci di contratto basate su progetto in Dynamics 365 Project Operations sono progettate per contenere i contratti di stima e fatturazione per componenti specifici del lavoro di progetto su un impegno. La struttura di una voce di contratto basata su progetto viene estesa per le stime di progetto e gli scenari di fatturazione con i seguenti concetti:

- Metodo di fatturazione
- Mapping di progetti e attività
- Classi di transazione incluse
- Limite da non superare
- Impostazione dell'esigibilità
- Stime utilizzando i dettagli della voce di contratto
- Clienti voce di contratto

I seguenti campi sono inclusi nella scheda **Generale** delle voci di contratto basate su progetto. Questi campi aiutano a creare le basi per una stima dettagliata e iniziale e le modalità di fatturazione per il lavoro basato su progetto.

| Campo | Descrizione | Impatto downstream |
| --- | --- | --- |
| **Nome** | Il nome della voce di contratto che identifica il componente discreto del contratto che si sta stimando. Per un contratto di progetto creato da un'offerta, questo valore viene copiato da un valore corrispondente della riga di offerta basata su progetto. | Questo valore di campo viene copiato nella riga di fattura di progetto creata da questa voce di contratto quando viene creata la fattura. |
| **Metodo di fatturazione** | In un contratto di progetto creato da un'offerta, questo valore viene copiato dal campo corrispondente della riga di offerta. Questo è un set di opzioni che rappresenta i due principali modelli di contratto supportati da Project Operations:</br>- **Prezzo fisso**</br>- **Tempistica e materiali** | In base al metodo di fatturazione della voce di contratto a cui si fa riferimento, verrà elaborata la transazione effettiva. Se la voce di contratto a cui fa riferimento il valore effettivo dispone di un metodo di fatturazione di tempo e materiale, viene creato un record dei costi e delle vendite non fatturate. Se la voce di contratto a cui fa riferimento il valore effettivo ha un metodo di fatturazione a prezzo fisso, viene creato solo un costo effettivo. |
| **Project** | Utilizza questo campo per identificare il progetto che verrà utilizzato per fornire il lavoro su questo impegno. | Il valore in questo campo viene utilizzato insieme ai campi **Attività incluse** e **Classi di transazione incluse** per risolvere il riferimento della voce di contratto in un record di riga effettivo o di stima. |
| **Includi tempo** | Un contrassegno indica se le transazioni di tempo o i costi di manodopera sul progetto selezionato vengono inclusi in questa voce di contratto. Il valore **No** indica che le transazioni di tempo o i costi di manodopera non verranno inclusi in questa voce di contratto. Il valore **Sì** indica che verranno inclusi. | Il valore del campo viene utilizzato insieme progetto per risolvere il riferimento della voce di contratto in un record di riga effettivo o di stima. |
| **Includi spesa** | Un contrassegno indica se i costi di spesa sul progetto selezionato verranno inclusi in questa voce di contratto. Il valore **No** indica che i costi di spesa non verranno inclusi in questa voce di contratto. Il valore **Sì** indica che verranno inclusi. | Il valore del campo viene utilizzato insieme progetto per risolvere il riferimento della voce di contratto in un record di riga effettivo o di stima. |
| **Includi commissione** | Un contrassegno indica se le commissioni sul progetto selezionato verranno incluse in questa voce di contratto. Il valore **No** indica che le commissioni non verranno incluse in questa voce di contratto. Il valore **Sì** indica che verranno inclusi. | Il valore del campo viene utilizzato insieme progetto per risolvere il riferimento della voce di contratto in un record di riga effettivo o di stima. |
| **Importo contratto** | In una voce di contratto a prezzo fisso, questo è il valore concordato che verrà fatturato al cliente per tutti i componenti di lavoro associati a questa voce di contratto. In una voce di contratto tempo e materiale, questo importo è il valore stimato che verrà fatturato al cliente per tutti i componenti di lavoro associati a questa voce di contratto. In un contratto di progetto creato da un'offerta, questo valore viene copiato dal campo corrispondente della riga di offerta. Quando una voce di contratto basata su progetto include dettagli di riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo nei dettagli della voce di contratto. | Quando la voce di contratto include i dettagli della riga, questo valore può essere modificato modificando gli importi dei dettagli della riga. In una voce di contratto a prezzo fisso, questo valore viene utilizzato per generare l'importo prima delle imposte sui passaggi fondamentali di fatturazione periodica. |
| **Imposta stimata** | L'utente può modificare questo campo per inserire l'importo delle imposte stimato nella voce di contratto. Quando una voce di contratto basata su progetto include dettagli di riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo delle imposte nei dettagli della voce di contratto. | Quando la voce di contratto include i dettagli della riga, questo valore può essere modificato modificando gli importi delle imposte dei dettagli della riga. In una voce di contratto a prezzo fisso, questo valore viene utilizzato per generare le imposte sui passaggi fondamentali di fatturazione periodica. |
| **Importo contratto al netto delle imposte** | L'importo della voce di contratto al netto delle imposte. Questo campo è di sola lettura e viene calcolato come **importo di contratto + imposte**. | In una voce di contratto a prezzo fisso, questo valore viene utilizzato per generare i passaggi fondamentali di fatturazione periodica. |
| **Limite da non superare** | L'utente può modificare questo campo ed è disponibile solo sulle voci di contratto basate su progetto che hanno un metodo di fatturazione per tempo e materiale. | L'utente può modificare questo campo. Quando un valore effettivo di tempo o spesa fa riferimento a questa voce di contratto per tempo e materiale, l'importo del valore effettivo viene valutato rispetto al limite da non superare della voce di contratto dopo la contabilizzazione per gli importi già spesi e confermati. |
| **Budget cliente** | Questo campo è modificabile e viene viene copiato dal campo corrispondente della riga di offerta se il contratto è stato creato da un'offerta. | Questo campo è utilizzato solo per informazioni e non ha alcun significato downstream. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regola di convalida per le opzioni nella scheda Generale delle voci di contratto basate su progetto

Regola: un progetto e una determinata classe di transazione possono essere inclusi solo in una voce di contratto basata su progetto in un contratto.

| Contratto | Voce di contratto | Project | Includi tempistica | Includi spesa | Includi commissione | Valido/Non valido | Motivo                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Sì          | Sì             | Sì         | Non valido       | Viola la regola. Il tempo, le spese e le commissioni sul progetto P1 sono inclusi in entrambe le voci di contratto, CL1 e CL2.                                                                                       |
| C1       | CL2           | P1      | Sì          | Sì             | Sì         | Non valido       | Viola la regola. Il tempo, le spese e le commissioni sul progetto P1 sono inclusi in entrambe le voci di contratto, CL1 e CL2.                                                                                       |
| C1       | CL1           | P1      | Sì          | No              | Sì         | Non valido       | Viola la regola. Il tempo e le commissioni sul progetto P1 sono inclusi in entrambe le voci di contratto, CL1 e CL2.                                                                                                   |
| C1       | CL2           | P1      | Sì          | Sì             | Sì         | Non valido       | Viola la regola. Il tempo e le commissioni sul progetto P1 sono inclusi in entrambe le voci di contratto, CL1 e CL2.                                                                                                   |
| C1       | CL1           | P1      | Sì          | No              | Sì         | Valido           | I tempi e le commissioni del progetto P1 sono inclusi in CL1. La spesa sul progetto P1 è inclusa in CL2. </br>   Non c'è sovrapposizione in ciò che viene incluso in ogni voce di contratto ed è quindi valido.  |
| C1       | CL2           | P1      | No           | Sì             | No          | Valido           | I tempi e le commissioni del progetto P1 sono inclusi in CL1. La spesa sul progetto P1 è inclusa in CL2. </br>   Non c'è sovrapposizione in ciò che viene incluso in ogni voce di contratto ed è quindi valido.  |
| C1       | CL1           | P1      | Sì          | Sì             | Sì         | Non valido       | Viola la regola. Il tempo, le spese e le commissioni sul progetto P1 sono inclusi nelle voci dei due contratti.                                                                                               |
| CL2      | CL2           | P1      | Sì          | Sì             | Sì         | Non valido       | Viola la regola. Il tempo, le spese e le commissioni sul progetto P1 sono inclusi nelle voci dei due contratti.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]