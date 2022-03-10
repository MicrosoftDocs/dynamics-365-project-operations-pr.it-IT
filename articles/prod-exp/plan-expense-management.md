---
title: Configurare la gestione delle spese
description: In questo articolo vengono descritte le considerazioni e le decisioni da prendere durante il processo di pianificazione prima di configurare la gestione delle spese in Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eca4362b0ff5d37b131e1d96e311aa48ac20397618314936944ba66e458dbdc2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007466"
---
# <a name="configure-expense-management"></a>Configurare la gestione delle spese

In questo argomento vengono descritte le considerazioni e le decisioni da prendere durante il processo di pianificazione prima di configurare la gestione delle spese. In Gestione spese è possibile archiviare informazioni su metodi di pagamento, richieste di viaggio, note spese, criteri e così via.

Poiché molte delle decisioni prese durante la pianificazione della configurazione per la gestione delle spese si basano sulla gerarchia e sulla struttura finanziaria dell'organizzazione, è necessario fare riferimento ai documenti di pianificazione per quelle aree.

## <a name="intercompany-expenses"></a>Spese interaziendali

Quando abiliti le spese interaziendali, consenti alle persone giuridiche e ai dipendenti di sostenere spese per conto di un'altra persona giuridica e riscuotere il pagamento dalla persona giuridica che impiega il dipendente all'interno dell'organizzazione. Ad esempio, un dipendente della persona giuridica A completa un progetto per la persona giuridica B e il progetto include le spese relative al viaggio. Se le spese interaziendali sono abilitate, il dipendente può quindi presentare una nota spese che registra la spesa nella persona giuridica B e la spesa deve quindi essere pagata dalla persona giuridica A. Se la tua organizzazione non ha più persone giuridiche, non devi abilitare le spese interaziendali.

**Decisione:** vuoi abilitare le spese interaziendali?

## <a name="financial-management"></a>Gestione finanziaria

La gestione delle spese è strettamente integrata con la gestione finanziaria della tua organizzazione. Gran parte della tua configurazione per la gestione delle spese sarà basata sulle decisioni che hai preso per i dati finanziari della tua organizzazione. Le sezioni seguenti descrivono le varie aree che richiedono pianificazione e decisioni, in base alle decisioni dei dati finanziari dell'organizzazione e alle linee guida del team di leadership.

### <a name="per-diems"></a>Diaria

È necessario definire la diaria dei dipendenti fornita dall'organizzazione. Poiché la diaria giornaliera viene generalmente utilizzata per coprire spese quali vitto, alloggio e altre spese accessorie, puoi creare regole per le diarie giornaliere offerte dall'organizzazione. Le tariffe giornaliere possono essere basate sul periodo dell'anno, sulla destinazione del viaggio o su entrambi. Quando definisci una regola per la diaria, puoi specificare che una percentuale della tariffa giornaliera sarà trattenuta se un lavoratore riceve vitto o servizi gratuiti. Puoi inoltre definire livelli di tariffe giornaliere per impostare un numero minimo e massimo di ore che la tariffa giornaliera può applicare al viaggio di un lavoratore.

**Decisioni:**

- Regole per la diaria predefinite per il primo e l'ultimo giorno:

    - Qual è il numero minimo di ore che un dipendente può richiedere per un giorno e ricevere la diaria?
    - È prevista una riduzione dell'importo offerto per i pasti del primo e dell'ultimo giorno? Se c'è una riduzione, qual è la percentuale della riduzione?
    - È prevista una riduzione dell'importo offerto per l'hotel del primo e dell'ultimo giorno? Se c'è una riduzione, qual è la percentuale della riduzione?
    - È prevista una riduzione dell'importo offerto per le altre spese sostenute nel primo e nell'ultimo giorno? Se c'è una riduzione, qual è la percentuale della riduzione?

- Regole per la diaria predefinite:

    - C'è una riduzione in percentuale della diaria giornaliera per ogni pasto se, ad esempio, il pasto è gratuito? Se c'è una riduzione, qual è la percentuale della riduzione per ogni pasto?
    - La riduzione del pasto è calcolata al giorno, per viaggio o in base al numero di pasti giornalieri?
    - Gli importi giornalieri devono essere arrotondati in modo regolare o per eccesso?
    - Le diarie sono calcolate su un periodo di 24 ore o su un giorno di calendario?

- Regole per la diaria basate sulla posizione:

    - Le tariffe per la diaria variano a seconda della località? Quali località sono incluse?
    - Se le tariffe per la diaria variano a seconda della località, per ciascuna località, quale percentuale è prevista per le seguenti tipologie di spese:

        - Vitto
        - Hotel
        - Altre spese

### <a name="expense-management-journals-and-accounts"></a>Giornali di registrazione e conti di gestione delle spese

La gestione delle spese richiede l'utilizzo di più giornali di registrazione e conti. È necessario decidere, ad esempio, se lo stesso conto viene utilizzato per anticipi di cassa e controversie con carte di credito.

**Decisioni:**

- In quale giornale di registrazione contabile vengono registrate le note spese approvate?
- Quale conto viene utilizzato per gli anticipi di cassa?
- Gli anticipi di cassa devono essere registrati immediatamente?

