---
title: Tolleranza pagamento e tolleranza sconto pagamento | Microsoft Docs
description: È possibile impostare la tolleranza di pagamento per chiudere una fattura quando il pagamento non copre l'intero importo della fattura.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: def9338cea3a1998aafac671e304c55f83fdece7
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "932720"
---
# <a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a>Utilizzare le tolleranze pagamento e le tolleranze sconto pagamento
È possibile impostare una tolleranza di pagamento per chiudere una fattura quando il pagamento non copre l'intero importo della fattura. È possibile impostare una tolleranza sconto pagamento per consentire uno sconto sul pagamento dopo che è trascorsa la data dello sconto sul pagamento.  

È possibile utilizzare le tolleranze di pagamento in modo che ogni importo inevaso abbia una tolleranza di pagamento massima consentita. Se la tolleranza di pagamento viene soddisfatta, l'importo pagamento viene quindi analizzato. Se l'importo del pagamento rappresenta un sottopagamento, l'importo inevaso viene chiuso completamente dal sottopagamento. Viene registrato un movimento contabile dettagliato nel movimento del pagamento in modo che non esista un importo residuo nel movimento di fattura collegato. Se l'importo del pagamento rappresenta un sovrapagamento, viene registrato un nuovo movimento contabile dettagliato nel movimento del pagamento in modo che non esista un importo residuo nel movimento di pagamento.

È possibile utilizzare le tolleranze sconto pagamento in modo che, se si accetta uno sconto sul pagamento dopo la relativa data di scadenza, tale evento verrà registrato nel conto degli sconti sul pagamento oppure nel conto delle tolleranze di pagamento.

## <a name="applying-payment-tolerance-to-multiple-documents"></a>Collegamento della tolleranza di pagamento a più documenti  
Un documento singolo ha la stessa tolleranza di pagamento indipendentemente dal fatto che sia applicato in modo autonomo o collegato con altri documenti. L'accettazione di uno sconto di pagamento ritardato quando si collega la tolleranza di pagamento a più documenti si verifica automaticamente per ogni documento in cui la seguente regola è vera:  

*data sconto sul pagamento < data di pagamento (nel movimento in questione) <= data tolleranza di pagamento*  

Questa regola si applica anche per stabilire se visualizzare avvisi quando si collega la tolleranza di pagamento a più documenti. L'avviso di tolleranza sconto pagamento viene visualizzato per ogni movimento che soddisfa i criteri di data. Per ulteriori informazioni, vedere [Esempio 2: calcoli di tolleranza per più documenti](finance-payment-tolerance-and-payment-discount-tolerance.md#example-2---tolerance-calculations-for-multiple-documents).

È possibile scegliere di visualizzare un avviso che è basato su situazioni di tolleranza differenti.  

- Il primo avviso riguarda la tolleranza di sconto sul pagamento. L'utente viene informato che è possibile accettare uno sconto di pagamento ritardato. Egli può quindi scegliere se accettare la tolleranza alla data dello sconto.  
- Il secondo avviso riguarda la tolleranza di pagamento. L'utente viene informato che tutti i movimenti possono venir chiusi a causa della differenza nella somma della tolleranza di pagamento massima per i movimenti collegati. Egli può quindi scegliere se accettare la tolleranza nell'importo di pagamento.

Per ulteriori informazioni, vedere [Abilitare o disabilitare gli avvisi di tolleranza pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).     

## <a name="to-set-up-tolerances"></a>Per impostare le tolleranze  
Le tolleranze relative a giorni e importi consentono di chiudere una fattura anche se il pagamento non copre l'intero importo riportato in fattura per svariati motivi. È ad esempio possibile che la data di scadenza per lo sconto sul pagamento sia stata superata, che siano state dedotte determinate merci oppure a causa di un semplice errore. Lo stesso principio è valido anche per note di credito e rimborsi.  

Per impostare le tolleranze è necessario impostare vari conti di tolleranza, specificare entrambi i metodi di registrazione della tolleranza di sconto sul pagamento e della tolleranza di pagamento, quindi eseguire il processo batch **Modifica tolleranza pagamento**.  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup registrazioni COGE** e quindi scegliere il collegamento correlato.  
2. Aprire la pagina **Setup registrazioni COGE**, impostare un conto di tolleranza a debito e a credito dei pagamenti relativi alle vendite e un conto di tolleranza a debito e a credito dei pagamenti relativi agli acquisti.  
3. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Categorie registrazione clienti** e quindi scegliere il collegamento correlato.    
4. Aprire la pagina **Cat. reg. clienti**, impostare un conto di tolleranza a debito e a credito dei pagamenti. Per ulteriori informazioni, vedere [Impostazione delle categorie di registrazione](finance-posting-groups.md).  
5. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup registrazioni fornitori** e quindi scegliere il collegamento correlato.  
6. Aprire la pagina **Cat. reg. fornitori**, impostare un conto di tolleranza a debito e a credito dei pagamenti.  
7. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità generale** e quindi scegliere il collegamento correlato.  
8. Aprire la pagina **Setup contabilità generale**.  
9. Nella Scheda dettaglio **Collegamento** compilare i campi **Registrazione toll. sconto pag.**, **Periodo di dilazione sconto pagamento** e **Registrazione toll. pagamento**.   
10. Scegliere l'azione **Modifica tolleranza pagamento**.
11. Nella pagina **Modifica tolleranza pagamento** compilare i campi **% tolleranza pagamento** e **Importo massimo tolleranza pagamento** e quindi scegliere **OK**.

