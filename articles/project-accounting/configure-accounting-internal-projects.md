---
title: Configurare la contabilità per i progetti interni
description: Questo argomento fornisce informazioni su come impostare le procedure contabili per i progetti interni in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078810"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="00642-103">Configurare la contabilità per i progetti interni</span><span class="sxs-lookup"><span data-stu-id="00642-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="00642-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="00642-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="00642-105">I progetti interni consentono alle aziende di tenere traccia dei costi relativi alle attività che non vengono fatturate a un cliente.</span><span class="sxs-lookup"><span data-stu-id="00642-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="00642-106">Esempi di progetti interni sono:</span><span class="sxs-lookup"><span data-stu-id="00642-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="00642-107">Sviluppo di un prodotto, come un'app mobile, e monitoraggio dei costi associati allo sviluppo.</span><span class="sxs-lookup"><span data-stu-id="00642-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="00642-108">Gestione dei tempi e delle spese di prevendita.</span><span class="sxs-lookup"><span data-stu-id="00642-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="00642-109">Questo progetto interno di prevendita può essere convertito in un secondo momento in un progetto fatturabile se si acquisisce l'offerta.</span><span class="sxs-lookup"><span data-stu-id="00642-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="00642-110">Qualsiasi progetto non associato a un contratto in Dynamics 365 Project Operations viene considerato interno.</span><span class="sxs-lookup"><span data-stu-id="00642-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="00642-111">I profili di costi e ricavi di progetto non sono usati per determinare le regole contabili per il progetto.</span><span class="sxs-lookup"><span data-stu-id="00642-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="00642-112">Il costo interno del progetto viene sempre registrato utilizzando i principi di profitti e perdite.</span><span class="sxs-lookup"><span data-stu-id="00642-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="00642-113">I conti contabili per le registrazioni sono definiti nella pagina **Impostazione registrazione contabile**.</span><span class="sxs-lookup"><span data-stu-id="00642-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="00642-114">Le transazioni temporali vengono registrate addebitando conto di **Costo** e accreditando il conto **Allocazione retribuzioni**.</span><span class="sxs-lookup"><span data-stu-id="00642-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="00642-115">Le transazioni di spesa vengono registrate addebitando conto di **Costo** e accreditando il **Conto di contropartita predefinito per le spese**.</span><span class="sxs-lookup"><span data-stu-id="00642-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="00642-116">Dopo che le transazioni sono state registrate nel progetto, se il progetto è associato a un contratto di progetto, il sistema annulla tutte le transazioni accumulate e crea nuove transazioni fatturabili.</span><span class="sxs-lookup"><span data-stu-id="00642-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="00642-117">Le transazioni fatturabili seguono le regole contabili definite nel rispettivo profilo di costi e ricavi del progetto.</span><span class="sxs-lookup"><span data-stu-id="00642-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


