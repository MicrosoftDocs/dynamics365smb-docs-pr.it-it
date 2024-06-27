---
title: Tolleranza di pagamento e di sconto pagamento
description: Questo articolo spiega come impostare la tolleranza di pagamento per chiudere una fattura quando il pagamento non copre completamente l'importo della fattura.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '118, 314, 395'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
ms.author: bholtorf
ms.reviewer: bholtorf
---
# <a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a>Usare le tolleranze pagamento e le tolleranze sconto pagamento

È possibile impostare una tolleranza di pagamento per chiudere una fattura quando il pagamento non copre l'intero importo della fattura. Ad esempio, le tolleranze pagamento sono in genere per importi di piccola entità per cui costerebbe di più la correzione che semplicemente accettarli. È possibile impostare una tolleranza sconto pagamento per consentire uno sconto sul pagamento dopo la data dello sconto sul pagamento.  

Utilizza le tolleranze di pagamento in modo che ogni importo inevaso abbia una tolleranza di pagamento massima consentita. Se la tolleranza di pagamento viene soddisfatta, l'importo pagamento viene quindi analizzato. Se l'importo del pagamento rappresenta un sottopagamento, questo chiude completamente l'importo inevaso. Viene registrato un movimento contabile dettagliato nel movimento del pagamento in modo che non esista un importo residuo nel movimento di fattura collegato. Se l'importo del pagamento rappresenta un sovrapagamento, viene registrato un nuovo movimento contabile dettagliato nel movimento del pagamento in modo che non esista un importo residuo nel movimento di pagamento.

Puoi impostare le tolleranze sconto pagamento in modo che, se accetti uno sconto dopo la relativa data di scadenza, tale evento viene registrato in un conto degli sconti sul pagamento oppure in un conto delle tolleranze di pagamento.

## <a name="applying-payment-tolerance-to-multiple-documents"></a>Collegamento della tolleranza di pagamento a più documenti

Un documento singolo ha la stessa tolleranza di pagamento indipendentemente dal fatto che sia collegata in modo autonomo o ad altri documenti. L'accettazione di uno sconto di pagamento ritardato quando si collega la tolleranza di pagamento a più documenti si verifica automaticamente per ogni documento in cui la seguente regola è vera:  

*data sconto sul pagamento < data di pagamento (nel movimento in questione) <= data tolleranza di pagamento*  

Questa regola determina anche se visualizzare avvisi quando si collega la tolleranza di pagamento a più documenti. L'avviso di tolleranza sconto pagamento viene visualizzato per ogni movimento che soddisfa i criteri di data. Per ulteriori informazioni, vedere [Esempio 2: calcoli di tolleranza per più documenti](finance-payment-tolerance-and-payment-discount-tolerance.md#example-2---tolerance-calculations-for-multiple-documents).

È possibile scegliere di visualizzare un avviso che è basato su situazioni di tolleranza differenti.  

- Il primo avviso riguarda la tolleranza di sconto sul pagamento. Vieni informato che è possibile accettare uno sconto di pagamento ritardato. Egli può quindi scegliere se accettare la tolleranza alla data dello sconto.  
- Il secondo avviso riguarda la tolleranza di pagamento. Vieni informato che tutti i movimenti possono venir chiusi a causa della differenza nella somma della tolleranza di pagamento massima per i movimenti collegati. Egli può quindi scegliere se accettare la tolleranza nell'importo di pagamento.

> [!NOTE]
> L'abilitazione del messaggio di avviso consentirà di scegliere come elaborare i pagamenti che rientrano nella tolleranza. Se non si abilita il messaggio e si specifica un livello di tolleranza, le fatture con importi entro la tolleranza verranno chiuse automaticamente e non sarà possibile scegliere di lasciare l'importo residuo. 

Per ulteriori informazioni, vedere [Abilitare o disabilitare gli avvisi di tolleranza pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings). 

## <a name="to-set-up-tolerances"></a>Per impostare le tolleranze