> [!IMPORTANT]  
>  Con questa procedura la tolleranza viene impostata solo per la valuta locale. Se si desidera che [!INCLUDE[d365fin](includes/d365fin_md.md)] gestisce le tolleranze sui pagamenti, le note di credito e i rimborsi in una valuta estera, è necessario eseguire il processo batch **Modifica tolleranza pagamento** con un valore nel campo **Codice valuta**.  

> [!NOTE]  
>  Se si desidera che venga visualizzato un messaggio di avviso tolleranza pagamento ogni volta che si registra un'applicazione della tolleranza, è necessario attivare l'Avviso tolleranza pagamento. Per ulteriori informazioni, vedere la sezione [Per abilitare o disabilitare gli avvisi di tolleranza pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).  
>   
>  Per disattivare la tolleranza per un cliente o un fornitore, è necessario bloccare le tolleranze nella relativa scheda cliente o scheda fornitore. Per ulteriori informazioni, vedere la sezione [Per bloccare la tolleranza pagamento per i clienti](finance-payment-tolerance-and-payment-discount-tolerance.md#to-block-payment-tolerance-for-customers).  
>   
>  Quando si imposta la tolleranza, [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica automaticamente l'esistenza di movimenti aperti e calcola la tolleranza anche per tali movimenti.

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a>Per abilitare o disabilitare gli avvisi di tolleranza pagamento
L'avviso tolleranza pagamento viene visualizzato quando si registra un collegamento con un saldo che rientra nella tolleranza consentita. Sarà quindi possibile decidere come registrare e documentare il saldo.    
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità generale** e quindi scegliere il collegamento correlato.  
2. Nella Scheda dettaglio **Collegamento** della pagina **Setup contabilità generale** selezionare la casella di controllo **Avviso tolleranza pagamento** per attivare l'avviso. Per disattivare l'avviso, deselezionare la casella di controllo.  

> [!NOTE]  
>  L'opzione predefinita per la pagina **Avviso tolleranza pag.** è **Mantieni il saldo come importo residuo**. L'opzione predefinita per la pagina **Avviso toll. sconto pag.** è **Non accettare lo sconto di pagamento ritardato**.

## <a name="to-block-payment-tolerance-for-customers"></a>Per bloccare la tolleranza pagamento per i clienti  
Per impostazione di default, la tolleranza di pagamento è consentita. Per disattivare la tolleranza di pagamento per un cliente o un fornitore, è necessario bloccare la tolleranza nella relativa scheda cliente o scheda fornitore. Di seguito viene descritto come eseguire l'operazione per un cliente. I passaggi sono simili per un fornitore.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cliente** o **Fornitore**e quindi scegliere il collegamento correlato.  
2. Nella Scheda dettaglio **Pagamenti** selezionare la casella di controllo **Blocca tolleranza pagam**.  

> [!NOTE]  
>  Se il cliente o il fornitore dispone di movimenti aperti, è necessario prima rimuovere la tolleranza di pagamento dai movimenti correntemente aperti.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a>Esempio 1: calcoli di tolleranza per un singolo documento
Di seguito sono descritti alcuni scenari di esempio mirati a illustrare i calcoli e le registrazioni della tolleranza prevista eseguiti in diverse situazioni.  

La pagina **Setup Registrazioni Generali** contiene il setup seguente:
- Periodo di dilazione sconto pagamento: 5G  
- Max. Tolleranza Pagamento: 5  

Gli scenari con l'alternativa A o B rappresentano quanto segue:  

- **A**: in questo caso l'avviso relativo alla tolleranza di sconto sul pagamento è stato disattivato OPPURE l'utente ha attivato l'avviso e ha scelto di consentire lo sconto sul pagamento in ritardo (Registra il saldo come tolleranza pagamento).  
- **B**: in questo caso l'utente ha attivato l'avviso e ha scelto di non consentire lo sconto sul pagamento in ritardo (Mantieni il saldo come importo residuo).  

|-|Mag.|Pagam.|Max Toll. Pag.|Data Sconto Pag.|Data Toll. Data|Data Pagamento|Pag.|Tipo Tolleranza|Tutti i Movimenti Chiusi|Data Toll. Mov. Cli.|Toll. Pag. C/G|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1.000|20|5|15/01/03|20/01/03|<=15/01/03|985|Toll. Pag.|Sì|0|-5|  
|2|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**<=15/01/03**|**980**|**Nessuno**|**Sì**|**0**|**0**|  
|3|1.000|20|5|15/01/03|c|<=15/01/03|975|Toll. Pag.|Sì|0|5|  
|4A|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|1005|Toll. Sconto Pag.|No, 25 in Pag.|20/-20|0|  
|5A|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|1000|Toll. Sconto Pag.|No, 20 in Pag.|20/-20|0|  
|6A|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|995|Toll. Sconto Pag.|No, 15 in Pag.|20/-20|0|  
|4B|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|1005|Toll. Pag.|Sì|0|-5|  
|**5B**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**16/01/03 – 20/01/03**|**1000**|**Nessuno**|**Sì**|**0**|**0**|  
|6B|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|995|Toll. Pag.|Sì|0|5|  
|7|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|985|Toll. Sconto Pag. Toll. Pag.|Sì|20/-20|-5|  
|8|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|980|Toll. Sconto Pag.|Sì|20/-20|0|  
|9|1.000|20|5|15/01/03|20/01/03|16/01/03 – 20/01/03|975|Toll. Sconto Pag. Toll. Pag.|Sì|20/-20|5|  
|10|1.000|20|5|15/01/03|20/01/03|>20/01/03|1005|Toll. Pag.|Sì|0|-5|  
|**11**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**>20/01/03**|**1000**|**Nessuno**|**Sì**|**0**|**0**|  
|12|1.000|20|5|15/01/03|20/01/03|>20/01/03|995|Toll. Pag.|Sì|0|5|  
|13|1.000|20|5|15/01/03|20/01/03|>20/01/03|985|Nessuno|No, 15 in fattura|0|0|  
|14|1.000|20|5|15/01/03|20/01/03|>20/01/03|980|Nessuno|No, 20 in fattura|0|0|  
|15|1.000|20|5|15/01/03|20/01/03|>20/01/03|975|Nessuno|No, 25 in fattura|0|0|  

### <a name="payment-range-diagrams"></a>Diagrammi dell'intervallo di pagamento  
I diagrammi degli intervalli di pagamento per lo scenario sopra illustrato sono:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Data di pagamento <=15/01/03 (scenari 1-3)  
Importo residuo in base a  

regole di collegamento normali  

![Regole di tolleranza pagamenti singoli 1](media/singlePmtTolRules(Pre1503).gif "Regole di tolleranza pagamenti singoli 1")  

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) Data di pagamento tra il 16/01/03 e il 20/01/03 (scenari 4-9)  
Importo residuo in base a  

regole di collegamento normali  

![Regole di tolleranza pagamenti singoli 2](media/singlePmtTolRules(GracePeriod).gif "Regole di tolleranza pagamenti singoli 2")  

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) Data di pagamento dopo il 20/01/03 (scenari 10-15)  
Importo residuo in base a  

