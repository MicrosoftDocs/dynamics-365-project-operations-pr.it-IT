---
title: Novità o modifiche nella versione di aggiornamento 22 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 22 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078824"
---
# <a name="project-service-automation-update-release-22-v3"></a>Versione di aggiornamento di Project Service Automation 22, V3

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 22 di Project Service Automation V3. Questa versione ha il numero di build V 3.10.33.48 ed è generalmente disponibile tramite un aggiornamento automatico a giugno 2020.

## <a name="update-release-22"></a>Rilascio 22 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug



**Tempo e spesa**

Sono stati risolti i seguenti problemi:

- Gli **inserimenti ore** non vengono aggiunti automaticamente nella pianificazione inserimenti ore dopo l'importazione.
- Il selettore della data della griglia **Inserimento ore** non riconosce le impostazioni internazionali dell'utente.

**Gestione risorse**

Sono stati risolti i seguenti problemi:

- In modalità manuale, le modifiche ai contorni di **Assegnazione risorse** non vengono riconosciute durante la generazione di **Requisiti di risorse**.
- Le **richieste di risorse** non supportano gli stati delle richieste personalizzati.

**Gestione progetti**

Sono stati risolti i seguenti problemi:

- L'utilizzo del doppio clic su ForecastGridControl non analizza correttamente i numeri del formato olandese.
- Le ore assegnate non vengono aggiornate correttamente quando le assegnazioni vengono modificate utilizzando il componente aggiuntivo del client desktop Microsoft Project.
- Le griglie Registrazione di progetto e Stime visualizzano un codice valuta di vendita errato quando la valuta del contratto è diversa dalla valuta del cliente e l'organizzazione è configurata per visualizzare i codici di valuta invece dei simboli di valuta.
- La data di fine di un membro del team aggiunge un giorno se la pianificazione dell'orario di lavoro è di 24 ore al giorno.
- Nella pianificazione del progetto, l'aggiunta di una categoria di transazione a un'attività non attiva il salvataggio automatico.
- Quando si aggiunge un membro del team al modello di progetto, viene visualizzato il seguente errore: "I requisiti di risorsa non possono essere associati a modelli di progetto". 
- Lo script della regola della barra multifunzione "msdyn.Approval.CanApproveOrReject" visualizza un errore di timeout.

**Sales**

Sono stati risolti i seguenti problemi:

- Messaggio di errore di convalida non visualizzato quando si seleziona un listino prezzi di costo nella ricerca Listino prezzi nel modulo/entità "Nuovo listino prezzi progetto offerta".
- La chiusura dell'offerta come vinta non consente di accedere al contratto creato se un processo aziendale collegato all'offerta è nella fase finale.
- Lo storno delle **vendite non fatturate** è collegato al costo originale quando viene richiamato un inserimento di ore.
- Dopo aver selezionato il pulsante **Conferma** lo stato della fattura non cambia in **Confermato** a meno che la fattura non venga aggiornata.