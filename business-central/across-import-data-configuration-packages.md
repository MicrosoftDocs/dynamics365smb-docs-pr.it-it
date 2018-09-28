---
title: Utilizzare Excel per importare dati in Business Central | Documenti Microsoft
description: Utilizzare il pacchetto di configurazione di default per aggiungere i dati del cliente in Excel e importare nuovamente i dati in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 45a236dfeb7a5ce489cf8917d6a08a92ca5c4e8b
ms.contentlocale: it-it
ms.lasthandoff: 06/28/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a>Importazione dei dati aziendali da altri sistemi contabili
Quando ci si iscrive a [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile scegliere di creare una società vuota nella quale caricare i propri dati e testare la nuova società in [!INCLUDE[d365fin](includes/d365fin_md.md)]. A seconda della soluzione contabile che l'azienda utilizza correntemente, è possibile trasferire le informazioni sui conti clienti, fornitori, magazzino e bancari.  

Dalla Gestione ruolo utente, è possibile avviare una guida al setup assistito che aiuta a trasferire i dati aziendali da un file di Excel o da altri formati. Il tipo di file che è possibile caricare dipende dalle estensioni disponibili. Ad esempio, è possibile migrare i dati da QuickBooks perché [!INCLUDE[d365fin](includes/d365fin_md.md)] include un'estensione che gestisce la conversione da QuickBooks. Se si desidera migrare i dati da altre soluzioni contabili, è necessario verificare se è disponibile un'estensione per quella soluzione oppure importare da Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] include modelli per i conti, i clienti, i fornitori e gli articoli di magazzino collegabili quando si importano i dati.

È possibile importare dati master e alcuni dati transazionali da altri sistemi finanziari in base al pacchetto di configurazione standard disponibile in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nella finestra **Pacchetti di configurazione** è possibile utilizzare il pacchetto per importare e convalidare i dati prima di applicare il pacchetto.  

> [!TIP]  
> In alternativa, usare le procedure guidate di migrazione dati per importare i dati da QuickBooks o Dynamics GP. Per ulteriori informazioni, vedere [Migrazione dei dati di QuickBooks](ui-extensions-quickbooks-data-migration.md) o [Migrazione dei dati di Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).

> [!NOTE]  
> Per le attività di implementazioni più importanti, è possibile utilizzare RapidStart Services per [!INCLUDE[d365fin](includes/d365fin_md.md)], un toolkit completo per la configurazione di nuove soluzioni basate sui requisiti aziendali dei clienti e sui dati di setup. RapidStart Services offre anche la funzionalità per l'importazione di dati aziendali. Per ulteriori informazioni, vedere [Impostare una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

## <a name="importing-data-from-configuration-packages"></a>Importazione di dati dei pacchetti di configurazione
[!INCLUDE[d365fin](includes/d365fin_md.md)] include un pacchetto di configurazione che è possibile esportare in Excel, nelle cui tabelle impostare i dati. Quindi, è possibile importare nuovamente i dati da Excel. Il pacchetto è costituito da 27 tabelle, inclusi i dati master, quali clienti, fornitori, articoli e conti, altre tabelle di setup di base, quali i metodi di spedizione, e le tabelle di transazioni, ad esempio intestazioni e righe delle vendite.  

> [!NOTE]  
>   L'utilizzo dei pacchetti di configurazione è una funzionalità avanzata, pertanto si raccomanda di contattare l'amministratore. Per ulteriori informazioni, vedere [Importazioni di dati del software di contabilizzazione legacy utilizzando un pacchetto di configurazione](across-import-data-configuration-packages.md).

## <a name="working-with-data-in-excel"></a>Utilizzo di dati in Excel
Quando si esporta il pacchetto di configurazione di default in Excel, la cartella di lavoro generata contiene un prospetto per ogni tabella del pacchetto. Per semplificare i task, è possibile avvantaggiarsi degli strumenti di modifica XML incorporati in Excel. È inoltre possibile utilizzare le funzioni incorporate di Excel per agevolare la formattazione dei dati e inserire i dati nella cella appropriata. Ad esempio, aggiungere un prospetto vuoto e copiarvi i dati legacy. Creare quindi una formula Excel per mappare i dati nel prospetto di trasformazione tra i campi del prospetto esportato e i dati legacy del cliente. Dopo aver eseguito la mappatura di tutti i dati, copiare l'intervallo dei dati nel prospetto della tabella.  

> [!IMPORTANT]  
>  Non modificare le colonne nei prospetti. Se vengono spostate, modificate o eliminate, il prospetto non può essere importato in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="tables-in-the-default-configuration-package"></a>Tabelle nel pacchetto di configurazione di default
Il pacchetto di configurazione di default supporta le seguenti tabelle:

-   Condizioni pagamento
-   Gruppo prezzi cliente
-   Metodo di spedizione
-   Agenti/Addetti acq.
-   Località
-   Conto C/G
-   Cliente
-   Fornitore
-   Articolo
-   Testate vendita
-   Righe vendite
-   Testate acquisti
-   Righe Acquisto
-   Righe registrazioni COGE
-   Righe reg. magazzino
-   Cat. reg. cliente
-   Cat. reg. fornitore
-   Cat. reg. magazzino
-   Unità di misura
-   Cat. reg. business
-   Cat. reg. articoli/servizi
-   Setup registrazioni COGE
-   Regioni
-   Categorie articolo
-   Prezzo vendita
-   Prezzo acquisto

## <a name="see-also"></a>Vedi anche
[Impostare una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Migrazione dei dati QuickBooks](ui-extensions-quickbooks-data-migration.md)  
[Migrazione dei dati Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

