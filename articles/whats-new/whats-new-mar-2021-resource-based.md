---
title: Novità di marzo 2021 - Project Operations per scenari basati su risorse/non stoccate
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di marzo 2021 di Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 95a9251707de3699322471535aa93070ba4fb2ae
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500013"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di marzo 2021 - Project Operations per scenari basati su risorse/non stoccate

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.8.0.91 
- Gestione progetti e contabilità in ambiente Dynamics 365 Finance versione 10.0.16 

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse


| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Determinazione dei prezzi e fatturazione | 2133873 | Risolto il problema della visualizzazione del simbolo di valuta **Prezzo di vendita unitario** nella griglia **Stime di spesa**. |
| Determinazione dei prezzi e fatturazione | 2174616 | Quando si chiude un'offerta, il listino prezzi personalizzato del contratto viene implementato nei dettagli della riga del contratto che vengono copiati dall'offerta. |
| Gestione delle opportunità | 2167475 | Importo fisso dell'imposta nella fattura di rettifica che ha originato un movimento effettivo non fatturato. |
| Gestione delle opportunità | 2176285 | L'importo dell'imposta non deve essere copiato dai dettagli della riga di offerta/contratto di vendita nei dettagli della riga di offerta/contratto di costo. |
| Gestione delle opportunità | 2188079 | La regola di fatturazione suddivisa non deve essere creata per i contratti che non sono basati su lavoro. |
| Pianificazione e rilevamento | 2125274 | L'attributo **Mappa doppia scrittura di progetto** per **Mapping data di inizio di progetto** è stato aggiornato da **msdyn\_taskearlieststart** a **msdyn\_actualstart**. |
| Pianificazione e rilevamento | 2138853 | Funzione di copia del progetto aggiornata per garantire che le righe di stima delle spese che fanno riferimento alle attività vengano copiate nel progetto di destinazione. |
| Pianificazione e rilevamento | 2154306 | Risolti i problemi con l'eliminazione delle stime di spesa in Project Operations per scenari basati su risorsa. |
| Pianificazione e rilevamento | 2173259 | Funzione di copia del progetto aggiornata per garantire che non visualizzi il messaggio di errore **Copia di WBS** in determinati scenari. |
| Ore e spesa | 2148910 | Risolto il problema di visualizzazione con la pagina **Modifica inserimento** nella griglia **Inserimento ore**. |
| Ore e spesa | 2159798 | Controlli rafforzati per garantire che le voci di spesa approvate non possano essere modificate. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Contabilità e gestione dei progetti in Dynamics 365 Finance

Per ulteriori informazioni vedi [Novità di gennaio 2021 - Project Operations per scenari basati su risorse/non stoccate](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Aggiornamenti normativi

Per informazioni sugli aggiornamenti normativi per le app Finance and Operations, vedi [Aggiornamenti normativi](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Un altro modo per conoscere gli aggiornamenti normativi è accedere a LCS e visualizzare gli aggiornamenti normativi pianificati utilizzando lo strumento di ricerca dei problemi. La ricerca dei problemi ti consente di cercare per paese, tipo di funzionalità e versione.


[!INCLUDE[footer-include](../includes/footer-banner.md)]