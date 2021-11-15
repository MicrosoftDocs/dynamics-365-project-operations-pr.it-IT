---
title: Prestazioni dell'API di pianificazione del progetto
description: Questo argomento fornisce informazioni sui benchmark delle prestazioni delle API di pianificazione del progetto e identifica le procedure consigliate per l'utilizzo ottimale.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a1abadbae044ccbd40077c6937262f0f17387bad
ms.sourcegitcommit: 5c536cf05e2cbfc1d15982e4695d726064a074da
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2021
ms.locfileid: "7750607"
---
# <a name="project-schedule-api-performance"></a>Prestazioni dell'API di pianificazione del progetto

_**Si applica a:** Project Operations per scenari basati su articoli non stoccati/risorse e Distribuzione semplice: dalla transazione alla fatturazione proforma, Project for the Web_

Questo argomento fornisce informazioni sui benchmark delle prestazioni delle API di pianificazione del progetto e identifica le procedure consigliate per l'utilizzo ottimale.

## <a name="project-scheduling-service"></a>Servizio di pianificazione del progetto
Il servizio di pianificazione del progetto è un servizio multi-tenant che viene eseguito in Microsoft Azure. È progettato per migliorare l'interazione fornendo un'esperienza rapida e fluida quando gli utenti lavorano ai progetti. Questo miglioramento si ottiene accettando le richieste di modifica, elaborandole e quindi restituendo immediatamente il risultato. Il servizio persiste in modo asincrono in Dataverse e non impedisce agli utenti di eseguire altre operazioni.

Le API di pianificazione del progetto si basano sul servizio di pianificazione del progetto per eseguire le richieste descritte in maggior dettaglio nelle sezioni successive di questo argomento.

Le API di pianificazione del progetto sono progettate per funzionare con le seguenti entità della struttura di suddivisione del lavoro:

  - Project
  - Attività di progetto
  - Dipendenza attività di progetto
  - Membro del team di progetto
  - Assegnazione risorse
  
Sono supportati sia i campi predefiniti che i campi personalizzati. Se non diversamente specificato, sono supportate tutte le operazioni comuni, come la creazione, l'aggiornamento e l'eliminazione. Per ulteriori informazioni, vedi [Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione](schedule-api-preview.md).

Come parte delle API di pianificazione del progetto, è stato aggiunto un modello di unità di lavoro. Questo modello è noto come OperationSet e può essere utilizzato quando è necessario elaborare più richieste in un'unica transazione.

L'illustrazione seguente mostra il flusso che sperimenta un partner quando viene utilizzata questa funzionalità.

![Dataverse e il flusso del servizio di pianificazione del progetto.](./media/dataverse-project-scheduling-service-flow.png)

**Passaggio 1**: un client effettua una chiamata API a un endpoint Open Data Protocol (OData) in Dataverse per creare un OperationSet.

**Passaggio 2**: dopo la creazione del nuovo OperationSet, il valore **OperationSetId** viene restituito.

**Passaggio 3**: il client utilizza il valore **OperationSetId** per effettuare un'altra richiesta API di pianificazione del progetto. Il risultato è una richiesta di creazione, aggiornamento o eliminazione su un'entità di pianificazione. Quando viene effettuata questa richiesta, viene eseguita la convalida dei metadati. Se la convalida non riesce, la richiesta viene terminata e viene restituito un errore.

**Passaggi 4a–4c**: questi passaggi rappresentano la fase di ACCETTAZIONE. Il cliente chiama l'API **ExecuteOperationSetV1**, che invia tutte le modifiche al servizio di pianificazione del progetto in un batch. Il servizio di pianificazione del progetto esegue le convalide sulle richieste nel batch. Eventuali errori di convalida annullano il batch e restituiscono un'eccezione al chiamante. Se il batch viene accettato correttamente dal servizio di pianificazione del progetto, lo stato dell'OperationSet viene aggiornato per riflettere il fatto che l'OperationSet viene elaborato dal servizio di pianificazione del progetto.

**Passaggio 5**: Questo passaggio rappresenta la fase di PERSISTENZA. Il servizio di pianificazione del progetto scrive in modo asincrono il batch su Dataverse in una transazione. Se l'operazione di scrittura ha esito positivo, OperationSet è contrassegnato come **Completato**. Eventuali errori ripristinano la transazione e il batch e OperationSet viene contrassegnato come **Non riuscito**.