regole di collegamento normali  

![Regole di tolleranza pagamenti singoli 3](media/singlePmtTolRules(Post0120).gif "Regole di tolleranza pagamenti singoli 3")  

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a>Esempio 2: calcoli di tolleranza per più documenti
Di seguito sono descritti alcuni scenari di esempio mirati a illustrare i calcoli e le registrazioni della tolleranza prevista eseguiti in diverse situazioni. Questi esempi contemplano solo gli scenari in cui tutti i movimenti del collegamento vengono chiusi.  

La pagina **Setup Registrazioni Generali** contiene il setup seguente:
- Periodo di dilazione sconto pagamento: 5D  
- Max. Tolleranza Pagamento: 5  

Gli scenari con l'alternativa A, B, C o D rappresentano quanto segue:  

- **A**: in questo caso l'avviso relativo alla tolleranza di sconto sul pagamento è stato disattivato OPPURE l'utente ha attivato l'avviso e ha scelto di consentire lo sconto sul pagamento in ritardo (Registrare come tolleranza sconto pagamento) in tutte le fatture.  
- **B**: in questo caso l'utente ha attivato l'avviso e ha scelto di non consentire lo sconto sul pagamento in ritardo in tutte le fatture.  
- **C**: in questo caso l'utente ha attivato l'avviso e ha scelto di consentire lo sconto sul pagamento in ritardo nella prima fattura ma non nella seconda.  
- **D**: in questo caso l'utente ha attivato l'avviso e ha scelto di non consentire lo sconto sul pagamento in ritardo nella prima fattura ma di consentirlo nella seconda.  

