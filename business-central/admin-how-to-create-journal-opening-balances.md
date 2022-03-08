---
title: Creare bilanci di apertura delle registrazioni | Documenti Microsoft
description: Business Central comprende diversi processi batch spediti al fine di agevolare il trasferimento dei saldi del conto esistenti a una società appena configurata. È possibile trasferire facilmente questi dati con le registrazioni.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5e1bb8e34e70d1d906850c157107b9b9701c6c50
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779859"
---
# <a name="create-journal-opening-balances"></a>Creare bilanci di apertura delle registrazioni

[!INCLUDE[prod_short](includes/prod_short.md)] comprende diversi processi batch spediti al fine di agevolare il trasferimento dei saldi del conto esistenti a una società appena configurata. È possibile trasferire questi dati con la registrazione di clienti, fornitori, magazzino o C/G.

Il primo passaggio consiste di creare un pacchetto di configurazione che include le tabelle di setup di queste registrazioni. La procedura seguente presuppone che questo passaggio sia completato. Per ulteriori informazioni, vedere [Impostare la configurazione della società](admin-set-up-company-configuration.md). Questa procedura descrive i passaggi successivi, tra cui il collegamento del pacchetto fornito da un partner.  

Prima di iniziare, assicurarsi di essere nella pagina Gestione ruolo utente Amministratore in quanto fornisce il contesto corretto per il lavoro di configurazione. Per ulteriori informazioni, vedere [Modificare le impostazioni di base](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Per collegare i movimenti in una registrazione a una nuova società

1. Configurare una nuova società e collegarla a un pacchetto di configurazione. Per ulteriori informazioni, vedere [Configurare una società con la procedura guidata RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    La nuova società non contiene informazioni sui bilanci di apertura delle registrazioni.  

2. Aprire il foglio di lavoro configurazione e importare dati esistenti relativi a clienti, articoli, fornitori, nonché la contabilità generale. Per ulteriori informazioni, vedere [Eseguire la migrazione dei dati dei clienti](admin-migrate-customer-data.md).  

    Ora i dati master sono in posizione. Successivamente, aggiungere i bilanci di apertura. I passaggi seguenti descrivono come creare righe di giornale di registrazione per conti CoGe, ma lo stesso si applica alla creazione di righe di giornale di registrazione per clienti, fornitori e articoli.  
3. Scegliere l'azione **Crea righe registrazioni conto C/G**.  
4. Compilare la Scheda dettaglio **Opzioni** come appropriato e impostare i filtri in base alle esigenze. Ad esempio, immettere un nome nel campo **Definizione registrazioni**.  
5. Scegliere il pulsante **OK**. I record sono ora contenuti nella registrazione, ma gli importi sono vuoti.  
6. Esportare la tabella delle registrazioni in Excel e immettere manualmente le informazioni relative a registrazioni e contropartita dei dati legacy.
7. Importare e collegare le informazioni della tabella nella nuova società. Le righe di registrazione sono pronte per la registrazione.  
8. Nel foglio di lavoro configurazione, selezionare la tabella delle righe di registrazione, quindi scegliere l'azione **Dati database**.  
9. Esaminare le informazioni, quindi scegliere l'azione **Registra**.  
10. Ripetere i passaggi per importare e registrare altri bilanci di apertura.  

> [!TIP]
> È possibile utilizzare gli stessi processi batch per aggiungere bilanci di apertura ogni volta che si registra un nuovo cliente o fornitore con cui già sono stati conclusi affari ma non è registrato in [!INCLUDE [prod_short](includes/prod_short.md)]. Basta cercare l'attività pertinente e quindi scegliere il collegamento pertinente.

## <a name="see-also"></a>Vedere anche

[Applicazione della configurazione a nuove società](admin-apply-configuration-to-new-companies.md)  
[Impostazione di una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]