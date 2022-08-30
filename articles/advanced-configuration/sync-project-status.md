---
title: Sincronizza lo stato del progetto per impedire l'accesso a progetti chiusi
description: Questo articolo spiega come sincronizzare lo stato del progetto per impedire l'immissione di progetti inattivi o chiusi.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348017"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sincronizza lo stato del progetto per impedire l'accesso a progetti chiusi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

## <a name="scenario"></a>Scenario

Contoso è disponibile con Microsoft Dynamics 365 Project Operations per scenari di risorse/materiali non stoccati. Nell'ambito delle normali attività aziendali, i progetti possono essere completati o sospesi. Puoi disattivare il progetto per assicurarti che non vengano generate spese o fatture.

## <a name="solution"></a>Soluzione

### <a name="prerequisites"></a>Prerequisiti

-   Deve essere installato Microsoft Dynamics 365 Finance 10.0.29 o versione successiva.
-   Mappa Dual Write 1.0.0.3 per Projects V2 (msdyn\_projects) deve essere installato o configurato manualmente come descritto di seguito.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Creare una versione aggiornata dell'integrazione di Project Operations con la mappa Projects V2 con doppia scrittura

Per aggiornare la mappa Projects V2 di Project Operations con doppia scrittura:

1. Vai all'area di lavoro **Gestione dati** e seleziona **Doppia scrittura**.
2. Seleziona il riquadro **Doppia scrittura**.
3. dalla colonna **Mappa della tabella**, individua e seleziona **Project V2 (msdyn\_projects)**, quindi seleziona Interrompi.
4. Seleziona il nome della mappa per aprire la mappa, quindi seleziona **[Nessuno]**.
5. Nella finestra di dialogo Seleziona colonna, seleziona **statecode \[Stato progetto\]**, quindi OK. Puoi digitare **stato** nel valore del filtro per restringere l'elenco.
6.  Seleziona **Aggiungi o modifica la trasformazione** nella colonna **tipo di mappa** per modificare la trasformazione.
7.  Dal **Tipo di trasformazione** seleziona **ValueMap**.
8.  Seleziona **Aggiungi mapping di valori**, quindi aggiungi le seguenti **Chiavi** e **Valori**:

   Key       | valore 
   ----------|-------
   InProcess | 0     
   Completato | 1     

![Screenshot che mostra il mapping a doppia scrittura](media/projectstage-dw-mapping.png)

9. Seleziona **Salva**.
10. In alto nella pagina **Doppia scrittura > Projects V2 (msdyn_projects)**, seleziona **Salva con nome**.
11. Da **Aggiungi tabella** nel campo **Editore**, seleziona **Editore predefinito CDS**.
12. Impostare il campo **Versione** su 1.0.0.3.
13. Digita una **Descrizione**, quindi seleziona **Salva**.
14. In alto nella pagina **Doppia scrittura > Projects V2 (msdyn_projects)**, seleziona **Esegui** per avviare la mappa, quindi seleziona **Sì** se viene chiesto di confermare prima dell'esecuzione. 

### <a name="close-a-newly-completed-project"></a>Chiudi un progetto appena completato

Dynamics 365 Finance utilizza il campo **fase del progetto** per differenziare i progetti **in corso** o **completati**. I progetti **completati** non possono sostenere spese o essere fatturati ai clienti.

1. Apri un progetto da disattivare.
2. Dalla barra, seleziona **Disattiva**.

> [!NOTE]
> Puoi inoltre disattivare o chiudere un progetto perché si comporteranno allo stesso modo nel contesto di Finance.

3. In Finance, apri la pagina **Riepilogo di tutti i progetti**.
4. Conferma che il progetto disattivato non viene visualizzato nell'elenco.
5. Nel filtro **mostra progetti** sopra l'elenco, modifica il valore da **Attivo** a **Tutto**.
6. Ora vedrai il progetto disattivato.

Se tenti di registrare il tempo o le spese per questo progetto in Finance, non dovresti vedere il progetto per la selezione. Se inserisci manualmente il numero del progetto su una spesa, vedrai un messaggio "La fase del progetto Completato non consente la registrazione nel progetto". La fatturazione e le altre funzioni di fatturazione devono essere disabilitate poiché lo saranno nel contesto di un progetto chiuso.

