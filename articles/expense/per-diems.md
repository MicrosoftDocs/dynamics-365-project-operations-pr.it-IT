---
title: Diaria
description: Questo argomento fornisce informazioni sulle regole per la diaria utilizzate in Gestione spese.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908278"
---
# <a name="per-diems"></a><span data-ttu-id="488b0-103">Diaria</span><span class="sxs-lookup"><span data-stu-id="488b0-103">Per diems</span></span>

<span data-ttu-id="488b0-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="488b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="488b0-105">Una diaria è un'indennità pagata a un lavoratore che viaggia per lavoro.</span><span class="sxs-lookup"><span data-stu-id="488b0-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="488b0-106">In Gestione spese, è possibile creare regole per la diaria per varie situazioni di viaggio.</span><span class="sxs-lookup"><span data-stu-id="488b0-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="488b0-107">Le tariffe giornaliere possono essere basate sul periodo dell'anno, sulla destinazione del viaggio o su entrambi.</span><span class="sxs-lookup"><span data-stu-id="488b0-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="488b0-108">Quando crei una regola per la diaria, puoi specificare che una percentuale della tariffa giornaliera sarà trattenuta se un lavoratore riceve vitto o servizi gratuiti.</span><span class="sxs-lookup"><span data-stu-id="488b0-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="488b0-109">È inoltre possibile impostare un numero minimo e massimo di ore che la tariffa giornaliera può applicare al viaggio di un lavoratore.</span><span class="sxs-lookup"><span data-stu-id="488b0-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="488b0-110">Configurazione</span><span class="sxs-lookup"><span data-stu-id="488b0-110">Configuration</span></span> 

1. <span data-ttu-id="488b0-111">Per aggiungere destinazioni delle trasferte giornaliere, vai a **Imposta** > **Calcoli e codici** > **Destinazioni trasferte giornaliere**.</span><span class="sxs-lookup"><span data-stu-id="488b0-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="488b0-112">Per ciascuna delle destinazioni aggiunte sopra, seleziona una tariffa giornaliera e una valuta valide tra una data di inizio e una data di fine specifiche per hotel, vitto e altre spese.</span><span class="sxs-lookup"><span data-stu-id="488b0-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="488b0-113">Le tariffe giornaliere e le valute sono configurate in **Imposta** > **Calcoli e codici** > **Trasferte giornaliere**.</span><span class="sxs-lookup"><span data-stu-id="488b0-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="488b0-114">Nella pagina **Destinazioni trasferte giornaliere**, configura i livelli di tariffe giornaliere.</span><span class="sxs-lookup"><span data-stu-id="488b0-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="488b0-115">I livelli di tariffe giornaliere consentono di definire la ripartizione percentuale di un'indennità giornaliera per hotel, vitto e altre spese.</span><span class="sxs-lookup"><span data-stu-id="488b0-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="488b0-116">Per specificare la riduzione percentuale del vitto per colazione, pranzo o cena, aggiorna i campi nella pagina **Parametri di gestione spese** nella scheda **Diaria**.</span><span class="sxs-lookup"><span data-stu-id="488b0-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="488b0-117">Inviare le spese utilizzando la diaria</span><span class="sxs-lookup"><span data-stu-id="488b0-117">Submit expenses using per diem</span></span>
<span data-ttu-id="488b0-118">Per inviare le spese utilizzando le diarie, utilizza la categoria di spesa **Diaria** quando crei una nota spese.</span><span class="sxs-lookup"><span data-stu-id="488b0-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="488b0-119">Inserisci la **Data inizio trasferta giornaliera**, la **Data fine trasferta giornaliera** e la **Destinazione trasferta giornaliera**.</span><span class="sxs-lookup"><span data-stu-id="488b0-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="488b0-120">L'importo verrà calcolato in base alle tariffe giornaliere per la destinazione selezionata e la riduzione per il vitto verrà calcolata in base ai livelli delle tariffe giornaliere.</span><span class="sxs-lookup"><span data-stu-id="488b0-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
