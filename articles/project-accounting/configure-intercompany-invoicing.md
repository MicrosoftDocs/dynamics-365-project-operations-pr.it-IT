---
title: Configurare la fatturazione interaziendale
description: Questo argomento fornisce informazioni ed esempi sulla configurazione della fatturazione interaziendale per i progetti.
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2dec6669a41161a23f74ea962df6d8708b905315
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287558"
---
# <a name="configure-intercompany-invoicing"></a>Configurare la fatturazione interaziendale

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Completare i seguenti passaggi per impostare la fatturazione interaziendale per i progetti in Dynamics 365 Project Operations. Le transazioni interaziendali sono transazioni di tempi e costi di un contratto di progetto che appartengono a una società o un'unità organizzativa, mentre le risorse del contratto di progetto fanno parte di una società o unità organizzativa diversa.

## <a name="example-configure-intercompany-invoicing"></a>Esempio: configurare la fatturazione interaziendale

Nell'esempio seguente, Contoso Robotics USA (USPM) è la persona giuridica richiedente e Contoso Robotics UK (GBPM) è la persona giuridica che effettua la concessione. 

1. **Configurare la contabilità interaziendale tra persone giuridiche**. Ciascuna coppia di persone giuridiche richiedente e che effettua la concessione deve essere configurata nella pagina Contabilità generale [Contabilità interaziendale](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. In Dynamics 365 Finance, vai a **Contabilità generale** > **Impostazione di registrazione** > **Contabilità interaziendale**. Creare un record con le seguenti informazioni:

        - **Società di origine** = **GBPM**
        - **Società di destinazione** = **USPM**

2. **Configurare la relazione commerciale tra persone giuridiche**. Il record del cliente che rappresenta la persona giuridica richiedente deve essere creato nella persona giuridica che effettua la concessione. Il record del fornitore che rappresenta la persona giuridica che effettua la concessione deve essere creato nella persona giuridica richiedente.

     1. In Finance, selezionare la persona giuridica **GBPM**.
     2. Vai a **Contabilità clienti** > **Cliente** > **Tutti i clienti**. Creare un nuovo record per la persona giuridica, **USPM**.
     3. Espandere **Nome**, filtrare i record per **Tipo** e selezionare **Persone giuridiche**. 
     4. Trovare e selezionare il record del cliente per **Contoso Robotics USA (USPM)**.
     5. Selezionare **Usa corrispondenza**. 
     6. Selezionare il gruppo di clienti e salvare il record.
     7. Selezionare la persona giuridica **USPM**.
     8. Andare a **Contabilità fornitori** > **Fornitori** > **Tutti i fornintori**. Creare un nuovo record per la persona giuridica, **GBPM**.
     9. Espandere **Nome**, filtrare i record per **Tipo** e selezionare **Persone giuridiche**. 
     10. Trovare e selezionare il record del cliente per **Contoso Robotics UK (GBPM)**.
     11. Selezionare **Usa corrispondenza**, selezionare il gruppo di fornitori, quindi salvare il record.
     12. Nel record del fornitore, selezionare **Generale** > **Configura** > **Interaziendale**.
     13. Nella scheda **Relazione commerciale**, impostare **Attivo** su **Sì**.
     14. Selezionare la società fornitore **GBPM** e in **Record del mio account**, selezionare il record del cliente che hai creato in precedenza nella procedura.

3. **Configurare le impostazioni interaziendali in Gestione progetti e parametri contabili**. 

    1. Selezionare la persona giuridica **USPM** e andare a **Contabilità e gestione dei progetti** > **Configurazione** > **Gestione progetti e parametri contabili**.
    2. Nella scheda **Interaziendale** selezionare la categoria di approvvigionamento per abbinare le fatture fornitore che vengono generate automaticamente.
    3. In **Categoria predefinita**, selezionare **Risorse interaziendali**.
    4. Selezionare la persona giuridica **GBPM** e andare a **Contabilità e gestione dei progetti** > **Configurazione** > **Gestione progetti e parametri contabili**.
    5. Nella scheda **Interaziendale**, selezionare una categoria di progetto predefinita per ogni tipo di transazione. Le categorie di progetto vengono utilizzate per la configurazione fiscale quando la categoria fatturata nelle transazioni interaziendali esiste solo nella persona giuridica mutuataria. Puoi scegliere di maturare ricavi per le transazioni interaziendali. Il rateo si verifica quando le transazioni vengono registrate tramite il giornale di registrazione Project Operations nella persona giuridica che effettua la concessione. Il giornale viene stornato quando viene registrata la fattura interaziendale.
    6. Nel gruppo **Quando si concedono in prestito risorse**, selezionare **...** > **Nuovo**. 
    7. Nella griglia, seleziona le informazioni seguenti:

          - **Persona giuridica richiedente** = **GBPM**
          - **Accumula ricavi** = **Sì**
          - **Categoria di foglio presenze predefinita** = **Predefinito: Ora**
          - **Categoria di spesa predefinita** = **Predefinito: Spesa**

4. **Impostare i conti dei costi e dei ricavi interaziendali nell'impostazione della registrazione contabile**. Il conto ricavi interaziendale viene accreditato quando la fattura cliente interaziendale viene registrata nella persona giuridica che effettua la concessione. Il conto costi interaziendale viene addebitato quando la fattura fornitore in sospeso viene registrata nella persona giuridica richiedente. Questi conti sono impostati nelle persone giuridiche corrispondenti. 
      
     1. In Finance, selezionare la persona giuridica richiedente **USPM**. 
     2. Vai a **Contabilità e gestione dei progetti** > **Configurazione** > **Registrazione** > **Impostazione della registrazione contabile**. 
     3. Nella scheda **Conti costi**, in **Tipo di conto CoGe**, selezionare **Costi interaziendali**. Creare un nuovo record con le seguenti informazioni:
      
        - **Persona giuridica che effettua la concessione** = **GBPM**
        - **Conto principale** = Selezionare il conto principale per il costo interaziendale
        
     4. Selezionare la persona giuridica che effettua la concessione **GBPM**. 
     5. Vai a **Contabilità e gestione dei progetti** > **Configurazione** > **Registrazione** > **Impostazione della registrazione contabile**. 
     6. Nella scheda **Conti ricavi**, in **Tipo di conto CoGe**, selezionare **Ricavi interaziendali**. Creare un nuovo record con le seguenti informazioni:

        - **Persona giuridica richiedente** = **USPM**
        - **Conto principale** = Selezionare il conto principale per i ricavi interaziendali 

5. **Imposta i prezzi di trasferimento per la manodopera**. Il prezzo di trasferimento interaziendale è configurato in Project Operations in Dataverse. Configura le [tariffe per il costo del lavoro](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) e le [tariffe per la fatturazione del lavoro](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) per la fatturazione interaziendale. I prezzi di trasferimento non sono supportati per le transazioni delle spese interaziendali. Il prezzo di vendita unitario tra le organizzazioni sarà sempre impostato sullo stesso valore del prezzo di costo unitario delle risorse.

      Il costo delle risorse per sviluppatori in Contoso Robotics UK è di 88 GBP l'ora. Contoso Robotics UK fatturerà a Contoso Robotics USA 120 USD per ogni ora in cui questa risorsa ha lavorato su progetti USA. Contoso Robotics USA fatturerà al cliente Adventure Works 200 USD per il lavoro svolto dalla risorsa per sviluppatori Contoso Robotics UK.

      1. In Project Operations su Dataverse, vai a **Vendita** > **Listini prezzi**. Creare un nuovo listino prezzi di costo chiamato **Tariffe di costo di Contoso Robotics UK**. 
      2. Nel listino prezzi di costo creare un record con le seguenti informazioni:
         - **Ruolo** = **Sviluppatore**
         - **Costo** = **88 GBP**
      3. Andare a **Impostazioni** > **Unità organizzative** e allegare questo listino prezzi all'unità organizzativa **Contoso Robotics UK**.
      4. Andare a **Vendite** > **Listini prezzi**. Creare un nuovo listino prezzi di costo chiamato **Tariffe di costo di Contoso Robotics USA**. 
      5. Nel listino prezzi di costo creare un record con le seguenti informazioni:
          - **Ruolo** = **Sviluppatore**
          - **Società resourcing** = **Contoso Robotics UK**
          - **Costo** = **120 USD**
      6. Andare a **Impostazioni** > **Unità organizzative** e allegare il listino prezzi **Tariffe di costo di Contoso Robotics USA** all'unità organizzativa **Contoso Robotics USA**.
      7. Andare a **Vendite** > **Listini prezzi**. Creare un listino prezzi di vendita chiamato **Tariffe per la fatturazione di Adventure Works**. 
      8. Nel listino prezzi di vendita creare un record con le seguenti informazioni:
          - **Ruolo** = **Sviluppatore**
          - **Società resourcing** = **Contoso Robotics UK**
          - **Tasso di fatturazione** = **200 USD**
      9. Andare a **Vendite** > **Contratti di progetto** e allegare il listino prezzi **Tariffe per la fatturazione di Adventure Works** al listino prezzi del progetto Adventure Works del contratto di progetto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]