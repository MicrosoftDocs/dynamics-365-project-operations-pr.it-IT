---
title: Configurare la contabilità per i progetti fatturabili
description: Questo argomento fornisce informazioni sulle opzioni di contabilità per i progetti fatturabili.
author: sigitac
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 629e3fc2f9069d104d459d0b4a6fa46c37f5c6f2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858658"
---
# <a name="configure-accounting-for-billable-projects"></a>Configurare la contabilità per i progetti fatturabili

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations supporta varie opzioni di contabilità per progetti fatturabili che includono transazioni di tempistica e materiali e prezzo fisso.

- **Transazioni temporali e materiali**: queste transazioni vengono fatturate man mano che il lavoro procede in base al consumo di ore, spese, articoli o commissioni sul progetto. Questi costi di transazione possono essere associati ai ricavi di ciascuna transazione e il progetto viene fatturato man mano che il lavoro procede. I ricavi del progetto possono inoltre essere maturati anche nel momento in cui si verifica la transazione. Durante la fatturazione, i ricavi vengono riconosciuti e, se applicabile, i ratei attivi vengono stornati.
- **Transazioni a prezzo fisso**: queste transazioni vengono fatturate in base a un programma di fatturazione basato sul contratto di progetto. I ricavi per transazioni a prezzo fisso possono essere riconosciuti alla fatturazione o calcolati e registrati periodicamente, in base ai metodi **Contratto completato** o **Percentuale completata**.

Un progetto è considerato fatturabile quando è associato a una o più voci di contratto. Una voce di contratto di progetto definisce autonomamente il metodo di fatturazione e i tipi di transazione consentiti.

Ad esempio, Fabrikam Robotics ha acquisito un contratto di progetto con la società Adatum per l'ottimizzazione delle attrezzature. Adatum pagherà un importo fisso di $10.000 USD per coprire le spese di progetto sostenute. Questo è un metodo di fatturazione a prezzo fisso. Le ore e le tariffe del progetto verranno fatturate per utilizzo. Questo è un metodo di fatturazione di tempistica e materiali. Tutto il lavoro sarà tracciato in un unico progetto denominato ottimizzazione delle attrezzature Adatum.

Un membro del team di progetto invia otto ore di lavoro sul progetto di ottimizzazione delle attrezzature Adatum. Quando il project manager approva questo tempo, il sistema utilizza il metodo di fatturazione di tempistica e materiali per creare transazioni effettive, una fattura e un conto. Questa transazione non sarà inclusa nel calcolo della stima dei ricavi a prezzo fisso.

Un altro membro del team di progetto presenta una spesa di viaggio per $2000,00 USD a fronte del progetto di ottimizzazione delle attrezzature Adatum. Quando il project manager approva questo invio, il sistema utilizza il metodo di fatturazione a prezzo fisso per creare transazioni effettive e un conto per questa spesa di progetto. Al cliente non verrà emessa fattura in base a questa transazione. La fattura verrà invece emessa utilizzando fasi di fatturazione configurate separatamente. Questa transazione di spesa, insieme alle stime di spesa, sarà inclusa nel calcolo della stima dei ricavi a prezzo fisso.

I principi contabili per le transazioni di progetto sono definiti nei profili di costi e ricavi del progetto. Per ogni transazione di progetto, il sistema determina il profilo di costi e ricavi del progetto appropriato utilizzando le regole del profilo di costi e ricavi del progetto che sono state configurate.

## <a name="define-project-cost-and-revenue-profiles"></a>Definire i profili di costi e ricavi di progetto 

I profili di costi e ricavi di progetto determinano le regole contabili per le transazioni di progetto. Questi profili vengono configurati in Gestione progetti e contabilità. 

Completa i seguenti passaggi per creare un nuovo profilo di costi e ricavi del progetto. 

