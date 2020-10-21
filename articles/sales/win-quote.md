---
title: Chiudere un'offerta
description: Questo argomento fornisce informazioni sulla chiusura delle offerte in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898896"
---
# <a name="close-a-quote"></a>Chiudere un'offerta

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Un'offerta di progetto può essere chiusa come acquisita o persa. Poiché le funzioni Attiva e Aggiorna non sono supportate sulle offerte in Microsoft Dynamics 365 Project Operations, puoi chiudere un'offerta in bozza.

## <a name="close-a-quote-as-won"></a>Chiudere un'offerta come acquisita

La chiusura di un'offerta di progetto come acquisita imposterà lo stato dell'offerta su **Chiusa** e il motivo stato **Acquisita**. La chiusura dell'offerta la rende di sola lettura e crea un contratto di progetto in bozza con tutte le informazioni sull'offerta. Poiché un'offerta chiusa non può essere riaperta, prima di chiudere un'offerta una finestra di dialogo di conferma confermerà le modifiche.

Il contratto di progetto creato da un'offerta di progetto è disponibile anche nel modulo Gestione progetti e contabilità di Project Operations. Se un contratto di progetto non è mappato a un progetto su nessuna delle voci, questo contratto di progetto viene reso disponibile come contratto di progetto inattivo e diventa attivo non appena un progetto viene mappato su almeno una delle voci di contratto.

Se l'offerta è collegata a un'opportunità, qualsiasi altra offerta di progetto dell'opportunità viene automaticamente chiusa come persa.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impatto finanziario della chiusura di un'offerta come acquisita

Se sono stati registrati dei valori effettivi per il tempo in un progetto mentre è ancora collegato a un'offerta in bozza, viene registrato solo il costo del tempo o della spesa. Dopo che un'offerta è stata chiusa come acquisita, l'applicazione effettuerà il refactoring dei costi annullando i valori effettivi di costo precedenti e ricreando nuovi valori effettivi di costo. L'applicazione elaborerà questi valori effettivi di costo in base al metodo di fatturazione della voce di contratto di progetto associata. Se i valori effettivi di costo fanno riferimento a una voce di contratto di tempistica e materiali, il sistema creerà automaticamente i valori effettivi di vendita non fatturati corrispondenti quando l'offerta viene chiusa e il contratto di progetto viene creato. Se i valori effettivi di costo fanno riferimento a una voce di contratto a prezzo fisso, l'applicazione interromperà la rielaborazione dei valori effettivi di costo in base alle regole di fatturazione separata per i clienti del contratto di progetto.

Tutti i valori effettivi rielaborati sono disponibili nel modulo Gestione progetti e contabilità affinché il contabile del progetto possa rivederli, aggiornarli e registrarli nella contabilità generale. 

## <a name="close-a-quote-as-lost"></a>Chiudere un'offerta come persa

La chiusura di un'offerta come persa imposterà lo stato su **Chiusa** e il motivo stato su **Persa**. La chiusura dell'offerta la rende di sola lettura. Poiché un'offerta chiusa non può essere riaperta, prima di chiudere un'offerta una finestra di dialogo di conferma confermerà le modifiche.

Se l'offerta di progetto chiusa come persa fa riferimento a un progetto in una delle sue righe, anche quel progetto viene contrassegnato come chiuso e tutte le prenotazioni di risorse da quel giorno in poi vengono annullate.

> [!NOTE]
> In Project Operations, la chiusura di un'offerta come acquisita o persa non influirà sullo stato dell'opportunità, che rimarrà aperta fino a quando non verrà chiusa manualmente.
