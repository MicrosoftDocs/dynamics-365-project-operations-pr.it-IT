---
title: Registrare le note spese
description: Questo articolo spiega come registrare le note spese.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524874"
---
# <a name="post-expense-reports"></a>Registrare le note spese

Dopo che una nota spese è stata approvata e trasferita al giornale di registrazione generale, può essere registrata. Quando si registra una nota spese, vengono identificate le spese idonee per il recupero dell'imposta sul valore aggiunto (IVA). Il compito di verificare e recuperare i pagamenti IVA è assegnato al dipendente che è responsabile della verifica della nota spese.

Se le spese in una nota spese vengono addebitate a un'azienda diversa dall'azienda che impiega il dipendente, è necessario verificare sia l'azienda a cui sono dovute tali spese sia l'azienda da cui sono dovute. Ad esempio, il dipendente che ha inviato una nota spese lavora per l'azienda DAT ma ha addebitato una spesa all'azienda DIR. In questo caso, DAT è l'azienda a cui è dovuta la spesa e DIR è l'azienda da cui è dovuta la spesa. Dopo aver verificato queste righe del giornale di registrazione, è possibile registrare le righe di spesa nella contabilità generale.

Per registrare una nota spese, nella pagina **Note spese approvate** seleziona la nota spese, quindi nel riquadro Azioni seleziona **Registra**.

È inoltre possibile registrare contemporaneamente tutte le note spese dell'elenco. Seleziona tutte le note spese, quindi seleziona **Registra**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Abilitare la funzionalità Possibilità di registrare la passività di spesa nella valuta del fornitore per il metodo di pagamento in contanti

La funzionalità **Possibilità di registrare la passività di spesa nella valuta del fornitore per il metodo di pagamento in contanti** consente di registrare le note spese nella valuta del fornitore per il metodo di pagamento in contanti.

Attualmente, quando invii le spese in contanti, le note spese vengono registrate nella valuta di contabilizzazione. A causa della conversione dell'importo tra la valuta della transazione, la valuta di contabilizzazione e la valuta del fornitore, ai fornitori viene pagato un importo errato se la data di transazione della spesa e la data di pagamento effettiva hanno tassi di cambio differenti.

Questa funzionalità garantirà che il saldo fornitore venga registrato nella valuta del fornitore al momento della registrazione della nota spese.

1. Vai ad **Aree di lavoro** \> **Gestione funzionalità**.
2. Nell'elenco, trova e seleziona **Possibilità di registrare la passività di spesa nella valuta del fornitore per il metodo di pagamento in contanti**, quindi seleziona **Abilita ora**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
