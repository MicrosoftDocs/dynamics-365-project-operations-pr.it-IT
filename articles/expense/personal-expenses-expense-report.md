---
title: Utilizzare le spese personali in una nota spese
description: Questo argomento fornisce informazioni su come utilizzare le spese personali sostenute dai dipendenti durante i viaggi per motivi di lavoro.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025689"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="25d1e-103">Utilizzare le spese personali in una nota spese</span><span class="sxs-lookup"><span data-stu-id="25d1e-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="25d1e-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="25d1e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25d1e-105">Durante un viaggio d'affari, un dipendente potrebbe addebitare le spese personali sulla carta di credito aziendale.</span><span class="sxs-lookup"><span data-stu-id="25d1e-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="25d1e-106">Se non è stato definito un processo per la gestione delle spese personali, il processo di approvazione della nota spese potrebbe essere interrotto quando un dipendente invia la propria nota spese dettagliata.</span><span class="sxs-lookup"><span data-stu-id="25d1e-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="25d1e-107">Esistono due metodi che puoi utilizzare per gestire le spese personali di un dipendente:</span><span class="sxs-lookup"><span data-stu-id="25d1e-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="25d1e-108">**Pagato dal dipendente**: La tua organizzazione non paga le spese personali che compaiono sulla fattura della carta di credito aziendale.</span><span class="sxs-lookup"><span data-stu-id="25d1e-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="25d1e-109">Il dipendente paga direttamente le spese al venditore della carta di credito.</span><span class="sxs-lookup"><span data-stu-id="25d1e-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="25d1e-110">**Pagato dalla società**: La tua organizzazione paga l'intero conto della carta di credito aziendale, quindi addebita le spese personali sul conto del lavoratore.</span><span class="sxs-lookup"><span data-stu-id="25d1e-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="25d1e-111">È possibile selezionare il metodo utilizzato dalla propria organizzazione nella pagina **Parametri di gestione spese**.</span><span class="sxs-lookup"><span data-stu-id="25d1e-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="25d1e-112">Abilita la funzione di suddivisione delle spese quando il campo dell'importo personale ha un valore definito</span><span class="sxs-lookup"><span data-stu-id="25d1e-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="25d1e-113">La caratteristica, **Abilita la funzione di suddivisione delle spese quando il campo dell'importo personale ha un valore definito** si applica solo alle note spese approvate utilizzando un flusso di lavoro a livello di riga.</span><span class="sxs-lookup"><span data-stu-id="25d1e-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="25d1e-114">I report vengono approvati andando su **Elabora note spese** > **Note spese assegnate a me** > **Apri nota spese**.</span><span class="sxs-lookup"><span data-stu-id="25d1e-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="25d1e-115">Per abilitare questa funzione, vai ad **Aree di lavoro** > **Gestione funzionalità**, seleziona **Abilita la funzione di suddivisione delle spese quando il campo dell'importo personale ha un valore definito**, quindi seleziona **Abilita ora**.</span><span class="sxs-lookup"><span data-stu-id="25d1e-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="25d1e-116">Quando la funzionalità è abilitata, le righe di spesa che utilizzano questa funzionalità generano due righe quando viene inviato il report.</span><span class="sxs-lookup"><span data-stu-id="25d1e-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="25d1e-117">Vengono generate due righe in modo che l'approvatore possa approvare ciascuna riga separatamente.</span><span class="sxs-lookup"><span data-stu-id="25d1e-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
