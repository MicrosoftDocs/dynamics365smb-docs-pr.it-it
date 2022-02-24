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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 9b5129e4e9ddfe60d969e705d62e023716cde5b6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311142"
---
# <a name="the-quickbooks-data-migration-extension"></a>Estensione di migrazione dei dati QuickBooks
Questa estensione consente di eseguire la migrazione di clienti, fornitori, articoli e conti da QuickBooks [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se l'azienda al momento utilizza QuickBooks, è possibile esportare le informazioni rilevanti e aprire una guida al setup assistito per caricare i dati in [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Per ulteriori informazioni, vedere [Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md).

## <a name="data-from-quickbooks-desktop"></a>Dati da QuickBooks Desktop
 
È possibile importare i seguenti dati da QuickBooks Online a Business Central:

- Clienti  
- Fornitori  
- Articoli  
- Piano dei conti  
- Transazioni di saldo iniziale di contabilità generale  
- Quantità disponibili per gli articoli di magazzino  
- Documenti aperti per clienti e fornitori, quali fatture, note di credito e pagamenti  

Verranno migrati solo gli importi complessivi relativi a documenti di vendita e acquisto. Non vengono aggiornati gli importi parzialmente pagati. Ad esempio, se un cliente ha pagato 300 dollari su un totale di 500 dollari di una fattura di vendita, l'importo che verrà migrato è quello completo, ovvero 500 dollari. Se si ricevono pagamenti parziali, è necessario aggiornare manualmente questi valori, prima o dopo aver migrato i dati. Si consiglia di applicare le transazioni inevase prima della migrazione, per semplificare le attività successive alla migrazione.

> [!NOTE]
> Non vengono migrati gli ordini di acquisto o di vendita.

## <a name="before-you-start"></a>Operazioni preliminari
Una parte importante del processo di migrazione consiste nello specificare i conti verso cui migrare le transazioni. Si consiglia di pianificare questa mappatura che prima della migrazione dei dati. Ad esempio, i conti in cui vengono registrate le transazioni relative a:

- La vendita di articoli o servizi ai clienti  
- L'acquisto di articoli o servizi dai fornitori  
- Rettifiche nella contabilità generale  

Business Central richiede che i conti di contabilità generale abbaino numeri assegnati ad essi. Assicurarsi che i numeri vengano assegnati ai conti in QuickBooks.
Se le transazioni in QuickBooks includono importi di imposte, è necessario configurare un conto per le imposte in base alle giurisdizioni fiscali di Business Central prima di registrare le transazioni.

Per ottenere i dati dall'applicazione QuickBooks Desktop sarà necessario scaricare lo strumento di esportazione di dati di Microsoft.  Le istruzioni per lo strumento sono contenute nella procedura di migrazione guidata dati in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lo strumento verrà collegato all'applicazione QuickBooks ed esporterà i dati applicabili in un file .zip.  

> [!NOTE]
> Attualmente lo strumento di esportazione di dati è compatibile solo con QuickBooks 2017 e 2018.

## <a name="finding-the-quickbooks-data-migration-extension"></a>Utilizzo dell'estensione per la migrazione dei dati QuickBooks
L'estensione per la migrazione dei dati QuickBooks si trova nella Guida setup assistito Migrazione dati ed è pronta all'uso. Se si è pronti per iniziare, dopo aver esportato i dati da QuickBooks, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup assistito** e quindi scegliere il collegamento correlato. Scegliere **Migra dati aziendali**, quindi seguire i passaggi nella guida.  

## <a name="what-do-i-do-after-i-migrate-data"></a>Operazioni successive alla migrazione dei dati
Dopo aver migrato i dati, le transazioni hanno come stato Non registrata, quindi è possibile esaminarle e apportare modifiche. Per verificare le transazioni, andare alla pagina in cui vengono in genere visualizzate. Ad esempio, per esaminare le fatture di vendita non registrate, andare alla pagina Fatture di vendita. Per verificare le registrazioni pagamenti, andare alla pagina Registrazioni pagamenti.
Esistono alcune operazioni consigliate: se le transazioni in QuickBooks presentano importi di markup o sconti, è necessario aggiungere manualmente gli importi alle transazioni relative in Business Central prima di registrarle.
Se si utilizza l'IVA, può essere necessario aggiungere una categoria di registrazione business e articoli/servizi nel Setup registrazione in modo che sia possibile registrare gli importi IVA.
Verificare i saldi iniziali per i conti della contabilità generale. QuickBooks non memorizza il saldo attuale per tutti i conti, potrebbe quindi essere necessario correggere i saldi iniziali.

## <a name="see-also"></a>Vedi anche
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)  
