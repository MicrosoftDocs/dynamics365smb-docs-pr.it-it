---
title: Impostare le valute aggiuntive
description: 'La contabilità generale è impostata per utilizzare la valuta locale (VL) e un''altra valuta viene impostata come valuta addizionale, con un tasso di cambio corrente assegnato.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'multiple currencies, foreign exchange rates'
ms.search.form: '5, 16,118, 483, 495'
ms.date: 07/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-an-additional-reporting-currency"></a>Impostare una valuta contabile addizionale

Con l'espandersi delle attività delle società in un numero sempre maggiore di paesi, diventa importante poter esaminare e riportare dati finanziari in più di una valuta.

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] se si stanno cercando informazioni in tempo reale sui tassi di cambio delle valute estere (FX) o sui tassi di cambio storici, queste informazioni vanno sotto il nome di valuta. Oltre a questo articolo, vedere anche [Aggiornamento dei tassi di cambio valuta](finance-how-update-currencies.md).

La contabilità generale è impostata per utilizzare la valuta locale (VL) ma è anche possibile impostarla per l'uso di un'altra valuta con un tasso di cambio corrente assegnato. Se si imposta una seconda valuta come valuta contabile addizionale, in [!INCLUDE[prod_short](includes/prod_short.md)] gli importi in ogni movimento C/G e in tutti gli altri movimenti, ad esempio i movimenti IVA, vengono registrati automaticamente sia nella valuta locale che nella valuta addizionale.

> [!Warning]
> La funzionalità Valuta contabile addizionale non deve essere utilizzata come base per la conversione del rendiconto finanziario se non se ne conoscono le limitazioni. Non esegue consente di eseguire la conversione dei rendiconti finanziari delle filiali estere come parte del consolidamento di una società. La valuta contabile addizionale può essere utilizzata soltanto per creare report in un'altra valuta, come se tale valuta fosse quella locale della società.
>
> Ad esempio, hai una grande quantità di crediti in sterline britanniche (GBP) e hai impostato la valuta contabile addizionale (VA) in GBP. In questo scenario, gli importi nei crediti che utilizzano GBP non verranno rettificati per gli utili/perdite di cambio nella VA, ma solo gli importi nei crediti che sono in altre valute. Ciò significa che se utilizzi VA per dichiarare i tuoi rendiconti finanziari, potrebbe risultare in saldi insoluti sottostimati o sopravvalutati dei crediti.

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Visualizzazione di report e importi nella valuta contabile addizionale
L'utilizzo di una valuta contabile addizionale può essere utile per il processo di creazione di report di una società nei seguenti casi:

- Società di paesi non UE che effettuano numerose transazioni con società di paesi UE. In questo caso, la società non UE potrebbe anche desiderare di creare report in euro per semplificare l'utilizzo dei report finanziari da parte dei partner commerciali UE.
- Società che desiderano visualizzare i report in una valuta maggiormente utilizzata a livello internazionale rispetto alla propria valuta locale.

Vari report finanziari sono basati sui movimenti C/G. Per visualizzare i dati del report nella valuta contabile addizionale, seleziona la casella di controllo **Mostra importi in valuta contabile addizionale** nella Scheda dettaglio **Opzioni** per il relativo report C/G.

## <a name="adjusting-exchange-rates"></a>Rettifica di tassi di cambio

Poiché i tassi di cambio oscillano costantemente, gli equivalenti in valuta addizionale nel sistema devono essere rettificati periodicamente. Se queste rettifiche non vengono apportate, gli importi che sono stati convertiti da valute estere (o addizionali) e registrati nella contabilità generale in valuta locale possono essere fuorvianti. Inoltre, i movimenti quotidiani registrati prima dell'immissione di un tasso di cambio quotidiano nell'applicazione devono essere aggiornati dopo l'immissione delle informazioni su tale tasso di cambio. Il processo batch **Rettifica tassi di cambio** viene utilizzato per rettificare i tassi di cambio dei movimenti cliente, fornitore e conti C/C bancari registrati. Consente inoltre di aggiornare gli importi nella valuta contabile addizionale nei movimenti C/G. Per ulteriori informazioni, vedere [Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md).

## <a name="setting-up-an-additional-reporting-currency"></a>Impostare una valuta contabile addizionale

Seguire questa procedura per impostare una valuta contabile addizionale:

- Specificare i conti C/G per la registrazione delle rettifiche al tasso di cambio.  
- Specificare il metodo della rettifica tasso di cambio per tutti i conti C/G.  
- Specificare il metodo di rettifica del tasso di cambio per i movimenti IVA.  
- Attivare la valuta contabile addizionale.  

