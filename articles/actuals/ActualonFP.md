---
title: Impatto dei valori effettivi in un impegno a prezzo fisso
description: Questo articolo fornisce informazioni sull'impatto sulla tabella Valori effettivi in vari eventi durante il ciclo di vita di un impegno di prezzo fisso in Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918133"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Impatto dei valori effettivi in un impegno a prezzo fisso

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

La tabella seguente elenca i valori effettivi di diversi tipi di transazione che vengono creati in vari eventi in un impegno di prezzo fisso.

| Evento | Valore effettivo costo | Valore effettivo vendite non fatturate | Valore effettivo vendite fatturate | Esempio |
|---|---|---|---|---|
| Le ore sono state create. | Non applicabile | Non applicabile | Non applicabile | <p>Bob Kozack, dell'unità organizzativa Fabrikam USA che ha un costo di 100 dollari USA (100 USD) all'ora, sta lavorando a un progetto chiamato "Arm Installation at Adatum". Questo progetto è mappato a un metodo di fatturazione a prezzo fisso nella riga del contratto. Ecco un inserimento ore di esempio di Bob Kozak:</p><p>Bob Kozack - 8 ore</p> |
| Le ore sono state inviate. | Non applicabile | Non applicabile | Non applicabile | Viene creata una riga del giornale di registrazione costi per l'inserimento ore. La tariffa di costo predefinita viene inserita nella scrittura contabile. |
| L'inserimento ore viene richiamato prima dell'approvazione. | Non applicabile | Non applicabile | Non applicabile | |
| Le ore sono approvate. | Viene creato un costo effettivo. | Non applicabile | Non applicabile | <p>Nuovo valore effettivo creato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800</li></ul> |
| L'approvazione delle ore è annullata. | <p>Lo stato di rettifica dei costi effettivi originali viene aggiornato su **Rettificato**.</p><p>Viene creato uno storno dei costi effettivi con stato di rettifica di **Non rettificabile**.</p> | Non applicabile | Non applicabile | <p>Valore effettivo esistente che viene aggiornato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800, *Rettificato*</li></ul><p>Nuovo valore effettivo creato per stornare l'impatto finanziario precedente:</p><ul><li>**Costo effettivo:** Bob Kozack, (8 ore), (USD 800), *Non rettificabile*</li></ul> |
| L'inserimento ore viene richiamato dopo l'approvazione. | <p>Lo stato di rettifica dei costi effettivi originali viene aggiornato su **Rettificato**.</p><p>Viene creato uno storno dei costi effettivi con stato di rettifica di **Non rettificabile**.</p> | Non applicabile | Non applicabile | <p>Valore effettivo esistente che viene aggiornato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800, *Rettificato*</li></ul><p>Nuovo valore effettivo creato per stornare l'impatto finanziario precedente:</p><ul><li>**Costo effettivo:** Bob Kozack, (8 ore), (USD 800), *Non rettificabile*</li></ul> |
| Il contratto è confermato. | <p>Lo stato di rettifica dei costi effettivi precedenti viene aggiornato su **Rettificato**.</p><p>Viene creato uno storno dei costi effettivi con stato di rettifica di **Non rettificabile**.</p><p>I nuovi costi effettivi vengono creati dopo la rivalutazione delle regole contrattuali.</p> | Non applicabile | Non applicabile | <p>Valore effettivo esistente che viene aggiornato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800, *Rettificato*</li></ul><p>Nuovo valore effettivo creato per stornare l'impatto finanziario precedente:</p><ul><li>**Costo effettivo:** Bob Kozack, (8 ore), (USD 800), *Non rettificabile*</li></ul><p>Nuovo valore effettivo creato per l'impatto finanziario rivalutato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800</li></ul> |
| Una fattura viene creata. | Non applicabile | Non applicabile | Non applicabile | |
| La fattura viene confermata con un passaggi fondamentale. | Non applicabile | Non applicabile | Vengono create nuove vendite effettive fatturate basate su passaggio fondamentale. | <p>Valore effettivo esistente che rimane invariato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, USD 800</li></ul><p>Nuovo valore effettivo creato per registrare i valori di vendita fatturati:</p><ul><li>**Vendite effettive fatturate:** Passaggio fondamentale, USD 5.000</li></ul> |
| La fattura viene corretta per accreditare il passaggio fondamentale. | Non applicabile | Non applicabile | Vengono create le vendite effettive fatturate di storno. | <p>Valore effettivo esistente che rimane invariato:</p><ul><li>**Costo effettivo:** Bob Kozack, 8 ore, 800 USD</li></ul><p>Valore effettivo esistente che viene aggiornato:</p><ul><li>**Vendite effettive fatturate:** Passaggio fondamentale, USD 5.000, *Rettificato*</li></ul><p>Nuovo valore effettivo creato per stornare i valori di vendita fatturati precedenti:</p><ul><li>**Vendite effettive fatturate:** Passaggio fondamentale, (USD 5.000), *Non rettificabile*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
