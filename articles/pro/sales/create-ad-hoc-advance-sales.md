---
title: Creare un anticipo ad hoc su un contratto
description: Questo argomento fornisce informazioni sulla creazione di un anticipo su un contratto secondo necessità.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bceed1372dbaf523426a4c34da7152d77fe108240c8c3e4e1390c43b1cf536a4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999141"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Creare un anticipo ad hoc su un contratto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Microsoft Dynamics 365 Project Operations supporta scenari di fatturazione che coinvolgono pagamenti anticipati e anticipi. Il processo per l'utilizzo di **Anticipi** in **Project Operations** è simile ai contratti **Acconto**. 

Completa i passaggi seguenti per fatturare un anticipo al cliente.

1. Vai alla pagina **Contratto di progetto** quindi seleziona la scheda **Anticipi e acconti**.
2. Nella griglia secondaria che elenca tutti gli anticipi e gli anticipi registrati in precedenza, seleziona **+ Nuovo acconto di contratto di progetto**. 

    Viene visualizzato il modulo **Creazione rapida** per registrare un pagamento anticipato o un anticipo.
    
3. La tabella seguente elenca i campi per la registrazione di un anticipo e le considerazioni da tenere presenti durante la creazione di nuovi:

    | Campo | Descrizione | Impatto downstream |
    | --- | --- | --- |
    | **Cliente contratto di progetto** | Questo campo indica a quale cliente del contratto verrà fatturato questo anticipo. | Se hai più clienti nel contratto e vuoi fatturare a ciascuno di essi un acconto o un importo anticipato specifico, crea un anticipo per ogni cliente individualmente. |
    | **Descrizione** | La descrizione dello scopo o della tempistica dell'anticipo per aiutare a identificare questo anticipo. | Questa descrizione viene visualizzata nella riga di fattura per questo anticipo. |
    | **Importo** | L'importo per il pagamento anticipato o l'anticipo. | Quest importo viene visualizzato nella riga di fattura per questo anticipo. |
    | **Data fattura** | La data in cui tale anticipo viene fatturato al cliente. | Questa è la data in cui il processo di creazione automatica della fattura crea una riga di fattura per questo anticipo. |
    | **Stato fattura** | Questa è un'impostazione dell'opzione che indica se questo anticipo viene aggiunto a una bozza di fattura per questo cliente. I valori possibili sono:</br>- **Non pronto per la fatturazione**</br>- **Pronto per la fatturazione** | Quando un anticipo o un pagamento anticipato è contrassegnato come **Pronto per la fatturazione**, viene aggiunto come riga di ora su una bozza di fattura. Solo un anticipo completamente fatturato può essere utilizzato per riconciliare i costi del progetto per il periodo di fatturazione successivo. |

4. Seleziona **Salva e chiudi** nella finestra di dialogo di creazione rapida per registrare l'anticipo o il pagamento anticipato.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]