La tolleranza su giorni e importi consente di chiudere una fattura anche se il pagamento non copre interamente l'importo in fattura. Ad esempio, perché la data di scadenza per lo sconto sul pagamento è passata, le merci sono state detratte, o a causa di un errore minore. Questo principio è valido anche per note di credito e rimborsi.  

Per impostare le tolleranze è necessario impostare vari conti di tolleranza, specificare entrambi i metodi di registrazione della tolleranza di sconto sul pagamento e della tolleranza di pagamento, quindi eseguire il processo batch **Modifica tolleranza pagamento**.  
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup registrazioni COGE**, quindi scegli il collegamento correlato.  
2. Aprire la pagina **Setup registrazioni COGE**, impostare un conto di tolleranza a debito e a credito dei pagamenti relativi alle vendite e un conto di tolleranza a debito e a credito dei pagamenti relativi agli acquisti.  
3. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cat. reg. clienti**, quindi scegli il collegamento correlato.    
4. Aprire la pagina **Cat. reg. clienti**, impostare un conto di tolleranza a debito e a credito dei pagamenti. Per ulteriori informazioni, vedere [Impostazione delle categorie di registrazione](finance-posting-groups.md).  
5. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup registrazioni fornitori**, quindi scegli il collegamento correlato.  
6. Aprire la pagina **Cat. reg. fornitori**, impostare un conto di tolleranza a debito e a credito dei pagamenti.  
7. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.  
8. Aprire la pagina **Setup contabilità generale**.  
9. Nella Scheda dettaglio **Collegamento** compilare i campi **Registrazione tolleranza sconto pagamento**, **Periodo di dilazione sconto pagamento** e **Registrazione toll. pagamento**.   
10. Scegliere l'azione **Modifica tolleranza pagamento**.

    > [!NOTE]
    > Quando scegli **Collega al più Vecchio** nel campo **Metodo di collegamento** su una pagina **Scheda cliente**, [!INCLUDE[prod_short](includes/prod_short.md)] non pubblicherà automaticamente le tolleranze di pagamento, anche quando rientrano nelle soglie impostate nella pagina **Impostazione contabilità generale**. [!INCLUDE[prod_short](includes/prod_short.md)] presuppone che l'impostazione Applica al più vecchio indichi che il cliente (o tu come cliente del fornitore) ha un conto con cui paga regolarmente il saldo. Pertanto, gli importi rimanenti non devono essere rimossi registrando un movimento di tolleranza di pagamento.

11. Nella pagina **Modifica tolleranza pagamento** compilare i campi **% tolleranza pagamento** e **Importo massimo tolleranza pagamento** e quindi scegliere **OK**.

> [!IMPORTANT]  
> Con questa procedura la tolleranza viene impostata solo per la valuta locale. Se si desidera che [!INCLUDE[prod_short](includes/prod_short.md)] gestisce le tolleranze sui pagamenti, le note di credito e i rimborsi in una valuta estera, è necessario eseguire il processo batch **Modifica tolleranza pagamento** con un valore nel campo **Codice valuta**.  

