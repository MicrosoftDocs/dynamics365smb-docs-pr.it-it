---
title: Esporre oggetti come servizi Web | Microsoft Docs
description: Pubblicare oggetti come servizi Web per renderli immediatamente disponibili per la propria soluzione di Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 952f2b9dc301b6941d13b4c23ac55f83b781739f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "922433"
---
# <a name="publish-a-web-service"></a>Pubblicare un servizio Web

I servizi Web sono un modo semplice ed efficace per rendere le funzionalità di applicazioni disponibili a vari sistemi e utenti esterni. [!INCLUDE[d365fin](includes/d365fin_md.md)] include vari oggetti che, per impostazione predefinita, vengono esposti come servizi Web in seguito all'integrazione in altri servizi Microsoft, ma è anche possibile aggiungere altri servizi Web.  

È possibile impostare un servizio Web nel client Windows o nel client Web. È necessario pubblicare il servizio Web per renderlo disponibile alle richieste di assistenza nella rete. Gli utenti possono individuare i servizi Web puntando un browser al percorso del server e richiedendo un elenco dei servizi disponibili. Quando si pubblica un servizio Web, diviene immediatamente disponibile in rete per gli utenti autenticati. Tutti gli utenti autorizzati possono accedere ai metadati per i servizi Web, ma solo gli utenti che dispongono di permessi sufficienti possono accedere ai dati effettivi.

## <a name="creating-and-publishing-a-web-service"></a>Creazione e pubblicazione di un servizio Web  
I seguenti passaggi illustrano come creare e pubblicare un servizio Web.  

### <a name="to-create-and-publish-a-web-service"></a>Per creare e pubblicare un servizio Web  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Servizi Web** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Servizi Web** selezionare **Nuovo**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** e **Pagina** sono tipi validi per servizi Web SOAP. **Pagina** e **Query** sono tipi validi per i servizi Web OData.  
    > Inoltre, se il database contiene più società, è possibile scegliere un ID oggetto specifico di una delle società.  
    > Il nome del servizio è visibile agli utenti del servizio Web e poiché è la base per l'identificazione e la distinzione dei servizi Web, è importante che sia un nome significativo.

3. Selezionare la casella di controllo nella colonna **Pubblicato**.  

Quando si pubblica il servizio Web, nei campi **URL OData** e **URL SOAP** è possibile vedere gli URL che sono generati per il servizio Web. È possibile verificare il servizio web immediatamente selezionando i collegamenti nei campi **URL SOAP** e **URL OData**. In alternativa, è possibile copiare il valore del campo e salvarlo per un successivo utilizzo.  

> [!IMPORTANT]
> Per le codeunit pubblicate come servizio Web SOAP, i metodi esposti nella codeunit devono essere contrassegnati come `[External]` nel codice.

Dopo la pubblicazione di un servizio Web, questo è immediatamente disponibile per le parti esterne. È possibile verificare la disponibilità del servizio Web utilizzando un browser, oppure è possibile scegliere il collegamento nei campi **URL SOAP** e **URL OData** nella pagina **Servizi Web**. La procedura seguente illustra come verificare la disponibilità del servizio Web per un uso successivo.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Per verificare la disponibilità di un servizio Web  

1. Nel browser immettere l'URL pertinente. Nella seguente tabella sono illustrati i tipi di URL che è possibile immettere per tipi di servizi Web diversi.  

    > [!div class="mx-tdBreakAll"]
    > |Tipo|Sintassi|Esempio|
    > |----------------|------|-------|
    > |SOAP |https://api.businesscentral.dynamics.com/*version*/*tenant*/WS/*CompanyName*/*entity*/ |`https://api.businesscentral.dynamics.com/v1.0/a10b3ee6-d9a2-42fe-926f-946e23bb8ddd/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|https://api.businesscentral.dynamics.com/*version*/*tenant*/ODataV4/Company('*CompanyName*')/*entity*|`https://api.businesscentral.dynamics.com/v1.0/a10b3ee6-d9a2-42fe-926f-946e23bb8ddd/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Per la ragione sociale viene osservata la distinzione tra maiuscole e minuscole.|

2. Esaminare le informazioni visualizzate nel browser. Verificare che sia possibile visualizzare il nome del servizio Web creato.  

Quando si accede a un servizio Web e si desidera scrivere i dati di nuovo in [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario specificare il nome della società. È possibile specificare la società come parte di URI come illustrato negli esempi, oppure è possibile specificare la società come parte dei parametri di query. Ad esempio, gli URI successivi scelgono lo stesso servizio Web OData e sono entrambi URI validi.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Vedere anche

[Amministrazione](admin-setup-and-administration.md)  
[Servizi Web di Business Central per sviluppatori](/dynamics365/business-central/dev-itpro/webservices/web-services)  
