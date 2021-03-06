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
# <a name="per-diems"></a>Diaria

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_


Una diaria è un'indennità pagata a un lavoratore che viaggia per lavoro. In Gestione spese, è possibile creare regole per la diaria per varie situazioni di viaggio. Le tariffe giornaliere possono essere basate sul periodo dell'anno, sulla destinazione del viaggio o su entrambi. Quando crei una regola per la diaria, puoi specificare che una percentuale della tariffa giornaliera sarà trattenuta se un lavoratore riceve vitto o servizi gratuiti. È inoltre possibile impostare un numero minimo e massimo di ore che la tariffa giornaliera può applicare al viaggio di un lavoratore.

## <a name="configuration"></a>Configurazione 

1. Per aggiungere destinazioni delle trasferte giornaliere, vai a **Imposta** > **Calcoli e codici** > **Destinazioni trasferte giornaliere**.
2. Per ciascuna delle destinazioni aggiunte sopra, seleziona una tariffa giornaliera e una valuta valide tra una data di inizio e una data di fine specifiche per hotel, vitto e altre spese. Le tariffe giornaliere e le valute sono configurate in **Imposta** > **Calcoli e codici** > **Trasferte giornaliere**.
3. Nella pagina **Destinazioni trasferte giornaliere**, configura i livelli di tariffe giornaliere. I livelli di tariffe giornaliere consentono di definire la ripartizione percentuale di un'indennità giornaliera per hotel, vitto e altre spese. 
4. Per specificare la riduzione percentuale del vitto per colazione, pranzo o cena, aggiorna i campi nella pagina **Parametri di gestione spese** nella scheda **Diaria**. 
    
## <a name="submit-expenses-using-per-diem"></a>Inviare le spese utilizzando la diaria
Per inviare le spese utilizzando le diarie, utilizza la categoria di spesa **Diaria** quando crei una nota spese. Inserisci la **Data inizio trasferta giornaliera**, la **Data fine trasferta giornaliera** e la **Destinazione trasferta giornaliera**. L'importo verrà calcolato in base alle tariffe giornaliere per la destinazione selezionata e la riduzione per il vitto verrà calcolata in base ai livelli delle tariffe giornaliere.
