---
title: Impostare il consolidamento di una società
description: Informazioni su come configurare il modo in cui i dati di diverse società in Business Central vengono riportati in una società di consolidamento.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="set-up-company-consolidation" />Impostare il consolidamento di una società

Prima di poter consolidare i movimenti di contabilità generale di due o più società separate (filiali) in una società consolidata, è necessario preparare i piani contabili e la società di consolidamento.  

In base alla complessità delle proprie società, esistono due modi per impostare il consolidamento:

* Se non sono necessarie impostazioni avanzate, come includere una società di cui si possiede solo una parte, è possibile utilizzare la guida al setup assistito **Consolidamento società** per impostare rapidamente un consolidamento. La guida consente di eseguire le operazioni di base.
* Se sono necessarie impostazioni più avanzate, è possibile eseguire un setup personalizzato della società consolidata e delle business unit.
  * In ogni business unit, specificare quali conti di contabilità generale devono essere inclusi nel consolidamento e il metodo di conversione del consolidamento per ogni conto.
  * Nella società di consolidamento impostare una scheda business unit per ogni società da includere nel consolidamento. Nella scheda business unit sono incluse informazioni quali le date dell'anno fiscale della business unit e la percentuale di ogni conto da includere nel consolidamento.

## <a name="simple-consolidation-setup" />Setup semplice del consolidamento

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]
Se il consolidamento è semplice, ad esempio perché si è il solo proprietario delle business unit da consolidare, la guida al setup assistito **Consolidamento società** consente l'esecuzione delle seguenti operazioni:

* Scegliere se creare una nuova società consolidata, oppure se consolidare i dati in una società già creata per il consolidamento. La società non deve contenere transazioni.
* Visualizzare un'anteprima dei risultati. [!INCLUDE[prod_short](includes/prod_short.md)] verifica la possibilità di trasferire correttamente transazioni e dati master alla società consolidata.

Per utilizzare la guida al setup assistito, attenersi a questa procedura:

1. Nella Gestione ruolo utente **Contabile**, scegliere l'azione **Setup assistito**.
2. Scegliere **Imposta creazione di report di consolidamento**, quindi completare ogni passaggio nella guida al setup assistito.

## <a name="advanced-consolidation-setup" />Setup avanzato del consolidamento

Se sono necessarie impostazioni più avanzate per il consolidamento, è possibile impostare il consolidamento manualmente. Ad esempio, se si possiedono solo parzialmente alcune società o se non si intende includere alcune società nel consolidamento.  

### <a name="set-up-the-consolidated-company" />Impostare la società consolidata

È necessario impostare in primo luogo la società consolidata. Una società consolidata viene impostata come qualsiasi altra società. Per ulteriori informazioni, vedere [Preparazione al business](ui-get-ready-business.md).  

Il seguente elenco illustra gli aspetti chiave della società consolidata.

