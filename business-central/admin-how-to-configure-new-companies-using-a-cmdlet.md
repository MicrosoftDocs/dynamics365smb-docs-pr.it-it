---
title: "Configurare le nuove società utilizzando un cmdlet | Documenti Microsoft"
description: "In vari scenari è possibile che si desideri caricare e importare un pacchetto di configurazione senza coinvolgere gli utenti o utilizzare l'interfaccia utente di RapidStart Services. A tal fine, utilizzare un cmdlet di Windows PowerShell."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ce8bfdb40d8d428f4b02abcbba4498d58d6481be
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a>Configurare nuove società utilizzando un cmdlet
In vari scenari è possibile che si desideri caricare e importare un pacchetto di configurazione senza coinvolgere gli utenti o utilizzare l'interfaccia utente di RapidStart Services. A tal fine, utilizzare un cmdlet di Windows PowerShell. Gli scenari in cui questo può risultare utile includono:  

- Eseguire l'importazione di dati tra più installazioni di [!INCLUDE[d365fin](includes/d365fin_md.md)].
- Configurazione delle aree di applicazione aggiuntive per più clienti.  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a>Per distribuire un pacchetto di configurazione utilizzando un cmdlet  

1. Preparare un pacchetto di RapidStart Services. Ad esempio, è possibile creare un pacchetto per importare determinati valori e i nomi della tabella e dei campi in cui inserire tali valori.  
2. Installare il pacchetto in un computer in cui verrà eseguito il cmdlet.  
3. Aprire [!INCLUDE[d365fin](includes/d365fin_md.md)] Administration Shell.  
4. Immettere **Invoke-NAVCodeUnit** e specificare le informazioni simili al seguente esempio.  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
Il cmdlet consente di importare il pacchetto in ogni società. Gli utenti possono iniziare a utilizzare la nuova funzionalità immediatamente.  

## <a name="see-also"></a>Vedi anche  
[Configurare nuove società](admin-how-to-configure-new-companies.md)  
[Applicazione della configurazione a nuove società](admin-apply-configuration-to-new-companies.md)  
[Impostare una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)  
[Microsoft Dynamics NAV - Cmdlet di Windows PowerShell](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