### <a name="to-specify-general-ledger-accounts-for-posting-exchange-rate-adjustments"></a>Per specificare i conti C/G per la registrazione delle rettifiche tasso di cambio.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Valute**, quindi scegli il collegamento correlato.  
2. Nella pagina **Valute** riempire i seguenti campi per la valuta contabile addizionale.  

|Campo|Description|  
|---------------------------------|---------------------------------------|  
|**Conto utili CG realizzati**|Il conto CoGe nel quale vengono registrati i profitti del tasso di cambio per le rettifiche valutarie tra la valuta locale e la valuta contabile addizionale.|  
|**Conto perdite CG realizzate**|Il conto C/G nel quale vengono registrate le perdite del tasso di cambio per le rettifiche valutarie tra la valuta locale e la valuta contabile addizionale.|  
|**Conto guadagni residui**|Il conto CoGe in cui registrare gli importi residui che rappresentano dei profitti nel caso in cui si effettui la registrazione nell'area di applicazione contabilità generale sia nella valuta locale che nella valuta contabile addizionale.|  
|**Conto perdite residue**|Il conto CoGe in cui registrare gli importi residui che rappresentano delle perdite nel caso in cui si effettui la registrazione nell'area di applicazione contabilità generale sia nella valuta locale che nella valuta contabile addizionale.|

> [!NOTE]  
>  Gli importi residui possono verificarsi quando gli importi in dare e in avere convertiti dalla valuta locale in una valuta contabile addizionale vengono arrotondati da [!INCLUDE[prod_short](includes/prod_short.md)].  

Per ogni conto C/G, è necessario specificare in che modo gli importi C/G per il conto vengono rettificati in caso di fluttuazioni del tasso di cambio tra la valuta locale e quella contabile addizionale.  

### <a name="to-specify-the-exchange-rate-adjustment-method-for-all-general-ledger-accounts"></a>Per specificare il metodo della rettifica tasso di cambio per tutti i conti C/G

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
2. Nella pagina **Piano dei conti**, selezionare il conto pertinente quindi scegliere l'azione **Modifica**.  
3. Nella pagina **Scheda conto GL** selezionare il metodo pertinente nel campo **Rettifica tasso di cambio**.  

    Se si effettua la registrazione in una valuta addizionale, specificare nel campo **Rettifica tasso di cambio** in che modo viene rettificato il conto C/G per le fluttuazioni del tasso di cambio tra la valuta locale e quella contabile addizionale. Nella tabella seguente vengono indicate le opzioni che è possibile scegliere.  

    |Campo|Descrizione|  
    |----------------------------------|---------------------------------------|  
    |**No Rettifica**|Non viene effettuata alcuna rettifica del tasso di cambio per il movimento C/G. Questa è l'opzione predefinita.<br /><br /> **NOTA:** TQuesta opzione deve essere selezionata se il tasso di cambio tra la valuta locale e quella contabile addizionale è sempre fisso.|  
    |**Rettifica Importo**|L'importo VL verrà rettificato per tutti gli utili e le perdite del tasso di cambio. Tali utili o perdite verranno registrati nel conto C/G nel campo **Importo** e nel campo **Conto utili C/G realizzati** o **Conto perdite C/G realizzate** della pagina **Valute** dei conti specificati per gli utili o le perdite.|  
    |**Rettifica Importo in Valuta-Addiz.**|La valuta contabile addizionale verrà rettificata per tutti gli utili e le perdite del tasso di cambio. Tali utili o perdite verranno registrati nel conto C/G nel campo **Importo in valuta addiz.** e nel campo **Conto utili C/G realizzati** o **Conto perdite C/G realizzate** della pagina **Valute** dei conti specificati per gli utili o le perdite.|  

    Gli utili e le perdite di conversione vengono registrati quando si esegue il processo batch **Rettifica tassi di cambio**. Durante il processo batch, viene individuato il tasso di cambio di rettifica nella pagina **Tassi di cambio valuta**, quindi vengono messi a confronto gli importi nei campi **Importo** e **Importo in valuta addiz.** nel movimento C/G per determinare se vi è un utile o una perdita di conversione. Nel processo batch viene utilizzata l'opzione selezionata nel campo **Rettifica tasso di cambio** per determinare come calcolare e registrare gli utili o le perdite di conversione nei conti C/G.  

4.  Chiudere la pagina **Scheda conto C/G**.  

