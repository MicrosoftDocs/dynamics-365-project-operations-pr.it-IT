---
title: Definire i calendari del progetto
description: Questo argomento fornisce informazioni sull'utilizzo di un calendario di progetto per tenere traccia della pianificazione del progetto.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d44a2d0d8c13fb9e93b9a6da15fb3a7ce8d764c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897996"
---
# <a name="define-project-calendars"></a><span data-ttu-id="bc36d-103">Definire i calendari del progetto</span><span class="sxs-lookup"><span data-stu-id="bc36d-103">Define project calendars</span></span>

<span data-ttu-id="bc36d-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="bc36d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bc36d-105">Per creare una pianificazione di progetto, creai un modello di calendario di progetto che definisce il numero di ore lavorative giornaliere e le chiusure aziendali.</span><span class="sxs-lookup"><span data-stu-id="bc36d-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="bc36d-106">Per creare un modello di calendario di progetto, associ un modello di lavoro al campo **Modello calendario** del progetto.</span><span class="sxs-lookup"><span data-stu-id="bc36d-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="bc36d-107">Segui questi passaggi per creare un modello di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bc36d-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="bc36d-108">Seleziona **Risorse** nel riquadro di spostamento di sinistra.</span><span class="sxs-lookup"><span data-stu-id="bc36d-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="bc36d-109">Nella pagina elenco **Risorse**, apri un record utente, quindi seleziona **Mostra ore lavorative**.</span><span class="sxs-lookup"><span data-stu-id="bc36d-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="bc36d-110">Verifica che le finestre pop-up siano consentite nella pagina del browser.</span><span class="sxs-lookup"><span data-stu-id="bc36d-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="bc36d-111">Ciò consente di visualizzare le ore lavorative impostate per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="bc36d-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="bc36d-112">Nella scheda **Vista mensile**, seleziona **Configura**.</span><span class="sxs-lookup"><span data-stu-id="bc36d-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="bc36d-113">Viene visualizzato un elenco con tre opzioni:</span><span class="sxs-lookup"><span data-stu-id="bc36d-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="bc36d-114">Nuova pianificazione settimanale</span><span class="sxs-lookup"><span data-stu-id="bc36d-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="bc36d-115">Pianificazione lavorativa per un giorno</span><span class="sxs-lookup"><span data-stu-id="bc36d-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="bc36d-116">Indisponibilità</span><span class="sxs-lookup"><span data-stu-id="bc36d-116">Time Off</span></span>

4. <span data-ttu-id="bc36d-117">Seleziona **Nuova pianificazione settimanale** e quindi imposta le opzioni per questa pianificazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="bc36d-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="bc36d-118">Puoi impostare una pianificazione settimanale ricorrente, parametri orari giornalieri, chiusure aziendali e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="bc36d-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="bc36d-119">Imposta l'intervallo di date, seleziona **Salva** e quindi seleziona **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="bc36d-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="bc36d-120">Torna alla pagina elenco **Risorse** e seleziona la risorsa per la quale imposti le ore lavorative.</span><span class="sxs-lookup"><span data-stu-id="bc36d-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="bc36d-121">Seleziona **Imposta calendario come** per impostare il modello di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bc36d-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="bc36d-122">Nella finestra di dialogo **Modello di lavoro**, immetti un nome per il modello di lavoro e quindi seleziona **Applica**.</span><span class="sxs-lookup"><span data-stu-id="bc36d-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="bc36d-123">Ora puoi associare il modello di lavoro a un modello di calendario di progetto.</span><span class="sxs-lookup"><span data-stu-id="bc36d-123">You can now associate the work template with a project calendar template.</span></span>
