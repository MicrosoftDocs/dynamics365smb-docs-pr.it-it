---
title: Gestione delle modifiche dell'aliquota IVA
description: Scopri come utilizzare lo strumento di modifica dell'aliquota IVA per Dynamics 365 Business Central per la modifica delle aliquote IVA in base alla legislazione locale.
author: jswymer
ms.topic: conceptual
ms.reviewer: bholtorf
ms.search.keywords: 'VAT, VAT rate, posting, tax, value-added tax'
ms.search.form: '550,'
ms.date: 06/16/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# Gestione delle variazioni dell'aliquota IVA

Le aliquote IVA possono variare in base alla legislazione locale. Qualsiasi modifica dell'IVA incide sui dati dell'utente in [!INCLUDE[prod_short](includes/prod_short.md)] indipendentemente dal fatto che l'aliquota IVA sia stata ridotta, aumentata o rimossa. L'IVA è collegata a molte entità in [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio clienti, fornitori, articoli, risorse, addebiti articolo e conti di contabilità generale. Le variazioni delle aliquote IVA si verificano in genere a una data specifica, da quel momento sarà necessario aver modificato l'impostazione IVA, i gruppi di registrazione e così via per assicurarsi che i nuovi ordini di vendita e gli ordini di acquisto vengano creati con la nuova aliquota IVA.

## Modifica delle aliquote IVA

L'approccio ottimale per la gestione di una variazione dell'aliquota IVA è di registrare e chiudere integralmente gli ordini aperti e gli altri documenti prima della data del cambio dell'aliquota IVA, per assicurarsi che questi non siano influenzati dalla modifica. Questo è l'approccio più pulito che consente di avviare nuovi ordini e documenti con la nuova aliquota IVA.

Si suggerisce il seguente approccio per gestire una variazione dell'aliquota IVA

1. Registrare e chiudere completamente ordini, registrazioni e altri documenti aperti prima della data del variazione. È possibile attendere la data della variazione purché non si aggiungano nuove righe e occorre assicurarsi che la data di validità sia precedente alla data di commutazione.  
2. Creare la nuova impostazione IVA.  
3. Effettuare la variazione dell'IVA sulle entità (clienti, fornitori, articoli e così via).  
4. Alla data della variazione dell'aliquota IVA creare nuovi documenti che utilizzeranno la nuova aliquota.  


> [!NOTE]  
> Al momento lo strumento di modifica dell'aliquota IVA è in aggiornamento. La funzionalità menzionata di seguito potrebbe non corrispondere alla funzionalità nel proprio ambiente. L'aggiornamento avrà luogo prima del 1° luglio 2020 e non sarà un aggiornamento mensile regolare. Al contrario, tutti gli ambienti verranno aggiornati automaticamente (aggiornamento rapido). Al termine dell'aggiornamento, questo messaggio non verrà più visualizzato.  

## Strumento di modifica dell'aliquota IVA

Lo strumento di modifica dell'aliquota IVA può aiutare a convertire le aliquote IVA in anagrafica, registrazioni e ordini, in una certa misura. Ciò è utile se si desidera convertire più facilmente l'IVA sull'anagrafica o se sono presenti ordini che non è possibile chiudere prima della data di variazione e che verranno elaborati per un periodo di tempo più lungo, oltre la data di variazione dell'aliquota IVA. Esistono alcune restrizioni e limitazioni nello strumento di modifica dell'aliquota IVA.

## Informazioni sulle limitazioni e sul processo di conversione dell'aliquota IVA

Lo strumento di modifica dell'aliquota IVA effettua le conversioni di aliquota IVA per anagrafica, registrazioni e ordini in modalità diverse. Le registrazioni e i dati master selezionati verranno aggiornati in base alla nuova categoria di registrazione articoli/servizi o a quella relativa agli articoli/servizi IVA. Se un ordine è stato spedito completamente o in parte, gli articoli spediti conserveranno la categoria di registrazione articoli/servizi o quella di articoli/servizi IVA corrente. Per gli articoli non spediti verrà creata una nuova riga ordine che verrà aggiornata in modo da corrispondere alle categorie di registrazione articoli/servizi o a quelle di articoli/servizi IVA correnti e nuove. Inoltre, verranno aggiornati di conseguenza le assegnazioni di addebito articoli, i modelli di configurazione per articoli, prenotazioni e le informazioni sulla tracciabilità degli articoli. 

Sulle righe dell'ordine, il prezzo unitario verrà aggiornato per tutte le righe di tipo articolo e risorsa, se si utilizzano prezzi IVA inclusa per l'articolo. Per altri tipi di riga è possibile decidere se aggiornare o meno il prezzo unitario.

Esistono alcuni elementi che lo strumento non converte:

* Ordini e fatture di vendita o di acquisto, in caso di registrazione delle spedizioni. Questi documenti vengono registrati utilizzando l'aliquota IVA corrente.  
* Documenti con fatture pagamento anticipato registrate. Ad esempio, se sono stati effettuati o ricevuti pagamenti anticipati relativi a fatture che non sono state completate prima dell'utilizzo dello strumento di modifica dell'aliquota IVA. In questo caso, vi sarà una differenza tra l'IVA dovuta e quella pagata nei pagamenti anticipati quando la fattura viene completata. Con lo strumento di modifica dell'aliquota IVA sarà possibile ignorare questi documenti che dovranno però essere aggiornati manualmente.  
* Ordini di vendita o di acquisto con l'integrazione warehouse qualora siano parzialmente spediti o ricevuti.  
* Spedizioni dirette.
* Ordini speciali. 
* Ordini di assemblaggio.
* Contratti di assistenza.  
* Note di credito.
* Ordini di reso.
* Prezzi sugli articoli (anagrafica)
* Prezzi sui prezzi di vendita (anagrafica)
* Categorie di registrazione business IVA per clienti e fornitori.

### Per preparare conversioni di modifica dell'aliquota IVA

Prima di impostare lo strumento di modifica dell'aliquota IVA, è necessario effettuare le preparazioni riportate di seguito.

* Se si effettuano transazioni in cui si utilizzano aliquote differenti, esse devono essere separate in gruppi differenti creando nuovi conti di contabilità generale per ogni aliquota o utilizzando filtri di dati per raggruppare le transazioni in base all'aliquota.  
* Se si creano nuovi conti di contabilità generale, è necessario creare nuove categorie di registrazioni generali.  
* Per ridurre il numero di documenti che vengono convertiti, registrare il maggior numero di documenti possibile e ridurre al minimo quelli non registrati.  
* Eseguire il backup dei dati.

### Per impostare lo strumento di modifica dell'aliquota IVA

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup modifiche aliquota IVA**, quindi scegli il collegamento correlato.  
2. Nelle Schede dettaglio **Dati master**, **Registrazioni** e **Documenti** scegliere un valore della categoria registrazione dall'elenco di opzioni per i campi necessari. Per ciascun gruppo è possibile scegliere se convertire le categorie di registrazione di articoli e servizi IVA o le categorie di registrazione di articoli e servizi generali oppure convertire entrambi i valori se sono disponibili nell'elemento dati master. Per alcune aree è anche possibile impostare un filtro per convertire solo un sottoinsieme di valori, ad esempio i conti C/G. 
3. Nella scheda dettaglio **Prezzi IVA inclusa**, scegliere i tipi di riga per gli ordini per i quali si desidera aggiornare i prezzi unitari. I prezzi unitari sulle righe di tipo articolo e risorsa verranno sempre aggiornati.

### Per impostare la conversione delle categorie di registrazione prodotti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup modifiche aliquota IVA**, quindi scegli il collegamento correlato.  
2. Nella pagina **Setup modifiche aliquota IVA** scegliere l'azione **Conv. cat. reg. art./serv. IVA** o **Conv. cat. reg. articolo/servizio**.  
3. Nel campo **Da codice** immettere la categoria di registrazione corrente.  
4. Nel campo **A codice** immettere la nuova categoria di registrazione.  

### Per eseguire la conversione della modifica dell'aliquota IVA

È possibile utilizzare lo strumento di modifica aliquota IVA per gestire le modifiche nell'aliquota IVA standard. Vengono eseguite le conversioni della categoria di registrazione generale e dell'IVA per modificare le aliquote IVA e gestire il reporting IVA accurato. In base all'impostazione vengono apportate le modifiche seguenti:  

* Le categorie registrazione generale e IVA vengono convertite.  
* Le modifiche vengono apportate nei conti di contabilità generale, nei clienti, nei fornitori, nei documenti aperti, nelle righe di registrazione e anche in altri documenti.  

> [!IMPORTANT]  
> Prima di eseguire la conversione modifica aliquota IVA, è possibile eseguire i test della conversione. A tale scopo, eseguire la procedura riportata di seguito, ma assicurarsi di deselezionare le caselle di controllo **Esegui conversione** e **Strumento di modifica aliquota IVA completato**. Durante la conversione di test, il campo **Convertito** nella tabella **Movimento log modifiche aliquota IVA** è stato rimosso e il campo **Data convertita** nella tabella **Movimento log modifiche aliquota IVA** è vuoto. Al termine della conversione, scegliere **Voci log modifiche aliquota IVA** per visualizzare i risultati del test di conversione. Verificare ciascun movimento prima di eseguire la conversione. In particolare, verificare le transazioni che usano un'aliquota IVA precedente.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Modifica aliquota IVA**, quindi scegli il collegamento **Setup modifiche aliquota IVA**.  
2. Verificare che sia già stata impostata la conversione della categoria di registrazione articoli/servizi IVA o quella relativa agli articoli/servizi.  
3. Selezionare la casella di controllo **Esegui conversione**.  

    > [!IMPORTANT]  
    >  Deselezionare la casella controllo **Strumento di modifica aliquota IVA completato**. La casella di controllo viene selezionata automaticamente al termine della conversione della modifica dell'aliquota IVA.  

4. Scegliere l'azione **Converti**.  
5. Al termine della conversione, scegliere l'azione **Voci log modifiche aliquota IVA** per visualizzare i risultati del test di conversione.  

> [!IMPORTANT]  
> Dopo la conversione, il campo **Convertito** nella tabella **Movimento log modifiche aliquota IVA** è selezionato e il campo **Data convertita** nella tabella **Movimento log modifiche aliquota IVA** visualizza la data di conversione.  

## Vedere anche

[Impostare l'IVA (imposta sul valore aggiunto)](finance-setup-vat.md)  
[Setup dell'IVA ad esigibilità differita](finance-setup-unrealized-vat.md)  
[Dichiarare l'IVA a un'autorità fiscale](finance-how-report-vat.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Funzionalità locale in Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
