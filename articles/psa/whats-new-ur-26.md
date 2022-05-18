---
title: Novità o modifiche nella versione di aggiornamento 26 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 26 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: cebfcd6425f11b74ce6331a093d8d3db3da356a0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577287"
---
# <a name="project-service-automation-update-release-26-v3"></a>Versione di aggiornamento di Project Service Automation 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 26 di Project Service Automation V3. Questa versione ha un numero di build di V3.10.44.59 ed è generalmente disponibile tramite un aggiornamento automatico a dicembre 2020.

## <a name="update-release-26"></a>Rilascio 26 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Ore e spesa**

Sono stati risolti i seguenti problemi:

- Gli utenti possono modificare l'attività su una voce di tempo che è stata approvata/inviata.
- Errore "Riferimento oggetto non impostato" durante il salvataggio dell'immissione dell'ora.
- L'importazione dell'inserimento ore dalle assegnazioni di risorse crea voci di ora con i valori DateTime non corretti.
- Quando sono installate le app Project Service Automation e Field Service, il pulsante **Nuovo** viene visualizzato due volte sulla barra dei comandi per le voci di tempo nell'app Field Service.
- Gli aggiornamenti alle celle **Consenti unità** e **Gruppo unità** ora funzionano nella griglia **Stime di spesa**.
- Il modulo **Aggiorna modifica inserimento orario** include la **Sequenza temporale**.
- L'approvazione del tempo per voci di orario non di progetto blocca il sistema durante la ricerca di un ruolo di approvazione del progetto.

**Gestione risorse**

Sono stati risolti i seguenti problemi:

- Aggiunta convalida nel plugin **PostProjectCreate** per verificare un requisito principale prima di crearne uno.
- Il modulo di creazione rapida **Membro del team di progetto** genera un'eccezione di riferimento null se i campi vengono rimossi dal modulo.
- La generazione di requisiti per 12 ore su 1 anno non funzionerà.
- Migliorata l'eccezione di riferimento null del messaggio di errore durante la creazione del requisito della risorsa.

**Gestione progetti**

Sono stati risolti i seguenti problemi:

- Convalida migliorata per affrontare l'eccezione di riferimento null generata nelplugin **PreProjectUpdate**.
- I progetti pubblicati dal componente aggiuntivo desktop di Microsoft Project eliminano le assegnazioni non assegnate.
- Aggiunta una nuova convalida quando il riferimento al progetto di un'attività non è valido a causa di un'eccezione di riferimento null nel plugin **PreValidateProjectTaskUpdate**.
- La griglia dei membri del team non mostra assegnazioni distinte nel record del membro del team.
- Aggiunta nuova convalida e messaggi di errore a causa di un'eccezione di riferimento null nel plugin **PreProjectTaskDelete**.

**Sales**

Sono stati risolti i seguenti problemi:

- Quando si seleziona una riga basata su progetto nel preventivo o contratto, il pulsante **Suggerimento** dovrebbe essere visibile solo quando si seleziona una linea basata sul prodotto associata a un prodotto esistente.
- Suddividi il privilegio **Create_Product** dal privilegio **Create_ProjectContract**.
- L'eliminazione di una riga della fattura causa l'errore di riferimento null su **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
