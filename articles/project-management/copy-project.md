---
title: Copiare un progetto
description: In questo articolo vengono fornite informazioni sulla copia dei progetti in Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925769"
---
# <a name="copy-a-project"></a>Copiare un progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Con Dynamics 365 Project Operations, puoi creare rapidamente nuovi progetti selezionando **Copia progetto** nel modulo **Progetti**. Per copiare un progetto, apri il progetto che desideri copiare e quindi seleziona **Copia progetto**. L'azione copierà quanto segue:

- Proprietà del progetto 
- Struttura di suddivisione del lavoro
- Membri del team di progetto
- Stime di progetto
- Stime di spesa del progetto
- Stime dei materiali di progetto
- Elenchi di controllo del progetto
- Bucket di progetto

## <a name="project-properties"></a>Proprietà del progetto

Quando il progetto viene copiato, vengono copiati i valori nei seguenti campi.

| Campo | Project Operations per materiali non stoccati | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| Cliente | :heavy_check_mark: | :heavy_check_mark: | |
| Modello calendario | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Valuta | :heavy_check_mark: | :heavy_check_mark: | |
| Unità di contratto | :heavy_check_mark: | :heavy_check_mark: | |
| Società proprietaria | :heavy_check_mark: | | |
| Responsabile di progetto | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Stato di progetto generale | :heavy_check_mark: | :heavy_check_mark: | |
| Commenti | :heavy_check_mark: | :heavy_check_mark: | |
| Stime | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Data di inizio prevista</p><p><strong>Nota:</strong> Questo campo specifica la data in cui il progetto viene creato dalla copia. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Data di fine stimata</p><p><strong>Nota:</strong> La data in questo campo viene modificata in base alla data di inizio del nuovo progetto che è stato creato dalla copia.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Lavoro (ore) | :heavy_check_mark: | :heavy_check_mark: | |
| Costo manodopera stimato | :heavy_check_mark: | :heavy_check_mark: | |
| Costo spese stimato | :heavy_check_mark: | :heavy_check_mark: | |
| Costo materiale stimato | | :heavy_check_mark: | |

> [!NOTE]
> Il progetto di copia è un'operazione a esecuzione prolungata. Vengono copiati anche i record del progetto, i relativi attributi e molte entità correlate. A causa dell'esecuzione prolungata dell'operazione, dopo l'avvio della copia, la pagina del progetto di destinazione è bloccata per la modifica fino al completamento dell'operazione di copia.

## <a name="work-breakdown-structure"></a>Struttura di suddivisione del lavoro

Quando il progetto viene copiato, viene copiata l'intera struttura di suddivisione del lavoro caricata dalle risorse. Le risorse denominate vengono sostituite dalle risorse generiche. Se le risorse denominate non hanno le stesse ore lavorative della risorsa generica, la pianificazione verrà ricalcolata e le durate delle attività potrebbero cambiare.

## <a name="project-team-members"></a>Membri del team di progetto

Quando un team di progetto viene copiato dal progetto di origine, vengono copiate le risorse generiche. Anche le assegnazioni di risorse generiche vengono gestite come se fossero nel progetto di origine. Le risorse denominate verranno convertite in membri generici del team.

> [!NOTE]
> I membri del team e le assegnazioni non vengono copiati in Project for the Web.

## <a name="estimates"></a>Stime

Quando il progetto viene copiato, le righe di risorse, spese e stima dei materiali vengono copiate dal progetto di origine. 

Per informazioni su come accedere a livello di codice a Copia progetto, vedi [Sviluppare modelli di progetto con Copia progetto](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Offerte e contratti

Offerte e contratti non sono collegati al progetto di destinazione.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