### <a name="to-specify-exchange-rate-adjustment-method-for-vat-entries"></a>Per specificare il metodo di rettifica del tasso di cambio per i movimenti IVA

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.  
2. Nella pagina **Setup contabilità generale** selezionare il metodo pertinente nel campo **Rettif. tasso di cambio IVA**.  
3. Se si effettua la registrazione in una valuta contabile addizionale, è possibile specificare nel campo **Rettif. tasso di cambio IVA** in che modo vengono rettificati i conti impostati per la registrazione IVA nella pagina **Setup registrazioni IVA** per le fluttuazioni del tasso di cambio tra la valuta locale e quella addizionale.  

    Quando si esegue il processo batch **Rettifica tassi di cambio**, viene individuato il tasso di cambio di rettifica nella pagina **Tassi di cambio valuta**, quindi vengono messi a confronto gli importi nei campi **Importo** e **Importo in valuta addiz.** nel movimento IVA per determinare se vi è un utile o una perdita di conversione. L'opzione selezionata in questo campo viene utilizzata dal processo batch per determinare come registrare gli utili e le perdite di conversione per i conti IVA.  

    Sono disponibili le stesse tre opzioni disponibili per i movimenti C/G, ma in questo caso i movimenti rettificati sono i movimenti IVA. Nella tabella seguente vengono indicate le opzioni che è possibile scegliere.

    |Campo|Description|  
    |----------------------------------|---------------------------------------|  
    |**No Rettifica**|Non viene effettuata alcuna rettifica del tasso di cambio per il movimento C/G. Questa è l'opzione predefinita.|  
    |**Rettifica Importo**|L'importo VL verrà rettificato per tutti gli utili e le perdite del tasso di cambio. Tali utili o perdite verranno registrati nel conto C/G nel campo **Importo** e nel campo **Conto utili C/G realizzati** o **Conto perdite C/G realizzate** della pagina **Valute** dei conti specificati per gli utili o le perdite.|  
    |**Rettifica Importo in Valuta-Addiz.**|La valuta contabile addizionale verrà rettificata per tutti gli utili e le perdite del tasso di cambio. Tali utili o perdite verranno registrati nel conto C/G nel campo **Importo in valuta addiz.** e nel campo **Conto utili C/G realizzati** o **Conto perdite C/G realizzate** della pagina **Valute** dei conti specificati per gli utili o le perdite.|  

### <a name="to-activate-the-additional-reporting-currency"></a>Per attivare la valuta contabile addizionale
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.  
2. Nella pagina **Setup contabilità generale** scegliere il campo **Valuta contabile addizionale** per selezionare la valuta addizionale in cui si desidera effettuare la registrazione.  
3. Quando si esce dal campo, verrà visualizzato un messaggio di conferma in [!INCLUDE[prod_short](includes/prod_short.md)] in cui sono descritti gli effetti dell'attivazione della valuta contabile addizionale.  
4. Selezionare il pulsante **Sì** per confermare che si desidera attivare la valuta.  
5. Verrà aperto il processo batch **Rett. valuta cont. addizionale**.

    Con questo processo è possibile convertire gli importi VL nei movimenti esistenti nella valuta contabile addizionale. Nel processo batch viene utilizzato un tasso di cambio predefinito copiato dal tasso di cambio valido alla data di lavoro nella pagina **Tassi di cambio valuta**. Gli importi residui che si verificano nella conversione della valuta locale in valuta contabile addizionale vengono registrati nei conti utili e nei conti perdite residui specificati nella pagina **Valute**. La data di registrazione e il numero di documento di questi movimenti saranno gli stessi del movimento C/G originale. Dopo la registrazione di tutti questi movimenti residui, con il processo batch viene registrato un movimento di arrotondamento alla data di chiusura di ogni anno chiuso nel conto profitti/perdite. In questo modo viene garantito che il saldo finale dei conti di entrata di ogni anno chiuso sia 0, sia in valuta locale sia nella valuta contabile addizionale.
6. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Scegliere **OK** per eseguire il processo batch.  

Dopo avere eseguito il processo batch, gli importi nei seguenti movimenti esistenti saranno espressi sia nella valuta locale che in quella contabile addizionale:  

- Movimenti C/G  
- Mov. collegamento articoli  
- Movimenti IVA  
- Movimenti contabili progetto  
- Movimenti valorizzazione  
- Righe degli ordini di produzione  
- Movimenti contabili ordini di produzione  

Per tutti i movimenti futuri dello stesso tipo gli importi vengono inoltre registrati sia nella valuta locale che in quella contabile addizionale.  

> [!NOTE]  
> Il campo **Valuta contabile addizionale** verrà attivata solo dopo aver fatto clic sul pulsante **OK** nel processo batch **Rett. valuta cont. addizionale**.  

## <a name="see-also"></a>Vedi anche

[Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md)  
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
