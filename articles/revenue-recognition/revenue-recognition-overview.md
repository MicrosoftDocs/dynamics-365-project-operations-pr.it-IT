---
title: Panoramica del riconoscimento ricavi
description: In questo argomento vengono fornite informazioni sul riconoscimento dei ricavi in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278873"
---
# <a name="revenue-recognition-overview"></a>Panoramica del riconoscimento ricavi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

In Dynamics 365 Project Operations, i principi di riconoscimento dei ricavi variano in base al metodo di fatturazione selezionato per un progetto o una parte del progetto. In questo argomento vengono fornite informazioni sul riconoscimento dei ricavi in Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transazioni contabilizzate utilizzando il metodo di fatturazione per tempo e materiali

- Il riconoscimento dei costi è collegato al riconoscimento dei ricavi. Il costo della transazione e le vendite non fatturate vengono registrati utilizzando l'estensione [Giornale di integrazione di Project Operations](../project-accounting/project-operations-integration-journal.md).
- Il profilo dei costi e dei ricavi del progetto determina se le transazioni di vendita non fatturate vengono registrate nella contabilità generale. Se l'opzione **Accumula ricavi** è selezionata, il sistema utilizza **Valore di vendita WIP** e i conti **Ricavi sospesi - Valore netto di vendita** durante la registrazione. Di seguito viene riportato un esempio di questo metodo.  

  | Tipo di transazione | Debito/Credito | Importa |
  | --- | --- | --- |
  | WIP - Valore netto di vendita | Dare | 100 |
  | Ricavi sospesi - Valore netto di vendita | Avere | 100 |

- I ricavi vengono riconosciuti durante la fatturazione. Il sistema utilizza il conto **Ricavi fatturati** durante la registrazione. Di seguito viene riportato un esempio di questo metodo.  

  | Tipo di transazione | Dare/Avere | Importa |
  | --- | --- | --- |
  | Saldo cliente | Dare | 120 |
  | IVA a debito | Avere | 20 |
  | Ricavi fatturati | Avere | 100 |

- Se i ricavi sono stati maturati quando vengono registrate le vendite non fatturate, il sistema stornerà i ricavi maturati al momento della fatturazione.

  | Tipo di transazione | Dare/Avere | Importa |
  | --- | --- | --- |
  | WIP - Valore netto di vendita | Avere | 100 |
  | Ricavi sospesi - Valore netto di vendita | Dare | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transazioni contabilizzate utilizzando il metodo di fatturazione a prezzo fisso

- Il riconoscimento dei costi e dei ricavi sono separati. Il costo della transazione viene registrato utilizzando l'estensione [Giornale di integrazione di Project Operations](../project-accounting/project-operations-integration-journal.md). Le transazioni di vendita non fatturate non vengono create.
- I ricavi possono essere riconosciuti durante la fatturazione se il costo del progetto e il profilo dei ricavi hanno **Principio utilizzato per i calcoli di completamento del progetto** impostato su **Nessuna WIP**. Utilizzare questo metodo solo per progetti semplici e a breve termine.
- I ricavi possono essere riconosciuti utilizzando le stime dei ricavi a prezzo fisso, sia con il metodo **Contratto completato** che **Percentuale di completamento del riconoscimento ricavi**.

## <a name="additional-resources"></a>Risorse aggiuntive
[Configurare la contabilità per l'articolo progetti fatturabili](../project-accounting/configure-accounting-billable-projects.md)

[Progetti di stima dei ricavi a prezzo fisso](rev-rec-percentage-completion-method.md)

[Gestire le stime dei ricavi](rev-rec-completed-contract-method.md)

[Metodi Costi di completamento](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]