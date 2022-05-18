---
title: Spese giornaliere
description: In questo argomento vengono fornite informazioni su come utilizzare le spese giornaliere.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596055"
---
# <a name="per-diem-expenses"></a>Spese giornaliere

> [!IMPORTANT] 
> La funzionalità descritta in questo argomento è disponibile per gli utenti interessati nell'ambito di una versione di anteprima.

Un pagamento giornaliero è un'indennità giornaliera fissa e predeterminata che un'azienda paga ai propri dipendenti per l'alloggio (hotel), i pasti e le spese accessorie che tali dipendenti devono sostenere quando viaggiano per lavoro. L'azienda paga questa indennità ai dipendenti invece di pagare le spese di viaggio effettive. I dipendenti possono utilizzare l'indennità giornaliera **Accessori/Altro** per coprire mance, servizio in camera, lavanderia o pulitura a secco per importanti riunioni di lavoro. La tariffa giornaliera può variare a seconda che il datore di lavoro scelga di rimborsare il costo combinato di vitto e alloggio o solo il costo di vitto e spese accessorie.

Le tariffe giornaliere possono essere basate sul periodo dell'anno, sulla destinazione del viaggio o su entrambi. Quando crei una regola relativa alla trasferta giornaliera, è possibile specificare che si tratterrà una percentuale della trasferta giornaliera se un dipendente riceve pasti o servizi gratuiti. È inoltre possibile impostare il numero minimo e massimo di ore per cui è possibile applicare la tariffa di trasferta giornaliera di un dipendente.

L'indennità giornaliera è calcolata come l'indennità totale offerta al giorno meno la riduzione del pasto (costo dei pasti gratuiti) fornita al dipendente.

## <a name="configure-per-diems"></a>Configurare le indennità giornaliere

Per configurare le indennità giornaliere, esegui la procedura seguente.

1. Vai in **Gestione spese** \> **Impostazioni** \> **Generale** \> **Parametri di gestione spese**.
2. Sulla scheda **Diaria**, nel campo **Calcola riduzione per vitto per**, seleziona come devono essere calcolate le diarie:

    - **Tipo di pasto per viaggio** – Calcola la diaria in base al tipo di pasto inserito (colazione, pranzo o cena) e alla riduzione del pasto specificata per ciascun tipo di pasto per l'indennità giornaliera per la durata del viaggio.
    - **Tipo di pasto per giorno** – Calcola la diaria in base al tipo di pasto inserito e alla riduzione del pasto specificata per ciascun tipo di pasto per l'indennità giornaliera per giorno.
    - **Numero di pasti al giorno** – Calcola la diaria in base al numero di pasti che vengono inseriti al giorno e alla riduzione dei pasti per il numero di pasti che vengono forniti ogni giorno.

3. Vai a **Gestione spese** \> **Impostazioni** \> **Calcoli e codici** \> **Destinazione trasferta giornaliera**.
4. Aggiungi le destinazioni in cui si possono utilizzare le diarie.
5. Per ogni destinazione che aggiungi, nella scheda **Diaria** seleziona la diaria giornaliera e la valuta valide tra le date di inizio e fine specifiche per alloggio, pasti e altre spese. Per configurare le diarie e le valute, accedi a **Gestione spese** \> **Impostazioni** \> **Calcoli e codici** \> **Trasferte giornaliere**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Trasferte giornaliere nell'interfaccia di spesa reinventata

La funzione diaria è supportata nella reinventata area di lavoro **Gestione spese** in Microsoft Dynamics 365 Finance versione 10.0.25 e successive.

Per abilitare le diarie, segui questi passaggi.

1. Nell'area di lavoro **Gestione funzionalità** trova e seleziona la funzionalità **Note spese riprogettate** nell'elenco, quindi seleziona **Abilita ora**.
2. Trova e seleziona la funzionalità **Interfaccia riprogettata per note spese giornaliere** nell'elenco e seleziona **Abilita ora**.

## <a name="how-the-feature-works"></a>Funzionamento della funzionalità

Questa sezione fornisce esempi per tre scenari di configurazione. Per ogni esempio, il campo **Calcola riduzione per vitto per** è impostato su un valore diverso. Per tutti e tre gli esempi, l'importo totale da pagare è lo stesso fino all'applicazione della riduzione del pasto. Dopo quel punto, l'importo totale da pagare differisce per ciascun esempio.

Per creare la spesa giornaliera utilizzata per tutti e tre gli esempi, attieniti alla seguente procedura.

1. Vai in **Aree di lavoro** \> **Gestione spese**.
2. Seleziona **Nuova nota spesa** oppure seleziona una nota spese esistente.
3. Aggiungi una nuova spesa. Nel campo **Categoria**, selezionare **Diaria**. Seleziona la destinazione e le date di inizio e fine del tuo viaggio. La diaria per alloggio, pasti e spese accessorie (altre spese) viene calcolata in base all'indennità giornaliera impostata per la destinazione selezionata.

    Ad esempio, selezioni **Redmond (Stati Uniti)** come destinazione. L'indennità giornaliera per quel luogo è di 150 dollari USA (150 USD) per l'alloggio, USD 75 per i pasti e USD 5 per spese accessorie. La data di inizio è il 10 gennaio e la data di fine è il 14 gennaio. Pertanto, la durata selezionata è di cinque giorni quando la configurazione selezionata è giorni di calendario con l'ora e l'ora selezionata inizia e termina alle 00:00 nelle date di inizio e fine. Ecco i calcoli:

    - Importo totale pagabile = 5 × (150 + 75 + 5) = 5 × 230 = USD 1.150
    - Pasto e quota accessoria dell'importo totale = 5 × (75 + 5) = USD 400

