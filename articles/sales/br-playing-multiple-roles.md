---
title: Stima le vendite e i costi del progetto quando una risorsa prenotabile ricopre più ruoli in un progetto
description: Questo argomento spiega come utilizzare le dimensioni dei prezzi per supportare le stime dei prezzi e dei costi per una risorsa che ricopre più ruoli in un progetto.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7ef9765b7db1c6650fb0599bf5fb4b4b6304be69
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013671"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Stima le vendite e i costi del progetto quando una risorsa prenotabile ricopre più ruoli in un progetto 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, distribuzione semplice: transazioni di fatturazione proforma e Project Operations per scenari di materiali stoccati basati sulla produzione_ 

Le aziende basate su progetti hanno spesso la necessità di una risorsa che ricopra più ruoli in un progetto. Ogni ruolo può avere un prezzo e un costo diverso. Ciò significa che il tempo della stessa risorsa su un progetto potrebbe ottenere una stima finanziaria diversa a seconda del tasso di fatturazione e di costo per ciascun ruolo. È possibile impostare i valori sul record del membro del team per la risorsa denominata con sostituzioni diverse su ciascuna delle attività a cui è assegnato il membro del team.

L'esempio seguente illustra come la semplice sostituzione di un valore consente a una risorsa di avere più ruoli in un progetto con costi e tariffe di fatturazione diversi.

## <a name="create-tasks"></a>Creare attività
Per creare attività, è necessario aggiungere attività, nonché attività di riepilogo, dopodiché è necessario assegnare l'attività prima di aggiungere la durata dell'attività. 

### <a name="add-tasks-and-summary-tasks"></a>Aggiungi attività e attività di riepilogo
Per aggiungere un'attività, eseguire la procedura seguente.

1. Vai a **Progetti** e apri il progetto a cui desideri aggiungere le attività.
2. Selezionare **Aggiungi nuova attività**. Denominare l'attività, quindi premere **Invio**.
3. Immettere il nome di un'altra attività e premere **Invio**. Ripeti questa operazione finché non hai un elenco completo delle attività.
3. Per far rientrare le attività nell'attività **Sommario**, seleziona i tre punti verticali accanto al nome dell'attività, quindi seleziona **Converti a sottoattività**. 

  > [!TIP]
  > Per selezionare più di un'attività, selezionare un'attività, tenere premuto **CTRL**, quindi selezionare un'altra attività.
  >
  > Puoi anche scegliere **Promuovi attività secondaria** per spostare le attività dalle attività **Sommario**.

### <a name="assign-tasks"></a>Assegnazione attività

Completare i seguenti passaggi per assegnare le attività.

1. Nella colonna **Assegnato a** per un'attività, selezionare l'icona della persona.
2. Scegli un membro del team dall'elenco o inserisci del testo per cercare un nome.

### <a name="add-task-duration-and-columns"></a>Aggiungi la durata e le colonne dell'attività

Spesso è più facile iniziare a costruire il tuo progetto con la durata. Completare la procedura seguente per aggiungere la durata di un'attività.

1. Nella colonna **Durata** per un'attività, digita il numero di giorni che ritieni siano necessari per completare l'attività. Se desideri utilizzare un'unità di tempo diversa, inserisci un numero più la parola **ore**,**settimane** o **mesi**.
2. Se vuoi che la tua attività venga visualizzata come passaggio fondamentale a forma di diamante nella visualizzazione **Sequenza temporale**, nella colonna **Durata**, inserisci **0 giorni**.
3. Premere **Invio** per passare al campo **Durata** dell'attività successiva e continuare a inserire le durate.

  > [!NOTE]
  > Non puoi inserire una durata per le attività di riepilogo.

Puoi aggiungere colonne al tuo progetto per fornire maggiori dettagli. Per fare ciò, seleziona la **colonna Aggiungi**. 

