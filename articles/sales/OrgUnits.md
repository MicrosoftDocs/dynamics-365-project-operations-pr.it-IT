---
title: Unità organizzative
description: Questo articolo descrive il concetto di unità organizzative e spiega come creare e gestire le unità organizzative in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921629"
---
# <a name="organizational-units-overview"></a>Panoramica delle unità organizzative

In Microsoft Dynamics 365 Project Operations, un'*unità organizzativa* è una divisione o un gruppo distinto di un'azienda di servizi professionali che impiega risorse fatturabili che hanno tassi di costo.

Per le società di servizi professionali che impiegano risorse tecniche in diverse aree o settori di attività, il costo per ricoprire un ruolo potrebbe variare a seconda dell'area o settore di attività in cui il ruolo viene ricoperto. In questo scenario, il concetto di unità organizzative è utile in quanto fornisce un modo di raggruppare un set di ruoli fatturabili in una divisione di un'azienda che ha una struttura di costi distinta per questi ruoli.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Il concetto di unità organizzative in Project Operations

In Project Operations, un'unità organizzativa ha una valuta specifica e listini prezzi di costo specifici.

La valuta di un'unità organizzativa è la valuta primaria utilizzata per tenere traccia dei costi.

Uno o più listini prezzi di costo possono essere associati a ogni unità organizzativa. Project Operations applica le seguenti limitazioni ai listini prezzi che è possibile associare a un'unità organizzativa:

- I listini prezzi devono essere nella valuta dell'unità organizzativa.
- I listini prezzi devono essere listini prezzi di costo.

Inoltre, è incluso un attributo per l'unità organizzativa nell'entità Risorsa. Ogni risorsa può essere assegnato a un'unità organizzativa.

### <a name="roles-of-organizational-units"></a>Ruoli delle unità organizzative

L'unità organizzativa svolge due ruoli in Project Operations:

- **Unità contratto** - L'unità organizzativa che rappresenta la divisione o gruppo dell'azienda che è il responsabile principale dell'acquisizione della vendita e della gestione della fornitura del lavoro e dei servizi al cliente. L'unità contratto è identificata dal campo **Unità contratto** nella sezione dell'intestazione delle pagine **Opportunità**, **Offerta**, **Contratto di progetto** e **Progetto**.
- **Unità gestione risorse** - L'unità organizzativa a cui una risorsa appartiene o è assegnata. Questa unità organizzativa può fornire le proprie risorse per alcuni ruoli nelle descrizioni dei lavori e nei progetti di proprietà dell'unità contratto.

