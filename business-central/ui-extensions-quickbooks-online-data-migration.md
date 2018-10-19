---
title: Utilizzo dell'estensione per la migrazione QuickBooks | Documenti Microsoft
description: Descrive come utilizzare l'estensione per migrare clienti, fornitori, articoli e conti da QuickBooks Online a Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e9b0a481f16d8f0bc1647640b62a81b3ea441028
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---

# <a name="the-quickbooks-online-data-migration-extension"></a>Estensione di migrazione dei dati QuickBooks Online
Questa estensione è inclusa nella Guida setup assistito **Migrazione dati** per semplificare la migrazione dei dati aziendali importanti da QuickBooks Online a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ad esempio, può essere utile quando l'attività si sviluppa e si è deciso di aggiornare l'app di gestione aziendale cominciando a utilizzare [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="what-data-can-i-import-from-quickbooks-online"></a>Quali dati si possono importare da QuickBooks Online?
È possibile importare i seguenti dati da QuickBooks Online a [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

* Clienti
* Fornitori
* Articoli
* Piano dei conti
* Transazioni di saldo iniziale di contabilità generale
* Quantità disponibili per gli articoli di magazzino
* Documenti aperti per clienti e fornitori, quali fatture, note di credito e pagamenti

Verranno migrati solo gli importi complessivi relativi a documenti di vendita e acquisto. Non vengono aggiornati gli importi parzialmente pagati. Ad esempio, se un cliente ha pagato 300 dollari su un totale di 500 dollari di una fattura di vendita, l'importo che verrà migrato è quello completo, ovvero 500 dollari. Se si ricevono pagamenti parziali, è necessario aggiornare manualmente questi valori, prima o dopo aver migrato i dati. Si consiglia di applicare le transazioni inevase prima della migrazione, per semplificare le attività successive alla migrazione.

> [!NOTE]  
>   Non vengono migrati gli ordini di acquisto o di vendita.

## <a name="before-you-start"></a>Operazioni preliminari
Una parte importante del processo di migrazione consiste nello specificare i conti verso cui migrare le transazioni. Si consiglia di pianificare questa mappatura che prima della migrazione dei dati. Ad esempio, i conti in cui vengono registrate le transazioni relative a:  

* La vendita di articoli o servizi ai clienti.
* L'acquisto di articoli o servizi dai fornitori.  
* Rettifiche nella contabilità generale.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] richiede che i conti di contabilità generale abbaino numeri assegnati ad essi. Assicurarsi che i numeri vengano assegnati ai conti in QuickBooks Online.

Se le transazioni in QuickBooks Online includono importi di imposte, è necessario configurare un conto per le imposte in base alle giurisdizioni fiscali di [!INCLUDE[d365fin](includes/d365fin_md.md)] prima di registrare le transazioni.

## <a name="how-do-i-start-using-the-extension"></a>Operazioni iniziali per l'utilizzo dell'estensione
Iniziare è semplice. È necessario solo eseguire la Guida di setup assistito **Migrazione di dati**. Ecco come:

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup assistito** e quindi scegliere **Migra dati aziendali**.
2. Seguire le istruzioni per ogni passaggio della Guida di setup assistito.

## <a name="what-do-i-do-after-i-migrate-data"></a>Operazioni successive alla migrazione dei dati
Dopo aver migrato i dati, le transazioni hanno come stato **Non registrata**, quindi è possibile esaminarle e apportare modifiche. Per verificare le transazioni, andare alla pagina in cui vengono in genere visualizzate. Ad esempio, per esaminare le fatture di vendita non registrate, andare alla finestra **Fatture di vendita**. Per verificare le registrazioni pagamenti, andare alla finestra **Registrazioni pagamenti**.   

Esistono alcune operazioni consigliate:

* Se le transazioni in QuickBooks Online presentano importi di markup o sconti, è necessario aggiungere manualmente gli importi alle transazioni relative in [!INCLUDE[d365fin](includes/d365fin_md.md)] prima di registrarle.
* Se si utilizza l'IVA, può essere necessario aggiungere una categoria di registrazione business e articoli/servizi nel Setup registrazione in modo che sia possibile registrare gli importi IVA.
* Verificare i saldi iniziali per i conti della contabilità generale. QuickBooks Online non memorizza il saldo attuale per tutti i conti, potrebbe quindi essere necessario correggere i saldi iniziali.

## <a name="see-also"></a>Vedi anche
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  