> [!NOTE]  
> Per ricevere un messaggio di avviso tolleranza pagamento ogni volta che si registra un collegamento della tolleranza, è necessario attivare l'Avviso tolleranza pagamento. Per ulteriori informazioni, vedere la sezione [Per abilitare o disabilitare gli avvisi di tolleranza pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).  
>
> Per disattivare la tolleranza per un cliente o un fornitore, blocca le tolleranze nella relativa scheda cliente o scheda fornitore. Per ulteriori informazioni, vedere la sezione [Per bloccare la tolleranza pagamento per i clienti](finance-payment-tolerance-and-payment-discount-tolerance.md#to-block-payment-tolerance-for-customers).  
>
> Quando si imposta la tolleranza, [!INCLUDE[prod_short](includes/prod_short.md)] verifica automaticamente l'esistenza di movimenti aperti e calcola la tolleranza anche per tali movimenti.

> [!IMPORTANT]  
> Quando abiliti il campo **Rettifica per sconto pagamento** nella pagina **Setup registrazioni IVA**, l'importo dell'IVA è considerato in quanto relativo agli importi **Tolleranze di pagamento** e **Sconti sui pagamenti** e l'IVA sarà ridotta per entrambi gli importi delle transazioni, se esistenti. Il sistema non può essere configurato per utilizzare la riduzione dell'IVA solo per un tipo di transazione.  

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a>Per abilitare o disabilitare gli avvisi di tolleranza pagamento

L'avviso tolleranza pagamento viene visualizzato quando si registra un collegamento con un saldo che rientra nella tolleranza consentita. Sarà quindi possibile decidere come registrare e documentare il saldo.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.  
2. Nella Scheda dettaglio **Collegamento** della pagina **Setup contabilità generale**, attivare l'opzione **Avviso tolleranza pag.** per attivare l'avviso. Per disattivare l'avviso, disattivare l'opzione.  

> [!NOTE]  
> L'opzione predefinita per la pagina **Avviso tolleranza pag.** è **Mantieni il saldo come importo residuo**. L'opzione predefinita per la pagina **Avviso tolleranza sconto pagamento** è **Non accettare lo sconto di pagamento ritardato**.

## <a name="to-block-payment-tolerance-for-customers"></a>Per bloccare la tolleranza pagamento per i clienti

Per impostazione di default, la tolleranza di pagamento è consentita. Per disattivare la tolleranza di pagamento per un cliente o un fornitore, blocca la tolleranza nella relativa scheda cliente o scheda fornitore. I passaggi seguenti descrivono come eseguire l'operazione per un cliente. I passaggi sono simili per un fornitore.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cliente** o **Fornitore**, quindi scegli il collegamento correlato.  
2. Nella Scheda dettaglio **Pagamenti** selezionare la casella di controllo **Blocca tolleranza pagam**.  

> [!NOTE]  
> Se il cliente o il fornitore dispone di movimenti aperti, è necessario prima rimuovere la tolleranza di pagamento dai movimenti correntemente aperti.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a>Esempio 1: calcoli di tolleranza per un singolo documento

Di seguito sono descritti alcuni scenari di esempio mirati a illustrare i calcoli e le registrazioni della tolleranza prevista eseguiti in diverse situazioni.  

La pagina **Setup Registrazioni Generali** contiene il setup seguente:

- Periodo di dilazione sconto pagamento: 5G  
- Max. Tolleranza Pagamento: 5  

Gli scenari con l'alternativa A o B rappresentano quanto segue:  

- **A**: in questo caso l'avviso relativo alla tolleranza di sconto sul pagamento viene disattivato oppure l'utente ha attivato l'avviso e ha scelto di consentire lo sconto sul pagamento in ritardo (Registra il saldo come tolleranza pagamento).  
- **B**: in questo caso l'utente ha attivato l'avviso e ha scelto di non consentire lo sconto sul pagamento in ritardo (Mantieni il saldo come importo residuo).  

|-|Mag.|Sconto pagamento|Tolleranza pagamento massima|Data sconto pagamento|Data tolleranza sconto pagamento|Data Pagamento|Pagamento|Tipo Tolleranza|Tutti i Movimenti Chiusi|Tolleranza sconto pagamento CG/CL|Tolleranza pagamento C/G|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1.000|20|5|15/01/03|20/01/03|<=15/01/03|985|PaymentTolerance|Sì|0|-5|  
|2|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**<=15/01/03**|**980**|**Nessuno**|**Sì**|**0**|**0**|  
|3|1.000|20|5|15/01/03|c|<=15/01/03|975|PaymentTolerance|Sì|0|5|  
|4A|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|1005|PaymentDiscountTolerance|No, 25 in pagamento|20/-20|0|  
|5A|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|1000|PaymentDiscountTolerance|No, 20 in pagamento|20/-20|0|  
|6A|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|995|PaymentDiscountTolerance|No, 15 in pagamento|20/-20|0|  
|4B|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|1005|PaymentTolerance|Sì|0|-5|  
|**5B**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**16/01/03 – 20/01/03**|**1000**|**Nessuno**|**Sì**|**0**|**0**|  
|6B|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|995|PaymentTolerance|Sì|0|5|  
|7|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|985|PaymentDiscountTolerance e PaymentTolerance|Sì|20/-20|-5|  
|8|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|980|PaymentDiscountTolerance|Sì|20/-20|0|  
|9|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|975|PaymentDiscountTolerance e PaymentTolerance|Sì|20/-20|5|  
|10|1.000|20|5|15/01/03|20/01/03|>20/01/03|1005|PaymentTolerance|Sì|0|-5|  
|**11**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**>20/01/03**|**1000**|**Nessuno**|**Sì**|**0**|**0**|  
|12|1.000|20|5|15/01/03|20/01/03|>20/01/03|995|PaymentTolerance|Sì|0|5|  
|13|1.000|20|5|15/01/03|20/01/03|>20/01/03|985|Nessuno|No, 15 in fattura|0|0|  
|14|1.000|20|5|15/01/03|20/01/03|>20/01/03|980|Nessuno|No, 20 in fattura|0|0|  
|15|1.000|20|5|15/01/03|20/01/03|>20/01/03|975|Nessuno|No, 25 in fattura|0|0|  

### <a name="payment-range-diagrams"></a>Diagrammi dell'intervallo di pagamento

I diagrammi degli intervalli di pagamento per lo scenario sono:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Data di pagamento <=15/01/03 (scenari 1-3)

Importo residuo in base a  

regole di collegamento normali  

![Regole di tolleranza pagamenti singoli 1.](media/singlePmtTolRules_Pre1503.gif "Regole di tolleranza pagamenti singoli 1")  

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) Data di pagamento tra il 16/01/03 e il 20/01/03 (scenari 4-9)

