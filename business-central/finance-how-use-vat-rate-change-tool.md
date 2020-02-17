---
title: Utilizzare lo strumento di modifica dell'aliquota IVA | Microsoft Docs
description: Utilizzare lo strumento di modifica dell'aliquota IVA
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/06/2020
ms.author: andregu
ms.openlocfilehash: 0fe23bb6b1d4ce6fbf73a1978a66f6d47b8e78fe
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992232"
---
# <a name="use-the-vat-rate-change-tool"></a>Utilizzare lo strumento di modifica dell'aliquota IVA

## <a name="understanding-the-vat-rate-conversion-process"></a>Informazioni sul processo di conversione dell'aliquota IVA  
Lo strumento di modifica dell'aliquota IVA effettua le conversioni di aliquota IVA per dati master, registrazioni e ordini in modalità diverse. Le registrazioni e i dati master selezionati verranno aggiornati in base alla nuova categoria di registrazione articoli/servizi o a quella relativa agli articoli/servizi IVA. Se un ordine è stato spedito completamente o in parte, gli articoli spediti conserveranno la categoria di registrazione articoli/servizi o quella di articoli/servizi IVA corrente. Per gli articoli non spediti verrà creata una nuova riga ordine che verrà aggiornata in modo da corrispondere alle categorie di registrazione articoli/servizi o a quelle di articoli/servizi IVA correnti e nuove. Inoltre, verranno aggiornati di conseguenza gli impegni, le assegnazioni di addebito articoli e le informazioni sulla tracciabilità degli articoli.  

Esistono alcuni elementi che lo strumento non converte:

* Ordini e fatture di vendita o di acquisto, in caso di registrazione delle spedizioni. Questi documenti vengono registrati utilizzando l'aliquota IVA corrente.  
* Documenti con fatture pagamento anticipato registrate. Ad esempio, se sono stati effettuati o ricevuti pagamenti anticipati relativi a fatture che non sono state completate prima dell'utilizzo dello strumento di modifica dell'aliquota IVA. In questo caso, vi sarà una differenza tra l'IVA dovuta e quella pagata nei pagamenti anticipati quando la fattura viene completata. Con lo strumento di modifica dell'aliquota IVA sarà possibile ignorare questi documenti che dovranno però essere aggiornati manualmente.  
* Spedizioni dirette o ordini speciali.  
* Ordini di vendita o di acquisto con l'integrazione warehouse qualora siano parzialmente spediti o ricevuti.  
* Contratti di assistenza.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Per preparare conversioni di modifica dell'aliquota IVA  
Prima di impostare lo strumento di modifica dell'aliquota IVA, è necessario effettuare le preparazioni riportate di seguito.

* Se si effettuano transazioni in cui si utilizzano aliquote differenti, esse devono essere separate in gruppi differenti creando nuovi conti di contabilità generale per ogni aliquota o utilizzando filtri di dati per raggruppare le transazioni in base all'aliquota.  
* Se si creano nuovi conti di contabilità generale, è necessario creare nuove categorie di registrazioni generali.  
* Per ridurre il numero di documenti che vengono convertiti, registrare il maggior numero di documenti possibile e ridurre al minimo quelli non registrati.  
* Eseguire il backup dei dati.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Per impostare lo strumento di modifica dell'aliquota IVA  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup modifiche aliquota IVA** e quindi scegliere il collegamento correlato.  
2. Nelle Schede dettaglio **Dati master**, **Registrazioni** e **Documenti** scegliere un valore della categoria registrazione dall'elenco di opzioni per i campi necessari. Per ciascun gruppo è possibile scegliere se convertire le categorie di registrazione di articoli e servizi IVA o le categorie di registrazione di articoli e servizi generali oppure convertire entrambi i valori se sono disponibili nell'elemento dati master. Per alcune aree è anche possibile impostare un filtro per convertire solo un sottoinsieme di valori, ad esempio i conti C/G. 

### <a name="to-set-up-product-posting-group-conversion"></a>Per impostare la conversione delle categorie di registrazione prodotti  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup modifiche aliquota IVA** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Setup modifiche aliquota IVA** scegliere l'azione **Conv. cat. reg. art./serv. IVA** o **Conv. cat. reg. articolo/servizio**.  
3. Nel campo **Da codice** immettere la categoria di registrazione corrente.  
4. Nel campo **A codice** immettere la nuova categoria di registrazione.  

### <a name="to-perform-vat-rate-change-conversion"></a>Per eseguire la conversione della modifica dell'aliquota IVA  
È possibile utilizzare lo strumento di modifica aliquota IVA per gestire le modifiche nell'aliquota IVA standard. Vengono eseguite le conversioni della categoria di registrazione generale e dell'IVA per modificare le aliquote IVA e gestire il reporting IVA accurato. In base all'impostazione vengono apportate le modifiche seguenti:  

* Le categorie registrazione generale e IVA vengono convertite.  
* Le modifiche vengono apportate nei conti di contabilità generale, nei clienti, nei fornitori, nei documenti aperti, nelle righe di registrazione e anche in altri documenti.  

> [!IMPORTANT]  
>  Prima di eseguire la conversione modifica aliquota IVA, è possibile eseguire i test della conversione. A tale scopo, eseguire la procedura riportata di seguito, ma assicurarsi di deselezionare le caselle di controllo **Esegui conversione** e **Strumento di modifica aliquota IVA completato**. Durante la conversione di test, il campo **Convertito** nella tabella **Movimento log modifiche aliquota IVA** è stato rimosso e il campo **Data convertita** nella tabella **Movimento log modifiche aliquota IVA** è vuoto. Al termine della conversione, scegliere **Voci log modifiche aliquota IVA** per visualizzare i risultati del test di conversione. Verificare ciascun movimento prima di eseguire la conversione. In particolare, verificare le transazioni che usano un'aliquota IVA precedente.     

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Modifica aliquota IVA** e quindi scegliere il collegamento **Setup modifiche aliquota**.  
2. Verificare che sia già stata impostata la conversione della categoria di registrazione articoli/servizi IVA o quella relativa agli articoli/servizi.  
3. Selezionare la casella di controllo **Esegui conversione**.  

    > [!IMPORTANT]  
    >  Deselezionare la casella controllo **Strumento di modifica aliquota IVA completato**. La casella di controllo viene selezionata automaticamente al termine della conversione della modifica dell'aliquota IVA.  

4. Scegliere l'azione **Converti**.  
5. Al termine della conversione, scegliere l'azione **Voci log modifiche aliquota IVA** per visualizzare i risultati del test di conversione.  

> [!IMPORTANT]  
>  Dopo la conversione, il campo **Convertito** nella tabella **Movimento log modifiche aliquota IVA** è selezionato e il campo **Data convertita** nella tabella **Movimento log modifiche aliquota IVA** visualizza la data di conversione.  
## <a name="see-also"></a>Vedere anche  
[Impostare l'IVA (imposta sul valore aggiunto)](finance-setup-vat.md)  
[Setup dell'IVA ad esigibilità differita](finance-setup-unrealized-vat.md)      
[Dichiarare l'IVA a un'autorità fiscale](finance-how-report-vat.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Funzionalità locale in Business Central](about-localization.md)
