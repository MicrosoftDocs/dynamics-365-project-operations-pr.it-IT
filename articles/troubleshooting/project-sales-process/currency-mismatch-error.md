---
title: Errore di corrispondenza valuta
description: Questo articolo fornisce informazioni sulla risoluzione dei problemi su un errore di mancata corrispondenza della valuta che si verifica quando si salvano tipi di record specifici.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914729"
---
# <a name="currency-mismatch-error"></a>Errore di corrispondenza valuta 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Quando salvi un progetto, un contratto, un preventivo o una risorsa prenotabile, potresti ricevere l'errore **La valuta della società proprietaria dell'offerta non corrisponde alla valuta dell'unità contratto. Per continuare, scegli una società proprietaria o un'unità contratto per l'offerta diversa**. Ciò avviene perché esiste una discrepanza tra la valuta dell'unità contratto per il record e la valuta della società proprietaria.


## <a name="resolution"></a>Risoluzione

Per risolvere questo problema, procedi come segue:
- Verifica la valuta dell'unità contratto per questo record. Puoi vedere la valuta aprendo il record dell'unità organizzativa e verificando il valore nella scheda **Generale**, nel campo **Valuta**.
- Verifica la valuta della società proprietaria. Puoi vedere la valuta andando in **Correlato** > **Movimenti contabili** nel record della società. Fai doppio clic sul record del movimento contabile associato alla società e verifica il valore nella scheda **Generale**, nel campo **Valuta di contabilizzazione**.

Se la valuta impostata nell'unità contratto e il record del movimento contabile non corrispondono, modifica la configurazione o seleziona valori diversi quando salvi il record. Il sistema richiede che questi record corrispondano per garantire flussi di fatturazione interaziendali corretti. Per ulteriori informazioni sulle configurazioni interaziendali, vedi [Creare transazioni interaziendali](../../project-accounting/create-intercompany-transactions.md).

Se al record della società non è associato alcun record di movimento contabile, manca una configurazione per l'impostazione dell'ambiente. La configurazione deve essere corretta dall'amministratore di sistema. L'amministratore di sistema deve andare in **Configurazioni a doppia scrittura** e arrestare e riavviare **Mappa doppia scrittura movimenti contabili** con la sincronizzazione iniziale di questa mappa e dei prerequisiti. Per ulteriori informazioni, vedi [Versioni della mappa a doppia scrittura di Project Operations](../../environment/resource-dual-write-maps.md).