1. Impostare un piano dei conti

    Per ulteriori informazioni, vedere [Impostazione o modifica del piano dei conti](finance-setup-chart-accounts.md).  

    I piani dei conti possono essere identici in una business unit e nella società consolidata oppure la società consolidata può avere un piano dei conti diverso. Se il piano dei conti di una business unit è diverso da quello della società consolidata, è necessario specificare il mapping tra i conti nei conti nella business unit. Per ulteriori informazioni, vedere la sezione [Preparare i conti di contabilità generale per il consolidamento](#glacc).

2. Aggiungere business unit

    Per consolidare i dati finanziari di diverse società in una società consolidata, è necessario immettere le informazioni relative alle filiali da includere come business unit e al livello in base al quale le cifre devono essere incluse.

    Per ulteriori informazioni, vedere la sezione [Aggiungere business unit](#busunit).
3. Se si esegue il consolidamento dei rendiconti finanziari di business unit in una valuta estera, è possibile specificare tassi di cambio.

    I tre tassi di cambio utilizzati nel programma sono **Tasso medio (manuale)**, **Tasso di chiusura** e **Ultimo tasso di chiusura**. Per ulteriori informazioni, vedere la sezione [Specificare i tassi di cambio per i consolidamenti](#exchrates).
4. È possibile consolidare le informazioni sulle dimensioni, nonché i conti della contabilità generale.

    Per ulteriori informazioni, vedere la sezione [Includere o escludere dimensioni](#dim).

### <a name="add-business-units" /><a name="busunit"></a>Aggiungere business unit

[!INCLUDE[prod_short](includes/prod_short.md)] consente di impostare un elenco di business unit da consolidare, verificare i dati contabili prima di eseguire il consolidamento, importare file e generare report relativi al consolidamento.  

1. Accedere alla società consolidata.
2. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Business unit**, quindi scegli il collegamento correlato.  
3. Scegliere **Nuovo** e compilare i campi necessari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Quando si compilano i campi **Data inizio** e **Data fine**, assicurarsi di essere in conformità con le norme GAAP relative ai periodi fiscali della business unit rispetto alla casa madre.
4. Ripetere il passaggio 3 per ogni business unit aggiuntiva

Se una business unit utilizza una valuta straniera, è necessario specificare il tasso di cambio da utilizzare nel consolidamento. È inoltre necessario immettere le informazioni di consolidamento nei conti C/G della business unit. Tali processi sono descritti nelle sezioni riportate di seguito.

### <a name="prepare-general-ledger-accounts-for-consolidation" /><a name="glacc"></a>Preparare i conti di contabilità generale per il consolidamento

Nel piano dei conti di una società che verrà consolidata devono essere specificati i conti per il consolidamento. Per ogni conto C/G di ogni società, è necessario specificare il conto C/G della società consolidata in cui verrà trasferito il saldo al momento del consolidamento. Questa mappatura consente il consolidamento di società con piani dei conti diversi.

Se il piano dei conti nella business unit differisce dalla società consolidata, è necessario preparare conti di contabilità generale per il consolidamento. È possibile specificare i conti in cui registrare debiti e crediti nonché il metodo da utilizzare per convertire le valute nella società consolidata. Ciò è utile se, ad esempio, si esegue spesso il report.

1. In [!INCLUDE [prod_short](includes/prod_short.md)] di ogni business unit, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
2. Aprire la scheda del conto e compilare i campi della Scheda dettaglio **Consolidamento**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="specify-exchange-rates-for-consolidations" /><a name="exchrates"></a>Specificare i tassi di cambio per i consolidamenti

Se una business unit utilizza una valuta diversa rispetto alla società consolidata, è necessario specificare i metodi dei tassi di cambio per ogni conto prima di eseguire il consolidamento. Per ogni conto, il contenuto del campo **Metodo conversione consol.** determina il tasso di cambio. Nella società consolidata, nel campo **Tabella tasso di cambio valuta** di ogni scheda business unit specificare se per il consolidamento saranno utilizzati i tassi di cambio della business unit o della società consolidata. Se si utilizzano i tassi di cambio della società consolidata, è possibile modificare i tassi di cambio per una business unit. Per le business unit, se nel campo **Tabella tasso di cambio valuta** della scheda business unit è indicato **Locale**, è possibile modificare il tasso di cambio nella scheda stessa. I tassi di cambio vengono copiati dalla tabella **Tassi di cambio valute**, ma è possibile modificarli prima del consolidamento.

Nella tabella seguente sono descritti i metodi dei tassi di cambio che è possibile utilizzare per i conti.

|Tasso di cambio | Uso tipico |
|---|---|
|Tasso medio (manuale) | il tasso medio per il periodo da consolidare viene calcolato manualmente. La media viene calcolata come media matematica o come valore approssimativo e viene specificata per ogni business unit. È utilizzato per i conti economici.|
|Tasso di chiusura | Utilizzato per i conti di bilancio patrimoniale.|
|Ultimo tasso di chiusura | Il tasso valido nel mercato del cambio estero alla data per cui lo stato patrimoniale o il conto economico viene preparato. Questo tasso viene specificato per ogni business unit. Utilizzato per i conti di bilancio patrimoniale.|
|Tasso storico | Il tasso di cambio valido al momento della transazione.|
|Tasso composito | Gli importi del periodo corrente vengono convertiti sulla base del tasso medio e aggiunti al saldo precedentemente registrato nella società consolidata. Questo metodo viene solitamente utilizzato per conti utili non distribuiti, poiché includono importi relativi a periodi diversi e sono quindi costituiti da importi convertiti con diversi tassi di cambio.|
|Tasso equo | È analogo al tasso **composito**. Le differenze sono registrate in conti di contabilità generale separati.|

Per specificare i tassi di cambio per le business unit, attenersi alla seguente procedura:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Business unit**, quindi scegli il collegamento correlato.  
2. Nella pagina **Lista business unit**, scegliere la business unit, quindi l'azione **Tasso medio (manuale)**.  
3. Nella pagina **Modifica tasso di cambio**, il campo **Importo tasso cambio relativo** contiene valori copiati dalla tabella **Tassi di cambio valute**, ma è possibile modificarli. Chiudere la pagina.  
4. Scegliere l'azione **Tasso di chiusura**.  
5. Nel campo **Importo tasso cambio relativo**, immettere il tasso di cambio.

### <a name="include-or-exclude-dimensions" /><a name="dim"></a>Includere o escludere dimensioni

È possibile consolidare le informazioni sulle dimensioni, nonché i conti della contabilità generale.

* Sulle dimensioni rilevanti, specificare il campo **Codice di consolidamento** o lasciarlo vuoto
  * Per escludere una dimensione dal consolidamento, lasciare il campo **Codice di consolidamento** vuoto sulla dimensione e non scegliere le dimensioni nel campo **Copia dimensioni** in qualsiasi funzione o report di consolidamento.
  * Per includere le informazioni sulla dimensione nel consolidamento, lasciare il campo **Codice di consolidamento** vuoto. Il consolidamento verrà tuttavia eseguito solo se i valori dimensioni nella business unit sono esattamente uguali a quelli nella società consolidata.
  * Per consolidare il codice del valore di dimensione nella business unit con un codice del valore di dimensione diverso nella società consolidata, compilare il campo **Codice consolidamento** nelle dimensioni rilevanti.  
* Aggiungere le dimensioni rilevanti ai conti di contabilità generale rilevanti

### <a name="exclude-a-company-from-consolidation" /><a name="exclude"></a>Escludere una società dal consolidamento

Se non si desidera includere una business unit nel consolidamento, è possibile escluderla. A questo proposito, passare alla scheda business unit e deselezionare la casella di controllo **Consolidare**.

### <a name="include-a-partially-owned-company-in-consolidation" /><a name="include"></a>Includere una società di cui si possiede soltanto una parte

Se si possiede solo una parte di una società, è possibile includere una percentuale di ogni transazione che corrisponde alla percentuale della società di cui si è possessore. Ad esempio, se si possiede il 70% della società, il consolidamento includerà € 70 di una fattura di € 100. Per specificare la percentuale della società posseduta, passare alla scheda business unit e immettere la percentuale nel campo **% consolidamento**.  

## <a name="see-also" />Vedere anche

[Consolidare dati finanziari di molteplici società](finance-consolidated-company-reporting.md)  
[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Esportazione dei dati aziendali in Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
