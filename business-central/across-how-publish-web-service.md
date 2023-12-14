---
title: Esporre oggetti come servizi Web
description: Pubblicare oggetti come servizi Web per renderli immediatamente disponibili per la propria soluzione di Business Central.
author: brentholtorf
ms.topic: conceptual
ms.search.form: 810
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="publish-a-web-service"></a>Pubblicare un servizio Web

I servizi Web sono un modo semplice ed efficace per rendere le funzionalità di applicazioni disponibili a diversi tipi di sistemi e utenti esterni. Per impostazione predefinita, [!INCLUDE[prod_short](includes/prod_short.md)] espone una serie di oggetti come servizi Web per una migliore integrazione con altri servizi Microsoft. È possibile aggiungere altri servizi Web in base alle esigenze dell'azienda.  

Configurare un servizio Web in [!INCLUDE[prod_short](includes/prod_short.md)] e quindi pubblicare il servizio Web in modo che sia disponibile per gli utenti autenticati. Tutti gli utenti autorizzati possono accedere ai metadati per i servizi Web, ma solo gli utenti che dispongono di permessi sufficienti possono accedere ai dati effettivi.  

## <a name="creating-and-publishing-a-web-service"></a>Creazione e pubblicazione di un servizio Web

I seguenti passaggi illustrano come creare e pubblicare un servizio Web.  

### <a name="to-create-and-publish-a-web-service"></a>Per creare e pubblicare un servizio Web

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Servizi Web**, quindi scegli il collegamento correlato.  
2. Nella pagina **Servizi Web** selezionare **Nuovo**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** e **Pagina** sono tipi validi per servizi Web SOAP. **Pagina** e **Query** sono tipi validi per i servizi Web OData. A partire dalla versione 16.3, **Codeunit** è anche un tipo valido per i servizi Web OData v4, ma non viene visualizzato alcun URL nell'interfaccia utente. Inoltre, se il database contiene più società, è possibile scegliere un ID oggetto specifico di una delle società.  
    > Il nome del servizio è visibile agli utenti del servizio Web e poiché è la base per l'identificazione e la distinzione dei servizi Web, è importante che sia un nome significativo.

3. Selezionare la casella di controllo nella colonna **Pubblicato**.  

Quando si pubblica il servizio Web, i campi **URL OData** e **URL SOAP** mostrano i nuovi URL. Tuttavia, per le codeunit esposte come azioni non associate OData v4, i campi URL non vengono visualizzati.  

È possibile verificare il servizio web immediatamente selezionando i collegamenti nei campi **URL SOAP** e **URL OData**. In alternativa, copiare il valore del campo e salvarlo per un successivo utilizzo. Per testare le codeunit esposte come azioni non associate OData v4, seguire le istruzioni nella sezione [Verifica della disponibilità del servizio Web](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) nel contenuto per gli sviluppatori.

> [!NOTE]
> Se gli oggetti esposti come servizi Web non devono essere accessibili da [!INCLUDE[prod_short](includes/prod_short.md)] online, è necessario contrassegnare i metodi esposti nel codice come `[Scope('OnPrem')]`. Per ulteriori informazioni, vedere [Attributo dell'ambito](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

Dopo la pubblicazione di un servizio Web, questo è immediatamente disponibile per le parti esterne. È possibile verificare la disponibilità del servizio Web utilizzando un browser oppure scegliere il collegamento nei campi **URL SOAP** e **URL OData** nella pagina **Servizi Web**. La procedura seguente illustra come verificare la disponibilità del servizio Web per un uso successivo.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Per verificare la disponibilità di un servizio Web

1. Nel browser immettere l'URL pertinente. Nella seguente tabella sono illustrati i tipi di URL che è possibile immettere per tipi di servizi Web diversi.  

    > [!div class="mx-tdBreakAll"]
    > |Tipo|Sintassi|Esempio|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Per la ragione sociale viene osservata la distinzione tra maiuscole e minuscole.|

2. Esaminare le informazioni visualizzate nel browser. Verificare che sia possibile visualizzare il nome del servizio Web creato.  

Quando si accede a un servizio Web e si desidera scrivere i dati di nuovo in [!INCLUDE[prod_short](includes/prod_short.md)], è necessario specificare il nome della società. È possibile specificare la società come parte di URI come illustrato negli esempi oppure specificare la società come parte dei parametri di query. Ad esempio, gli URI successivi scelgono lo stesso servizio Web OData e sono entrambi URI validi.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Vedere anche

[Amministrazione](admin-setup-and-administration.md)  
[Servizi Web di Business Central per sviluppatori](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[Limiti richieste OData](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
