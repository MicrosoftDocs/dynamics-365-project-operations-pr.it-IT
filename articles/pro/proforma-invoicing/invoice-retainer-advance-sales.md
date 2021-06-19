---
title: Fatturazione di un anticipo o di un acconto
description: Questo argomento fornisce informazioni su come fatturare un acconto o un anticipo in Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 238b55e906fb66415cf46d3abc8827d85c174dd7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003996"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Fatturare un pagamento anticipato o in acconto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations supporta contratti basati su acconto e anticipi una tantum. In un contratto di progetto, puoi registrare una pianificazione di acconti o di un anticipo una tantum. Tuttavia, la registrazione a livello di contratto di progetto non rende immediatamente disponibile per l'uso un acconto o un anticipo. Per utilizzare un acconto o un anticipo su una fattura che addebita effettivamente l'importo al cliente, devi prima fatturare l'acconto o l'acconto.

Completa questa procedura per fatturare un acconto o un anticipo.

1. Seleziona **Vendite** > **Fatturazione** > **Acconti e anticipi**. 
2. Nella pagina **Acconti e anticipi** utilizza il filtro per selezionare l'acconto o l'anticipo specifico da fatturare e contrassegnalo come **Pronto per la fatturazione**.
3. Crea una fattura manualmente dalla pagina elenco o dei dettagli **Contratto di progetto**. L'acconto o l'anticipo è indicato sulla bozza di fattura nella sezione **Anticipi e acconti** della pagina **Fattura**.
4. Conferma la fattura. Ciò renderà l'acconto o l'anticipo disponibile per l'uso. Puoi verificare la fattura nella pagina elenco **Acconti e anticipi**. Per un acconto o un anticipo fatturato, l'importo disponibile viene mostrato nella griglia.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Creare un acconto o un anticipo dalla griglia Fattura

Puoi creare un acconto o un anticipo direttamente in una fattura.

1. In una bozza di fattura, nella griglia secondaria **Anticipi e acconti** seleziona **Nuovo** per creare un nuovo acconto o anticipo. 
2. Nella pagina **Creazione rapida** aggiungi le informazioni necessarie e seleziona **Salva**. L'acconto o l'anticipo viene creato nel contratto di progetto relativo alla fattura. L'acconto o l'anticipo viene contrassegnato automaticamente come **Pronto per la fatturazione** e viene quindi aggiunto alla griglia secondaria **Acconti e anticipi** della pagina **Fattura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Riconciliare un anticipo o un acconto fatturato

Dopo che un acconto o un anticipo è stato fatturato, possono essere utilizzati o riconciliati in una fattura con tempi, spese, passaggi fondamentali o altri costi basati su progetto. Il cliente vedrà l'importo della fattura ridotto dell'importo in acconto o anticipo utilizzato su questa fattura.

Su ogni fattura generata per un contratto di progetto che ha fatturati acconti o anticipi, Project Operation applica automaticamente l'acconto o l'anticipo alla fattura.

Questo può essere visto nella griglia **Acconti e anticipi applicati** della pagina **Fattura**. La tabella seguente fornisce informazioni sui campi della griglia **Acconti e anticipi applicati** della pagina **Fattura progetto**.

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| Descrizione | Griglia **Acconti e anticipi applicati** della pagina **Fattura progetto** |Questo campo di sola lettura fornisce una descrizione dell'acconto o dell'anticipo utilizzato in questa fattura. Il valore non può essere modificato nella fattura. Questo valore può essere aggiornato nella griglia secondaria della pagina **Contratto di progetto**. | Questo campo può essere visualizzato al cliente sulla fattura stampata per indicare quale acconto o anticipo è stato applicato alla fattura. |
| Data consegna | Griglia **Acconti e anticipi applicati** della pagina **Fattura progetto**  | Questo campo di sola lettura fornisce la data della fattura dell'acconto o dell'anticipo utilizzato in questa fattura. Il valore non può essere modificato nella fattura. Questo valore può essere aggiornato nella griglia secondaria della pagina **Contratto di progetto**. | Questo campo può essere visualizzato al cliente sulla fattura stampata per indicare la data in cui l'acconto o l'anticipo è stato fatturato per la prima volta al cliente. |
| Importa | Griglia **Acconti e anticipi applicati** della pagina **Fattura progetto**  | Questo campo di sola lettura fornisce l'importo dell'acconto o dell'anticipo utilizzato in questa fattura. Il valore non può essere modificato nella fattura. Questo valore può essere aggiornato nella griglia secondaria della pagina **Contratto di progetto**. | Questo campo può essere visualizzato al cliente sulla fattura stampata per indicare l'importo originale dell'acconto o dell'anticipo che è stato pagato dal cliente. |
| Importo utilizzato | Griglia **Acconti e anticipi applicati** della pagina **Fattura progetto**  | Questo campo di sola lettura fornisce il valore calcolato che riepiloga l'importo di acconto o anticipo utilizzata. | Questo campo può essere visualizzato al cliente sulla fattura stampata per indicare l'importo dell'acconto o dell'anticipo che è stato già utilizzato. |
| Importo totale | Griglia **Acconti e anticipi applicati** della pagina **Fattura progetto**  | Questo campo modificabile fornisce l'importo dell'acconto o dell'anticipo utilizzato in questa fattura di progetto. Questo importo non può essere superiore a quanto disponibile per l'anticipo. Il sistema calcola automaticamente questo valore come differenza tra i campi **Importo** e **Importo utilizzato** della griglia. Puoi diminuire questo importo per utilizzare meno di quanto disponibile, ma non puoi aumentare l'importo per utilizzare più di quanto disponibile. | Questo campo può essere visualizzato al cliente sulla fattura stampata per indicare l'importo dell'acconto o dell'anticipo che viene utilizzato nella fattura. |
| Importo dell'acconto sul saldo. | Griglia **Acconti e anticipi applicati** della pagina **Fattura progetto**  | Questo campo di sola lettura fornisce il valore dell'importo di acconto o anticipo rimanente dopo la conferma della fattura. | Questo campo può essere visualizzato al cliente sulla fattura stampata per indicare l'importo residuo dell'acconto o dell'anticipo dopo che la fattura viene confermata e pagata. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]