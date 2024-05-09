---
title: Utilizzare Excel per importare dati
description: Utilizzare il pacchetto di configurazione di default per aggiungere i dati del cliente in Excel e importare nuovamente i dati in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'migration, Excel'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Importare i dati aziendali da altri sistemi contabili

Quando ci si iscrive a [!INCLUDE[prod_short](includes/prod_short.md)], è possibile scegliere di creare una società vuota nella quale caricare i propri dati e testare la nuova società in [!INCLUDE[prod_short](includes/prod_short.md)]. A seconda della soluzione contabile che l'azienda utilizza correntemente, è possibile trasferire le informazioni sui conti clienti, fornitori, magazzino e bancari.  

Dalla Gestione ruolo utente, è possibile avviare una guida al setup assistito che aiuta a trasferire i dati aziendali da un file di Excel o da altri formati. Il tipo di file che è possibile caricare dipende dalle estensioni disponibili. Ad esempio, è possibile migrare i dati da QuickBooks perché [!INCLUDE[prod_short](includes/prod_short.md)] include un'estensione che gestisce la conversione da QuickBooks. Se si desidera migrare i dati da altre soluzioni contabili, è necessario verificare se è disponibile un'estensione per quella soluzione oppure importare da Excel.  

[!INCLUDE[prod_short](includes/prod_short.md)] include modelli per i conti, i clienti, i fornitori e gli articoli di magazzino collegabili quando si importano i dati. Per importare immagini articolo, è possibile utilizzare una funzione dedicata nella pagina **Setup magazzino**. Per ulteriori informazioni, vedere [Importare molteplici immagini articolo](inventory-how-import-item-pictures.md).

> [!TIP]  
> Si consiglia di usare le procedure guidate di migrazione dati per importare i dati da Dynamics GP, Dynamics NAV o QuickBooks. Per ulteriori informazioni, vedere [Eseguire la migrazione dei dati locali in Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) nel contenuto amministrativo o [Migrazione dei dati di QuickBooks](ui-extensions-quickbooks-data-migration.md).

## Utilizzare i dati in Excel

Puoi utilizzare il componente aggiuntivo di Excel per preparare il contneuto esistente per l'uso in [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Visualizzare e modificare in Excel da Business Central](across-work-with-excel.md).  

## Importare di dati dei pacchetti di configurazione

Per un lavoro di implementazione più ampio, puoi impostare pacchetti di configurazione specifici per la soluzione. Per ulteriori informazioni, vedere [Impostare pacchetti di configurazione aziendale ](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (solo in inglese) nel contenuto per amministratori.  

> [!NOTE]  
> L'utilizzo dei pacchetti di configurazione è una funzionalità avanzata, pertanto si raccomanda di contattare il partner rivenditore. Per ulteriori informazioni, vedere [Configurare i pacchetti di configurazione dell'azienda](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (solo in inglese).

È possibile importare dati master e alcuni dati transazionali da altri sistemi finanziari in base al pacchetto di configurazione standard disponibile in [!INCLUDE[prod_short](includes/prod_short.md)]. Nella pagina **Pacchetti di configurazione** è possibile utilizzare il pacchetto per importare e convalidare i dati prima di applicare il pacchetto. Ad esempio, puoi esportare il pacchetto di configurazione in Excel e configurare qui i tuoi dati. Quindi, è possibile importare nuovamente i dati da Excel. Il pacchetto è costituito da 27 tabelle, inclusi i dati master, quali clienti, fornitori, articoli e conti, altre tabelle di setup di base, quali i metodi di spedizione, e le tabelle di transazioni, ad esempio intestazioni e righe delle vendite.  

Quando si esporta il pacchetto di configurazione di default in Excel, la cartella di lavoro generata contiene un prospetto per ogni tabella del pacchetto. Per semplificare i task, è possibile avvantaggiarsi degli strumenti di modifica XML incorporati in Excel. È inoltre possibile utilizzare le funzioni incorporate di Excel per agevolare la formattazione dei dati e inserire i dati nella cella appropriata. Ad esempio, aggiungere un prospetto vuoto e copiarvi i dati legacy. Creare quindi una formula Excel per mappare i dati nel prospetto di trasformazione tra i campi del prospetto esportato e i dati legacy del cliente. Dopo aver eseguito la mappatura di tutti i dati, copiare l'intervallo dei dati nel prospetto della tabella.  

> [!IMPORTANT]  
> Non modificare le colonne nei prospetti. Se vengono spostate, modificate o eliminate, il prospetto non può essere importato in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> I campi di tipo BLOB non possono essere esportati/importati utilizzando Excel.

### Tabelle nel pacchetto di configurazione di default

Il pacchetto di configurazione di default supporta le seguenti tabelle:

- Condizioni pagamento
- Gruppo prezzi cliente
- Metodo di spedizione
- Agenti/Addetti acq.
- Località
- Conto C/G
- Cliente
- Fornitore
- Articolo
- Testate vendita
- Righe vendite
- Testate acquisti
- Righe Acquisto
- Righe registrazioni COGE
- Righe reg. magazzino
- Cat. reg. cliente
- Cat. reg. fornitore
- Cat. reg. magazzino
- Unità di misura
- Righe Cat. reg. business
- Righe Cat. reg. articoli/servizi
- Setup registrazioni COGE
- Regioni
- Categoria articoli
- Prezzo vendita
- Prezzo acquisto

## Vedi anche

[Eseguire la migrazione dei dati locali in Business Central Online (solo in inglese)](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[Configurare i pacchetti di configurazione dell'azienda](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)  
[Migrazione dei dati QuickBooks](ui-extensions-quickbooks-data-migration.md)  
[Importare molteplici immagini articolo](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]