![Unità contratto e unità di gestione risorse.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Domande frequenti sull'unità organizzativa

Di seguito sono riportate alcune delle domande più frequenti sulle unità organizzative:

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Qual è la correlazione tra l'entità Unità organizzativa in Project Operations e l'entità Organizzazione già esistente in Dynamics 365?

L'entità Organizzazione in Dynamics 365 rappresenta il nome dell'istanza globale di Dynamics 365. Questo nome è in genere il nome dell'azienda globale.

L'entità Unità organizzativa rappresenta un gruppo o una divisione dell'azienda globale. Questo gruppo o divisione ha un set di ruoli e un listino prezzi di costo per tali ruoli e questi ruoli e il listino prezzi differiscono da ruoli e listino prezzi di altri gruppi o divisioni dell'azienda.

Quando si installa Project Operations, un'unità organizzativa predefinita viene creata in base all'organizzazione. Tutte le risorse esistenti vengono assegnate all'unità organizzativa predefinito. Se nuovi utenti o risorse di Active Directory sono importati in Dynamics 365, il processo di importazione utenti li assegna all'unità organizzativa predefinita in Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Quali sono le differenze tra l'entità Unità organizzativa e l'entità Business Unit?

In Dynamics 365, l'entità Business Unit è un costrutto di sicurezza. L'associazione di un utente con una Business Unit determina le entità e i record di entità a cui l'utente ha accesso. Determina inoltre le autorizzazioni (creazione, lettura, scrittura, eliminazione, aggiunta, aggiunta a, assegnazione o condivisione) che l'utente ha per tali record di entità.

L'entità Unità organizzativa rappresenta un gruppo o una divisione di un'azienda che ha tassi di costo distinti per i dipendenti ad esso assegnati. L'associazione di una risorsa e un'unità organizzativa determina il costo della risorsa per un impegno di progetto.

Quando implementi Dynamics 365, ottimizza l'autorizzazione di sicurezza per la gerarchia delle business unit e l'assegnazione degli utenti alle business unit. Assegna tutti gli utenti che devono in genere accedere allo stesso set di record alla stessa business unit. L'unità organizzativa non influisce sull'accesso o sull'autorizzazione di sicurezza.

**Esempio che mostra una potenziale differenza nella modellazione di unità organizzative e business unit**

Contoso, Ltd, ha un florida attività in materia di tecnologia Microsoft. Alfonso e Lina sono entrambi sviluppatori di C\#, ma è Lina è negli Stati Uniti mentre Alfonso è in India. La maggior parte degli impegni di progetto richiede risorse di Contoso India e Contoso US e Alfonso e Lina richiedono lo stesso livello di accesso di sicurezza ai progetti in questo settore. Tuttavia, il costo degli sviluppatori di Contoso India differisce in modo significativo dal costo degli sviluppatori di Contoso US.

Di seguito è descritto un modo ottimale di progettare tale scenario utilizzando Dynamics 365 e Project Operations.

1. Crea il settore inerente alla tecnologia Microsoft come business unit e associa Alfonso e Lina a tale unità. In questo modo, hai la garanzia che entrambi i dipendenti hanno lo stesso livello di accesso di sicurezza a tutti i progetti in quel settore. Entrambi potranno controllare l'avanzamento del progetto e generare report su tempistica, utilizzo del materiale, spese e aggiornamenti delle attività.
2. Crea due unità organizzative per garantire che il costo del progetto venga riflesso correttamente.
3. Associa Lina a Contoso US e Alfonso a Contoso India.
4. Assegna i listini prezzi di costo appropriati a entrambe le unità organizzative. In questo modo, hai la garanzia che i costi registrati per Alfonso e Lina rispecchino accuratamente la differenza nei costi tra Contoso US e Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Le unità organizzative sono correlate alle aree di vendita in Dynamics 365?

Non vi è alcuna associazione o relazione tra le aree di vendita e le unità organizzative. Un'area di vendita è in genere un'area geografica in cui avviene la vendita. Un listino prezzi di vendita può essere associato a ogni area di vendita.

Un'unità organizzativa è una divisione o un gruppo interno di un'azienda che tiene traccia dei costi per un set di ruoli che vende ad altre divisioni o a clienti esterni.

**Esempio che mostra una potenziale differenza nella modellazione di unità organizzative e aree di vendita**

Contoso, Ltd. ha due centri di sviluppo: Contoso US e Contoso India. I costi delle risorse differiscono notevolmente tra questi due centri di sviluppo. Contoso vende servizi IT in molti mercati internazionali, ad esempio America Latina, Nord America, Asia Pacifico, Europa occidentale e Medio Oriente. I tassi di fatturazione per gli stessi ruoli di progetto possono variare ampiamente tra questi mercati. Contoso US e Contoso India devono essere configurati come unità organizzative e ognuna deve avere il proprio listino prezzi di costo. Asia Pacifico, America Latina, Nord America, Europa occidentale e Medio Oriente devono essere configurati come aree di vendita e ognuna deve avere il proprio listino prezzi di vendita.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Perché esiste una restrizione in relazione all'associazione dei listini prezzi alle unità organizzative?

I prezzi di vendita sono in genere univoci nelle aree geografiche o nei mercati in cui i servizi vengono venduti. Le divisioni interne di una società non hanno in genere un proprio prezzo di vendita per lo stesso tipo di servizi. Tuttavia, le divisioni interne hanno un costo del venduto differente, a seconda delle competenze delle persone che impiegano e della condizioni di lavoro dell'area geografica in cui operano. Poiché le unità organizzative sono organizzate come divisioni interne di un'azienda, possono avere solo listini prezzi di costo.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Perché non è possibile associare listini prezzi di vendita a unità organizzative?

In Project Operations, i listini prezzi di vendita possono essere associati a clienti e aree di vendita. Le entità transazionali come Opportunità, Offerta, Contratto di progetto e Progetto utilizzano listini prezzi di vendita associati all'account del cliente o all'area di vendita per determinare i tassi di fatturazione e i ricavi potenziali relativi all'impegno di progetto.

I listini prezzi di costo sono associati alle unità organizzative. Le entità transazionali come Opportunità, Offerta, Contratto di progetto e Progetto utilizzano listini prezzi di costo associati all'unità contratto per determinare i costi relativi all'impegno di progetto.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Le unità organizzative sono gerarchiche in Project Operations?

Nr. Nella versione corrente di Project Operations, le unità organizzative non sono gerarchiche. Pertanto non è possibile eseguire queste attività:

- Configurare un modello per impostare come predefiniti i prezzi di costo che attraversano la gerarchia.
- Generare report sui ricavi o sul costo di cui è stato eseguito il rollup a diversi livelli della gerarchia dell'unità organizzativa.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Siamo una grande azienda multinazionale che ha una gerarchia complessa e multilivello di centri di costo, divisioni e uffici di fatturazione. Come possiamo utilizzare al meglio il concetto di unità organizzativa nella versione corrente di Project Operations?

Quando è presente una gerarchia complete di centri di costo, divisioni, uffici di fatturazione e così via, i nodi foglia di quella gerarchia devono essere configurati come unità organizzative distinte.

Nell'esempio seguente è illustrata una gerarchia tipica.

**Contoso India**

- Settore SAP

    - Consulenti tecnici
    - Consulenti funzionali

- Settore tecnologia Microsoft

    - Consulenti tecnici
    - Consulenti funzionali

**Contoso US**

- Settore SAP

    - Consulenti tecnici
    - Consulenti funzionali

- Settore tecnologia Microsoft

    - Consulenti tecnici
    - Consulenti funzionali

Se la gerarchia è simile a quella dell'esempio, è necessario configurarla come elenco semplice, come illustrato di seguito:

- Contoso India - Settore SAP - Consulenti tecnici
- Contoso India - Settore SAP - Consulenti funzionali
- Contoso India - Settore tecnologia Microsoft - Consulenti funzionali
- Contoso India - Settore tecnologia Microsoft - Consulenti funzionali
- Contoso US - Settore SAP - Consulenti tecnici
- Contoso US - Settore SAP - Consulenti funzionali
- Contoso US - Settore tecnologia Microsoft - Consulenti tecnici
- Contoso US - Settore tecnologia Microsoft - Consulenti funzionali

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Siamo una piccola azienda di servizi professionali che opera come un'unica divisione. Come possiamo utilizzare al meglio il concetto di unità organizzativa nella versione corrente di Project Operations?

Se l'azienda opera come un'unica unità che ha un listino prezzi di costo, non è necessario configurare alcune unità organizzativa. Durante l'installazione di Project Operations, crea un'unità organizzativa predefinita che ha lo stesso nome dell'organizzazione. Per impostazione predefinita, tutti gli utenti sono assegnati a questa unità organizzativa. Ogni volta che il sistema richiede la selezione di un'unità organizzativa, questa unità organizzativa viene selezionata per impostazione predefinita.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Quando un progetto viene creato a partire da un'offerta o una voce di contratto di progetto, l'unità contratto predefinita viene generata dall'offerta o dal contratto di progetto. Qual è l'unità contratto predefinita se un progetto viene creato prima delle entità di vendita come Offerta o Contratto di progetto?

Quando un progetto viene creato in modo autonomo, l'unità contratto predefinita del progetto è basata sull'utente che l'ha creata. Quell'utente è anche il responsabile di progetto predefinito. Se il progetto viene mappato a un'entità di vendita ad esempio un'offerta o un contratto di progetto, l'unità contratto bozza del progetto è invece basata sull'entità di vendita. In questo caso, le stime di progetto potrebbero essere ricalcolate, in quanto il listino prezzi di costo viene utilizzato per calcolare le modifiche alla stima di costo se l'unità contratto viene modificata. Il listino prezzi di vendita è utilizzato per calcolare le stime di vendita che verranno modificate di modo che siano sincronizzate con il listino prezzi di progetto dell'offerta.

I campi **Unità contratto** e **Valuta** del progetto vengono bloccati per la modifica, in quanto devono essere sincronizzati con i valori dell'entità di vendita (offerta o contratto di progetto) a cui il progetto viene mappato.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Creare e gestire unità organizzative in Project Operations

Segui la seguente procedura per creare un'unità organizzativa in Project Operations.

1. Vai in **Impostazioni \> Unità organizzative**.
2. Selezionare **Nuovo**.
3. Nell'area **Generale** inserisci un nome per l'unità organizzativa nel campo **Nome**. Quindi imposta gli altri campi come richiesto.
4. Seleziona **Salva** per creare il record e poter continuare a modificarlo.
5. In **Listini prezzi**, seleziona il segno più (**+**) per aggiungere un listino prezzi. Puoi solo aggiungere listini prezzi con il contesto **Costo** di seguito.
6. Nel campo **Nome** seleziona il pulsante **Cerca** e seleziona un listino prezzi che desideri rendere disponibile in questa unità organizzativa. Continua ad aggiungere i listini prezzi in base alle esigenze.
7. Una volta terminata l'aggiunta di listini prezzi, seleziona **Salva** nell'angolo inferiore destro della pagina.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