## <a name="performance-methodology"></a>Metodologia delle prestazioni
Il tempo di esecuzione è definito come il tempo che intercorre tra la chiamata all'API **ExecuteOperationSetV1** fino a quando il servizio di pianificazione del progetto non ha finito di scrivere su Dataverse. Tutte le operazioni vengono eseguite per un totale di 2.200 volte e vengono riportate le misure del tempo di esecuzione di P99. Vengono misurate le operazioni a record singolo e in blocco.

Per un'operazione a record singolo, OperationSet contiene una richiesta. Per le operazioni in blocco, contiene 20, 50 o 100 richieste. Ogni dimensione del blocco è segnalata separatamente.

Queste operazioni vengono eseguite su una distribuzione UR 15 Project Operations Lite in Nord America.

## <a name="results"></a>Risultati
### <a name="create-operations"></a>Creare operazioni
#### <a name="single-record-create-operations"></a>Operazioni di creazione di record singoli
La tabella seguente mostra i tempi di esecuzione per la creazione di un singolo record. I tempi sono in secondi.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo&nbsp;di&nbsp;record&nbsp;</th>
    <th class="tg-0lax" colspan="2">Inserimento ore</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campi obbligatori</th>
    <th class="tg-0lax">Tutti i campi supportati</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Attività</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Assegnazione</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro del team</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dipendenza</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operazioni di creazione in blocco
La tabella seguente mostra i tempi di esecuzione per la creazione di molti record. Nello specifico, Microsoft ha misurato i tempi di esecuzione per la creazione di 20, 50 e 100 record in un singolo OperationSet. I tempi sono in secondi.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipo&nbsp;di&nbsp;record&nbsp;</th>
    <th class="tg-0lax" colspan="6">Inserimento ore</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 record</th>
    <th class="tg-0lax" colspan="2">50 record</th>
    <th class="tg-0lax" colspan="2">100 record</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campi obbligatori</th>
    <th class="tg-0lax">Tutti i campi supportati</th>
    <th class="tg-0lax">Campi obbligatori</th>
    <th class="tg-0lax">Tutti i campi supportati</th>
    <th class="tg-0lax">Campi obbligatori</th>
    <th class="tg-0lax">Tutti i campi supportati</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Attività</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Assegnazione</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dipendenza</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Le operazioni di creazione in blocco nelle entità **Progetto** e **Membro del team** non sono incluse in questa tabella, perché il runtime per tali operazioni è simile al runtime quando l'API per la creazione di un singolo record viene chiamata più volte. Queste API vengono eseguite immediatamente in Dataverse.

L'illustrazione seguente mostra un grafico dei tempi di esecuzione per le entità **Attività**, **Assegnazione**, e **Dipendenza** quando vengono creati 20, 50 e 100 record e vengono utilizzati tutti i campi supportati.