Importo residuo in base a  

regole di collegamento normali  

![Regole di tolleranza pagamenti singoli 2.](media/singlePmtTolRules_GracePeriod.gif "Regole di tolleranza pagamenti singoli 2")  

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) Data di pagamento dopo il 20/01/03 (scenari 10-15)

Importo residuo in base a  

regole di collegamento normali  

![Regole di tolleranza pagamenti singoli 3.](media/singlePmtTolRules_Post0120.gif "Regole di tolleranza pagamenti singoli 3")  

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a>Esempio 2: calcoli di tolleranza per più documenti

Di seguito sono descritti alcuni scenari di esempio mirati a illustrare i calcoli e le registrazioni della tolleranza prevista eseguiti in diverse situazioni. Questi esempi contemplano solo gli scenari in cui tutti i movimenti del collegamento vengono chiusi.  

La pagina **Setup Registrazioni Generali** contiene il setup seguente:
- Periodo di dilazione sconto pagamento: 5D  
- Max. Tolleranza Pagamento: 5  

Gli scenari con l'alternativa A, B, C o D rappresentano quanto segue:  

- **A**: in questo caso l'avviso relativo alla tolleranza di sconto sul pagamento viene disattivato oppure l'utente ha attivato l'avviso e ha scelto di consentire lo sconto sul pagamento in ritardo (Registrare come tolleranza sconto pagamento) in tutte le fatture.  
- **B**: in questo caso l'utente ha attivato l'avviso e ha scelto di non consentire lo sconto sul pagamento in ritardo in tutte le fatture.  
- **C**: in questo caso l'utente ha attivato l'avviso e ha scelto di consentire lo sconto sul pagamento in ritardo nella prima fattura ma non nella seconda.  
- **D**: in questo caso l'utente ha attivato l'avviso e ha scelto di non consentire lo sconto sul pagamento in ritardo nella prima fattura ma di consentirlo nella seconda.  