|-|Mag.|Sconto Pag.|Max Toll. Pag.|Data Sconto Pag.|Data Toll. Data|Data Pagamento|Pag.|Tipo Tolleranza|Tutti i Movimenti Chiusi|Data Toll. Mov. Cli.|Toll. Pag. C/G|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1920|Toll. Pag.|Sì|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**<=15/01/03**|**1910**|**Nessuno**|**Sì**|**0**<br /><br /> **0**|0 <br />0|  
|3|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1900|Toll. Pag.|Sì|0<br /><br /> 0|5 <br />5|  
|4B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1980|Toll. Pag.|Sì|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**16/01/03 – 17/01/03**|**1970**|**Nessuno**|**Sì**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1960|Toll. Pag.|Sì|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1920|Toll. Sconto Pag. Toll. Pag.|Sì|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1910|Toll. Sconto Pag.|Sì|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1900|Toll. Sconto Pag. Toll. Pag.|Sì|60/60|5 <br />5|  
|10B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|2010|Toll. Pag.|Sì|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**18/01/03 – 20/01/03**|**2000**|**Nessuno**|**Sì**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1990|Toll. Pag.|Sì|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1980|Toll. Sconto Pag. Toll. Pag.|Sì|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1970|Toll. Sconto Pag.|Sì|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1960|Toll. Sconto Pag. Toll. Pag.|Sì|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1950|Toll. Sconto Pag. Toll. Pag.|Sì|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1940|Toll. Sconto Pag.|Sì|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1930|Toll. Sconto Pag. Toll. Pag.|Sì|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1920|Toll. Sconto Pag. Toll. Pag.|Sì|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1910|Toll. Sconto Pag.|Sì|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1900|Toll. Sconto Pag. Toll. Pag.|Sì|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|2010|Toll. Pag.|Sì|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**21/01/03 – 22/01/03**|**2000**|**Nessuno**|**Sì**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1990|Toll. Pag.|Sì|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1980|Toll. Sconto Pag. Toll. Pag.|Sì|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1970|Toll. Sconto Pag.|Sì|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1960|Toll. Sconto Pag. Toll. Pag.|Sì|0/0<br /><br /> 30/30|5 <br />5|  
|28|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|2010|Toll. Pag.|Sì|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**>22/01/03**|**2000**|**Nessuno**|**Sì**|**0**|**0**|  
|30|1.000 <br />1.000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|1990|Toll. Pag.|Sì|0|5|  

### <a name="payment-range-diagrams"></a>Diagrammi dell'intervallo di pagamento  
I diagrammi degli intervalli di pagamento per lo scenario sopra illustrato sono:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Data di pagamento <=15/01/03 (scenari 1-3)  
Importo residuo in base a  

regole di collegamento normali  

![Regole di tolleranza per più pagamenti 1](media/multiplePmtTolRules(Pre1503).gif "Regole di tolleranza per più pagamenti 1")  

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) Data di pagamento tra il 16/01/03 e il 17/01/03 (scenari 4-9)  
Importo residuo in base a  

regole di collegamento normali  

![Regole di tolleranza per più pagamenti 2](media/multiplePmtTolRules(GracePeriodInv1).gif "Regole di tolleranza per più pagamenti 2")  

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) Data di pagamento tra il 18/01/03 e il 20/01/03 (scenari 10-21)  
Importo residuo in base a  

regole di collegamento normali  

![Regole di tolleranza per più pagamenti 3](media/multiplePmtTolRules(GracePeriodInv1-2).gif "Regole di tolleranza per più pagamenti 3")  

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) Data di pagamento tra il 21/01/03 e il 22/01/03 (scenari 22-27)  
Importo residuo in base a  

regole di collegamento normali  

![Regole di tolleranza per più pagamenti 4](media/multiplePmtTolRules(GracePeriodInv2).gif "Regole di tolleranza per più pagamenti 4")  

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) Data di pagamento dopo il 22/01/03 (scenari 28-30)  
Importo residuo in base a  

regole di collegamento normali  

![Regole di tolleranza per più pagamenti 5](media/multiplePmtTolRules(Post0122).gif "Regole di tolleranza per più pagamenti 5")  

(1) Se il pagamento ricade in questi intervalli, tutti i movimenti di collegamento possono essere chiusi con o senza tolleranza.  

(2) Se il pagamento ricade in questi intervalli, i movimenti di collegamento non possono essere chiusi, nemmeno con tolleranza.

## <a name="see-also"></a>Vedi anche  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
