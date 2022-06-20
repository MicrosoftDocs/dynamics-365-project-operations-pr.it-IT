---
title: Requisiti degli articoli per contratti di progetto con più fonti di finanziamento
description: Questo articolo fornisce informazioni su come configurare e utilizzare i requisiti degli articoli con più fonti di finanziamento.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a54ca1ec5e78d9d0af7b67914f6a63154c7347d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931197"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Requisiti degli articoli per contratti di progetto con più fonti di finanziamento

_**Si applica a:** Project Operations per scenari basati su materiali stoccati/produzione_

Alcuni contratti per forniture basate su progetto potrebbero richiedere più fonti di finanziamento. Questo articolo spiega come selezionare e configurare le fonti di finanziamento desiderate quando sono necessarie più fonti per un progetto o un contratto di progetto.

## <a name="terminology"></a>Terminologia

- **Fonte di finanziamento** – L'entità che finanzia il lavoro del contratto di progetto. Questa entità può essere un'organizzazione interna o un conto fattura esterno (cliente o concessione).
- **Cliente del progetto** – L'entità a cui viene consegnato il lavoro di progetto.
- **Conto fattura** – L'entità esterna che paga per il lavoro di progetto.

## <a name="example"></a>Esempio

Contoso ha vinto un contratto di rinnovo delle apparecchiature con due dei suoi clienti: Adatum US e Adatum Corporate. Il contratto include hardware e servizi di installazione che saranno consegnati ad Adatum US (il cliente del progetto). L'hardware sarà finanziato da Adatum Corporate (conto fattura 1) e il lavoro di installazione sarà finanziato da Adatum US (conto fattura 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Impostare le regole predefinite del conto fattura per i requisiti dell'articolo

### <a name="prerequisites"></a>Prerequisiti

- Microsoft Dynamics 365 Finance and Operations **versione 10.0.27 o successiva** è necessario per utilizzare i requisiti dell'articolo con più conti fattura.
- Il tuo sistema amministratore deve abilitare la funzionalità **Consenti requisiti articolo con più fonti di finanziamento per scenari in stock/produzione di Project Operations** nell'area di lavoro **Gestione funzionalità**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Impostare le regole predefinite del conto fatture

Per impostare le regole predefinite per il conto fatture, effettua i seguenti passaggi.

1. Vai a **Gestione progetti e contabilità** \> **Imposta** \> **Parametri Gestione progetti e contabilità**.
1. Sulla scheda **Generale** nella sezione **Ordini cliente e requisiti articoli** imposta l'opzione **Consenti progetti con più fonti di finanziamento** su **sì**.
1. Nel campo **Cliente predefinito** specifica da dove proviene per impostazione predefinita il cliente della consegna del progetto sul fabbisogno di articolo:

    - **Da fonte di finanziamento** – Il cliente predefinito per la consegna del progetto proviene dalla fonte di finanziamento. Se più fonti di finanziamento sono associate al contratto di progetto, verrà utilizzata la prima fonte di finanziamento nell'elenco.
    - **Dal progetto** – Il cliente di consegna del progetto predefinito proviene dal cliente selezionato nel campo **Conto record di progetto**.

1. Facoltativo: imposta o modifica il conto fatture predefinito sui record del progetto:

    1. Vai a **Gestione progetto e contabilità** \> **Progetti** \> **Tutti i progetti** e apri i dettagli del record di progetto.
    2. Sulla scheda **Generale** imposta o aggiorna il campo **Conto fatture predefinito**. Il conto specificato verrà utilizzato come conto fatture predefinito per i nuovi requisiti articolo creati per il progetto. Se lasci vuoto il campo, per impostazione predefinita verrà utilizzato il conto fatture della prima fonte di finanziamento del contratto di progetto. Tuttavia, gli utenti potranno modificare il conto quando salvano il record.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Selezionare il conto fatture da utilizzare quando si crea un requisito articolo

Per selezionare il conto fatture da utilizzare quando crei un requisito articolo, segui questi passaggi.

1. Vai a **Gestione progetto e contabilità** \> **Progetti** \> **Tutti i progetti** e seleziona il record di progetto.
1. Sulla scheda **Piano** seleziona **Requisiti articolo**.
1. Crea un nuovo record di requisito articolo.

    - Per impostazione predefinita, il campo **Conto fatture** nel record è impostato sul conto fatture impostato per il progetto. È possibile modificare il valore del campo **Conto fatture** e quindi salvare il record. Dopo che il record è stato salvato, non è più possibile aggiornare il valore di **Conto fatture**. Se devi aggiornare il valore di **Conto fatture** per il requisito articolo, elimina il requisito articolo esistente e quindi crearne uno nuovo con il valore desiderato.
    - Per impostazione predefinita, il campo **Cliente** per il requisito articolo è impostato in base al valore **Cliente predefinito** impostato nella pagina **Parametri Gestione progetti e contabilità**.

    Quando il record del requisito articolo viene salvato, il sistema lo associa al record di intestazione **Ordine cliente requisito articolo**. Se nessuna intestazione dell'ordine cliente aperta ha il conto fatture selezionato, il sistema ne creerà uno e assocerà ad esso la riga del requisito articolo.

> [!NOTE]
> I requisiti articolo vengono sempre fatturati per intero sul conto fatture impostato nel record. Il sistema attualmente non supporta le regole di allocazione dei finanziamenti che hanno requisiti articolo e non dividerà la registrazione in base all'impostazione delle regole di allocazione dei finanziamenti.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Creare un requisito articolo da un record di previsione articolo

Per creare un requisito articolo da un record di previsione articolo, segui questi passaggi:

1. Vai a **Gestione progetto e contabilità** \> **Progetti** \> **Tutti i progetti** e seleziona il record di progetto.
1. Sulla scheda **Piano** seleziona **Previsioni articolo**.
1. Crea un nuovo record di previsione articolo.
1. Opzionale: sulla scheda **Progetto** nel campo **Fonte di finanziamento** seleziona il conto fatture desiderato.
1. Seleziona **Crea requisito articolo** e conferma il messaggio ricevuto.

    > [!NOTE]
    > Il sistema copia il valore di **Fonte di finanziamento** dal record di previsione articolo nel record di requisito articolo appena creato.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Conto fatture predefinito quando il sistema crea automaticamente un requisito articolo da una riga ordine di acquisto

Se l'opzione **Crea requisito articolo** è impostata su **sì** nella pagina **Parametri Gestione progetti e contabilità**, il sistema crea automaticamente un requisito articolo quando viene salvata una nuova riga dell'ordine di acquisto del progetto. Per impostazione predefinita, i campi **Conto fatture** e **Requisito articolo** sono impostati sul valore del campo **Conto fatture predefinito** nel record del progetto. Il sistema attualmente non supporta l'aggiornamento o la modifica del conto fatture per record di questo tipo.
