---
title: Novità o modifiche nella versione di aggiornamento 20 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 20 di Project Service Automation V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: db416343ac9ac2591007e83be80493a48f9ae904
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280673"
---
# <a name="project-service-automation-update-release-20-v3"></a>Versione di aggiornamento di Project Service Automation 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 20 di Project Service Automation V3. Questa versione ha il numero di build V 3.10.31.37 ed è generalmente disponibile tramite un aggiornamento automatico a giugno 2020.

## <a name="update-release-20"></a>Rilascio 20 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Gestione progetti**

Sono stati risolti i seguenti problemi:

- L'importazione dei membri del team di progetto con un metodo di allocazione che richiede ore genera un messaggio di errore non chiaro quando le ore specificate sono zero.
- Gli utenti ricevono un errore non corretto quando il numero massimo di caratteri è stato inserito nel campo **Descrizione** per un'attività di progetto.
- La pagina di **download del componente aggiuntivo Microsoft Dynamics 365 Project Service Automation** reindirizza alla pagina di download in inglese quando le impostazioni della lingua dell'utente sono impostate sul giapponese.
- Quando si verifica un errore del server, l'etichetta di sincronizzazione sulla scheda **Pianifica** del modulo **Progetti** a volte rimane.
- Gli aggiornamenti delle attività ridondanti vengono inviati al server quando un'attività viene modificata.

**Sales**

Sono stati risolti i seguenti problemi:

- Sul modulo **Contratto**, fai doppio clic su **Crea fattura** crea due fatture per un singolo record effettivo.
- In Internet Explorer 11, gli utenti non sono in grado di creare voci di spesa.
- Lo storno del costo e lo storno dei valori effettivi di vendita non fatturati non sono collegati.
- Il pulsante **Aggiorna valori effettivi** sul modulo **Progetto** non aggiorna **Ore effettive attività**.
- Il plug-in **PreValidateProjectTeamMemberCreate** può creare risorse prenotabili generiche duplicate quando l'attributo **msdyn_isgenericresourceprojectscoped** è impostato su **False**.
- **Ricalcola** cancella i costi addebitabili dei dettagli della riga di offerta basata sul prodotto e dei dettagli della voce di contratto.
- In scenari specifici, il plug-in **PostEstimateLineUpdate** visualizza un errore di eccezione di riferimento Null.
- Durata della scala cronologica sul **Grafico Analisi redditività** non corrisponde alla durata dei costi nel dettaglio della riga di offerta a prezzo fisso dell'offerta.
- Le impostazioni predefinite per i valori delle unità e delle unità di vendita non vengono applicate correttamente per le categorie di spesa nei moduli **Dettagli voce di contratto** e **Dettagli riga di offerta**.
- Gli elenchi **Prezzo di costo unità organizzativa** consentono sovrapposizioni della data di validità.
- Gli utenti non sono autorizzati a modificare **OrgUnit** quando il tipo di ordine non è basato sul lavoro perché questa operazione genererà un errore di eccezione di riferimento Null.
- Quando si tenta di passare dal modulo **Dettagli riga di offerta**, indietro nella scheda **Offerta**, il modulo si aggiorna e visualizza la scheda **Riepilogo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]