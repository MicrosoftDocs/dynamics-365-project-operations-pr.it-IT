---
title: Applicare i dati dimostrativi di Project Operations a un ambiente ospitato su cloud di Finance
description: Questo argomento spiega come applicare i dati dimostrativi da Project Operations a un ambiente ospitato su cloud di Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096627"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a>Applicare i dati dimostrativi di Project Operations a un ambiente ospitato su cloud di Finance

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

> [!IMPORTANT]
> Questo argomento si applica solo a Microsoft Dynamics 365 Finance versione 10.0.13 e può essere eseguito solo su un ambiente ospitato su cloud. Completa i passaggi in questo argomento **PRIMA** di applicare aggiornamenti di qualità all'ambiente.

1. Nel progetto LCS, apri la pagina **Dettagli ambiente**. Questa include i dettagli necessari per connettersi all'ambiente utilizzando Remote Desktop Protocol (RDP).

![Dettagli degli ambienti ](./media/1EnvironmentDetails.png)

Il primo set di credenziali evidenziate sono le credenziali dell'account locale e contengono un collegamento ipertestuale alla connessione Desktop remoto. Le credenziali includono il nome utente e la password dell'amministratore dell'ambiente. Il secondo set di credenziali viene utilizzato per accedere a SQL Server in questo ambiente.

2. Collegati in remoto all'ambiente tramite il collegamento ipertestuale in **Account locali** e utilizza le **Credenziali account locale** per l'autenticazione.
3. Vai a **Internet Information Services** > **Pool di applicazioni** > **AOSService** e arresta il servizio. A questo punto arresta il servizio in modo da poter continuare a sostituire il database SQL.

![Arrestare AOS](./media/2StopAOS.png)

4. Vai a **Servizi** e arresta i seguenti due elementi:

- Microsoft Dynamics 365 Unified Operations: Batch Management Service
- Microsoft Dynamics 365 Unified Operations: Data Import Export Framework

![Arrestare i servizi](./media/3StopServices.png)

5. Apri Microsoft SQL Server Management Studio. Accedi con le credenziali del server SQL e utilizza l'utente e la password di axdbadmin dalla pagina LCS **Dettagli ambienti**.

![SQL Server Management Studio](./media/4SSMS.png)

6. In Esplora oggetti, **Database** e individua **AXDB**. Sostituirai il database con un nuovo database che si trova nell'[Area download](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Copia il file zip nella VM a cui sei collegato in remoto ed estrai il contenuto dello zip.
8. In SQL Server Management Studio, fai clic con il pulsante destro del mouse su **AxDB** e quindi seleziona **Attività** > **Ripristina** > **Database**.

![Ripristina database](./media/5RestoreDatabase.png)

9. Seleziona **Dispositivo di origine** e vai al file estratto dallo zip che hai copiato.

![Dispositivi di origine](./media/6SourceDevice.png)

10. Seleziona **Opzioni** e quindi seleziona **Sovrascrivi database esistente** e **Chiudi connessioni esistenti al database di destinazione**. 
11. Seleziona **OK**.

![Ripristinare le impostazioni](./media/7RestoreSetting.png)

Riceverai la conferma che il ripristino AXDB è andato a buon fine. Dopo aver ricevuto questa conferma, puoi chiudere SQL Services Management Studio.

12. Torna a **Internet Information Services** > **Pool di applicazioni** > **AOSService** e avvia AOSService.
13. Vai a **Servizi** e avvia i due servizi che hai arrestato in precedenza.

14. Individua lo strumento AdminUserProvisioning su questa VM. Guarda in K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Esegui il file .ext utilizzando il tuo indirizzo utente nel campo **Indirizzo e-mail**. 
16. Seleziona **Invia**.

![Provisioning utente amministratore](./media/8AdminUserProvisioning.png)

Questo processo richiede un paio di minuti per il completamento. Dovresti ricevere un messaggio di conferma che l'utente amministratore è stato aggiornato correttamente.

17. Infine, esegui il prompt dei comandi come amministratore ed esegui iisreset

![Ripristino IIS](./media/9IISReset.png)

18. Chiudi la sessione Desktop remoto e utilizza la pagina **Dettagli ambiente** di LCS per accedere all'ambiente e confermare che funzioni come previsto.

![Finance and Operations](./media/10FinanceAndOperations.png)