1. Vai a **Gestione progetti e contabilità** > **Configura** > **Registrazione** > **Profili di costi e ricavi di progetto**. 
2. Seleziona **Nuovo** per creare un nuovo profilo di costi e ricavi di progetto.
3. Nel campo **Nome**, immetti il nome e una breve descrizione del profilo.
4. Nel campo **Metodo di fatturazione**, seleziona **Tempistica e materiali** o **Prezzo fisso**.
5. Espandi la Scheda dettaglio **Contabilità generale**. I campi di questa scheda definiscono i principi contabili utilizzati quando le transazioni di progetto vengono inserite nel giornale di registrazione utilizzando il giornale di integrazione di Project Operations e quindi fatturate tramite la proposta di fatturazione progetto.
6. Seleziona le informazioni appropriate nei seguenti campi della Shceda dettaglio **Contabilità generale**:

    - **Registra costi: ora**:

       - *Nessun libro mastro*: il costo per le transazioni temporali non verrà registrato nel libro mastro quando viene registrato il giornale di registrazione delle integrazioni Project Operations. Tuttavia, il contabile può registrare i costi utilizzando la funzione Registra costi in un secondo momento.
       - **Saldo**: il costo per le transazioni a tempo verrà addebitato al tipo di conto CoGe,*WIP - Valore di costo* e accreditato su *Allocazione retribuzioni conto* in Impostazioni registrazione contabile. Il contabile utilizzerà la funzione Registra costi per spostare periodicamente questo costo da un conto Saldo a un conto Profitti e perdite.
       - **Profitti e perdite**: durante la registrazione del giornale di integrazione di Project Operations, il costo della transazione temporale verrà addebitato al tipo di conto CoGe *Costo* e accreditato su *Allocazione retribuzioni conto* definito nella scheda **Costo** della pagina **Impostazioni registrazione contabile** (**Gestione del progetto e contabilità** \> **Configura** \> **Registrazione** \> **Impostazione registrazione contabile**). Questa è l'impostazione più comune per le transazioni di tempistica e materiali.
        - *Mai in contabilità generale*: il costo per le transazioni orarie non verrà mai registrato nella contabilità generale.

    - **Registra costi – spesa**:

         - **Saldo**: durante la registrazione del giornale di integrazione di Project Operations, il costo della transazione di spesa verrà addebitato al tipo di conto CoGe *WIP - Valore di costo* come definito nella scheda **Costo** della pagina **Impostazione registrazione contabile** e accreditato sul conto di contropartita nella riga del giornale di registrazione. I conti di contropartita predefiniti per le spese sono definiti in **Gestione del progetto e contabilità** > **Configura** \> **Registrazione** \> **Conto di contropartita predefinito per le spese**. Il contabile utilizzerà la funzione **Registra costi** per spostare periodicamente questo costo da un conto Saldo a un conto Profitti e perdite.
        - **Profitti e perdite**: durante la registrazione del giornale di integrazione di Project Operations, il costo della transazione di spesa verrà addebitato al tipo di conto CoGe *Costo* come definito nella scheda **Costo** della pagina **Impostazione registrazione contabile** e accreditato sul conto di contropartita nella riga del giornale di registrazione. I conti di contropartita predefiniti per le spese sono definiti in **Gestione del progetto e contabilità** \> **Configura** \> **Registrazione** \> **Conto di contropartita predefinito per le spese**.
      
    - **Registra costi - articolo**:

         - **Saldo**: durante la registrazione del giornale di registrazione integrazione Project Operations, il costo della transazione dell'articolo verrà addebitato al tipo di conto CoGe *WIP - Valore costo - articolo* come definito nella scheda **Costo** della pagina **Impostazione registrazione contabile** e accreditato come segue:
    
              - Per l'utilizzo del tipo di documento: sul conto **Costo - articolo** in **Impostazione registrazione contabile**.  
              - Per il documento di tipo Acquisto: **Conto di integrazione approvvigionamento** in **Parametri di contabilità e gestione di progetti**.
           Il contabile utilizzerà la funzione **Registra costi** per spostare periodicamente questo costo da un conto Saldo a un conto Profitti e perdite.
        - **Profitti e perdite**: durante la registrazione del giornale di registrazione integrazione Project Operations, il costo della transazione dell'articolo verrà addebitato al tipo di conto CoGe *Costo* come definito nella scheda **Costo** della pagina **Impostazione registrazione contabile** e accreditato come segue:
         
             - Per l'utilizzo del tipo di documento: sul conto **Costo - articolo** in **Impostazione registrazione contabile**.  
             - Per il documento di tipo Acquisto: **Conto di integrazione approvvigionamento** in **Parametri di contabilità e gestione di progetti**.
       
    - **Fatturazione acconti**:

        - **Saldo**: durante la registrazione della proposta di fatturazione progetto, una transazione in acconto (passaggio fondamentale di fatturazione) verrà accreditata al tipo di conto CoGe *WIP fatturato - in acconto* come definito nella scheda **Ricavi** della pagina **Impostazione registrazione contabile** e addebitato sul conto del saldo del cliente.
         - **Profitti e perdite**: durante la registrazione della proposta di fatturazione progetto, una transazione in acconto (passaggio fondamentale di fatturazione) verrà accreditata al tipo di conto CoGe *Ricavi fatturati - in acconto* come definito nella scheda **Ricavi** della pagina **Impostazione registrazione contabile** e addebitato sul conto del saldo del cliente. I conti del saldo del cliente sono definiti in **Contabilità clienti** \> **Configura** \> **Profili di registrazione dei clienti**.

   Quando definisci i profili di registrazione per i metodi di fatturazione tempo e materiali, hai la possibilità di maturare ricavi per tipo di transazione (ora, spesa, articolo e commissione). Se l'opzione **Accumula ricavi** è impostata su **Sì**, le transazioni di vendita non fatturate nel giornale di registrazione dell'integrazione di Project Operations verranno registrate nella contabilità generale. Il valore di vendita viene addebitato al conto **WIP - conto del valore delle vendite** e accreditato sul conto **Ricavi maturati - valore delle vendite** che è stato configurato nella pagina **Impostazione registrazione contabile**, nella scheda **Ricavi**. 
  
  > [!NOTE]
  > L'opzione **Accumula ricavi** è disponibile solo quando il rispettivo tipo di transazione **Costo** viene registrato nel conto profitti e perdite.
    