Se durante il viaggio sono stati forniti colazione, pranzo e cena, tali pasti devono essere contabilizzati come riduzione del pasto.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Esempio 1: diaria in cui le riduzioni dei pasti si basano sul tipo di pasto per viaggio

In questo esempio, la riduzione del pasto è del 30% per la colazione, del 30% per il pranzo e del 40% per la cena. Sulla pagina **Parametri di gestione spese** il campo **Calcola riduzione per vitto per** è impostato su **Tipo di pasto per viaggio**. Ecco i calcoli se al dipendente sono state fornite tre colazioni, due pranzi e zero cene:

- Riduzione del pasto = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22.50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112,50
- Pasti e spese accessorie = 400 – 112,50 = USD 287,50
- Importo totale pagabile = Indennità totale – Riduzione pasti = 1.150 – 112,50 = USD 1.037,50

![Diaria in cui la riduzione dei pasti si basa sul tipo di pasto per viaggio.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Esempio 2: diaria in cui le riduzioni dei pasti si basano sul tipo di pasto per giorno

In questo esempio, la riduzione del pasto è del 30% per la colazione, del 30% per il pranzo e del 40% per la cena. Sulla pagina **Parametri di gestione spese** il campo **Calcola riduzione per vitto per** è impostato su **Tipo di pasto per giorno**. In questo caso, nella griglia **Pasti** nella finestra di dialogo **Modifica spesa**, deseleziona le caselle di controllo per indicare quali pasti sono stati forniti durante il viaggio.

Ad esempio, ecco i calcoli se è stata fornita la colazione per i primi tre giorni del viaggio:

- Riduzione del pasto giornaliera per ciascuno dei primi tre giorni = 75 × 30% = USD 22,50
- Riduzione totale del pasto = 3 × 22,50 = USD 67,50
- Pasti e spese accessorie per i giorni da 1 a 3 = 75 – 22,50 = USD 57,50
- Totale pasti e spese accessorie = Somma di pasti e spese accessorie in cinque giorni = 400 – 67,50 = USD 332,50
- Importo totale pagabile = Importo totale – Riduzione pasti = 1.150 – 67,50 = USD 1.082,50

![Diaria in cui la riduzione dei pasti si basa sul tipo di pasto per giorno.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Esempio 3: diaria in cui le riduzioni dei pasti si basano sul numero di pasti per giorno

In questo esempio, la riduzione del pasto viene calcolata in base al numero di pasti forniti al giorno (ovvero il campo **Calcola riduzione per vitto per** nella pagina **Parametri di gestione spese** è impostato su **Numero di pasti al giorno**). Nella griglia **Pasti** nella finestra di dialogo **Modifica spesa**, deseleziona le caselle di controllo per indicare quali pasti sono stati forniti.
In questo caso, la riduzione del pasto si basa solo sul numero di pasti forniti, e non sul tipo di pasto (Colazione/pranzo/cena) fornito.

Ecco i calcoli della diaria quando l'indennità giornaliera è USD 150 per l'alloggio, USD 75 per i pasti e USD 5 per le spese accessorie:

- **Importo totale pagabile** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1.150
- **Un pasto:** Riduzione del pasto = 20% = USD 15
- **Due pasti:** Riduzione del pasto = 50% = USD 37,50
- **Tre pasti:** Riduzione del pasto = 100% = USD 75

Ecco i calcoli per **pasti e indennità accessorie**, che include USD 5 per le spese accessorie:

- Giorno 1 - Due pasti forniti = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Giorno 2 - Due pasti forniti = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Giorno 3 - Un pasto fornito = (75 – 15) + 5 = 60 + 5 = USD 65
- Giorno 4 - Zero pasti forniti = (75-0) + 5 = 75 + 5 = USD 80
- Giorno 5 - Tre pasti forniti = (75 – 75) + 5 = 0 + 5 = USD 5

- Totale pasti e spese accessorie = Pasti e spese accessorie per il giorno 1+ giorno 2 +giorno 3+giorno 4+ giorno 5 = USD 235
- Riduzione totale del pasto = Riduzione del pasto per il Giorno 1+ Giorno 2 +Giorno 3+Giorno 4+ Giorno 5= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Importo totale pagabile = Indennità totale – Totale riduzione pasti = USD 1.150 – USD 165 = USD 985

![Diaria in cui la riduzione dei pasti si basa sul numero di pasti per giorno.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> A partire dalla versione Finance 10.0.23, se si utilizza l'interfaccia spese riprogettata, non è possibile creare spese giornaliere con date sovrapposte. Se tenti viene visualizzato un messaggio di errore.
