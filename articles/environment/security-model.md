---
title: Modello di sicurezza
description: Questo argomento fornisce informazioni sul modello di sicurezza in Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8acaa86dec8ebca8f9850877d345e30be3e3a919
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951214"
---
# <a name="security-model"></a>Modello di sicurezza

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations contiene un modello di sicurezza unico che consente un modello di sicurezza aziendale basato sui ruoli che collabora con i gruppi di Microsoft Office. 


## <a name="security-roles"></a>Ruoli di sicurezza
Le funzionalità front-end di Project Operations includono i seguenti ruoli:

| Ruolo                          | Descrizione                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Responsabile operativo              | Supporta la creazione di report tra progetti.                                                                                                            | Business Unit              |
| Responsabile approvazione di progetto              | Approva tempistica e spese per un progetto.                                                                                                                              | Business Unit |
| Amministratore fatturazione di progetto | Crea la proposta di fatturazione.                                                                                                                                                 | Business Unit |
| Responsabile di progetto               | Crea il piano di progetto e richiede risorse.                                                                                                                              | Business Unit |
| Risorsa di progetto              | Membri del team che possono essere prenotati e registrare il tempo.                                                                                                          | Business Unit|
| Responsabile delle risorse              | Tutte le funzioni di gestione delle risorse, come soddisfare le richieste di risorse e le prenotazioni, sono separate per supportare una configurazione ibrida di responsabile di progetto + responsabile delle risorse e un ruolo di responsabile delle risorse unico e centralizzato. | Business Unit |


Microsoft Project per il Web include i ruoli seguenti:

| Ruolo           | Descrizione                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Utente di Project   | Utente collaborativo di Project che è in grado di creare i propri progetti e visualizzare eventuali progetti condivisi. | Utente   |
| Sistema di Project | Ruolo utilizzato per il contesto dell'applicazione. I clienti non dovrebbero utilizzare questo ruolo di sistema.                                    | Generale |

## <a name="security-enforcement"></a>Applicazione della sicurezza
Le azioni eseguite a livello di progetto vengono eseguite nel contesto dell'utente connesso. Ciò significa che per creare, aprire o eliminare un progetto, l'utente deve avere accesso disponibile in CDS. L'accesso in CDS può essere concesso attraverso uno qualsiasi dei possibili meccanismi inclusi nella piattaforma. Ad esempio, un utente con un ambito più ampio può accedere al progetto o se è stata eseguita un'azione esplicita di condivisione del progetto che concede l'accesso all'utente.

È importante tenerne conto quando si creano progetti in Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Moderna collaborazione di gruppo con Project Operations
Project per il Web e Project Operations supportano i gruppi moderni per la collaborazione. Gli utenti aggiunti al progetto tramite un gruppo possono modificare il piano del progetto.

Project per il Web aggiunge automaticamente gli utenti al gruppo al momento dell'assegnazione.

I gruppi consentono di lavorare in modo collaborativo sulle autorizzazioni del progetto e sugli elementi di collaborazione di supporto. Il diagramma seguente illustra gli eventi e i cambiamenti di stato che si verificano durante il processo di assegnazione del gruppo.

Project Operations non crea un gruppo tramite un'azione implicita, ma solo tramite l'azione esplicita di selezione dei gruppi.

La ricerca dei membri del gruppo nella finestra di dialogo **Gestione gruppo** è limitata a coloro che sono impostati come parte del gruppo di sicurezza dell'ambiente. Per ulteriori informazioni, vedi [Controllo accesso utente agli ambienti: gruppi di sicurezza e licenze](/power-platform/admin/control-user-access).

![Modalità gruppo](./media/groupsmode.png)

1. Il progetto è creato ed è di proprietà dell'utente che lo crea.
2. Il proprietario del progetto viene aggiornato nel team.
3. Il team del proprietario viene mappato al gruppo di Office specificato o creato.
4. Il proprietario originale del progetto viene aggiunto al gruppo di Office.

## <a name="deployment-recommendation"></a>Consigli per la distribuzione
Man mano che il modello di collaborazione del gruppo di Office si evolve, verranno aggiunte funzionalità per fornire un controllo più dettagliato nel tempo. Si consiglia ai clienti che distribuiscono Project Operations oggi di concentrarsi su un modello di sicurezza di Microsoft Dynamics 365 tradizionale.

Per ulteriori informazioni, vedi [Sicurezza in Common Data Service](/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Sicurezza di Project Operations e Microsoft Dynamics 365 Finance
Project Operations include i seguenti ruoli:

- Responsabile di progetto
- Contabile di progetto

Per ulteriori informazioni sulla sicurezza in Finance, vedi [Sicurezza basata sui ruoli](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]