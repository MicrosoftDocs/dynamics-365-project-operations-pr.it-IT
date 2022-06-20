---
title: Impatto dei valori effettivi per un progetto interno
description: Questo articolo fornisce informazioni sull'impatto sulla tabella Valori effettivi in vari eventi per un progetto interno in Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921353"
---
# <a name="actuals-impact-for-an-internal-project"></a>Impatto dei valori effettivi per un progetto interno

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

La tabella seguente elenca i valori effettivi di diversi tipi di transazione che vengono creati in vari eventi in un impegno di progetto interno.

| Evento | Valore effettivo costo | Esempio |
|---|---|---|
| Le ore sono state create. | Non applicabile | <p>Bob Kozack, dell'unità organizzativa Fabrikam USA che ha un costo di 100 dollari USA (100 USD) all'ora, sta lavorando a un progetto chiamato "Arm Installation at Adatum". Questo progetto è mappato a un metodo di fatturazione a prezzo fisso nella riga del contratto. Ecco un inserimento ore di esempio di Bob Kozak:</p><p>Bob Kozack - 8 ore</p> |
| Le ore sono state inviate. | Non applicabile | Viene creata una riga del giornale di registrazione costi per l'inserimento ore. La tariffa di costo predefinita viene inserita nella scrittura contabile. |
| L'inserimento ore viene richiamato prima dell'approvazione. | Non applicabile | |
| Le ore sono approvate. | Viene creato un costo effettivo. | <p>Nuovo valore effettivo creato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800</li></ul> |
| L'approvazione delle ore è annullata. | <p>Lo stato di rettifica dei costi effettivi originali viene aggiornato su **Rettificato**.</p><p>Viene creato uno storno dei costi effettivi con stato di rettifica di **Non rettificabile**.</p> | <p>Valore effettivo esistente che viene aggiornato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800, *Rettificato*</li></ul><p>Nuovo valore effettivo creato per stornare l'impatto finanziario precedente:</p><ul><li>**Costo effettivo:** Bob Kozack, (8 ore), (USD 800), *Non rettificabile*</li></ul> |
| L'inserimento ore viene richiamato dopo l'approvazione. | <p>Lo stato di rettifica dei costi effettivi originali viene aggiornato su **Rettificato**.</p><p>Viene creato uno storno dei costi effettivi con stato di rettifica di **Non rettificabile**.</p> | <p>Valore effettivo esistente che viene aggiornato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800, *Rettificato*</li></ul><p>Nuovo valore effettivo creato per stornare l'impatto finanziario precedente:</p><ul><li>**Costo effettivo:** Bob Kozack, (8 ore), (USD 800), *Non rettificabile*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
