---
title: Creare una nuova società con i pacchetti di configurazione
description: Usa le tabelle e le pagine di RapidStart Services per creare una nuova società per la quale vuoi effettuare l'implementazione di un cliente.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 2d75c136fdd0dcf2891468d722008ab0bf183cbb
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512414"
---
# <a name="create-a-new-company-based-on-configuration-packages"></a>Creare una nuova società basata sui pacchetti di configurazione

Per utilizzare RapidStart Services per [!INCLUDE[prod_short](includes/prod_short.md)], è necessario dapprima creare una nuova società per la quale si desidera effettuare l'implementazione di un cliente. Quando si crea una nuova società, le tabelle e le pagine standard di [!INCLUDE[prod_short](includes/prod_short.md)] vengono create, ma non sono disponibili dati al loro interno.

Inoltre, è possibile collegare dati di setup specifici alla società dopo l'inizializzazione. Le informazioni vengono fornite in un pacchetto di configurazione, un file con estensione rapidstart che offre il contenuto in un formato compresso.  

Pacchetti di configurazione di esempio, inclusi i file specifici di ciascun paese/regione, sono inclusi nella società demo CRONUS. Attenersi alle procedure riportate di seguito per utilizzare il pacchetto di configurazioni di esempio con una nuova società.  

## <a name="to-use-the-sample-configuration-packages"></a>Per utilizzare i pacchetti di configurazione di esempio

1. Apri la società di dimostrazione CRONUS. Per ulteriori informazioni, vedere [Modificare le impostazioni di base](ui-change-basic-settings.md).  
2. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Pacchetti di configurazione**, quindi scegli il collegamento correlato.  
3. Sceglie il pacchetto rilevante dalla lista, quindi scegli l'azione **Esporta pacchetto**.  

Attieniti alla procedura riportata di seguito per creare una nuova società e utilizzare il pacchetto di configurazione come parte del processo.  

## <a name="to-create-a-new-company"></a>Per creare una nuova società

1. Creare una nuova società. Per ulteriori informazioni, vedere [Creazione di nuove società in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).
2. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Pacchetti di configurazione**, quindi scegli il collegamento correlato.  
3. Scegli l'azione **Importa pacchetto** e specifica il file .rapidstart che vuoi importare.  

Dopo aver creato una nuova società, le tabelle vengono automaticamente compilate, anche se non esiste alcun modello della società collegato. Ad esempio, è possibile esaminare i codici standard per transazioni di registrazione e batch nella pagina **Codice origine**. Se si immette una versione locale di [!INCLUDE[prod_short](includes/prod_short.md)], è consigliabile verificare la tabella e considerare eventuali problemi relativi alla lingua locale.

## <a name="about-data-tables"></a>Informazioni sulle tabelle dati

Le tabelle dati di [!INCLUDE[prod_short](includes/prod_short.md)] presentano due tipologie di base: master e setup. Quando si imposta una configurazione di società, è possibile utilizzare queste tipologie per identificare la strategia di configurazione.  

### <a name="master-data-tables"></a>Tabelle di dati master

Nella seguente tabella vengono elencati alcuni esempi di tabelle di dati master. Quando si inizializza una nuova società, queste tabelle sono vuote.  

|Nr. tabella|Nome tabella|  
|-------------------|--------------------|  
|15|Conto C/G|  
|18|Cliente|  
|23|Fornitore|  
|27|Articolo|  
|5050|Contatto|  

### <a name="setup-data-tables"></a>Tabelle dati di setup

Nella seguente tabella vengono elencate tabelle dei dati di setup, dove vengono acquisite le informazioni di impostazione nel questionario di configurazione. Queste tabelle contengono informazioni di base al momento della creazione della società.  

|Nr. tabella|Nome tabella|  
|-------------------|--------------------|  
|98|Setup contabilità generale|  
|311|Setup contabilità clienti|  
|312|Setup contabilità fornitori|  
|313|Setup magazzino|  

Oltre alle tabelle dei dati di setup, in [!INCLUDE[prod_short](includes/prod_short.md)] sono presenti tabelle dati di tipo setup che specificano le informazioni principali relative alla società e ai relativi processi aziendali. La tabella riportata di seguito ne elenca alcuni.  

|Nr. tabella|Nome tabella|  
|-------------------|--------------------|  
|3|Condizioni pagamento|  
|4|Valuta|  
|6|Gruppi prezzi cliente|  
|5700|Unità di stockkeeping|

## <a name="see-also"></a>Vedi anche

[Applicazione della configurazione a nuove società](admin-apply-configuration-to-new-companies.md)  
[Impostazione di una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]