---
title: Utilizzo dell'estensione Pagamenti e riconciliazioni (DK) | Documenti Microsoft
description: Questa estensione semplifica l'esportazione dei file preformattati per soddisfare i requisiti bancari per l'invio elettronico.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 06/19/2020
ms.author: bholtorf
ms.openlocfilehash: 7e8a56492c1c848f4f3b371e1411c11f159c3cf3
ms.sourcegitcommit: 6200a08e91d507bab01d1d5b805fe8ea3f44a58a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/22/2020
ms.locfileid: "3496752"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a>Estensione Pagamenti e riconciliazioni (DK)

Eseguire pagamenti veloci e senza errori esportando file formattati specificamente per gli scambi con i fornitori o la banca. Questi file accelerano i processi di pagamento e riconciliazione ed eliminano gli errori che possono verificarsi quando si immettono manualmente le informazioni su un sito Web della banca.  

Questa estensione supporta i formati di file per diverse banche danesi. Quando si esportano le informazioni di pagamento in un file, l'estensione crea un pacchetto dei dati nel formato richiesto dalla banca. Ad esempio, i formati includono Bankdata-V3, BEC, SDC e FIK, utilizzati da diverse banche e alcuni formati specifici per alcune banche, ad esempio Danske Bank e Nordea. L'estensione include anche alcuni formati per l'importazione e la riconciliazione di rendiconti bancari.  

> [!Note]
> Per utilizzare l'estensione, è necessario conoscere il formato richiesto dalla banca o dal fornitore. Alcune banche o fornitori rendono disponibili queste informazioni sui loro siti Web; tuttavia, potrebbe essere necessario contattare il servizio clienti per ottenere le informazioni necessarie.  

## <a name="supported-bank-formats"></a>Formati bancari supportati
Questa estensione si applica ai seguenti formati di file per i file di pagamento:  

* BANKDATA-V3  
* BEC-INDLAND  
* BEC-CSV  
* DANSKEBANK-CMKV  
* DANSKEBANK-CMKXKSX  
* DANSKEBANK  
* FIK71  
* NORDEA-ERHVERV-CSV  
* NORDEA  
* NORDEA-UNITEL-V3  
* SDC  
* SDC-CSV  

## <a name="to-set-up-the-extension"></a>Per impostare l'estensione

Ecco alcuni passaggi per iniziare.  

* Consentire l'esportazione dei dati di pagamento. Per agevolare la protezione dei dati, questa funzionalità non è disponibile per impostazione predefinita.  
* Impostare gli acquisti e la contabilità fornitori in modo che non richiedano numeri di documenti esterni sulle fatture. Se necessario, è possibile utilizzare il numero di riferimento per fare riferimento a una fattura specifica.  
* Specificare il metodo di pagamento per ogni fornitore. I metodi di pagamento definiscono il modo in cui vengono pagate le fatture del fornitore. Ad esempio, tramite banca, contanti, assegno o conto.  
* Specificare il tipo di formato da utilizzare per ogni conto bancario. Ad esempio, NORDEA, DANSKEBANK, SDC, ecc.  

Inoltre, è necessario assegnare i fornitori a una **Categoria registrazione business** e una **Categoria registrazione fornitori**. L'impostazione del paese per il fornitore deve essere la Danimarca (DK). Per ulteriori informazioni, vedere [Impostazione delle categorie di registrazione](finance-posting-groups.md).  

### <a name="to-allow-d365fin-to-export-payment-data"></a>Consentire a [!INCLUDE[d365fin](includes/d365fin_md.md)] l'esportazione dei dati di pagamento.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni pagamenti** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Modifica registrazioni pagamenti** scegliere il batch **Banca**.  
3. Scegliere la casella controllo **Consenti esportazione pagamento**.  

### <a name="to-specify-a-payment-method-for-a-vendor"></a>Per specificare il metodo di pagamento per un fornitore

La seguente tabella mostra le combinazioni dei metodi di pagamento FIK e GIRO supportate da [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Combinazione|Tipo 01 | Tipo 04 | Tipo 71 | Tipo 73 |
|----|--------|---------|---------|---------|
|Nr. di conto Giro o Nr. creditore FIK? | Nr. di conto Giro | Nr. di conto Giro | Nr. creditore FIK | Nr. creditore FIK|
|Consente messaggi al destinatario? | Sì |No |No | Sì |
|Contiene il numero di riferimento di pagamento? | No | Sì, 16 cifre. | Sì, 15 cifre. | No|

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fornitori** e quindi scegliere il collegamento correlato.  
2. Aprire la scheda, espandere la scheda **Pagamenti**, nel campo **Metodo pagamento** selezionare il metodo di pagamento.  
3. A seconda dell'opzione selezionata, è necessario compilare altri campi. Vedere la tabella sopra per una descrizione delle combinazioni.  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a>Per specificare il formato da utilizzare per un conto corrente bancario

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.  
2. Aprire la scheda del conto corrente bancario.  
3. Nel campo **Formato esportazione pagamento**, selezionare il formato del file di esportazione.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a>Scegliere le informazioni di pagamento FIK o Giro per le fatture fornitore

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture acquisto** e quindi scegliere il collegamento correlato.
2. Scegliere il fornitore. Ricordare che deve trattarsi di un fornitore danese con un indirizzo in Danimarca.
3. Creare una fattura. I campi **Metodo di pagamento** e **Nr. fornitore** vengono compilati in base alle impostazioni nella scheda Fornitore. Se necessario, è possibile modificare questi valori.
4. Nel campo **Riferimento pagamento**, immettere il numero a 15 cifre della fattura del fornitore.  

    > [!Tip]
    > È necessario aggiungere solo le ultime 11 cifra del numero. [!INCLUDE[d365fin](includes/d365fin_md.md)] aggiungerà quattro zeri all'inizio del numero.  

5. Contabilizzare la fattura.

## <a name="to-use-the-extension-to-export-payment-data"></a>Per utilizzare l'estensione per esportare i dati di pagamento

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni pagamenti** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Suggerisci Registrazioni pagamenti fornitore**.  

    > [!Tip]
    > Se si desidera esportare solo pagamenti specifici, utilizzare le opzioni per filtrare i dati.  

3. Se necessario, è possibile aggiungere i filtri per esportare solo i pagamenti specifici.  
4. Nel campo **Tipo pagamento banca**, scegliere **Pagamento elettronico**.  
5. Scegliere l'azione **Esporta**.  

## <a name="see-also"></a>Vedere anche

[Personalizzazione di Business Central per [!INCLUDE[d365fin](includes/d365fin_md.md)] con le estensioni](ui-extensions.md)  
[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
