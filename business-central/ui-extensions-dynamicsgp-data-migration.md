---
title: Migrare i dati da Dynamics GP tramite l'estensione per la migrazione dei dati | Documenti Microsoft
description: Utilizzare l'estensione per la migrazione dei dati di Dynamics GP per migrare i dati relativi a clienti, fornitori, articoli di magazzino, conti C/G, transazioni aperte di contabilità fornitori e clienti di e conti da Dynamics GP a Business Central.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: cf401500c34d8d40acc153a591229684770afa64
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "917478"
---
# <a name="the-dynamics-gp-data-migration-extension"></a>Estensione di migrazione dei dati Dynamics GP 
L'estensione semplifica la migrazione dei dati relativi a clienti, fornitori, articoli di magazzino, conti C/G, transazioni aperte di contabilità fornitori e clienti di e conti da Dynamics GP a [!INCLUDE[prodshort](includes/prodshort.md)]. Se l'azienda al momento utilizza Dynamics GP, è possibile esportare i record rilevanti e aprire una guida al setup assistito per aggiungere i dati in [!INCLUDE[prodshort](includes/prodshort.md)]. L'estensione di migrazione è utilizzabile con tutte le versioni supportate di Microsoft Dyanmics GP. Per ulteriori informazioni, vedere [Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md).

## <a name="exporting-data-from-dynamics-gp"></a>Esportazione dei dati da Dynamics GP
È necessario aver esportato alcuni o tutti i clienti, i fornitori, gli articoli di magazzino e gli account di contabilità generale esistenti utilizzando la funzionalità di esportazione dei dati di Dynamics GP. Quando si selezionano i dati da esportare, è possibile selezionare i seguenti tipi:

* Conto  
* Cliente  
* Articolo  
* Fornitore  

Quando viene creato il file di esportazione, si avrà un file zip che contiene diversi file txt che saranno determinati da ciò che è stato selezionato durante il processo di esportazione dei dati.  Saranno presenti anche file txt aggiuntivi che contengono informazioni di supporto necessarie per l'installazione all'interno della nuova società di [!INCLUDE[prodshort](includes/prodshort.md)].

L'estensione per la migrazione dei dati di Dynamics GP mappa automaticamente i dati esportati in modo che i dati dell'utente siano disponibili rapidamente nella nuova società [!INCLUDE[prodshort](includes/prodshort.md)].

## <a name="whats-new-in-the-october-2018-release"></a>Novità nella versione di ottobre 2018

Nella versione, è stata ampliata la quantità di dati che vengono trasferiti in [!INCLUDE[prodshort](includes/prodshort.md)] da Dynamics GP.

Nella procedura guidata di migrazione, ora è possibile scegliere come eseguire la migrazione del piano dei conti di Dynamics GP. È possibile migrare il piano esistente oppure creare un nuovo piano dei conti basato sul piano dei conti esistente.  

Se si sceglie di utilizzare il piano dei conti esistente, i conti verranno impostati come il segmento principale di conto di Dynamics GP e i segmenti aggiuntivi verranno impostati come dimensioni all'interno di [!INCLUDE[prodshort](includes/prodshort.md)].  

Se si sceglie di creare un nuovo piano dei conti, nella procedura guidata verrà visualizzata una pagina di informazioni sul conto in modo che sia possibile scaricare la cartella di lavoro, apportare le modifiche pertinenti e quindi importare di nuovo la cartella di lavoro per modificare i propri conti.  

Sarà necessario scaricare la cartella di lavoro di Excel e associare un nuovo numero di conto a ciascun numero di conto nel foglio di Excel. Ogni account dovrà avere il proprio numero oppure la migrazione genererà un errore. Dopo avere completato la mappatura, è possibile continuare con la procedura guidata di migrazione importando la cartella di lavoro di Excel appena aggiornata. La procedura guidata verificherà che ogni riga abbia un numero di conto univoco e che nessuna riga contenga un nuovo numero di conto vuoto.  

Con la modifica alla mappatura del grafico delle opzioni del conto, si noterà anche una modifica al tipo di dati che si trovano nelle registrazioni COGE per i numeri di conto.  

- Se si sceglie di utilizzare i numeri di conto esistenti, il saldo iniziale del segmento principale (nuovo numero di conto) verrà riportato come somma del numero di conto principale al momento della migrazione.  
- Se si sceglie di creare nuovi numeri di conto, verranno fornite informazioni di riepilogo per l'equivalente di due anni fiscali in base ai periodi fiscali impostati in Dynamics GP.

Nelle versioni precedenti di [!INCLUDE[prodshort](includes/prodshort.md)], la procedura guidata effettuava la migrazione di una transazione di riepilogo per il saldo cliente/fornitore in Dynamics GP. Ora vengono trasferite le transazioni aperte dettagliate per clienti e fornitori al momento della migrazione. Cosa significa? Se il cliente ha registrato 3 transazioni in sospeso nel modulo Contabilità clienti, la procedura guidata trasferisce tali transazioni in [!INCLUDE[prodshort](includes/prodshort.md)] con l'importo inevaso come importo del documento. La stessa situazione si verifica per il modulo Contabilità fornitori.  

Gli articoli di magazzino vengono importati con il metodo di valutazione dei costi selezionato al momento dell'esecuzione della procedura guidata di configurazione della società. Agli articoli in assistenza viene assegnato automaticamente al metodo di valutazione FIFO. Attualmente viene trasferita la Giacenza per gli articoli al momento della migrazione.  Questa quantità viene portata nell'ubicazione vuota.  

L'ultima opzione visualizzate nella procedura guidata di migrazione dati per Dynamics GP è la possibilità di specificare l'opzione di registrazione. Questa impostazione specifica se si desidera registrare automaticamente tutte le transazioni nelle registrazioni COGE non appena la migrazione sposta i dati in [!INCLUDE[prodshort](includes/prodshort.md)] o se si desidera registrare manualmente in modo che tutte le transazioni vengano gestite in batch all'interno della pagina delle registrazioni COGE per poter verificare le informazioni prima di registrarle. Questa opzione è visibile nella pagina delle opzioni del piano dei conti.


## <a name="see-also"></a>Vedi anche
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Personalizzazione di [!INCLUDE[prodshort](includes/prodshort.md)] utilizzando le estensioni ](ui-extensions.md)  
