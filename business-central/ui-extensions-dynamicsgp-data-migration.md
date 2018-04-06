---
title: Migrare i dati da Dynamics GP tramite l'estensione per la migrazione dei dati | Documenti Microsoft
description: Utilizzare l'estensione per la migrazione dei dati di Dynamics GP per migrare i dati relativi a clienti, fornitori, articoli di magazzino e conti da Dynamics GP a Business Central.
documentationcenter: 
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
ms.openlocfilehash: 5d689a43e3debe51cfbb9306252d0c9f75e7bb70
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-business-central"></a>Estensione di migrazione dei dati di Dynamics GP per Business Central 
Questa estensione consente di eseguire la migrazione di clienti, fornitori, articoli di magazzino e conti da Dynamics GP a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se l'azienda al momento utilizza Dynamics GP, è possibile esportare i record principali rilevanti e aprire una guida al setup assistito per aggiungere i dati in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Migrare i dati aziendali da altri sistemi contabili](upload-data.md).

## <a name="exporting-data-from-dynamics-gp"></a>Esportazione dei dati da Dynamics GP
È necessario avere esportato alcuni o tutti i clienti, i fornitori, gli articoli di magazzino e i conti esistenti su un file, utilizzando la funzionalità Dynamics GP per l'esportazione dei dati. Ai fini di [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile esportare i seguenti tipi di dati:

* Conto  
* Cliente  
* Articolo  
* Fornitore  

L'estensione per la migrazione dei dati di Dynamics GP mappa automaticamente i dati esportati in modo che i dati dell'utente siano disponibili rapidamente nella nuova società [!INCLUDE[d365fin](includes/d365fin_md.md)]. Durante il processo le informazioni di supporto di setup vengono create, come le categorie di registrazione. Gli articoli di magazzino verranno introdotti nel sistema con il FIFO come il metodo di valutazione del costo. I conti verranno impostati come il segmento di conto principale di Dynamics GP con dimensioni, poiché [!INCLUDE[d365fin](includes/d365fin_long_md.md)] non ha segmenti di conto.

## <a name="see-also"></a>Vedi anche
[Importazione dei dati aziendali da altri sistemi contabili](upload-data.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)  