Per ulteriori informazioni, vedere [Creare un progetto](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Imposta il ruolo e l'unità organizzativa per un membro generico del team di progetto
Completa i seguenti passaggi per impostare un ruolo e un'unità organizzativa per un membro generico del team.

1. Nella pagina **Attività**, selezionare la riga **Attività** per **Attività A**. 
2. In **Assegnato a**, selezionare **Aggiungi risorsa generica**. Questa operazione apre la pagina per la **creazione rapida di membri del team**.
3. Nella pagina **Creazione rapida dei membri del team** specifica gli attributi del membro del team generico che può eseguire questa attività.
4. Seleziona il ruolo e l'unità organizzativa appropriati, quindi seleziona **Salva e chiudi**. Un membro del team generico viene creato e assegnato a questa attività. 
5. Ripeti i passaggi da 1 a 4 per **Attività B**. Tuttavia,**Attività B** deve avere un ruolo e un'unità organizzativa diversi da quelli assegnati al membro generico del team **Attività A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Imposta il ruolo e l'unità organizzativa per un'attività di progetto
Completa i seguenti passaggi per impostare un ruolo e un'unità organizzativa per un'attività.

1. Dopo aver creato **Attività A**, seleziona l'attività, quindi seleziona l'icona **i** per aprire il riquadro **Dettagli attività**. 
2. Nel riquadro **Dettagli attività**, scorrere fino in fondo e selezionare **Visualizza dettagli** per aprire la pagina **Dettagli attività**.
3. Nella pagina **Dettagli attività**, in **Ruolo** e **Unità organizzativa**, aggiungi i valori richiesti per eseguire questa attività per la risorsa. 

  > [!NOTE]
  > Se completi questo scenario utilizzando i dati dimostrativi di Project Operations, seleziona **Responsabile della consulenza** come ruolo e **Fabrikam US** come unità organizzativa.

4. Seleziona **Attività B**, quindi seleziona l'attività.
5. Seleziona l'icona **i** per aprire il riquadro **Dettagli attività**. 
6. Nel riquadro **Dettagli attività**, scorrere fino in fondo e selezionare **Visualizza dettagli** per aprire la pagina **Dettagli attività**.
7. Nella pagina **Dettagli attività**, in **Ruolo** e **Unità organizzativa**, aggiungi i valori richiesti da una risorsa che deve eseguire questa attività. I valori in **Ruolo** e **Unità organizzativa** per **Attività B** devono essere diversi da quelli per **Attività A**. 

  > [!NOTE]
  > Se completi questo scenario utilizzando i dati dimostrativi di Project Operations, seleziona **Tecnico di rete** come ruolo e **Fabrikam US** come unità organizzativa.

8. Salva e chiudi la pagina **Dettagli attività**. 

## <a name="team-member-and-estimates-behavior"></a>Membro del team e stima del comportamento 
Per capire il comportamento sulla griglia **Membro del team** e le stime, completare i seguenti passaggi.

1. Nella griglia **Membro del team**, seleziona i due membri generici del team, quindi seleziona **Genera requisiti**. Vengono generati i requisiti della risorsa. 
2. Seleziona la riga del membro del team per **Consulting Lead** e poi seleziona **Prenota**. La scheda di pianificazione si apre con un elenco di risorse. Seleziona una risorsa e quindi seleziona **Prenota** per prenotare la risorsa a tale requisito.
3. Seleziona la riga del membro del team per **Tecnico di rete** e poi seleziona **Prenota**. La scheda di pianificazione si apre con un elenco di risorse. Seleziona la stessa risorsa come sopra e quindi seleziona **Prenota** per prenotare la risorsa per tale requisito.

### <a name="team-member-grid"></a>Griglia del membro del team 

Nella griglia **Membro del team**, i due record generici dei membri del team vengono eliminati e sostituiti con una sola risorsa. Esiste un insieme di valori per quella risorsa, un insieme di valori predefinito per **Ruolo** e **Unità organizzativa**.

Quando espandi la riga per quel record del membro del team, puoi vedere assegnazioni distinte sul record del membro del team per entrambe le attività. Ogni riga di assegnazione ha valori specifici dell'attività per **Ruolo** e **Unità organizzativa**. 

### <a name="estimates-grid"></a>Griglia delle stime 

Nella griglia **Stime**, entrambe le assegnazioni per la stessa risorsa hanno un prezzo diverso. Il prezzo dell'assegnazione per la risorsa nell'**Attività A** viene calcolato utilizzando il valore dell'attributo **Ruolo** di **Consulting Lead**. Il prezzo dell'assegnazione per la stessa risorsa nell' **Attività B** viene calcolato utilizzando il valore dell'attributo **Ruolo** di **Tecnico di rete**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]