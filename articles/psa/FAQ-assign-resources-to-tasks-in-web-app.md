---
title: Come si assegna una risorsa prenotabile a un'attività nell'app Web
description: Una panoramica dei modi in cui è possibile assegnare risorse prenotabili.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146578"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Come si assegna una risorsa prenotabile a un'attività nell'app Web (app Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vi sono due modi per assegnare una risorsa a un'attività in Project Service. È possibile prenotare una risorsa come membro del team e quindi assegnarla a un'attività. Oppure, è possibile creare un membro del team generico mediante l'assegnazione di ruoli nelle attività, generare un team e quindi soddisfare i requisiti di supporto con una risorsa con nome.

Si noti che se si desidera assegnare una risorsa prenotabile a un'attività, il membro del team della risorsa prenotabile deve avere prenotazioni disponibili sufficienti. Il tipo di esecuzione della prenotazione deve essere Prenota definitivamente e lo stato Impegnato. Se non vi sono prenotazioni sufficienti per la risorsa, Project Service rimuove l'assegnazione e visualizza il messaggio di errore seguente:

*Impossibile assegnare la risorsa all'attività - le risorse seguenti non hanno ore prenotate sufficienti per il progetto*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Prenotare una risorsa come membro del team e quindi assegnarla a un'attività

Con questo metodo si aggiunge una risorsa al team di progetto e quindi si assegnano le attività alla risorsa nella pianificazione del progetto. Di seguito viene descritto come procedere:
1.  Nella griglia dei membri del team, aggiungere un nuovo membro del team selezionando **Nuovo**.
2.  Nella schermata per la creazione rapida di membri del team, selezionare il nome della risorsa prenotabile e impostare un ruolo.
3.  Selezionare le date **Da** e **A**.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot dell'aggiunta di un membro del team](media/FAQ-Resources-to-Tasks2-1.png "Screenshot dell'aggiunta di un membro del team")
 
4.  Selezionare uno dei seguenti metodi di allocazione per la prenotazione della risorsa:
    - **Piena capacità** prenota l'intera capacità della risorsa per le date di inizio e fine specificate.
    - **Percentuale capacità** prenota la risorsa per una percentuale della capacità della risorsa per le date di inizio e di fine specificate.
    - **Per ore - Distribuzione uniforme** prenota la risorsa per un determinato numero di ore, con una distribuzione giornaliera uniforme durante il periodo tra la data di inizio e quella di fine specificate.
    - **Per ore - Spese iniziali** prenota la risorsa per un determinato numero di ore, applicando spese iniziali alle ore giornaliere durante il periodo tra la data di inizio e quella di fine specificate.

    Non selezionare **Nessuno** in quanto aggiunge la risorsa al team ma non crea prenotazioni che assorbano la capacità della risorsa.
5.  Seleziona **Salva**.

    Si noti che le ore della prenotazione devono essere sufficienti per coprire le ore di lavoro e gli intervalli di date delle attività a cui si assegna la risorsa. Se non sono allineate, non è possibile assegnare la risorsa all'attività.

6.  Nella struttura di suddivisione del lavoro per l'attività, fare clic sull'elenco a discesa della cella della risorsa. Eseguire quindi le operazioni seguenti: 

    1. Seleziona **Aggiungi**.
    2. Selezionare l'elenco a discesa in **Risorse** e selezionare il membro del team aggiunto in precedenza.
    3. Seleziona **OK**. Il membro del team è ora assegnato all'attività.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot dell'aggiunta di risorse con la struttura di suddivisione del lavoro](media/FAQ-Resources-to-Tasks2-2.png "Screenshot dell'aggiunta di risorse con la struttura di suddivisione del lavoro")
 
Nella griglia dei membri del team, viene visualizzata l'aggregazione delle ore assegnate alla risorsa in Ore assegnate. È inferiore o uguale alle ore prenotate per la risorsa. 

> [!div class="mx-imgBorder"] 
> ![Screenshot delle ore assegnate per una risorsa](media/FAQ-Resources-to-Tasks2-3.png "Screenshot delle ore assegnate per una risorsa")
 
Se l'attività che si tenta di assegnare alla risorsa inizia dopo la data di fine delle prenotazioni delle risorse, la risorsa non sarà visualizzata nell'elenco a discesa.

