---
title: Impostazione di una società con RapidStart Services
description: Puoi creare una nuova società in Business Central con RapidStart Services per migliorare la produttività automatizzando e semplificando le attività ricorrenti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 8610, 8614, 8615, 8620, 8632
ms.date: 03/28/2022
ms.author: edupont
ms.openlocfilehash: b2d3378e9c06221bc91977883a53bba8514c6afc
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518313"
---
# <a name="set-up-a-company-with-rapidstart-services"></a>Impostazione di una società con RapidStart Services

È possibile impostare una nuova società in [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando RapidStart Services, uno strumento progettato per accelerare i tempi di distribuzione, migliorare la qualità dell'implementazione, introdurre un approccio ripetibile alle implementazioni e migliorare la produttività mediante l'automazione e la semplificazione di task ricorrenti.  

Usa queste funzionalità per scalare la tua attività come rivenditore. La maggior parte delle pagine si applica a entrambi [!INCLUDE [prod_short](includes/prod_short.md)] online e in locale. Tuttavia, alcuni processi si basano sull'accesso ai file su disco e sono troppo complessi per essere utilizzati in [!INCLUDE [prod_short](includes/prod_short.md)] online. Per [!INCLUDE [prod_short](includes/prod_short.md)] in locale, probabilmente vorrai usare Windows PowerShell per distribuire. Per ulteriori informazioni, vedi [Amministrazione di Business Central in locale](/dynamics365/business-central/dev-itpro/administration/administration) e [Amministrazione di Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration), rispettivamente.  

RapidStart Services consente di ottenere una panoramica del processo di setup della nuova società grazie a un prospetto in cui è possibile impostare le tabelle più frequentemente utilizzate nel processo di configurazione di nuove società. Nell'ambito di questa operazione, è possibile creare un questionario per assistere i clienti durante la raccolta delle informazioni relative al setup. I clienti possono scegliere di utilizzare il questionario per impostare le aree di applicazione o di aprire direttamente la pagina di setup e ed eseguire l'impostazione da questa posizione. È importante tenere presente che RapidStart Services consente ai clienti di preparare la società con i dati di setup di default che sarà possibile ottimizzare e personalizzare. Infine, quando si utilizza RapidStart Services, è possibile configurare ed eseguire la migrazione dei dati dei clienti esistenti, ad esempio una lista di clienti o articoli, alla nuova società.

È possibile utilizzare i componenti seguenti per accelerare il setup della società:  

- Configurazione guidata  
- Foglio di lavoro configurazione  
- Pacchetti di configurazione  
- Modelli di configurazione  
- Questionario sulla configurazione  

> [!Note]  
> Sono presenti aree di [!INCLUDE[prod_short](includes/prod_short.md)] che è necessario impostare manualmente. Comprendono l'aggiunta di utenti, l'impostazione dei periodi contabili e delle dimensioni per Business Intelligence. Per ulteriori informazioni, vedere [Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

|**Per**|**Vedere**|  
|------------|-------------|  
|Creare una nuova società e importare modelli e dati di setup di base.|[Impostare la configurazione della società](admin-set-up-company-configuration.md)|  
|Distribuire il pacchetto configurato al cliente per l'implementazione.|[Applicazione della configurazione a nuove società](admin-apply-configuration-to-new-companies.md)|
|Definire e convalidare i valori di setup del cliente per tutte le aree essenziali, quali informazioni sulla società, contabilità generale, magazzino, vendita o produzione.|[Raggruppare i valori di setup del cliente](admin-gather-customer-setup-values.md)|  
|Configurare i record dei dati master utilizzando modelli per preparare la migrazione dei dati clienti esistenti.|[Preparazione per la migrazione dei dati dei clienti](admin-use-templates-to-prepare-customer-data-for-migration.md)|  
|Definire tabelle e campi, convalidare dati clienti esistenti ed eseguire la migrazione di dati nel database di [!INCLUDE[prod_short](includes/prod_short.md)].|[Eseguire la migrazione dei dati dei clienti](admin-migrate-customer-data.md)|
|Prepararsi a riutilizzare le configurazioni aziendali in altre società (nei contenuti per sviluppatori e amministratori).|[Creare pacchetti di configurazione di società personalizzati](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)|
|Trovare soluzioni ai problemi noti nel toolkit RapidStart Services.|[Suggerimenti e consigli: RapidStart Services](admin-tips-and-tricks-rapidstart-services.md)|  

## <a name="see-also"></a>Vedere anche

[Amministrazione](admin-setup-and-administration.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Impostare aree di applicazione complesse utilizzando le procedure ottimali](set-up-complex-application-areas-using-best-practices.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]