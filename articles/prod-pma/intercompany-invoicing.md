---
title: Fatturazione interaziendale
description: Questo articolo fornisce informazioni ed esempi sulla fatturazione interaziendale per i progetti.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f66af9b7e2cb0e18a5464b23216ff03b63a0a3
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685385"
---
# <a name="intercompany-invoicing"></a>Fatturazione interaziendale

[!include [banner](../includes/banner.md)]

Questo articolo fornisce informazioni ed esempi sulla fatturazione interaziendale per i progetti.

La tua organizzazione potrebbe avere più divisioni, filiali e altre persone giuridiche che trasferiscono prodotti e servizi tra loro per i progetti. La persona giuridica che fornisce il servizio o il prodotto è denominata *entità giuridica mutuante*, mentre la persona giuridica che riceve il servizio o il prodotto è denominata *persona giuridica mutuataria*. 

La seguente illustrazione mostra uno scenario tipico in cui due persone giuridiche, SI FR (la persona giuridica mutuante) e SI USA (la persona giuridica mutuataria) condividono le risorse per consegnare un progetto per il cliente A. Per questo scenario, SI FR è incaricata di fornire il lavorare al cliente A. 

[![Esempio di fatturazione interaziendale.](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

L'obiettivo è rendere più flessibili e avanzati il controllo dei costi, il riconoscimento dei ricavi, le tasse e il prezzo di trasferimento per le transazioni di progetti interaziendali. Inoltre, vengono fornite le seguenti funzionalità:

-   Crea fatture cliente a fronte di un progetto in una persona giuridica mutuante utilizzando fogli presenze interaziendali, spese e fatture fornitore in una persona giuridica mutuataria.
-   Supporta il calcolo delle imposte e i costi indiretti.
-   Differisci il riconoscimento dei ricavi in una persona giuridica mutuataria e quando una persona giuridica mutuante deve rilevare il costo.
-   Accumula i ricavi del lavoro in corso (WIP) nella persona giuridica mutuataria.
-   Imposta i prezzi di trasferimento che possono essere basati su vari modelli di prezzo. Di seguito sono riportati alcuni esempi.
    -   **Quantità**: l'importo che inserisci nel campo **Prezzi** è il costo effettivo per quantità o unità.
    -   **Importo spese**: il prezzo/costo per transazione più l'importo delle spese che inserisci nel campo **Prezzi**.
    -   **Percentuale spese**: il prezzo di trasferimento è il prezzo/costo per transazione moltiplicato per la percentuale di spese che inserisci nel campo **Prezzi**.
    -   **Percentuale del prezzo di vendita**: la percentuale del prezzo di vendita che viene trasferita alla persona giuridica mutuante.
    -   **Importo inferiore al prezzo di vendita**: l'importo trattenuto dalla persona giuridica mutuataria dai prezzi di vendita prima del trasferimento alla persona giuridica mutuante.
    -   **Rapporto di contribuzione**: il numero che immetti nel campo **Prezzi** è il rapporto di contribuzione, espresso come percentuale del prezzo di vendita.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Esempio 1: configurare i parametri per la fatturazione interaziendale
In questo esempio, USSI è una persona giuridica mutuante e le sue risorse riferiscono il tempo a fronte della persona giuridica mutuataria, FRSI, proprietaria del contratto con il cliente finale. Le ore e le spese riportate dai dipendenti USSI possono essere incluse nella fattura del progetto generata da FRSI. Inoltre, esiste una terza fonte di transazioni che può avere origine dall'entità giuridica mutuante (USSI in questo esempio) quando fornisce servizi di fornitori condivisi alle filiali (come FRSI) e quindi trasferisce tali costi ai progetti all'interno di tali filiali. Tutti i documenti di fatturazione e i calcoli delle imposte corrispondenti vengono completati da Finance. 

Per questo esempio, FRSI deve essere un cliente della persona giuridica USSI e USSI deve essere un fornitore della persona giuridica FRSI. Puoi quindi configurare una relazione interaziendale tra le due persone giuridiche. La procedura seguente mostra come configurare i parametri in modo che entrambe le persone giuridiche possano partecipare alla fatturazione interaziendale.

1. Configura FRSI come cliente nella persona giuridica USSI e configura USSI come fornitore nella persona giuridica FRSI. Esistono tre punti di ingresso per i passaggi necessari per questa attività.

   | Passaggio |                                                       Punto di accesso                                                        |                                                                                                                                                                                               Descrizione                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | In USSI, fai clic su <strong>Contabilità clienti</strong>&gt; <strong>Clienti</strong> &gt; <strong>Tutti i clienti</strong>. |                                                                                                                                                                  Crea un nuovo record cliente per FRSI e seleziona il gruppo di clienti.                                                                                                                                                                  |
   |  G   |    In FRSI, fai clic su <strong>Contabilità fornitori</strong> &gt; <strong>Fornitori</strong> &gt; <strong>Tutti i fornitori</strong>.     |                                                                                                                                                                    Crea un nuovo record fornitore per USSI e seleziona il gruppo di fornitori.                                                                                                                                                                    |
   |  C   |                                  In FRSI, apri il record fornitore appena creato.                                  | Nel riquadro azioni, nella scheda <strong>Generale</strong>, nel gruppo <strong>Configura</strong>, seleziona <strong>Interaziendale</strong>. Nella pagina <strong>Interaziendale</strong>, nella scheda <strong>Relazione commerciale</strong>, imposta l'opzione <strong>Attivo</strong> su <strong>Sì</strong>. Nel campo <strong>Società cliente</strong>, seleziona il record del cliente creato nel passaggio A. |


2. Fai cli su **Gestione progetti e contabilità** &gt; **Imposta** &gt; **Parametri Gestione progetti e contabilità**, quindi fai clic sulla scheda **Interaziendale**. Il modo in cui configuri i parametri dipende dal fatto che tu sia la persona giuridica mutuataria o la persona giuridica mutuante.
   -   Se sei la persona giuridica mutuataria, seleziona la categoria di approvvigionamento da utilizzare per abbinare le fatture fornitore, che vengono generate automaticamente.
   -   Se sei la persona giuridica mutuante, per ciascuna persona giuridica mutuataria, seleziona una categoria di progetto predefinita per ogni tipo di transazione. Le categorie di progetto vengono utilizzate per la configurazione fiscale quando la categoria fatturata nelle transazioni interaziendali esiste solo nella persona giuridica mutuataria. Puoi scegliere di maturare ricavi per le transazioni interaziendali. Questo accantonamento viene effettuato quando le transazioni vengono registrate e viene quindi stornato quando viene registrata la fattura interaziendale.

3. Fai clic su **Gestione progetti e contabilità** &gt; **Imposta** &gt; **Prezzi** &gt; **Prezzo di trasferimento**.
4. Seleziona una valuta, un tipo di transazione e un modello di prezzo di trasferimento. La valuta utilizzata nella fattura è la valuta configurata nel record del cliente per la persona giuridica mutuataria nella persona giuridica mutuante. La valuta viene utilizzata per abbinare le voci nella tabella dei prezzi di trasferimento.
5. Fai clic su **Contabilità generale** &gt; **Impostazione di registrazione** &gt; **Contabilità interaziendale** e configura una relazione per USSI e FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Esempio 2: creare e registrare un foglio presenze interaziendale
USSI, la persona giuridica mutuante, deve creare e registrare il foglio presenze per un progetto da FRSI, la persona giuridica mutuataria. Esistono due punti di ingresso per i passaggi necessari per questa attività.

| Passaggio | Punto di accesso                                                                       | Descrizione                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Gestione progetti e contabilità** &gt; **Fogli presenze** &gt; **Tutti i fogli presenze** | Crea un nuovo foglio presenze. Nella riga del foglio presenze, nel campo **Persona giuridica**, seleziona **FRSI**. Nel campo **ID progetto**, seleziona il progetto in FRSI. Immetti le ore per ogni giorno della settimana. |
| G    | Pagina **Foglio presenze**                                                                | Al termine del flusso di lavoro, registra il foglio presenze e prendi nota del numero del giustificativo.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Esempio 3: creare e registrare una fattura fornitore interaziendale
USSI, la persona giuridica mutuante, deve creare e registrare la fattura fornitore interaziendale per un progetto da FRSI, la persona giuridica mutuataria. Questa fattura fornitore rappresenta la manodopera e le spese esternalizzate eseguite dai fornitori pagati da USSI. Esistono due punti di ingresso per i passaggi necessari per questa attività.

| Passaggio | Punto di accesso                                                                                      | Descrizione                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Contabilità fornitori** &gt; **Fatture** &gt; **Fatture fornitore aperte** &gt; **Nuova fattura fornitore** | Crea una nuova fattura fornitore e immetti i servizi che sono stati acquistati per conto del progetto FRSI.                                                                                                                                                                                  |
| G    | Pagina **Fattura fornitore**                                                                      | Immetti le righe che rappresentano i servizi esternalizzati per conto di FRSI. Nella Scheda dettaglio **Dettagli riga**, nella scheda **Progetto** per la riga fattura, nel campo **Società di progetto**, inserisci **FRSI**. Immetti il progetto e le informazioni corrispondenti. Quindi registra la la fattura fornitore. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Esempio 4: creare e registrare la fattura interaziendale
USSI, la persona giuridica mutuante, deve creare e registrare la fattura interaziendale. Esistono due punti di ingresso per i passaggi necessari per questa attività.

| Passaggio | Punto di accesso                                                                                             | Descrizione                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Gestione progetti e contabilità** &gt; **Fatture di progetto** &gt; **Fattura cliente interaziendale**  | Fai clic su **Nuovo** per aprire la pagina **Crea fattura interaziendale**.                                                                                  |
| G    | **Gestione progetti e contabilità** &gt; **Fatture di progetto** &gt; **Fatture cliente interaziendale** | Nella pagina **Crea fattura interaziendale**, immetti la persona giuridica, specifica la transazione da includere, quindi fai clic su **Cerca**. |
| C    | **Gestione progetti e contabilità** &gt; **Fatture di progetto** &gt; **Fatture cliente interaziendale** | Seleziona le transazioni da fatturare o fai clic su **Seleziona tutto** per fatturare tutte le transazioni nell'elenco, quindi fai clic su **OK**.                  |
| D    | Pagina **Fattura interaziendale**                                                                       | Viene visualizzata la proposta di fattura cliente interaziendale.                                                                                             |
| E    | Pagina **Fattura interaziendale**                                                                       | Fai clic su **Post**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Esempio 5: registrare la fattura fornitore e fatturare al cliente
Quando la persona giuridica mutuante, USSI, registra la fattura cliente interaziendale, viene creata una fattura fornitore in sospeso corrispondente nella persona giuridica mutuataria, FRSI. Dopo che questa fattura fornitore viene registrata, FRSI fattura anche al cliente del progetto le ore immesse da USSI. Esistono tre punti di ingresso per i passaggi necessari per questa attività.

| Passaggio | Punto di accesso                                                                                        | Descrizione                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Contabilità fornitori** &gt; **Fatture** &gt; **Fatture fornitore in sospeso**                            | Rivedi la fattura per verificare che i valori del foglio presenze siano inclusi e quindi registra la fattura fornitore.                  |
| G    | **Gestione progetti e contabilità** &gt; **Fatture di progetto** &gt; **Proposte fattura progeto** | Crea una nuova fattura di progetto per il progetto e verifica che vengano visualizzate le transazioni orarie registrate.            |
| C    | Pagina **Fattura di progetto**                                                                       | Seleziona la fattura del progetto, quindi fai clic su **Visualizza dettagli** per rivedere il costo e l'importo delle vendite. Quindi registra la la fattura. |


Per altre informazioni, vedi [Configurare la fatturazione del progetto interaziendale](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]