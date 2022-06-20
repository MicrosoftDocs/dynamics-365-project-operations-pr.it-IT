---
title: Configurare le risorse di progetto
description: Questo articolo fornisce informazioni sulla configurazione o sulla richiesta delle risorse di progetto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a4e6fe829d6b39aed9eb6aaea42f245fc997593
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933773"
---
# <a name="set-up-project-resources"></a>Configurare le risorse di progetto

[!include [banner](../includes/banner.md)]

Devi configurare un calendario e associarlo a un dipendente o a un lavoratore. Il calendario viene utilizzato per pianificare il progetto e l'orario di lavoro delle risorse riservate al progetto. Durante la configurazione del calendario, i project manager possono eseguire il livellamento delle risorse come parte dell'ottimizzazione delle risorse. In base alla pianificazione del calendario, è possibile applicare restrizioni alle risorse. Puoi configurare un calendario nella pagina **Calendari**.

Quando configuri un lavoratore come risorsa del progetto, puoi selezionare tra i lavoratori che lavorano nell'azienda per cui stai configurando le risorse. In alternativa, puoi selezionare lavoratori di altre società nella tua organizzazione. Questi lavoratori sono noti come risorse interaziendali.

Le seguenti procedure spiegano come configurare un lavoratore come risorsa di progetto nella propria azienda e come configurare una risorsa di progetto interaziendale.

## <a name="set-up-a-worker-as-a-project-resource"></a>Configurare un lavoratore come risorsa del progetto

1. Nella pagina **Lavoratori** pagina, nell'elenco **Lavoratori**, seleziona il lavoratore che stai aggiungendo come risorsa del progetto e apri il record del lavoratore.
2. Nel riquadro azioni seleziona **Progetto**&gt; **Imposta** &gt;**Impostazione progetto**.
3. Seleziona un calendario e quindi chiudi la pagina.

Puoi inoltre specificare progetti predefiniti per una risorsa come tipo di pre-assegnazione. Le pre-assegnazioni possono essere utilizzate quando il responsabile delle risorse o il project manager sa in anticipo su quali progetti lavorerà la risorsa. Le pre-assegnazioni possono anche essere basate sulla richiesta di uno sponsor del progetto o di un cliente. Per pre-assegnare un progetto, nella pagina **Assegna progetti**, nella scheda **Progetti**, nell'elenco **Progetti rimanenti**, seleziona il progetto appropriato.

## <a name="set-up-an-intercompany-resource"></a>Configurare una risorsa interaziendale

Quando si configura un lavoratore come risorsa interaziendale, devi completare la configurazione sia nella società mutuante che nella società mutuataria.

### <a name="in-the-lending-company"></a>Nella società mutuante

1. In Finance, verifica che la società mutuante sia selezionata, quindi completa la procedura nella sezione precedente, "Configurare un lavoratore come risorsa di progetto".
2. Nella pagina **Contabilità interaziendale**, seleziona **Nuovo**.
3. Nel campo **ID persona giuridica**, seleziona la società mutuante. Compila i campi rimanenti come necessario e quindi seleziona **Salva**.
4. Nella pagina **Prezzo di trasferimento**, seleziona **Nuovo**.
5. Nel campo **Persona giuridica richiedente**, seleziona la società appropriata.
6. Per prestare alla società mutuataria solo la risorsa che hai creato all'inizio di questa sezione, nel campo **Risorsa**, seleziona il nome della risorsa che hai creato. Per rendere disponibili alla società mutuataria tutte le risorse della società mutuante, lascia vuoto il campo **Risorsa**.
7. Nella pagina **Parametri Gestione progetti e contabilità**, nella scheda **Interaziendale**, imposta l'opzione **Abilita programmazione risorse interaziendale e fogli presenze** su **Sì**.

### <a name="in-the-borrowing-company"></a>Nella società mutuataria

- Nella pagina **Elenco risorse**, nel filtro di ricerca, inserisci il nome della risorsa che hai creato per la società mutuante, per verificare che il nome sia incluso nell'elenco delle risorse per la società mutuataria.

## <a name="request-project-resources"></a>Richiedere risorse di progetto
La funzionalità per la pianificazione delle risorse di progetto consente solo ai responsabili delle risorse di distribuire le risorse con personale su impegni o progetti. Per abilitare questa funzionalità, completa le seguenti attività o verifica che siano state completate:

- Configura le sequenze numeriche.
- Configura i flussi di lavoro di gestione dei progetti e contabilità.
- Abilita i flussi di lavoro delle richieste di risorse.

Dopo che le attività precedenti sono state completate, puoi completare le seguenti attività come richiesto:

- Crea una richiesta di risorse da una risorsa con personale con prenotazione provvisoria.
- Monitora le richieste di risorse.
- Soddisfa richieste di risorse.
- Richiedi una risorsa con personale da una struttura di suddivisione del lavoro.
- Prenota risorse per un progetto senza dover richiedere una risorsa con personale.


[!INCLUDE[footer-include](../includes/footer-banner.md)]