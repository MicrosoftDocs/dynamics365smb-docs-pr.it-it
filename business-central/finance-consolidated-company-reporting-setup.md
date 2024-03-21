---
title: Impostare il consolidamento di una società
description: Informazioni su come configurare il modo in cui i dati di diverse società in Business Central vengono riportati in una società di consolidamento.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 09/25/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# Impostare il consolidamento di una società

Prima di poter consolidare i movimenti di contabilità generale di due o più società (filiali) in una società consolidata, è necessario preparare i piani contabili e la società di consolidamento.  

In base alla complessità delle proprie società, esistono due modi per impostare il consolidamento:

* Se non sono necessarie impostazioni avanzate, come includere una società di cui si possiede solo una parte, è possibile utilizzare la guida al setup **Consolidamento società** per impostare rapidamente un consolidamento. La guida consente di eseguire le operazioni di base.
* Se sono necessarie impostazioni più avanzate, è possibile eseguire un setup personalizzato della società consolidata e delle business unit.
  * In ogni business unit, specificare i conti di contabilità generale da includere nel consolidamento e il metodo di conversione per ogni conto.
  * Nella società consolidata, imposta una scheda Business unit per ogni società da includere nel consolidamento. Nella scheda Business unit sono incluse informazioni quali le date dell'anno fiscale della business unit e la percentuale di ogni conto da includere nel consolidamento.

## Setup semplice del consolidamento

Se il consolidamento è semplice, ad esempio perché sei il solo proprietario delle business unit da consolidare, la guida **Consolidamento società** ti consente di:

* Creare una nuova società consolidata o consolidare una società che hai già creato. La società non deve contenere transazioni.
* Visualizzare un'anteprima dei risultati. [!INCLUDE[prod_short](includes/prod_short.md)] verifica la possibilità di trasferire senza errori transazioni e dati master alla società consolidata.

Per utilizzare la guida al setup assistito, attenersi a questa procedura:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , entrare in **Setup assistito**e poi scegliere il link relativo.
2. Scegli **Elaborazione consolidamenti**, quindi completa ogni passaggio nella guida al setup assistito Consolidamento della società.

## Setup avanzato del consolidamento

Se sono necessarie impostazioni più avanzate per il consolidamento, è possibile impostare il consolidamento manualmente. Ad esempio, se possiedi solo parzialmente alcune società o se non intendi includere alcune società.  

### Impostare la società consolidata

È necessario impostare in primo luogo la società consolidata. Una società consolidata viene impostata come qualsiasi altra società. Per saperne di più sull'impostazione di una società, vedi [Preparazione al business](ui-get-ready-business.md).  

Il seguente elenco illustra gli aspetti chiave della società consolidata.

