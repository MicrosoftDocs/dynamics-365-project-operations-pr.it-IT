---
title: Panoramica sulla ritenuta ai fornitori
description: Questo argomento fornisce una panoramica delle capacità di ritenuta ai fornitori.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f9e4a1e63e47524bb622771f645c04e61c279496
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588465"
---
# <a name="vendor-retention-overview"></a>Panoramica sulla ritenuta ai fornitori

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

La tua organizzazione potrebbe voler trattenere una parte dei pagamenti ai fornitori che lavorano su progetti per la tua organizzazione. Ad esempio, prima di pagare il fornitore, potresti volerti assicurare che gli articoli e i servizi forniti soddisfino le tue aspettative.

Quando si negoziano gli acquisti per i progetti con i fornitori, puoi specificare i termini della ritenuta ai fornitori che includono la percentuale o l'importo da trattenere. Quando il fornitore consegna articoli e servizi, deduci la percentuale o l'importo di ritenuta specificato dal tuo pagamento al fornitore. Quando il progetto è completo o raggiunge una fase intermedia come specificato nel contratto del fornitore, rilasci l'importo trattenuto e crei un pagamento al fornitore.

## <a name="vendor-retention-example"></a>Esempio di ritenuta ai fornitori

L'esempio seguente mostra come viene conservata una percentuale dell'importo di una fattura fornitore in base alla percentuale di completamento per un progetto.

Contoso Robotics USA ha stipulato un contratto con il fornitore Fabrikam per la fornitura di 100 ore di formazione per il progetto di rinnovo delle apparecchiature. Il valore totale del contratto è di 30.000 USD con un prezzo di acquisto concordato di 300 USD all'ora.

La formazione sarà erogata in tre fasi con il seguente calendario:

- Fase 1: 50 ore o il 50 percento del progetto
- Fase 2: 30 ore o l'80 percento del progetto in totale
- Fase 3: 20 ore o il 100 percento del progetto

Nella tabella seguente sono elencati i termini della trattenuta.

| **Percentuale di unità consegnate** | **Percentuale da trattenere** | **Percentuale da rilasciare** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

Dalle transazioni risultano i seguenti importi:

- Fase 1:
  - L'importo da pagare è 50 x 300 ovvero 15.000.
  - Il 20% dell'importo oppure 3.000, viene trattenuto e verrà rilasciato in una fase successiva.
  - L'importo che viene pagato al venditore è 12.000.
- Fase 2:
  - L'importo da pagare è 30 x 300 ovvero 9.000.
  - Il 10 percento dell'importo oppure 900, viene trattenuto.
  - Il 10 percento dei 3.000 che sono stati trattenuti nella Fase 1 oppure 300, viene rilasciato.
  - L'importo che viene pagato al venditore è 8.400. Questo importo è di 9.000 meno la trattenuta 900 più 300 che sono stati rilasciati dalla trattenuta della Fase 1.
- Fase 3:
  - L'importo da pagare è 20 x 300 ovvero 6.000.
  - Nessun importo viene trattenuto.
  - L'importo che viene rilasciato è 3.600. Questo importo è costituito dai 3.000 che sono stati trattenuti nella Fase 1, meno i 300 della Fase 1 che sono stati rilasciati nella Fase 2, più i 900 che sono stati trattenuti nella Fase 2.
  - L'importo che viene pagato al venditore è 9.600. Tale importo è costituito dall'importo trattenuto di 3.600 più i 6.000 per il completamento della Fase 3.

L'importo totale pagato al venditore dopo che le tre fasi sono state completate è 30.000, che è l'importo totale dell'ordine di acquisto (15.000 + 9.000 + 6.000).
