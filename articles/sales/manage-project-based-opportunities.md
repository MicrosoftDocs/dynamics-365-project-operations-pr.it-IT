---
title: Gestire opportunità basate su progetto
description: Questo argomento fornisce informazioni su come utilizzare le opportunità correlate ai progetti.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f39940ac063a8c202f33797ed649518907563e31
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600425"
---
# <a name="manage-project-based-opportunities"></a>Gestire opportunità basate su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le società basate su progetti in genere includono operazioni per la consegna distribuite in più paesi e aree geografiche. Il costo dell'esecuzione e della consegna del progetto può variare in base all'area geografica o alla divisione che gestisce la consegna. A sua volta, questo può influire sui margini della transazione. La consegna di servizi basati su progetti comporta in genere grandi quantità di tempo in termini di risorse umane, spese considerevoli per viaggi, costi dei materiali e altre spese.

Le opportunità basate su progetto in Dynamics 365 Project Operations sono progettate con estensioni a Dynamics 365 Sales. Questo argomento fornisce i dettagli sui diversi campi e sulla logica di business inclusi nella funzionalità aggiuntiva richiesta dalle società basate su progetti per gestire le opportunità basate su progetti.

## <a name="view-all-project-based-opportunities"></a>Visualizzare tutte le opportunità basate su progetto

Un elenco di tutte le opportunità basate su progetto può essere visualizzato dalla pagina elenco **Opportunità**. 

1. Vai a **Vendite** > **Opportunità**.
2. Usa **Cambia vista** per selezionare altre visualizzazioni filtrate delle opportunità. Puoi creare visualizzazioni personalizzate con criteri di filtro personalizzati per configurare queste visualizzazioni e le opzioni di spostamento.

Le opportunità di progetto possono essere create o eliminate da questa pagina elenco o dalla pagina dei dettagli.

## <a name="business-process-flow-for-project-based-deals"></a>Processo aziendale per transazioni basate su progetti

I seguenti flussi di processi aziendali sono supportati per le transazioni basate su progetto in Project Operations:

- Processo aziendale da lead a opportunità
- Processo di vendita opportunità

### <a name="lead-to-opportunity-business-process"></a>Processo aziendale da lead a opportunità 
Il processo aziendale dal lead a opportunità supporta le seguenti fasi:

| Fase | Entità mappata | Funzionalità |
| --- | --- | --- |
| Impostazione come qualificato | Lead | Qualifica il lead e crea un account, contatto e/o opportunità. |
| Sviluppa | Opportunità | Sviluppa l'opportunità per aggiungere altre informazioni sul lavoro, sulle parti interessate chiave e sulla concorrenza coinvolti. |
| Proponi | Opportunità | Sviluppa la proposta e ottieni l'approvazione dal team di revisione interno. |
| Chiuso | Opportunità | Acquisisci l'opportunità per chiudere la transazione. |

### <a name="opportunity-sales-process"></a>Processo di vendita opportunità
Il processo di vendita opportunità in Project Operations è un'estensione del flusso aziendale del processo di vendita opportunità dell'applicazione Sales. Questo processo aziendale è progettato per supportare per impostazione predefinita le fasi seguenti in un'opportunità basata su progetto.

| Fase | Entità mappata | Funzionalità |
| --- | --- | --- |
| Impostazione come qualificato | Opportunità | Qualifica il lead e crea un account, contatto e/o opportunità. |
| Proponi | Offerta | Sviluppa la proposta usando le offerte di progetto e ottieni l'approvazione dal team di revisione interno. |
| Contratto | Contratto di progetto | Acquisisci l'offerta per creare il contratto e inizia l'esecuzione e la consegna del progetto. |
| Chiuso | Contratto di progetto | Termina il lavoro e chiudi il contratto di progetto. |

> [!NOTE]
> Se il contratto basato su progetto è iniziato con un lead, il processo aziendale da lead a opportunità ha la precedenza.
>
> Se il contratto basato su progetto è iniziato con un'opportunità, il processo di vendita opportunità ha la precedenza.

Puoi modificare il flusso di processo aziendale del prodotto o creare i tuoi flussi di processi aziendali per monitorare il processo di vendita secondo necessità. Per ulteriori informazioni sul flusso di processi aziendali, vedi [Panoramica dei processi aziendali](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]