|-|Mag.|Sconto pagamento|Tolleranza pagamento massima|Data sconto pagamento|Data tolleranza sconto pagamento|Data Pagamento|Pagamento|Tipo Tolleranza|Tutti i Movimenti Chiusi|Tolleranza sconto pagamento CG/CL|Tolleranza pagamento C/G|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1920|PaymentTolerance|Sì|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**<=15/01/03**|**1910**|**Nessuno**|**Sì**|**0**<br /><br /> **0**|0 <br />0|  
|3|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1900|PaymentTolerance|Sì|0<br /><br /> 0|5 <br />5|  
|4B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1980|PaymentTolerance|Sì|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**16/01/03 – 17/01/03**|**1970**|**Nessuno**|**Sì**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1960|PaymentTolerance|Sì|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1920|PaymentDiscountTolerance e PaymentTolerance|Sì|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1910|PaymentDiscountTolerance|Sì|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1900|PaymentDiscountTolerance e PaymentTolerance|Sì|60/60|5 <br />5|  
|10B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|2010|PaymentTolerance|Sì|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**18/01/03 – 20/01/03**|**2000**|**Nessuno**|**Sì**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1990|PaymentTolerance|Sì|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1980|PaymentDiscountTolerance e PaymentTolerance|Sì|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1970|PaymentDiscountTolerance|Sì|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1960|PaymentDiscountTolerance e PaymentTolerance|Sì|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1950|PaymentDiscountTolerance e PaymentTolerance|Sì|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1940|PaymentDiscountTolerance|Sì|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1930|PaymentDiscountTolerance e PaymentTolerance|Sì|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1920|PaymentDiscountTolerance e PaymentTolerance|Sì|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1910|PaymentDiscountTolerance|Sì|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1900|PaymentDiscountTolerance e PaymentTolerance|Sì|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|2010|PaymentTolerance|Sì|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**21/01/03 – 22/01/03**|**2000**|**Nessuno**|**Sì**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1990|PaymentTolerance|Sì|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1980|PaymentDiscountTolerance e PaymentTolerance|Sì|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1970|PaymentDiscountTolerance|Sì|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1960|PaymentDiscountTolerance e PaymentTolerance|Sì|0/0<br /><br /> 30/30|5 <br />5|  
|28|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|2010|PaymentTolerance|Sì|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**>22/01/03**|**2000**|**Nessuno**|**Sì**|**0**|**0**|  
|30|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|1990|PaymentTolerance|Sì|0|5|  

### <a name="payment-range-diagrams-1"></a>Diagrammi dell'intervallo di pagamento

I diagrammi degli intervalli di pagamento per lo scenario sono:  

#### <a name="1-payment-date-011503-scenarios-1-3-1"></a>(1) Data di pagamento <=15/01/03 (scenari 1-3)

Importo residuo in base a  

regole di collegamento normali  

:::image type="content" source="media/multiplePmtTolRules_Pre1503.gif" alt-text="Regole di tolleranza per più pagamenti 1a":::

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) Data di pagamento tra il 16/01/03 e il 17/01/03 (scenari 4-9)

Importo residuo in base a  

regole di collegamento normali  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv1-2.gif" alt-text="Regole di tolleranza per più pagamenti 2":::

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) Data di pagamento tra il 18/01/03 e il 20/01/03 (scenari 10-21)

Importo residuo in base a  

regole di collegamento normali  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv1.gif" alt-text="Regole di tolleranza per più pagamenti 3":::

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) Data di pagamento tra il 21/01/03 e il 22/01/03 (scenari 22-27)

Importo residuo in base a  

regole di collegamento normali  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv2.gif" alt-text="Regole di tolleranza per più pagamenti 4":::

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) Data di pagamento dopo il 22/01/03 (scenari 28-30)

Importo residuo in base a  

regole di collegamento normali  

:::image type="content" source="media/multiplePmtTolRules_Post0122.gif" alt-text="Regole di tolleranza per più pagamenti 5":::

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.

## <a name="see-also"></a>Vedere anche

[Dati finanziari](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
