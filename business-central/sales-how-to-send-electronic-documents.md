---
title: Inviare documenti elettronici
description: Scopri come utilizzare Business Central per inviare fatture elettroniche e note di credito in formato PEPPOL.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# Inviare documenti elettronici

La versione generica di [!INCLUDE[prod_short](includes/prod_short.md)] supporta l'invio delle fatture e delle note di credito elettroniche nel formato PEPPOL, supportato dai principali provider di servizi di scambio documenti. Un provider di servizi di Exchange per documenti invia i documenti elettronici tra i partner commerciali. Per fornire supporto per altri formati di documenti elettronici, è possibile utilizzare il framework di scambio dati.  

 Nella versione generica di [!INCLUDE[prod_short](includes/prod_short.md)], un servizio di scambio documenti è preconfigurato e pronto per l'installazione nell'azienda. Per ulteriori informazioni, vedere [Impostare un servizio di scambio documenti](across-how-to-set-up-a-document-exchange-service.md). Tuttavia, in alcuni casi, è necessario installare un'app. Per ulteriori informazioni, vedere [Domande frequenti sulla fatturazione elettronica](faq-electronic-invoicing.yml).  

 Per inviare una fattura di vendita come documento elettronico PEPPOL, selezionare l'opzione **Documento elettronico** nella finestra di dialogo **Registra e invia**. Nella finestra di dialogo è inoltre possibile impostare il profilo di invio documenti predefinito del cliente. Innanzitutto, è necessario impostare diversi dati principali, ad esempio le informazioni sulla società, i clienti, gli articoli e le unità di misura. Questi dati vengono utilizzati per identificare i partner commerciali e gli articoli durante la conversione dei dati nei campi in [Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### Per inviare una fattura di vendita elettronica

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture vendite**, quindi seleziona il collegamento correlato.  

2. Creare una nuova fattura di vendita.  

3. Una volta che la fattura di vendita è pronta per essere fatturata, scegliere l'azione **Registra e invia**.  

     Se il profilo di invio predefinito del cliente è **Documento elettronico**, verrà visualizzato nella finestra di dialogo **Conferma registrazione e invio**. In questo modo, è necessario soltanto scegliere il pulsante **Sì** per registrare e inviare la fattura in formato elettronico nel formato selezionato.  

4. Nella finestra di dialogo **Conferma registrazione e invio** scegliere il pulsante AssistEdit a destra del campo **Invia documento a**.  

5. Nella finestra di dialogo **Invia documento a**, nel campo **Documento elettronico**, scegliere **Tramite il servizio di Exchange per documenti**.  

6. Nel campo **Formato** scegliere **PEPPOL**.  

7. Scegliere il pulsante **OK**. Viene visualizzata la finestra di dialogo **Conferma registrazione e invio**. Nel campo **Invia documento a** viene aggiunto **Documento elettronico (PEPPOL)**.  

8. Scegliere il pulsante **Sì**.  

     La fattura di vendita viene registrata e inviata al cliente in formato PEPPOL.  

    > [!NOTE]  
    >  È inoltre possibile inviare una fattura di vendita registrata come documento elettronico. La procedura è uguale a quella descritta in questo argomento per i documenti di vendita non registrati. Nella pagina **Fatt. di vend. reg.** scegliere l'azione **Log attività** per visualizzare lo stato del documento elettronico.  

## Vedi anche

[Fatturazione delle vendite](sales-how-invoice-sales.md)  
[Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md)  
[Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Impostare un servizio di scambio documenti](across-how-to-set-up-a-document-exchange-service.md)  
[Impostare le definizioni di scambio dati](across-how-to-set-up-data-exchange-definitions.md)  
[Scambio di dati in modalità elettronica](across-data-exchange.md)  
[Domande frequenti sulla fatturazione elettronica](faq-electronic-invoicing.yml)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
