---
title: Impostazioni di progetto
description: In questo argomento vengono fornite informazioni sulle impostazioni per la gestione di progetti.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 5f6fec091c50f35589e333fce4b3a296dd736d10dd2f56b6c11209a55b493836
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996936"
---
# <a name="project-settings"></a>Impostazioni di progetto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Utilizza le impostazioni seguenti per accedere alle funzionalità di pianificazione di progetti.

## <a name="work-template"></a>Modello di lavoro

Per creare una pianificazione di progetto, creai un modello di calendario di progetto che definisce il numero di ore lavorative giornaliere e le chiusure aziendali. Per creare un modello di calendario di progetto, associ un modello di lavoro al campo **Modello calendario** del progetto. Segui questi passaggi per creare un modello di lavoro.

1. In PSA, nel riquadro di navigazione sinistro, fai clic su **Risorse**. 
2. Nella pagina elenco **Risorse**, apri un record utente, quindi seleziona **Mostra ore lavorative**.

  > [!NOTE]
  > Verifica che le finestre pop-up siano consentite nella pagina del browser. Ciò consente di visualizzare le ore lavorative impostate per la risorsa.
  
3. Nella scheda **Vista mensile**, fai clic su **Configura**. Viene visualizzato un elenco con tre opzioni: 

  - Nuova pianificazione settimanale
  - Pianificazione lavorativa per un giorno
  - Indisponibilità

> ![Opzioni di Configura.](media/project-13.png)

4. Seleziona **Nuova pianificazione settimanale** e quindi imposta le opzioni per questa pianificazione delle risorse. Puoi impostare una pianificazione settimanale ricorrente, parametri orari giornalieri, chiusure aziendali e altro ancora.
5. Imposta l'intervallo di date, seleziona **Salva** e quindi fai clic su **Chiudi**. 
6. Torna alla pagina elenco **Risorse** e seleziona la risorsa per la quale imposti le ore lavorative. 
7. Seleziona **Imposta calendario come** per impostare il modello di lavoro. 
8. Nella finestra di dialogo **Modello di lavoro**, immetti un nome per il modello di lavoro e quindi seleziona **Applica**. 

Ora puoi associare il modello di lavoro a un modello di calendario di progetto.

## <a name="resource-roles"></a>Ruoli risorsa

Il termine *ruolo risorsa* fa riferimento al set di competenze, qualifiche e certificazioni che una persona deve avere per eseguire un insieme specifico di attività in un progetto. PSA ti consente di determinare il costo del tempo di una risorsa e di fatturarlo in base al ruolo a cui quella risorsa è associata. Ogni organizzazione deve impostare questi ruoli utilizzando il riquadro di navigazione sinistro nel menu **Project Service**.

Ogni organizzazione deve impostare questi ruoli nella pagina **Categorie di risorse attive**. Per aprire questa pagina, nel riquadro di navigazione sinistro, seleziona **Ruoli risorsa**.

## <a name="price-lists"></a>Listini prezzi

I listini prezzi consentono di impostare i prezzi di costo e di vendita per ruoli risorsa, categorie di spese, prodotti e altri elementi in un'organizzazione. Prima di impostare le stime finanziarie per il lavoro da eseguire per un progetto, devi creare un listino prezzi di costo e vendita di backup. Nella sezione dei parametri, devi impostare anche un listino prezzi di costo e vendita predefinito applicabile a tutti i progetti creati nell'organizzazione. Nella pagina **Parametri progetto attivi**, verifica di aver impostato un listino prezzi di costo e vendita predefinito.


[!INCLUDE[footer-include](../includes/footer-banner.md)]