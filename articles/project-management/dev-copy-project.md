---
title: Sviluppare i modelli di progetto con Copia progetto
description: Questo argomento fornisce informazioni su come creare modelli di progetto utilizzando l'azione personalizzata Copia progetto.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590903"
---
# <a name="develop-project-templates-with-copy-project"></a>Sviluppare i modelli di progetto con Copia progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations supporta la capacità di copiare un progetto e ripristinare eventuali assegnazioni alle risorse generiche che ne rappresentano il ruolo. I clienti possono utilizzare questa funzionalità per creare modelli di progetto di base.

Quando selezioni **Copia progetto**, lo stato del progetto di destinazione viene aggiornato. Usa il **motivo stato** per determinare quando l'azione di copia è stata completata. La selezione di **Copia progetto** aggiorna anche la data di inizio del progetto sulla data di inizio corrente se non viene rilevata alcuna data di destinazione nell'entità del progetto di destinazione.

## <a name="copy-project-custom-action"></a>Azione personalizzata Copia progetto

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Parametri di input

Sono presenti tre parametri di input:

- **ReplaceNamedResources** o **ClearTeamsAndAssignments** – Imposta solo una delle opzioni. Non impostarle entrambi.

    - **\{"ReplaceNamedResources":true\}** – Il comportamento predefinito per Project Operations. Eventuali risorse denominate vengono sostituite con risorse generiche.
    - **\{"ClearTeamsAndAssignments":true\}** – Il comportamento predefinito per Project for the Web. Tutte le assegnazioni e i membri del team vengono rimossi.

- **SourceProject** – Il riferimento all'entità del progetto di origine da cui copiare. Il parametro non può essere Null.
- **Target** – Il riferimento all'entità del progetto di destinazione in cui copiare. Il parametro non può essere Null.

Nella seguente tabella viene fornito un riepilogo dei tre parametri.

| Parametro                | Type             | valore                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **True** o **False** |
| ClearTeamsAndAssignments | Boolean          | **True** o **False** |
| SourceProject            | Riferimento entità | Progetto di origine.    |
| Target                   | Riferimento entità | Progetto di destinazione    |

Per ulteriori valori predefiniti delle azioni, vedi [Usare le azioni API Web](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Convalide

Le seguenti convalide sono eseguite.

1. Controlla i valori Null e recupera i progetti di origine e di destinazione per confermare l'esistenza di entrambi i progetti nell'organizzazione.
2. Il sistema convalida che il progetto di destinazione sia valido per la copia verificando le seguenti condizioni:

    - Non vi è alcuna attività precedente sul progetto (compresa la selezione della scheda **Attività**) e il progetto è stato appena creato.
    - Non esiste una copia precedente, non è stata richiesta l'importazione su questo progetto e il progetto non ha uno stato **Non riuscito**.

3. L'operazione non viene chiamata tramite HTTP.

## <a name="specify-fields-to-copy"></a>Specificare i campi da copiare

Quando l'azione viene chiamata, **Copia progetto** guarda la vista del progetto **Copia colonne di progetto** per determinare quali campi copiare quando il progetto viene copiato.

### <a name="example"></a>Esempio

L'esempio seguente mostra come chiamare l'azione personalizzata **CopyProjectV3** con il set di parametri **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
