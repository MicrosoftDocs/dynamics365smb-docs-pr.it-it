---
title: Importare i dati di gestione legacy in Dynamics 365 | Documenti Microsoft
description: "È possibile migrare i dati relativi a clienti, fornitori e magazzino, ad esempio, da Excel, QuickBooks o Dynamics GP in Dynamics 365."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: QuickBooks, transfer, import, migrate, initialize, implement
ms.date: 09/25/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 3f1df4bf771586c5e3e4d79d23c26051bf19c763
ms.contentlocale: it-it
ms.lasthandoff: 11/10/2017

---
# <a name="importing-business-data-from-other-finance-systems"></a>Importazione dei dati aziendali da altri sistemi contabili
Quando ci si iscrive a [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile scegliere di creare una società vuota nella quale caricare i propri dati e testare la nuova società in [!INCLUDE[d365fin](includes/d365fin_md.md)]. A seconda della soluzione contabile che l'azienda utilizza correntemente, è possibile trasferire le informazioni sui conti clienti, fornitori, magazzino e bancari.  

Dalla pagina home è possibile avviare una guida al setup assistito che aiuta a trasferire i dati aziendali da un file di Excel o da altri formati. Il tipo di file che è possibile caricare dipende dalle estensioni disponibili. Ad esempio, è possibile migrare i dati da QuickBooks perché [!INCLUDE[d365fin](includes/d365fin_md.md)] include un'estensione che gestisce la conversione da QuickBooks. Se si desidera migrare i dati da altre soluzioni contabili, è necessario verificare se è disponibile un'estensione per quella soluzione oppure importare da Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] include modelli per i conti, i clienti, i fornitori e gli articoli di magazzino collegabili quando si importano i dati.  

## <a name="importing-data-from-quickbooks-desktop-quickbooks-online-or-dynamics-gp"></a>Importazione di dati da QuickBooks Desktop, QuickBooks Online o Dynamics GP
Se al momento l'azienda utilizza QuickBooks o Dynamics GP, è possibile esportare le informazioni pertinenti in un file. Per trasferire i dati è possibile aprire la guida al setup assistito.
Ad esempio, se il file include clienti e fornitori, è possibile scegliere di trasferire solo i dati dei clienti. Il resto delle informazioni può essere trasferito in un secondo momento.  

Il setup assistito include un'opzione che consente di modificare la configurazione predefinita del trasferimento, ma consigliamo di utilizzare questo setup avanzato solo se si ha familiarità con le tabelle di database. Nella maggioranza delle aziende la mappatura predefinita da QuickBooks o Dynamics GP a [!INCLUDE[d365fin](includes/d365fin_md.md)] trasferirà le informazioni desiderate.  

Per ulteriori informazioni, vedere [Migrazione dei dati di QuickBooks Desktop](ui-extensions-quickbooks-data-migration.md), [Migrazione dei dati di QuickBooks Online](ui-extensions-quickbooks-online-data-migration.md) o [Migrazione dei dati di Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="importing-data-from-configuration-packages"></a>Importazione di dati dei pacchetti di configurazione
[!INCLUDE[d365fin](includes/d365fin_md.md)] include un pacchetto di configurazione che è possibile esportare in Excel, nelle cui tabelle impostare i dati. Quindi, è possibile importare nuovamente i dati da Excel. Il pacchetto è costituito da 27 tabelle, inclusi i dati master, quali clienti, fornitori, articoli e conti, altre tabelle di setup di base, quali i metodi di spedizione, e le tabelle di transazioni, ad esempio intestazioni e righe delle vendite.  

> [!NOTE]  
>   L'utilizzo dei pacchetti di configurazione è una funzionalità avanzata, pertanto si raccomanda di contattare l'amministratore. Per ulteriori informazioni, vedere [Importazioni di dati del software di contabilizzazione legacy utilizzando un pacchetto di configurazione](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Vedi anche
[Finanza](finance.md)  
[Importazione di dati del software di contabilizzazione legacy utilizzando un pacchetto di configurazione](across-import-data-configuration-packages.md)  
[Migrazione dei dati QuickBooks Desktop](ui-extensions-quickbooks-data-migration.md)  
[Migrazione dei dati online QuickBooks](ui-extensions-quickbooks-online-data-migration.md)  
[Migrazione dei dati Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)   
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

