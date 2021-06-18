---
title: Gestire i lead - semplice
description: In questo argomento vengono fornite informazioni sulla gestione dei lead basati su progetto (pro).
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 67480459478ffb8a157a2943af919dc63721b779
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994726"
---
# <a name="manage-leads---lite"></a>Gestire i lead - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

I lead basati su progetto possono essere gestiti e qualificati in Project Operations. Il processo di gestione dei lead include la creazione di lead basati sul lavoro e la qualificazione di tali lead. 

## <a name="list-of-project-sales-leads"></a>Elenco di lead di progetto

Nella sezione **Vendite**, nel riquadro di spostamento a sinistra, apri la pagina elenco **Lead** per visualizzare un elenco di tutti i record di lead nel sistema. I lead nell'elenco sono basati sul lavoro e altri tipi di lead che possono essere creati se si dispone anche di Dynamics 365 Sales o applicazioni di Dynamics 365 Field Service.

Puoi creare un visualizzazione filtrata per vedere solo i lead basati su progetto creando un filtro sul valore **Tipo**. Ad esempio, puoi scegliere di mostrare solo i lead basati sul lavoro.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Creazione di un nuovo lead per una transazione basata su progetto

Quando un lead basato sul progetto è qualificato, vengono creati un'opportunità e un account. Un'opportunità basata su progetto è il punto di partenza per le attività di incremento delle vendite nella fase Opportunità. Le opportunità basate su progetto hanno funzionalità esclusive che sono necessarie per il lavoro del progetto di vendita. Queste funzionalità includono:

- Metodi di fatturazione tempistica e materiali e a prezzo fisso
- Listini prezzi con più date di validità per risorse umane, spese e materiale necessario per i progetti.

Affinché un lead qualificato crei automaticamente un'opportunità, imposta l'attributo **Tipo** su **Basato sul lavoro** quando crei il lead. Se scegli un tipo diverso, il lead non creerà un'opportunità basata su progetto quando è qualificato. Se l'opportunità basata su progetto non viene creata, le funzionalità specifiche del progetto non saranno disponibili nei processi di vendita downstream.

La tabella seguente include importanti informazioni sul campo per un lead e le implicazioni downstream di tali campi.

| **Campo** | **Luogo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- | --- |
| Argomento | Scheda Generale | Questo campo di testo dovrebbe contenere una breve descrizione della transazione. | L'argomento del lead sarà predefinito come l'argomento dell'opportunità e il nome dell'offerta e il contratto di progetto. |
| Tipo | Scheda Generale | Questo campo di set di opzioni include le seguenti opzioni:</br>- Basato su lavoro (disponibile solo quando è installato Project Operations)</br>- Basato su articolo (disponibile solo quando sono installati Project Operations e Sales)</br>- Basato su manutenzione di servizio (disponibile quando è installato Field Service) | Quando il valore di questo campo è impostato su **Basato sul lavoro** sul lead, il lead è qualificato per creare un'opportunità basata sul progetto. È necessaria un'opportunità basata su progetto per abilitare tutte le estensioni e funzionalità specifiche del progetto nel processo di vendita downstream per questa transazione. |
| Nome | Scheda Generale | Nome del contatto del prospect | Quando il lead basato è qualificato, vengono creati un'opportunità, un contatto e un account. Il nome del contatto è il valore qui impostato. |
| Cognome | Scheda Generale | Cognome del contatto del prospect | Quando il lead basato è qualificato, vengono creati un'opportunità, un contatto e un account. Il cognome del contatto è il valore qui impostato. |
| Azienda | Scheda Generale | Nome dell'azienda del potenziale cliente | Quando il lead basato è qualificato, vengono creati un'opportunità, un contatto e un account. Il cognome dell'account creato è il valore qui impostato. |
| Valuta | Scheda Dettagli | Valuta del potenziale cliente | Quando il lead basato è qualificato, vengono creati un'opportunità, un contatto e un account. La valuta dell'account creato è il valore qui impostato. |

## <a name="qualify-a-new-project-based-lead"></a>Qualificare un nuovo lead basato su progetto

I lead che hanno il valore **Tipo** impostato su **Basato su lavoro** sono chiamati lead basati su progetto. Quando un lead basato su progetto viene qualificato, viene creato quanto segue:

- Un account che utilizza il campo **Azienda** dal lead.
- Un record del contatto associato all'account in base ai valori nei campi **Nome** e **Cognome** sul lead.
- Un'opportunità basata su progetto che ha il campo **Tipo** impostato su **Basato su lavoro**.

Per informazioni più dettagliate sulla qualificazione dei lead, vedi [Qualificare o convertire i lead](/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Processo aziendale per transazioni basate su progetti

I seguenti flussi di processi aziendali sono supportati per le transazioni basate su progetto in Project Operations:

- Processo aziendale da lead a opportunità
- Processo di vendita opportunità

Il processo aziendale dal lead a opportunità supporta le seguenti fasi:

| Nome fase | Entità mappata | Funzionalità |
| --- | --- | --- |
| Impostazione come qualificato | Lead | Qualifica il lead e crea un account, contatto e/o opportunità. |
| Sviluppa | Opportunità | Sviluppa l'opportunità per aggiungere altre informazioni sul lavoro, sulle parti interessate chiave e sulla concorrenza coinvolti. |
| Proponi | Opportunità | Sviluppa la proposta e ottieni l'approvazione dal team di revisione interno. |
| Chiuso | Opportunità | Acquisisci l'opportunità per chiudere la transazione. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]