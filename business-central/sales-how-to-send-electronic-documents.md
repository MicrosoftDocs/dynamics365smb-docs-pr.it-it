---
title: Inviare documenti elettronici | Documenti Microsoft
description: Informazioni su come inviare le fatture elettronicamente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 110c81bdf6de02e16a1e1185028f6b803290f3d7
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192663"
---
# <a name="send-electronic-documents"></a>Inviare documenti elettronici
La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta l'invio delle fatture e delle note di credito elettroniche nel formato PEPPOL, che è supportato dai principali provider di servizi di scambio documenti. Un provider di servizi di Exchange per documenti invia i documenti elettronici tra i partner commerciali. Per fornire supporto per altri formati di documenti elettronici, è possibile utilizzare il framework di scambio dati.  

 Nella versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)], un servizio di scambio documenti è preconfigurato e pronto per l'installazione nell'azienda. Per ulteriori informazioni, vedere [Impostare un servizio di scambio documenti](across-how-to-set-up-a-document-exchange-service.md).  

 Per inviare una fattura di vendita come documento elettronico PEPPOL, selezionare l'opzione **Documento elettronico** nella finestra di dialogo **Registra e invia** in cui è anche possibile impostare il profilo di invio documenti predefinito del cliente. Innanzitutto, è necessario impostare diversi dati principali, ad esempio le informazioni sulla società, i clienti, gli articoli e le unità di misura. Questi dati vengono utilizzati per identificare i partner commerciali e gli articoli durante la conversione dei dati nei campi in [Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a>Per inviare una fattura di vendita elettronica  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture vendite** e quindi scegliere il collegamento correlato.  

2.  Creare una nuova fattura di vendita.  

3.  Una volta che la fattura di vendita è pronta per essere fatturata, scegliere l'azione **Registra e invia**.  

     Se il profilo di invio predefinito del cliente è **Documento elettronico**, sarà mostrato nella finestra di dialogo **Conferma registrazione e invio** e basterà scegliere il pulsante **Sì** per registrare e inviare elettronicamente la fattura nel formato selezionato.  

4.  Nella finestra di dialogo **Conferma registrazione e invio** scegliere il pulsante AssistEdit a destra del campo **Invia documento a**.  

5.  Nella finestra di dialogo **Invia documento a**, nel campo **Documento elettronico**, scegliere **Tramite il servizio di Exchange per documenti**.  

6.  Nel campo **Formato** scegliere **PEPPOL**.  

7.  Scegliere il pulsante **OK**. Viene visualizzata la finestra di dialogo **Conferma registrazione e invio**. Nel campo **Invia documento a** viene aggiunto **Documento elettronico (PEPPOL)**.  

8.  Scegliere il pulsante **Sì**.  

     La fattura di vendita viene registrata e inviata al cliente come documento elettronico in formato PEPPOL.  

    > [!NOTE]  
    >  È inoltre possibile inviare una fattura di vendita registrata come documento elettronico. La procedura è uguale a quella descritta in questo argomento per i documenti di vendita non registrati. Nella pagina **Fatt. di vend. reg.** scegliere l'azione **Log attività** per visualizzare lo stato del documento elettronico. Per ulteriori informazioni, vedere **Log attività**.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche  
[Fatturare le vendite](sales-how-invoice-sales.md)  
[Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md)  
[Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Impostare un servizio di scambio documenti](across-how-to-set-up-a-document-exchange-service.md)  
[Impostare le definizioni di scambio dati](across-how-to-set-up-data-exchange-definitions.md)  
[Scambio di dati in modalità elettronica](across-data-exchange.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
