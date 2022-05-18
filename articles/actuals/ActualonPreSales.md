---
title: Impatto dei valori effettivi durante la fase di prevendita di un impegno
description: Questo argomento fornisce informazioni sull'impatto sulla tabella Valori effettivi in vari eventi mentre un impegno è nella fase di prevendita in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577241"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Impatto dei valori effettivi durante la fase di prevendita di un impegno

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

La tabella seguente elenca i valori effettivi di diversi tipi di transazione che vengono creati in vari eventi durante la fase di prevendita di un impegno di progetto.

| Evento | Valore effettivo costo | Esempio |
|---|---|---|
| Le ore sono state create. | Non applicabile | <p>Bob Kozack, dell'unità organizzativa Fabrikam USA che ha un costo di 100 dollari USA (100 USD) all'ora, sta lavorando a un progetto chiamato "Arm Installation at Adatum". Questo progetto è mappato a un metodo di fatturazione a prezzo fisso nella riga del contratto. Ecco un inserimento ore di esempio di Bob Kozak:</p><p>Bob Kozack - 8 ore</p> |
| Le ore sono state inviate. | Non applicabile | Viene creata una riga del giornale di registrazione costi per l'inserimento ore. La tariffa di costo predefinita viene inserita nella scrittura contabile. |
| L'inserimento ore viene richiamato prima dell'approvazione. | Non applicabile | |
| Le ore sono approvate. | Viene creato un costo effettivo. | <p>Nuovo valore effettivo creato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800</li></ul> |
| L'approvazione delle ore è annullata. | <p>Lo stato di rettifica dei costi effettivi originali viene aggiornato su **Rettificato**.</p><p>Viene creato uno storno dei costi effettivi con stato di rettifica di **Non rettificabile**.</p> | <p>Valore effettivo esistente che viene aggiornato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800, *Rettificato*</li></ul><p>Nuovo valore effettivo creato per stornare l'impatto finanziario precedente:</p><ul><li>**Costo effettivo:** Bob Kozack, (8 ore), (USD 800), *Non rettificabile*</li></ul> |
| L'inserimento ore viene richiamato dopo l'approvazione. | <p>Lo stato di rettifica dei costi effettivi originali viene aggiornato su **Rettificato**.</p><p>Viene creato uno storno dei costi effettivi con stato di rettifica di **Non rettificabile**.</p> | <p>Valore effettivo esistente che viene aggiornato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800, *Rettificato*</li></ul><p>Nuovo valore effettivo creato per stornare l'impatto finanziario precedente:</p><ul><li>**Costo effettivo:** Bob Kozack, (8 ore), (USD 800), *Non rettificabile*</li></ul> |
| L'offerta viene acquisita e viene creato un contratto. | <p>Lo stato di rettifica dei costi effettivi precedenti viene aggiornato su **Rettificato**.</p><p>Viene creato uno storno dei costi effettivi con stato di rettifica di **Non rettificabile**.</p><p>I nuovi costi effettivi vengono creati dopo la rivalutazione delle regole contrattuali.</p> | <p>Valore effettivo esistente che viene aggiornato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800, *Rettificato*</li></ul><p>Nuovo valore effettivo creato per stornare l'impatto finanziario precedente:</p><ul><li>**Costo effettivo:** Bob Kozack, (8 ore), (USD 800), *Non rettificabile*</li></ul><p>Nuovi valori effettivi che vengono creati per l'impatto finanziario rivalutato quando viene acquisita l'offerta e viene creato il contratto:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800</li><li>**Vendite effettive non fatturate:** Bob Kozack, 8 ore, USD 1.600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
