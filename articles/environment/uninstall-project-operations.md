---
title: Disinstallare Dynamics 365 Project Operations
description: In questo articolo sono riportate informazioni su come disinstallare Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911969"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Disinstallare Dynamics 365 Project Operations 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Per disinstallare Dynamics 365 Project Operations, devi avere assegnato il ruolo di amministratore.

1. Vai a **Impostazioni** > **Soluzioni**.

    ![Pagina Impostazioni.](./media/uninstall-proj-ops-solutions.png)
  
2. Rimuovi le soluzioni nell'ordine esatto in cui sono elencate nella tabella seguente. 

    | Passaggio | Nome soluzione                                    | Nota                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Se non la trovi, ignora questa soluzione.                                                            |
    | 2 | ProjectOperations_Anchor                           | Se non la trovi, ignora questa soluzione.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Se non la trovi, ignora questa soluzione.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Se non la trovi, ignora questa soluzione.                                                            |
    | 5 | ProjectService                                     | Nessuna nota aggiuntiva.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Nessuna nota aggiuntiva.                                                                         |
    | 7 | ProjectServiceCore                                 | Nessuna nota aggiuntiva.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Se non la trovi, ignora questa soluzione.                                                            |
    | 9 | FieldServiceCommon                                 | Necessario per la doppia scrittura con Dynamics 365 Finance o Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Necessario per la doppia scrittura con Dynamics 365 Finance o Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Richiesto per Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Richiesto per Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Richiesto per Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Richiesto per Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Richiesto per Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Richiesto per Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Richiesto per Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Se non la trovi, ignora questa soluzione.                                                            |
    | 19 | Dynamics365Notes                                   | Se non la trovi, ignora questa soluzione.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Se non la trovi, ignora questa soluzione.                                                            |
    | 21 | DualWriteCore                                      | Se non la trovi, ignora questa soluzione.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Se non la trovi, ignora questa soluzione.                                                            |
    | 23 | Dynamics365AssetManagement                         | Se non la trovi, ignora questa soluzione.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Se non la trovi, ignora questa soluzione.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Se non la trovi, ignora questa soluzione.                                                            |
    | 26 | HCMCommon                                          | Se non la trovi, ignora questa soluzione.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Se non la trovi, ignora questa soluzione.                                                            |
    | 28 | Parte                                              | Se non la trovi, ignora questa soluzione.                                                            |
    | 29 | Dynamics365Company                                 | Se non la trovi, ignora questa soluzione.                                                            |
    | 30 | CurrencyExchangeRates                              | Se non la trovi, ignora questa soluzione.                                                            |
    | 31 | AssetCommon                                        | Se non la trovi, ignora questa soluzione.                                                            |