7. Espandi la Scheda dettaglio **Stima**. I campi di questa scheda definiscono le impostazioni di calcolo per le stime dei ricavi a prezzo fisso. I campi di questa scheda si applicano solo ai profili di costi e ricavi del progetto con un metodo di fatturazione di tipo **Prezzo fisso**.
8. Seleziona le informazioni appropriate nei seguenti campi della Shceda dettaglio **Stima**:

    - **Principio utilizzato per i calcoli di completamento del progetto**:

        - **Contratto completato** : l'abbinamento dei costi e il riconoscimento dei ricavi non si verificano fino alla fine del progetto. I costi si riflettono come WIP nel saldo fino al completamento del progetto.
        - **Percentuale completata**: i ricavi maturati vengono calcolati e registrati nel libro mastro ogni periodo in base alla percentuale di completamento del progetto. Sono disponibili più metodi per calcolare la percentuale di completamento. Questi metodi possono essere automatici in base alla configurazione o manuali.
        - **Nessun WIP**: questa configurazione viene utilizzata per progetti a prezzo fisso con un breve arco di tempo e in cui la fattura e i costi si verificano nello stesso periodo. In questo caso, il valore del campo **Fatturazione acconti** nella Scheda dettaglio **Contabilità generale** viene impostato automaticamente su **Profitti e perdite** per garantire che i ricavi siano riconosciuti al momento della fatturazione. Il processo di stima dei ricavi non verrà utilizzato per questo profilo di costi e ricavi del progetto.

    - **Principio di corrispondenza**: questo campo determina il modo in cui il valore di vendita calcolato (ricavo maturato) verrà registrato nel libro mastro.

        - Utilizzando il principio **Valore delle vendite**, il sistema calcolerà il valore delle vendite abbinando costi e ricavi e quindi registrandolo come un unico importo.
        - Utilizzando il principio **Produzione e profitto**, il sistema suddividerà il valore delle vendite in costi realizzati e profitto calcolato. Questi vengono registrati separatamente.

    - **Modelli di costo**: consenti il reggruppamento delle transazioni del progetto in base al tipo di transazione e alla categoria di progetto e definisci le regole di calcolo della percentuale di completamento per questi gruppi.
    - **Codici periodo**: definisci la frequenza con cui vengono calcolate le stime dei ricavi per un dato profilo di costi e ricavi del progetto.
    - **Categorie per stima**: utilizzato per la registrazione del valore di vendita (ricavo maturato) nelle transazioni di progetto. Innanzitutto, configura la categoria di progetto dedicata per un tipo di transazione **Commissione** e quindi imposta il flag, **Stima** per questa categoria di progetto. Successivamente, a seconda del principio di corrispondenza selezionato, scegli questa categoria di progetto nel valore **Vendite** o il campo **Profitto** nel profilo costi e ricavi del progetto.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Configurazioni di esempio per i profili di costi e ricavi del progetto

