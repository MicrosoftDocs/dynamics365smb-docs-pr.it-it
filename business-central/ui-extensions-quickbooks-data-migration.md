---
title: Utilizzo dell'estensione per la migrazione QuickBooks | Documenti Microsoft
description: Descrive come utilizzare l'estensione per importare clienti, fornitori, articoli e conti da QuickBooks Desktop a Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e53db4c1eef2a2f158f289e9f89ad291436a9b1a
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="the-quickbooks-data-migration-extension-for-business-central"></a>Estensione di migrazione dei dati QuickBooks per Business Central
Questa estensione consente di eseguire la migrazione di clienti, fornitori, articoli e conti da QuickBooks [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se l'azienda al momento utilizza QuickBooks, è possibile esportare le informazioni rilevanti e aprire una guida al setup assistito per caricare i dati in [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Per ulteriori informazioni, vedere [Importazione dei dati aziendali da altri sistemi contabili](upload-data.md).

## <a name="exporting-data-from-quickbooks-desktop"></a>Esportazione di dati da QuickBooks Desktop
È necessario aver esportato alcuni o tutti i clienti, i fornitori, gli articoli di magazzino e i conti esistenti in un file IIF (Intuit Interchange Format). L'estensione per la migrazione dei dati QuickBooks include una mappatura predefinita dei dati QuickBooks affinché i dati esistenti possano essere utilizzati per testare la nuova azienda con [!INCLUDE[d365fin](includes/d365fin_md.md)]. La mappatura predefinita sarà sufficiente nella maggior parte dei casi, ma è possibile modificare la mappatura nella guida al setup assistito.  
Nel menu File di QuickBooks è presente un'utilità per l'esportazione di elenchi. Ai fini di [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile esportare i seguenti elenchi:

* Lista clienti  
* Lista fornitori  
* Elenco articoli  
* Lista conti  

I dati esportati vengono salvati come file IIF, che può essere successivamente caricato in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="finding-the-quickbooks-data-migration-extension"></a>Utilizzo dell'estensione per la migrazione dei dati QuickBooks
L'estensione per la migrazione dei dati QuickBooks si trova nella Guida setup assistito Migrazione dati ed è pronta all'uso. Per utilizzare l'estensione dopo aver esportato i dati da QuickBooks, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup assistito**, quindi scegliere il collegamento correlato. Scegliere **Migra dati aziendali**, quindi seguire i passaggi nella guida.  

## <a name="see-also"></a>Vedi anche
[Importazione dei dati aziendali da altri sistemi contabili](upload-data.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)  