![Grafico del tempo di esecuzione della creazione dei record.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Operazioni di aggiornamento
#### <a name="single-record-update-operations"></a>Operazioni di aggiornamento di record singoli
La tabella seguente mostra i tempi di esecuzione per l'aggiornamento di un singolo record. I tempi sono in secondi.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo&nbsp;di&nbsp;record&nbsp;</th>
    <th class="tg-0lax" colspan="2">Inserimento ore</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campi obbligatori </th>
    <th class="tg-0lax">Tutti i campi supportati</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Attività</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro del team</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Le operazioni di aggiornamento nelle entità **Assegnazione delle risorse** e **Dipendenza attività di progetto** non sono supportate.

#### <a name="bulk-update-operations"></a>Operazioni di aggiornamento in blocco
La tabella seguente mostra i tempi di esecuzione per l'aggiornamento di molti record. Nello specifico, Microsoft ha misurato i tempi di esecuzione per l'aggiornamento di 20, 50 e 100 record in un singolo OperationSet. I tempi sono in secondi.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipo&nbsp;di&nbsp;record&nbsp;</th>
    <th class="tg-0lax" colspan="6">Inserimento ore</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 record</th>
    <th class="tg-0lax" colspan="2">50 record</th>
    <th class="tg-0lax" colspan="2">100 record</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campi obbligatori</th>
    <th class="tg-0lax">Tutti i campi supportati</th>
    <th class="tg-0lax">Campi obbligatori</th>
    <th class="tg-0lax">Tutti i campi supportati</th>
    <th class="tg-0lax">Campi obbligatori</th>
    <th class="tg-0lax">Tutti i campi supportati</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Attività</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro del team</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Le operazioni di aggiornamento nelle entità **Assegnazione delle risorse** e **Dipendenza attività di progetto** non sono supportate.

L'illustrazione seguente mostra un grafico dei tempi di esecuzione per le entità Attività e Membro del team quando vengono aggiornati 20, 50 e 100 record e vengono utilizzati tutti i campi supportati.

![Grafico del tempo di esecuzione dell'aggiornamento dei record.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operazioni di eliminazione
#### <a name="single-record-delete-operations"></a>Operazioni di eliminazione di record singoli
La tabella seguente mostra i tempi di esecuzione per l'eliminazione di un singolo record. I tempi sono in secondi.

| Tipo di record | Inserimento ore  |
|-------------|-------|
| Attività        | 20.12 |
| Assegnazione  | 10.86 |
| Membro del team | 12.52 |
| Dipendenza  | 20.89 |

> [!NOTE]
> Le operazioni di eliminazione nell'entità **Progetto** non sono supportate.

#### <a name="bulk-delete-operations"></a>Operazioni di eliminazione in blocco
La tabella seguente mostra i tempi di esecuzione per l'eliminazione di molti record. Nello specifico, Microsoft ha misurato i tempi di esecuzione per l'elimnazione di 20, 50 e 100 record in un singolo OperationSet. I tempi sono in secondi.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo&nbsp;di&nbsp;record&nbsp;</th>
    <th class="tg-0lax" colspan="3">Inserimento ore</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 record</th>
    <th class="tg-0lax">50 record</th>
    <th class="tg-0lax">100 record</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Attività</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Assegnazione</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro del team</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dipendenza</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Le operazioni di eliminazione nell'entità **Progetto** non sono supportate.

L'illustrazione seguente mostra un grafico dei tempi di esecuzione per le entità **Attività**, **Assegnazione**, **Membro del team**, e **Dipendenza** quando vengono eliminati 20, 50 e 100 record.

![Grafico del tempo di esecuzione dell'elimnazione dei record.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Osservazioni
Per ogni operazione sul record, l'API **ExecuteOperationSet** impiega circa 800 millisecondi per inviare una richiesta al servizio di pianificazione del progetto. Il servizio di pianificazione del progetto impiega quindi circa cinque secondi per elaborare il payload e chiamare Dataverse. Il resto del tempo di esecuzione viene impiegato nell'esecuzione della logica aziendale e nella scrittura dei dati nel database in Dataverse.

Quando 100 record vengono creati, aggiornati o eliminati, l'API **ExecuteOperationSet** impiega circa tre secondi per inviare la richiesta al servizio di pianificazione del progetto. Il servizio di pianificazione del progetto impiega quindi circa cinque secondi per elaborare le richieste e chiamare Dataverse. Le operazioni in blocco devono pagare un'**imposta per il servizio di pianificazione del progetto** una tantum per tutti i record in OperationSet. Pertanto, le operazioni in blocco hanno un tempo di esecuzione medio significativamente inferiore rispetto alle operazioni su record singolo.

## <a name="scenarios"></a>Scenari
La tabella seguente mostra i tempi di esecuzione quando le API di pianificazione del progetto vengono utilizzate per realizzare scenari specifici. I tempi sono in secondi.

| Scenario                                                                   | Inserimento ore  |
|----------------------------------------------------------------------------|-------|
| Crea un progetto con 40 attività.                                      | 36.01 |
| Crea un progetto con 40 attività e 20 dipendenze.                  | 38.11 |
| Crea un progetto con 40 attività e 30 assegnazioni.                   | 60.17 |
| Crea un progetto con 40 attività, 20 dipendenze e 30 assegnazioni. | 60.27 |

## <a name="best-practices"></a>Procedure consigliate
In base ai risultati dello scenario precedente, le API hanno prestazioni migliori nelle seguenti condizioni:

  - Raggruppa il maggior numero possibile di operazioni. Il tempo di esecuzione medio per le operazioni in blocco è migliore del tempo di esecuzione medio per le operazioni su record singolo. Più piccolo è il numero di OperationSet in uso, più veloce sarà il tempo medio di esecuzione.
  - Imposta solo gli attributi minimi necessari per realizzare il tuo scenario. Sii selettivo per i tipi di campi non obbligatori inclusi in una richiesta OperationSet. I campi che contengono chiavi esterne o campi di rollup influiranno negativamente sulle prestazioni.