Da notare che è possibile assegnare una risorsa a un numero di ore maggiore delle relative ore prenotate se la risorsa ha della capacità non assegnata. In questo caso, la risorsa sarà assegnata solo parzialmente in base alle relative prenotazioni. È possibile visualizzare queste ore di attività non assegnate aggiungendo la colonna Ore senza personale alla struttura di suddivisione del lavoro.

Se le risorse sono assegnate alle relative ore prenotate (uguali alle relative ore assegnate), verrà visualizzato il messaggio di errore seguente quando si tenta di assegnare ulteriori attività:

*Impossibile assegnare la risorsa all'attività - le risorse seguenti non hanno ore prenotate sufficienti per il progetto.*

Inoltre, il membro del team responsabile di progetto predefinito che viene aggiunto al team quando si crea il progetto viene aggiunto senza prenotazioni e non può essere assegnato ad alcuna attività. Non sarà quindi visualizzato nell'elenco a discesa per le attività.

Per assegnare questa risorsa, è necessario rimuoverla dal team e aggiungerla nuovamente con un metodo di allocazione diverso da Nessuno. Il motivo per cui viene aggiunta al team alla creazione del progetto è che in questo modo un progetto ha almeno un responsabile approvazione di progetto predefinito.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Creare un membro del team generico mediante l'assegnazione di ruoli nelle attività

Questo metodo assicura che le risorse hanno prenotazioni sufficienti per le attività. Innanzitutto, si crea una risorsa segnaposto o generica che descrive le caratteristiche della risorsa con nome che si desidera utilizzare per le attività generando un team dopo aver assegnato ruoli alle attività. Di seguito viene descritto come procedere:

1. Nella struttura di suddivisione del lavoro, selezionare un'attività.
2. Selezionare l'icona a discesa **Ruolo assegnato** nella cella della risorsa.
3. Selezionare l'elenco a discesa **Ruolo** e selezionare il ruolo per la risorsa generica.
4. Seleziona **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot dell'uso della struttura di suddivisione del lavoro per aggiungere una risorsa](media/FAQ-Resources-to-Tasks2-4.png "Screenshot dell'uso della struttura di suddivisione del lavoro per aggiungere una risorsa")
 
Dopo aver completato l'assegnazione dei ruoli alle attività nella struttura di suddivisione del lavoro, selezionare **Genera team di progetto**. Project Service crea il numero minimo di membri del team generici in base ai ruoli, alle unità gestione risorse dell'organizzazione e al calendario del progetto aggregando le assegnazioni delle attività.

> [!div class="mx-imgBorder"] 
> ![Screenshot della generazione del team di progetto](media/FAQ-Resources-to-Tasks2-5.png "Screenshot della generazione del team di progetto")
 
Nella griglia dei membri del team, saranno visualizzate le risorse di tipo Risorsa generica con il ruolo e il nome posizione. Se due risorse sono necessarie affinché un ruolo completi il lavoro, la funzionalità Genera team crea due membri del team e utilizza il nome posizione per distinguerli.

> [!div class="mx-imgBorder"] 
> ![Screenshot dell'aggiunta di due risorse generiche](media/FAQ-Resources-to-Tasks2-6.png "Screenshot dell'aggiunta di due risorse generiche")
 
È possibile aprire il requisito di risorsa di supporto per il membro del team generico selezionando il collegamento sotto Requisito di risorsa.

> [!div class="mx-imgBorder"] 
> ![Screenshot dell'apertura del requisito di risorsa di supporto](media/FAQ-Resources-to-Tasks2-7.png "Screenshot dell'apertura del requisito di risorsa di supporto")

Selezionare **Prenota** per la risorsa generica e utilizzare la scheda di pianificazione per trovare e prenotare una risorsa reale. È anche possibile inviare il requisito che deve essere soddisfatto da un responsabile delle risorse selezionando **Invia richiesta**.

Quando la risorsa generica viene soddisfatta con una risorsa denominata, la risorsa generica viene rimossa dal team e le assegnazioni delle attività per la risorsa generica sono assegnate alla risorsa denominata che ha soddisfatto il requisito di risorsa della risorsa generica.
 