1. Imposta il piano dei conti.

    Per ulteriori informazioni sull'impostazione di un piano dei conti, vedi [Impostazione o modifica del piano dei conti](finance-setup-chart-accounts.md).  

    I piani dei conti possono essere identici in una business unit e nella società consolidata oppure la società consolidata può avere un piano dei conti diverso. Se il piano dei conti di una business unit differisce da quello della società consolidata, devi mappare i conti ai conti nella business unit. Per ulteriori informazioni, vedi la sezione [Preparare i conti di contabilità generale per il consolidamento](#glacc).

2. Aggiungi business unit.

    Per consolidare i dati di più società, devi impostare le filiali come business unit e specificare quanta parte dei relativi saldi includere. Per saperne di più sulle business unit, vedi la sezione [Aggiungere business unit](#busunit).

3. Specifica i tassi di cambio, se necessario.

    Specifica i tassi di cambio se consoliderai i dati per le business unit che utilizzano valute diverse. I tre tassi di cambio che puoi usaree sono **Tasso medio (manuale)**, **Tasso di chiusura** e **Ultimo tasso di chiusura**. Per saperne di più sui tassi di cambio, vedi la sezione [Specificare i tassi di cambio per i consolidamenti](#exchrates).

4. Consolida le informazioni sulle dimensioni e i conti CoGe.

    Per ulteriori informazioni, vedi la sezione [Includere o escludere dimensioni](#dim).

### <a name="busunit"></a>Aggiungere business unit

Nella società consolidata, imposta ogni società di cui vuoi consolidare i dati come business unit. Prima di eseguire un consolidamento e generare il report di consolidamento, è consigliabile verificare i dati finanziari in ogni business unit.

Una parte importante dell'impostazione della business unit consiste nel specificare in che modo tale unit condividerà i propri dati finanziari con la società consolidata. Sono disponibili opzioni automaticche e manuali:

* Per utilizzare un processo manuale, per [!INCLUDE [prod_short](includes/prod_short.md)] online e locale, puoi esportare un file .xml che contiene i movimenti C/G della unit. Importa quindi il file nella società consolidata.
* Per automatizzare lo scambio di dati, per [!INCLUDE [prod_short](includes/prod_short.md)] online puoi utilizzare un'API that [!INCLUDE [prod_short](includes/prod_short.md)] fornisce per condividere i dati tra ambienti. Se le tue società si trovano nello stesso ambiente, puoi utilizzare l'opzione **Database**.

> [!NOTE]
> L'opzione API ti consente anche di condividere i movimenti C/G di altri ambienti di [!INCLUDE [prod_short](includes/prod_short.md)]. Per utilizzare l'opzione API, l'utente che configura il consolidamento deve disporre dell'autorizzazione per accedere ai movimenti CoGe. Ad esempio, i set di autorizzazioni D365 Basic e D365 Read forniscono l'accesso.

1. Accedere alla società consolidata.
2. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Business unit**, quindi scegli il collegamento correlato.  
3. Scegli **Nuovo** e compila i campi necessari nella Schede dettaglio **Generale** e **Conti G/L**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Quando si compilano i campi **Data inizio** e **Data fine**, assicurarsi di essere in conformità con le norme GAAP relative ai periodi fiscali della business unit rispetto alla casa madre.
4. Nella Scheda dettaglio **Importazione dati** nel campo **Importazione dati predefinita**, specifica come condividerai i movimenti C/G con la società consolidata:

   * Per condividere i dati tra società nello stesso ambiente, scegli **Database**.
   * Per condividere i dati tra società in ambienti diversi, scegli **API**, quindi compila il campo **Endpoint dell'API**.
        
        Per ottenere l'URL dell'endpoint, nell'istanza [!INCLUDE [prod_short](includes/prod_short.md)] della società della business unit, apri la pagina **Scheda business unit** e scegli l'azione **Setup**. 
   * Per esportare un file .xml e condividerlo manualmente, scegli **Formato file**.

### <a name="glacc"></a>Preparare i conti di contabilità generale per il consolidamento

Nel piano dei conti di una società che verrà consolidata devono essere specificati i conti per il consolidamento. Per ogni conto C/G di ogni società, devi specificare il conto C/G della società consolidata a cui trasferire il saldo. Questo mapping ti consente di consolidare le società che hanno piani dei conti diversi.

Se il piano dei conti nella business unit differisce dalla società consolidata, è necessario preparare conti di contabilità generale per il consolidamento. È possibile specificare i conti in cui registrare debiti e crediti nonché il metodo da utilizzare per convertire le valute nella società consolidata.

1. In [!INCLUDE [prod_short](includes/prod_short.md)] di ogni business unit, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
2. Aprire la scheda del conto e compilare i campi della Scheda dettaglio **Consolidamento**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="exchrates"></a>Specificare i tassi di cambio per i consolidamenti

Se una business unit utilizza una valuta diversa rispetto alla società consolidata, è necessario specificare i metodi dei tassi di cambio per ogni conto prima di eseguire il consolidamento. Per ogni conto, il contenuto del campo **Metodo conversione consol.** determina il tasso di cambio. Nella società consolidata, nel campo **Tabella tasso di cambio valuta** di ogni scheda business unit specificare se per il consolidamento saranno utilizzati i tassi di cambio della business unit o della società consolidata. Se si utilizzano i tassi di cambio della società consolidata, è possibile modificare i tassi di cambio per una business unit. Per le business unit, se nel campo **Tabella tasso di cambio valuta** della scheda business unit è indicato **Locale**, è possibile modificare il tasso di cambio nella scheda stessa. I tassi di cambio vengono copiati dalla tabella **Tassi di cambio valute**, ma è possibile modificarli prima del consolidamento.

Nella tabella seguente sono descritti i metodi dei tassi di cambio che è possibile utilizzare per i conti.

|Tasso di cambio | Uso tipico |
|---|---|
|Tasso medio (manuale) | il tasso medio per il periodo da consolidare viene calcolato manualmente. La media viene calcolata come media matematica o come valore approssimativo e viene specificata per ogni business unit. Da utilizzare per i conti economici.|
|Tasso di chiusura | Utilizzato per i conti di bilancio patrimoniale.|
|Ultimo tasso di chiusura | Il tasso valido nel mercato del cambio estero alla data per cui lo stato patrimoniale o il conto economico viene preparato. Questo tasso viene specificato per ogni business unit. Da utilizzare per i conti di bilancio patrimoniale.|
|Tasso storico | Il tasso di cambio valido al momento della transazione.|
|Tasso composito | Gli importi del periodo corrente vengono convertiti sulla base del tasso medio e aggiunti al saldo precedentemente registrato nella società consolidata. In genere si utilizza questo metodo per i conti profitti/perdite. Tali conti includono importi di periodi diversi, pertanto contengono importi convertiti con tassi di cambio diversi.|
|Tasso equo | Questa opzione è simile a **Tasso composito**. Le differenze sono registrate in conti di contabilità generale separati.|

Per specificare i tassi di cambio per le business unit, attenersi alla seguente procedura:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Business unit**, quindi scegli il collegamento correlato.  
2. Nella pagina **Lista business unit**, scegliere la business unit, quindi l'azione **Tasso medio (manuale)**.  
3. Nella pagina **Modifica tasso di cambio**, il campo **Importo tasso cambio relativo** contiene valori copiati dalla tabella **Tassi di cambio valute**, ma è possibile modificarli. Chiudere la pagina.  
4. Scegliere l'azione **Tasso di chiusura**.  
5. Nel campo **Importo tasso cambio relativo**, immettere il tasso di cambio.

### <a name="dim"></a>Includere o escludere dimensioni

È possibile consolidare le informazioni sulle dimensioni, nonché i conti della contabilità generale.

* Nelle dimensioni, specifica il campo **Codice di consolidamento** o lascialo vuoto.
  * Per escludere una dimensione dal consolidamento, lascia il campo **Codice di consolidamento** vuoto sulla dimensione e non scegliere le dimensioni nel campo **Copia dimensioni** in qualsiasi funzione o report di consolidamento.
  * Per includere le informazioni sulla dimensione nel consolidamento, lasciare il campo **Codice di consolidamento** vuoto. Il consolidamento verrà tuttavia eseguito solo se i valori dimensioni nella business unit sono esattamente uguali a quelli nella società consolidata.
  * Per consolidare il codice del valore di dimensione nella business unit con un codice del valore di dimensione diverso nella società consolidata, compila il campo **Codice consolidamento** nelle dimensioni.  
* Aggiunge le dimensioni ai conti di contabilità generale.

### <a name="exclude"></a>Escludere una società dal consolidamento

Se non desideri includere una business unit nel consolidamento, puoi escluderla. A questo proposito, passa alla scheda business unit e deseleziona la casella di controllo **Consolidare**.

### <a name="include"></a>Includere una società di cui si possiede soltanto una parte

Se possiedi solo una parte di una società, puoi includere una percentuale di ogni transazione che riflette la percentuale della società che possidedi. Ad esempio, se possiedi il 70% della società, il consolidamento includi € 70 di una fattura di € 100. Per specificare la percentuale della società posseduta, passa alla scheda business unit e immetti la percentuale nel campo **% consolidamento**.  

## Vedi anche

[Consolidare dati finanziari di molteplici società](finance-consolidated-company-reporting.md)  
[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Esportazione dei dati aziendali in Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]