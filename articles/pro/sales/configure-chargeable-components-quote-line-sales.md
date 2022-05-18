---
title: Configurare i componenti addebitabili di una riga di offerta
description: Questo argomento fornisce informazioni sulla configurazione dei componenti addebitabili e non addebitabili di una riga di offerta basata su progetto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3c9bd23f4e78e3ea5ae8f74ff1a4829a11f91929
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598401"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Configurare i componenti addebitabili di una riga di offerta 

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma, Project Operations per scenari basati su risorse/materiali non stoccati_

Una riga di offerta basata su progetto ha il concetto di componenti *inclusi* e *addebitabili*.

I componenti inclusi sono soggetti a:

  - Metodo di fatturazione e suddivisioni dei clienti
  - Limite da non superare 
  - Impostazioni della frequenza della fattura definite nella riga di offerta basata su progetto

Un sottoinsieme dei componenti inclusi può essere contrassegnato come addebitabile usando il campo **Tipo di fatturazione**. Il campo **Tipo di fatturazione** è un set di opzioni che consente i seguenti valori nel contesto di una riga di offerta:

  - Addebitabile
  - Non addebitabile

I componenti addebitabili possono essere definiti sulle attività, sui ruoli e sulle categorie di transazioni.

L'esigibilità è definita nelle attività per una riga di offerta e si applica a tutte le classi di transazione incluse in quella riga. Se il campo **Includi attività** è impostato su **Intero progetto** o viene lasciato vuoto, la scheda **Attività addebitabili** non è disponibile.

L'esigibilità è definita nei ruoli di una riga di offerta e si applica solo alla classe di transazione **Tempo**. Se il campo **Includi tempo** è impostato su **No** su una riga di offerta di progetto, la scheda **Ruoli addebitabili** non è disponibile.

L'esigibilità è definita nelle categorie di transazione per una riga di offerta e si applica solo alla classe di transazione **Spesa**. Se il campo **Includi spese** è impostato su **No** su una riga di offerta di progetto, la scheda **Categorie addebitabili** non è disponibile.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Aggiornare un'attività di progetto in modo che sia addebitabile o non addebitabile

Un'attività di progetto può essere addebitabile o non addebitabile nel contesto di una specifica riga di offerta basata su progetto, il che rende possibile la seguente configurazione.

Se una riga di offerta basata su progetto include **Tempo** e l'attività **T1**, l'attività è associata alla riga di offerta come addebitabile. Se è presente una seconda riga di offerta che include **Spese**, puoi associare l'attività **T1** nella riga di offerta come non addebitabile. Il risultato è che tutto il tempo registrato sull'attività è addebitabile e tutte le spese registrate sull'attività non sono addebitabili.

Il tipo di fatturazione di un'attività può essere configurato nella scheda **Attività addebitabili** di una riga di offerta basata su progetto aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Attività riga offerta**. In alternativa, puoi aggiornare il tipo di fatturazione per un'attività di progetto nel campo **Tipo di fatturazione** nella griglia secondaria dell'impostazione fatturazione attività di un progetto che mostra le righe di offerta associate a un'attività.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aggiornare un ruolo in modo che sia addebitabile o non addebitabile

Un ruolo può essere addebitabile o non addebitabile nel contesto di una specifica riga di offerta basata su progetto.

Il tipo di fatturazione di un ruolo può essere configurato nella scheda **Ruoli addebitabili** di una riga di offerta aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Ruoli addebitabili**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aggiornare una categoria di transazione in modo che sia addebitabile o non addebitabile

Una categoria di transazione può essere addebitabile o non addebitabile su una specifica riga di offerta.

Il tipo di fatturazione di una transazione può essere configurato nella scheda **Categorie addebitabili** di una riga di offerta aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Categorie addebitabili**.

### <a name="resolve-chargeability"></a>Risolvere l'esigibilità
Una stima o un valore effettivo creato per il tempo sarà considerato addebitabile solo se:

   - **Tempo** è incluso nella riga di offerta.
   - **Ruolo** è configurato come addebitabile nella riga di offerta.
   - **Attività incluse** è impostato su **Attività selezionate** nella riga di offerta. 

Se queste tre condizioni sono soddisfatte, anche l'**Attività** è configurata come addebitabile. 

Una stima o un valore effettivo creato per le spese è considerato addebitabile solo se: 

   - **Spesa** è incluso nella riga di offerta.
   - **Categoria di transazione** è configurato come addebitabile nella riga di offerta.
   - **Attività incluse** è impostato su **Attività selezionate** nella riga di offerta.

Se queste tre condizioni sono soddisfatte, anche l'**Attività** è configurata come addebitabile. 

