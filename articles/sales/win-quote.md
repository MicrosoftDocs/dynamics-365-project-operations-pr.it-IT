---
title: Chiudere un'offerta
description: In questo articolo vengono fornite informazioni sulla chiusura delle offerte in Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 45bdfe5fb9eddb8f96ed1bc017596c8fe436245e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931887"
---
# <a name="close-a-quote"></a>Chiudere un'offerta

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Un'offerta di progetto può essere chiusa come acquisita o persa. Dal momento che le funzioni Attiva e Revisiona non sono supportate nelle offerte in Microsoft Dynamics 365 Project Operations, puoi chiudere un'offerta in bozza.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]