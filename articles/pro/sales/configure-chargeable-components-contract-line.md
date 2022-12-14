---
title: Configurare componenti addebitabili di una voce di contratto di progetto
description: In questo articolo vengono fornite informazioni su come aggiungere componenti addebitabili alle righe di contratto in Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 33296c93964cc88499e7a98d499b99463e59d62a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825569"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Configurare componenti addebitabili di una voce di contratto di progetto

_**Si applica a:** Distribuzione lite: dalla transazione alla fatturazione proforma, Project Operations per scenari basati su risorse/materiali non stoccati_

Una voce di contratto di progetto ha i componenti *inclusi* e *addebitabili*.

I componenti inclusi sono componenti soggetti a:

  - Metodo di fatturazione e suddivisioni dei clienti
  - Limite da non superare 
  - Impostazioni della frequenza della fattura definite nella voce di contratto basata su progetto

Un sottoinsieme dei componenti inclusi può essere contrassegnato come addebitabile usando il campo **Tipo di fatturazione**. Il campo **Tipo di fatturazione** è un set di opzioni che consente i seguenti valori nel contesto di una voce di contratto:

  - Addebitabile
  - Non addebitabile

I componenti addebitabili possono essere definiti sulle attività, sui ruoli e sulle categorie di transazioni.

L'esigibilità è definita nelle attività per una voce di contratto di progetto e si applica a tutte le classi di transazione incluse in quella riga. Se il campo **Includi attività** di una voce di contratto è vuoto o impostato su **Intero progetto**, la scheda **Attività addebitabili** non è disponibile.

L'esigibilità definita nei ruoli per una voce di contratto di progetto si applica solo alla classe di transazione **Tempo**. Se il campo **Includi tempo** di una voce di contratto è impostato su **No**, la scheda **Ruoli addebitabili** non è disponibile.

L'esigibilità è definita nelle categorie di transazione per una voce di contratto di progetto e si applica solo alla classe di transazione **Spesa**. Se il campo **Includi spese** è impostato su **No**, la scheda **Categorie addebitabili** non è disponibile.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Aggiornare un'attività di progetto in modo che sia addebitabile o non addebitabile

Un'attività di progetto può essere addebitabile o non addebitabile in una specifica voce di contratto, il che rende possibile la seguente configurazione:

Se una voce di contratto basata su progetto include **Tempo** e l'attività **T1** è associata ad essa come addebitabile. Se è presente una seconda voce di contratto che include **Spesa**, puoi associare l'attività T1 nella voce di contratto come non addebitabile. Il risultato è che tutto il tempo registrato sull'attività è addebitabile e tutte le spese non sono addebitabili.

Il tipo di fatturazione di un'attività può essere configurato nella scheda **Attività addebitabili** di una voce di contratto aggiornando il campo **Tipo di fatturazione** nella griglia secondaria delle attività voce di contratto. In alternativa, puoi aggiornare il campo **Tipo di fatturazione** nella griglia secondaria dell'impostazione fatturazione attività di un progetto che mostra le voci di contratto associate a un'attività.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Aggiornare un ruolo come addebitabile o non addebitabile

Un ruolo può essere addebitabile o non addebitabile su una specifica voce di contratto.

Il tipo di fatturazione di un ruolo può essere configurato nella scheda **Ruoli addebitabili** di una voce di contratto. Per fare ciò, aggiorna il campo **Tipo di fatturazione** nella griglia secondaria **Ruoli addebitabili**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Aggiornare una categoria di transazione come addebitabile o non addebitabile

Una categoria di transazione può essere addebitabile o non addebitabile su una specifica voce di contratto.

Il tipo di fatturazione di una transazione può essere configurato nella scheda **Categorie addebitabili** di una voce di contratto basata di progetto. Per fare ciò, aggiorna il campo **Tipo di fatturazione** nella griglia secondaria **Categorie addebitabili**.

### <a name="resolve-chargeability"></a>Risolvere l'esigibilità

Una stima o un valore effettivo creato per il tempo è considerato addebitabile solo se:

   - **Tempo** è incluso nella voce di contratto.
   - **Ruolo** è configurato come addebitabile nella voce di contratto.
   - **Attività incluse** è impostato su **Attività selezionate** nella voce di contratto.
 
 Se queste tre condizioni sono soddisfatte, anche l'attività è configurata come addebitabile. 

Una stima o un valore effettivo creato per le spese è considerato addebitabile solo se:

   - **Spesa** è incluso nella voce di contratto
   - **Categoria di transazione** è configurato come addebitabile nella voce di contratto
   - **Attività incluse** è impostato su **Attività selezionata** nella voce di contratto
  
 Se queste tre condizioni sono soddisfatte, l'**attività** è configurata come addebitabile. 

Una stima o un valore effettivo creato per il materiale è considerato addebitabile solo se:

   - **Materiali** è incluso nella voce di contratto
   - **Attività incluse** è impostato su **Attività selezionate** nella voce di contratto

Se queste due condizioni sono soddisfatte, l'**attività** è configurata come addebitabile. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Include il tempo</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Include la spesa</strong>
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
Fatturazione in base a valore effettivo tempo: <strong>addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: <strong>addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: <strong>addebitabile</strong>
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
Fatturazione in base a valore effettivo tempo: <strong>addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo spesa: <strong>addebitabile</strong>
                </p>
                <p>
Tipo di fatturazione in base a valore effettivo materiale: <strong>addebitabile</strong>
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