Una stima o un valore effettivo creato per il materiale sarà considerato addebitabile solo se:

   - **Materiali** è incluso nella riga di offerta.
   - **Attività incluse** è impostato su **Attività selezionate** nella riga di offerta.

Se queste due condizioni sono soddisfatte, anche l'**Attività** deve essere configurata come addebitabile. 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Include Tempo</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Include Spesa</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Include Materiali</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Attività incluse</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ruolo</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Categoria.</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Attività</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Impatto esigibilità</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sì </p>
            </td>
            <td width="78" valign="top">
                <p>
Sì </p>
            </td>
            <td width="63" valign="top">
                <p>
Sì </p>
            </td>
            <td width="75" valign="top">
                <p>
Progetto intero </p>
            </td>
            <td width="65" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="70" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="65" valign="top">
                <p>
Non può essere impostato </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: addebitabile </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: addebitabile </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: addebitabile </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sì </p>
            </td>
            <td width="78" valign="top">
                <p>
Sì </p>
            </td>
            <td width="63" valign="top">
                <p>
Sì </p>
            </td>
            <td width="75" valign="top">
                <p>
Solo le attività selezionate </p>
            </td>
            <td width="65" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="70" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="65" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: addebitabile </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: addebitabile </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: addebitabile </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sì </p>
            </td>
            <td width="78" valign="top">
                <p>
Sì </p>
            </td>
            <td width="63" valign="top">
                <p>
Sì </p>
            </td>
            <td width="75" valign="top">
                <p>
Solo le attività selezionate </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non addebitabile</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="65" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: addebitabile </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: addebitabile </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sì </p>
            </td>
            <td width="78" valign="top">
                <p>
Sì </p>
            </td>
            <td width="63" valign="top">
                <p>
Sì </p>
            </td>
            <td width="75" valign="top">
                <p>
Solo le attività selezionate </p>
            </td>
            <td width="65" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="70" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non addebitabile</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: <strong>non addebitabile</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sì </p>
            </td>
            <td width="78" valign="top">
                <p>
Sì </p>
            </td>
            <td width="63" valign="top">
                <p>
Sì </p>
            </td>
            <td width="75" valign="top">
                <p>
Solo le attività selezionate </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non addebitabile</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non addebitabile</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: <strong>non addebitabile</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sì </p>
            </td>
            <td width="78" valign="top">
                <p>
Sì </p>
            </td>
            <td width="63" valign="top">
                <p>
Sì </p>
            </td>
            <td width="75" valign="top">
                <p>
Solo le attività selezionate </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non addebitabile</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Non addebitabile</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: addebitabile </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Sì </p>
            </td>
            <td width="63" valign="top">
                <p>
Sì </p>
            </td>
            <td width="75" valign="top">
                <p>
Progetto intero </p>
            </td>
            <td width="65" valign="top">
                <p>
Non può essere impostato </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Addebitabile</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Non può essere impostato </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: <strong>non disponibile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: addebitabile </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: addebitabile </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Sì </p>
            </td>
            <td width="63" valign="top">
                <p>
Sì </p>
            </td>
            <td width="75" valign="top">
                <p>
Progetto intero </p>
            </td>
            <td width="65" valign="top">
                <p>
Non può essere impostato </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Non addebitabile</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Non può essere impostato </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: <strong>non disponibile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: addebitabile </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sì </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Sì </p>
            </td>
            <td width="75" valign="top">
                <p>
Progetto intero </p>
            </td>
            <td width="65" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="70" valign="top">
                <p>
Non può essere impostato </p>
            </td>
            <td width="65" valign="top">
                <p>
Non può essere impostato </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: addebitabile </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: <strong>non disponibile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: addebitabile </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sì </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Sì </p>
            </td>
            <td width="75" valign="top">
                <p>
Progetto intero </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non addebitabile</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Non può essere impostato </p>
            </td>
            <td width="65" valign="top">
                <p>
Non può essere impostato </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: <strong>non disponibile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: addebitabile </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sì </p>
            </td>
            <td width="78" valign="top">
                <p>
Sì </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Progetto intero </p>
            </td>
            <td width="65" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="70" valign="top">
                <p>
Addebitabile </p>
            </td>
            <td width="65" valign="top">
                <p>
Non può essere impostato </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: addebitabile </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: addebitabile </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: <strong>non disponibile</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sì </p>
            </td>
            <td width="78" valign="top">
                <p>
Sì </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Progetto intero </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non addebitabile</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Non addebitabile</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Non può essere impostato </p>
            </td>
            <td width="350" valign="top">
                <p>
Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: <strong>non disponibile</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
