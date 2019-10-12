---
title: Prezzi e sconti speciali e alternativi per i fornitori | Microsoft Docs
description: È possibile definire prezzi e accordi di sconto diversi e alternativi e applicarli ai documenti di acquisto per i fornitori.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2495292a967d81cd64694d3a238399e964c1d94f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316718"
---
# <a name="record-special-purchase-prices-and-discounts"></a>Registrare i prezzi di acquisto e gli sconti speciali
I differenti accordi relativi a prezzi e sconti applicati quando si effettuano acquisti da fornitori diversi devono essere definiti in modo che le regole e i valori concordati vengano applicati ai documenti di acquisto creati per il fornitore.

Dopo aver registrato prezzi speciali e gli sconti riga di vendita e di acquisto, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantisce che il profitto sul commercio degli articoli sia sempre ottimale calcolando automaticamente il miglior prezzo delle vendite e dei documenti di acquisto e delle righe di registrazione magazzino. Per ulteriori informazioni, vedere [Calcolo del prezzo migliore](purchasing-how-record-purchase-price-discount-payment-agreements.md#best-price-calculation).

Per quanto riguarda i prezzi, è possibile fare in modo che venga inserito un prezzo di acquisto speciale nelle righe di acquisto quando si verifica una determinata combinazione di fornitore, articolo, quantità minima, unità di misura o data di inizio o di fine.

Nel caso degli sconti, è possibile impostare e utilizzare due tipi di sconti:

| Tipo di sconto: | Descrizione |
| --- | --- |
| **Sconto riga acquisto** |È possibile fare in modo che venga inserito uno sconto sull'importo nelle righe di acquisto quando si verifica una determinata combinazione di fornitore, articolo, quantità minima, unità di misura o data di inizio o di fine. Il principio è lo stesso dei prezzi di acquisto. |
| **Sconto fattura** |Uno sconto in percentuale che viene sottratto dal totale del documento se l'importo del valore di tutte le righe di un documento di acquisto supera un determinato valore minimo. |

Poiché gli sconti riga acquisto e i prezzi di acquisto sono basati su una combinazione di articolo e fornitore, è anche possibile immettere questa configurazione dalla scheda articolo, in cui sono definiti le regole e i valori. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Per impostare un prezzo di acquisto speciale per un fornitore
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fornitori** e quindi scegliere il collegamento correlato.
2. Aprire la scheda fornitore interessata e scegliere l'azione **Prezzi**.

    Il campo **Tipo di acquisto** è già impostato su **Fornitore** e il campo **Codice acquisto** è impostato sul numero del fornitore.
3. Compilare i campi della riga in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Compilare una riga per ogni combinazione per la quale il fornitore concede uno sconto riga acquisto.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Per impostare uno sconto riga per un fornitore
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fornitori** e quindi scegliere il collegamento correlato.
2. Aprire la scheda fornitore interessata e scegliere l'azione **Sconti riga**.

    Il campo **Tipo di acquisto** è già impostato su **Fornitore** e il campo **Codice acquisto** è impostato sul numero del fornitore.
3. Compilare i campi della riga in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Compilare una riga per ogni combinazione per la quale il fornitore concede uno sconto riga acquisto.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Per impostare uno sconto su fattura per un fornitore
Una volta informati degli sconti su fattura concessi dai fornitori, immettere il codice sconto fattura nelle schede fornitore e impostare le condizioni per ciascun codice.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fornitori** e quindi scegliere il collegamento correlato.
2. Aprire la scheda fornitore relativa al fornitore al quale saranno applicati gli sconti fattura.
3. Nel campo **Cod. sconto fatt.** selezionare un codice per le condizioni di sconto fattura in questione che verrà utilizzato per calcolare gli sconti fattura per il fornitore.

    > [!NOTE]  
    >   I codici sconto fattura sono rappresentati da schede fornitore esistenti. Questo consente di assegnare rapidamente le condizioni dello sconto fattura ai fornitori perché basterà selezionare il nome di un altro fornitore che avrà le stesse condizioni.

    Continuare a impostare le nuove condizioni dello sconto fattura di acquisto.
4. Nella pagina **Scheda fornitore** scegliere l'azione **Sconti fattura**. Verrà visualizzata la pagina **Sconti fattura fornitori**.
5. Nel campo **Codice valuta** immettere il codice per una valuta alla quale sono collegate le condizioni dello sconto fattura nella riga. Lasciare il campo vuoto se si desidera impostare le condizioni di sconto fattura in valuta locale.
6. Nel campo **Importo minimo** immettere l'importo minimo che una fattura deve avere affinché le possa essere applicato lo sconto.
7. Nel campo **% sconto** immettere lo sconto fattura sotto forma di percentuale dell'importo fattura.
8. Ripetere i passaggi da 5 a 7 per ogni valuta per la quale il fornitore riceverà uno sconto fattura diverso.

Lo sconto fattura è ora impostato e assegnato al fornitore in questione. Quando si seleziona il codice fornitore nel campo **Cod. sconto fatt.** nelle altre schede fornitore, lo stesso sconto fattura viene assegnato a quei fornitori.

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a>Per scegliere una modalità di registrazione degli sconti di acquisto  
Quando si registra una fattura di acquisto che include uno o più sconti, si può scegliere fra due modalità di registrazione degli importi dello sconto. Gli sconti possono essere registrati separatamente oppure possono essere sottratti dagli sconti fattura.  

Prima di effettuare questa operazione, è necessario avere precedentemente impostato i conti necessari per la registrazione degli importi degli sconti nel piano dei conti. Verificare inoltre di avere immesso i numeri di conto corretti nel setup registrazioni COGE nei campi **Conto sconto riga acquisto** e **Conto sconto fattura acquisto**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità fornitori e acquisti** e quindi scegliere il collegamento correlato.
2. Nel campo **Registrazione sconti** scegliere uno dei criteri seguenti per la registrazione degli sconti.

|**Modalità di registrazione dello sconto**|**Sconto fattura**|**Sconto riga**|  
|------------------------------------|--------------------------|-----------------------|  
|**Tutti gli sconti**|Registrati separatamente|Registrati separatamente|  
|**Sconti Fattura**|Registrati separatamente|Sottratti|  
|**Sconti Riga**|Sottratti|Registrati separatamente|  
|**Nessuno sconto**|Sottratti|Sottratti|  

## <a name="purchase-invoice-discounts-and-service-charges"></a>Sconti fatture di acquisto e addebiti assistenza
Se esistono condizioni fisse per gli sconti sulle fatture con un fornitore qualsiasi, è possibile immettere tali condizioni in relazione ai corrispondenti fornitori. Lo sconto verrà calcolato quando si compila una fattura di acquisto.  

 Prima di utilizzare gli sconti fattura con gli acquisti, è necessario specificare i fornitori che offrono gli sconti.  

 Per collegare le percentuali di sconto a importi di fatturazione specifici, utilizzare le pagine **Sconti fattura fornitori**. È possibile immettere un numero qualsiasi di percentuali in ogni pagina. A ogni fornitore è possibile associare una propria pagina oppure è possibile collegare più fornitori alla stessa pagina.  

 Oltre a una percentuale di sconto, è possibile collegare l'importo di un addebito di assistenza a un importo della fattura specifico.  

 È possibile definire le condizioni per gli sconti fattura in VL per i fornitori a livello nazionale e in valuta estera per i fornitori esteri.  

 È inoltre possibile impostare [!INCLUDE[d365fin](includes/d365fin_md.md)] affinché vengano calcolati automaticamente gli sconti fattura per le offerte, gli ordini programmati, gli ordini, le fatture o le note di credito.  

> [!TIP]  
>  Prima di immettere le informazioni, è opportuno preparare uno schema della struttura di sconto da utilizzare. In questo modo, sarà più semplice visualizzare quali fornitori si possono collegare alla stessa pagina dello sconto fattura. Minore è il numero delle pagine da impostare, più veloce risulta l'inserimento delle informazioni principali.

## <a name="best-price-calculation"></a>Calcolo del prezzo migliore
Dopo aver registrato prezzi speciali e gli sconti riga di vendita e di acquisto, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantisce che il profitto sul commercio degli articoli sia sempre ottimale calcolando automaticamente il miglior prezzo delle vendite e dei documenti di acquisto e delle righe di registrazione magazzino.

Con il termine "miglior prezzo" si intende il prezzo più basso ammissibile che gode dello sconto riga più alto possibile praticabile in una specifica data. [!INCLUDE[d365fin](includes/d365fin_md.md)] calcola automaticamente questo prezzo quando inserisce il prezzo unitario e la percentuale di sconto riga per gli articoli in nuove righe di documenti e di registrazione.

> [!NOTE]  
>   Di seguito viene descritto come viene calcolato il prezzo migliore per le vendite. Il calcolo è lo stesso per gli acquisti.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] controlla la combinazione del cliente di fatturazione e dell'articolo e quindi calcola il prezzo unitario applicabile e la percentuale di sconto riga utilizzando i seguenti criteri:

    - Il cliente usufruisce di uno speciale accordo relativo a prezzi o sconti o appartiene a un gruppo che ne usufruisce?
    - L'articolo o il gruppo sconto articolo specificato nella riga è incluso in uno di tali accordi prezzi o sconti?
    - La data dell'ordine, o la data di registrazione per le fatture e le note di credito, è compresa nell'intervallo di validità dell'accordo prezzi o sconti?
    - È stato specificato un codice unità di misura? In caso affermativo, in [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno controllati i prezzi o gli sconti aventi lo stesso codice di unità di misura, altrimenti verranno verificati prezzi o gli sconti a cui non è associato alcun codice di unità di misura.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica se si applicano accordi di prezzo/sconto alle informazioni sul documento o sulla riga di registrazione, quindi inserisce il prezzo unitario e percentuale di sconto della riga, utilizzando i seguenti criteri:

    - C'è un requisito di quantità minima nell'accordo di prezzo/sconto che è soddisfatto?
    - C'è un requisito di valuta nell'accordo di prezzo/sconto che è soddisfatto? In caso affermativo, il prezzo più basso e lo sconto riga più alto per tale valuta vengono immessi, anche se VL fornirebbe un prezzo migliore. Se non esistono accordi prezzi o sconti riga per il codice di valuta specificato, in [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno automaticamente selezionati il prezzo più basso e lo sconto riga più alto per la valuta locale.

Se non è possibile calcolare alcun prezzo speciale per l'articolo specificato nella riga, viene recuperato l'ultimo costo diretto o il prezzo unitario dalla scheda articolo immesso.

## <a name="see-also"></a>Vedi anche
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