Tempi e materiali - nessun WIP

![Profilo di costi e ricavi: tempo e materiali - nessun WIP](media/time-material-no-wip.png)

Tempi e materiali - WIP (ricavi)

![Profilo di costi e ricavi: tempo e materiali - WIP](media/time-material-with-wip.png)

Prezzo fisso - Nessun WIP

![Profilo di costi e ricavi: prezzo fisso - nessun WIP](media/fixed-price-no-wip.png)

Prezzo fisso - contratto completato

![Profilo di costi e ricavi: prezzo fisso - contratto completato](media/fixed-price-completed-contract.png)

Prezzo fisso - percentuale di completamento

![Profilo di costi e ricavi: prezzo fisso - percentuale di completamento](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Esempi di evento di contabilità per i profili di costi e ricavi del progetto di esempio.

| Evento di contabilità                  | Tempistica e materiali - Nessun WIP                       | Tempistica e materiali - WIP                                                                                           | Prezzo fisso - Nessun WIP                                            | Prezzo fisso - Contratto completato                                                                            | Prezzo fisso - Percentuale di completamento                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Inserimento nel giornale di registrazione delle transazioni temporali    | Debito - Costo <br>Credito - Allocazione retribuzioni          | Debito - Costo <br>Credito - Allocazione retribuzioni <br>Debito - Valore vendite WIP <br>Credito - Valore delle vendite ricavi maturati                | Debito - Costo <br>Credito - Allocazione retribuzioni                         | Debito - Costo <br>Credito - Allocazione retribuzioni                                                                    | Debito - Costo <br>Credito - Allocazione retribuzioni                       |
| Inserimento nel giornale di registrazione delle transazioni di spesa | Debito - Costo <br>Credito - Conto di contropartita predefinito per le spese | Debito - Costo <br>Credito - Conto di contropartita predefinito per le spese <br>Debito - Valore vendite WIP <br>Credito - Valore delle vendite ricavi maturati      | Debito - Costo <br>Credito - Conto di contropartita predefinito per le spese                 | Debito - Costo<br> Credito - Conto di contropartita predefinito per le spese                                                            | Debito - Costo <br>Credito - Conto di contropartita predefinito per le spese               |
| Fatturazione al cliente                | Debito - Saldo cliente <br>Credito - Ricavi fatturati | Debito - Saldo cliente <br>Credito - Ricavi fatturati <br>Credito - Valore vendite WIP Debito - Valore vendite ricavi maturati | Debito - Saldo cliente <br>Credito - Ricavi fatturati - in acconto | Debito - Saldo cliente <br>Credito - WIP- Fatturati in acconto                                                  | Debito - Saldo cliente <br>Credito - WIP- Fatturati in acconto    |
| Registrare stima ricavi             | Non applicabile                                   | Non applicabile                                                                                                    | Non applicabile                                                  | Debito - Valore costo WIP <br>Credito - Costo                                                                         | Debito - WIP - Valore vendite <br>Credito - Valore delle vendite ricavi maturati |
| Elimina                         | Non applicabile                                   | Non applicabile                                                                                                    | Non applicabile                                                  | Credito - Valore costo WIP <br>Debito - Costo <br>Credito - Ricavi maturati - Valore delle vendite <br>Debito - WIP fatturato in acconto | Debito - WIP- Fatturato in acconto <br>Credito - WIP - Valore vendite     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Configurare le regore dei profili di costi e ricavi di progetto

Le regole del profilo dei costi e dei ricavi del progetto determinano il profilo dei costi e dei ricavi del progetto che deve essere utilizzato durante l'elaborazione delle transazioni di progetto fatturabili. Definisci le regole andando a **Gestione del progetto e contabilità** \> **Configura** \> **Registrazione** \> **Regole del profilo dei costi e dei ricavi del progetto**.

Le regole possono essere definite dal contratto di progetto, dal gruppo di progetto o da un progetto specifico. Il sistema sceglierà sempre per prima la regola di granularità più alta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