### <a name="payment-methods"></a>Modalità di pagamento

Quando si consente ai dipendenti di sostenere spese per conto dell'azienda, è necessario definire i metodi di pagamento che i dipendenti possono utilizzare. Ad esempio, potresti consentire ai dipendenti di utilizzare contanti o una carta di credito aziendale. Potresti anche consentire ai dipendenti di utilizzare carte di credito personali e quindi rimborsare i dipendenti. È necessario prendere le seguenti decisioni per ogni metodo di pagamento consentito.

**Decisioni:**

- Quali metodi di pagamento sono consentiti?
- A chi spetta le spese del metodo di pagamento?
- Esiste un tipo di conto di compensazione? Se esiste un tipo di conto di compensazione, che cos'è?
- Se esiste un conto di compensazione, che cos'è il conto?
- Se il metodo di pagamento è una carta di credito, il metodo di pagamento deve essere utilizzato solo con le transazioni importate?

### <a name="expense-categories-and-shared-categories"></a>Categorie di spesa e categorie condivise

Quando i dipendenti creano una nota spese, ogni spesa che registrano deve essere associata a una categoria di spesa. Le categorie di spesa derivano da categorie condivise che possono essere condivise tra le persone giuridiche dell'organizzazione. Queste categorie possono anche essere condivise in Gestione progetti e contabilità, a seconda del modo in cui è definita l'organizzazione. In base alla definizione dell'organizzazione e alle linee guida del team di implementazione, è necessario determinare se le categorie utilizzate nella gestione delle spese verranno utilizzate solo in Gestione spese o se debbano essere condivise tra Gestione progetti e contabilità e Gestione spese. Nota che queste categorie possono essere condivise tra progetto e spesa o progetto e produzione e non tra spesa e produzione. È necessario prendere le seguenti decisioni per ciascuna categoria di spesa.

**Decisioni:**

- Qual è la categoria di spesa? Gli esempi includono categorie per voli, hotel o chilometraggio.
- La categoria di spesa può essere utilizzata anche in Gestione progetti e contabilità?
- Qual è il tipo di spesa?
- Qual è il metodo di pagamento predefinito per la categoria di spesa?
- Le spese nella categoria di spesa devono essere dettagliate?
- Qual è il conto predefinito principale per la categoria di spesa?
- Qual è la fascia IVA articoli predefinita per la categoria di spesa?
- Sono consentiti metodi di pagamento aggiuntivi per la categoria di spesa? Se sono consentiti metodi di pagamento aggiuntivi, quali sono?
- Ci sono sottocategorie in questa categoria di spesa? In caso affermativo, devi anche prendere le decisioni seguenti:

    - Alcune delle sottocategorie sono escluse dal recupero IVA?
    - Qual è la fascia IVA articoli delle sottocategorie?

Se la categoria di spesa viene utilizzata anche in Gestione progetti e contabilità, rispondi alle domande rimanenti. Altrimenti, vai alla sezione successiva.

- Quali conti di costo verranno utilizzati per le seguenti spese?

    - Costo
    - Allocazione retribuzioni
    - WIP - valore costo
    - Elemento di costo
    - WIP - elemento valore di costo
    - Perdita maturata
    - WIP - perdita maturata

- Quali ricavi di costo verranno utilizzati per le seguenti opzioni?

    - Ricavi fatturati
    - Ricavi maturati - valore delle vendite
    - WIP - valore delle vendite
    - Ricavi maturati - produzione
    - WIP - produzione
    - Ricavi maturati - profitti
    - WIP - profitti
    - Ricavi maturati - abbonamento
    - WIP - abbonamento

### <a name="taxes"></a>Imposte

Per le imposte relative alle spese, è necessario determinare cosa è incluso o abilitato nelle note spese.

**Decisioni:**

- L'IVA è inclusa negli importi delle spese?
- Il recupero dell'IVA deve essere abilitato sulle spese?

    > [!NOTE]
    > Se quando hai pianificato la contabilità generale hai deciso di applicare l'IVA statunitense e utilizzare le regole fiscali, non puoi abilitare il recupero dell'IVA sulle spese. (Per applicare l'IVA negli Stati Uniti e utilizzare le regole fiscali, imposta l'opzione **Applica le regole di tassazione IVA** su **Sì**.)

## <a name="policies"></a>Criteri

Creando criteri di nota spese, puoi aiutare la tua organizzazione a risparmiare tempo e denaro quando i dipendenti sostengono le spese per suo conto. I criteri aiutano a garantire che i dipendenti rispettino il budget, forniscano tutte le informazioni richieste e spendano denaro solo quando necessario. È necessario prendere le seguenti decisioni per ogni criterio della nota spese e ogni criterio di approvazione della nota spese creato.

**Decisioni:**

- Qual è il nome del criterio?
- A cosa serve il criterio di spesa?
- Se in precedenza hai deciso di abilitare le spese interaziendali, a quali società della tua organizzazione verrà applicato questo criterio?
- Quando entra in vigore il criterio?
- Quando scade il criterio?
- Qual è la regola dei criteri?
- Qual è il risultato della regola dei criteri?


[!INCLUDE[footer-include](../includes/footer-banner.md)]