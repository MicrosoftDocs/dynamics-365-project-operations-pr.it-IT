---
title: Area di lavoro per dispositivi mobili Immissione ora progetto
description: In questo argomento vengono fornite informazioni sull'area di lavoro per dispositivi Immissione ora progetto. Questa area di lavoro consente agli utenti di accedere e risparmiare tempo a fronte di un progetto utilizzando il proprio dispositivo mobile.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752658"
---
# <a name="project-time-entry-mobile-workspace"></a>Area di lavoro per dispositivi mobili Immissione ora progetto

[!include [banner](../includes/banner.md)]

In questo argomento vengono fornite informazioni sull'area di lavoro per dispositivi **Immissione ora progetto**. Questa area di lavoro consente agli utenti di accedere e risparmiare tempo a fronte di un progetto utilizzando il proprio dispositivo mobile.

Quest'area di lavoro per dispositivi mobili deve essere utilizzata con l'app dispositivi mobili Dynamics 365. 

## <a name="overview"></a>Panoramica
Come parte del loro lavoro quotidiano, le risorse del progetto sono spesso in loco o in viaggio. L'area di lavoro per dispositivi mobili **Immissione ora progetto** consente agli utenti di inserire il loro tempo fatturabile o non fatturabile per un progetto sul dispositivo mobile di loro scelta. Pertanto, le risorse del progetto possono registrare gli inserimenti di ore sempre e ovunque. Possono anche visualizzare gli inserimenti di ore che sono già stati registrati. 

In particolare, nell'area di lavoro per dispositivi mobili **Immissione ora progetto**, gli utenti possono eseguire queste attività:

-   Per qualsiasi data selezionata, inserisci il numero di ore che hai dedicato a un'attività specifica.
-   Cerca per nome progetto o cliente per trovare il progetto per cui inserire l'ora.
-   Specifica la categoria e l'impegno per il tempo che hai trascorso.
-   Registra il tempo come fatturabile o non fatturabile per il progetto.
-   Inserisci eventuali commenti esterni o interni.

## <a name="prerequisites"></a>Prerequisiti
I prerequisiti differiscono, in base alla versione di Microsoft Dynamics 365 che è stata distribuita per la tua organizzazione.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Prerequisiti se usi Dynamics 365 Finance
Se Finance è stato distribuito per la tua organizzazione, l'amministratore di sistema deve pubblicare l'area di lavoro per dispositivi mobili **Immissione ora progetto**. Per istruzioni, vedi [Pubblicare un'area di lavoro per dispositivi mobili](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Prerequisiti se utilizzi la versione 1611 con Platform update 3 o successiva
Se la versione 1611 con Platform update 3 o successiva è stata distribuita per la tua organizzazione, l'amministratore di sistema deve completare i seguenti prerequisiti. 

<table>
<thead>
<tr class="header">
<th>Prerequisito</th>
<th>Ruolo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementa KB 4018050.</td>
<td>Amministratore di sistema</td>
<td>KB 4018050 è un aggiornamento X++ o un hotfix dei metadati che contiene l'area di lavoro per dispositivi mobili <strong>Immissione ora progetto</strong>. Per implementare KB 4018050, l'amministratore di sistema deve seguire questi passaggi.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Scarica l'aggiornamento rapido dei metadati da Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installa l'hotfix per i metadati</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Crea un pacchetto distribuibile</a> che contiene i modelli <strong>ApplicationSuite</strong> e <strong>ProjectMobile</strong>, quindi carica il pacchetto distribuibile su LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Applica il pacchetto distribuibile</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Pubblica l'area di lavoro per dispositivi mobili <strong>Immissione ora progetto</strong>.</td>
<td>Amministratore di sistema</td>
<td>Vedi <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Pubblicare un'area di lavoro per dispositivi mobili</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Scaricare e installare l'app per dispositivi mobili

Scarica e installa l'app per dispositivi mobili Finance and Operations:

-   [Per telefoni Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Per iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Accedere all'app per dispositivi mobili
1.  Avvia l'app sul dispositivo mobile.
2.  Immetti l'URL di Dynamics 365.
3.  La prima volta che accedi, ti vengono richiesti il nome utente e la password. Immetti le tue credenziali.
4.  Dopo aver effettuato l'accesso, vengono visualizzate le aree di lavoro disponibili per la tua azienda. Tieni presente che se l'amministratore di sistema pubblica una nuova area di lavoro in un secondo momento, dovrai aggiornare l'elenco delle aree di lavoro per dispositivi mobili.

[![Trascinare verso il basso](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Immettere l'ora utilizzando l'area di lavoro per dispositivi mobili Immissione ora progetto
1.  Sul tuo dispositivo mobile, seleziona l'area di lavoro **Immissione ora progetto**.
2.  Seleziona **Inserimento ore**. Vengono visualizzate le date del calendario per la settimana corrente.
3.  Per una data selezionata, seleziona **Azioni** &gt; **Nuovo inserimento**.
4.  Immetti il numero di ore da registrare.
5.  Seleziona il progetto per l'inserimento ore. Un elenco mostra i progetti caricati nella tua app per l'utilizzo offline. Per impostazione predefinita, vengono caricati 50 elementi, ma uno sviluppatore può modificare questo numero. Per altre informazioni, vedi [Piattaforma per dispositivi mobili](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Se il tuo progetto non è nell'elenco, seleziona **Cerca**. Cerca per nome o passa alla ricerca per nome progetto o cliente.
7.  Seleziona una categoria. Un elenco mostra le categorie caricate nella tua app per l'utilizzo offline. Per impostazione predefinita, vengono caricati 50 elementi, ma uno sviluppatore può modificare questo numero. Per altre informazioni, vedi [Piattaforma per dispositivi mobili](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Se la tua categoria non è nell'elenco, seleziona **Cerca**. Cerca per categoria o passa alla ricerca per nome della categoria.
9.  Selezionare un impegno. Un elenco mostra gli impegni caricati nella tua app per l'utilizzo offline. Per impostazione predefinita, vengono caricati 50 elementi, ma uno sviluppatore può modificare questo numero. Per altre informazioni, vedi [Piattaforma per dispositivi mobili](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Se il tuo impegno non è nell'elenco, seleziona **Cerca**. Cerca per numero di attività o passa alla ricerca per scopo.

11. Seleziona la proprietà della riga.
12. Facoltativo: immetti eventuali commenti esterni o interni.
13. Seleziona **Fatto**.
