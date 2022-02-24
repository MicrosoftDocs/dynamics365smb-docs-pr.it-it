---
title: Ricevere e convertire documenti elettronici | Documenti Microsoft
description: È possibile ricevere documenti elettronici direttamente da partner commerciali o da un servizio OCR.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 8571e0cbaa7104d6db8fc29ca11530a2c42464de
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953493"
---
# <a name="receive-and-convert-electronic-documents"></a>Ricevere e convertire documenti elettronici
La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta la ricezione delle fatture e delle note di credito elettroniche e la ricezione delle fatture elettroniche nel formato PEPPOL, che è supportato dai principali provider di servizi di scambio documenti. Per ricevere una fattura da un fornitore come documento PEPPOL elettronico, occorre elaborare il documento nella pagina Documenti in entrata per convertirlo in una fattura di acquisto o una riga registrazioni COGE in [!INCLUDE[d365fin](includes/d365fin_md.md)].

 Oltre a ricevere i documenti elettronici direttamente dai partner commerciali, è possibile ricevere i documenti elettronici da un servizio OCR che ha convertito i file di immagine o PDF in documenti elettronici.  

 Prima di ricevere i documenti elettronici tramite il servizio di scambio documenti, è necessario impostare i vari dati master, ad esempio informazioni sulla società, fornitori, articoli e unità di misura. Questi dati vengono utilizzati per identificare i partner commerciali e gli articoli durante la conversione dei dati presenti negli elementi del file di documento in entrata nei campi di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Impostare un servizio di scambio documenti](across-how-to-set-up-a-document-exchange-service.md).  

 Prima di ricevere i documenti elettronici tramite il servizio OCR, è necessario impostare e abilitare la connessione del servizio preconfigurata. Per ulteriori informazioni, vedere [Impostare documenti in entrata](across-how-setup-income-documents.md).  

 Il traffico dei documenti elettronici in entrata e in uscita da [!INCLUDE[d365fin](includes/d365fin_md.md)] viene gestito dalla funzionalità coda processi. Prima di ricevere i documenti elettronici, la coda processi in questione deve essere avviata.  

 È possibile avviare la conversione dei documenti elettronici manualmente, come descritto nella procedura, oppure consentire a un flusso di lavoro di convertire i documenti elettronici automaticamente quando vengono ricevuti. La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] include un modello di workflow, *Da documento elettronico in entrata tramite OCR per aprire il flusso di lavoro della fattura di acquisto*, pronto per essere copiato in un workflow ed essere abilitato. Per ulteriori informazioni, vedere [Workflow](across-workflow.md).  

> [!NOTE]  
>  Quando si convertono i documenti elettronici ricevuti dal servizio OCR in documenti o righe di registrazione in [!INCLUDE[d365fin](includes/d365fin_md.md)], più righe del documento di origine vengono sommate in una riga. La singola riga sarà di tipo Conto C/G e i campi **Descrizione** e **Nr.** (conto C/G) saranno vuoti. Il valore nel campo **Importo** sarà pari all'importo totale IVA esclusa di tutte le righe del documento di origine.  
>   
>  Per assicurarsi che i campi **Descrizione** e **Nr.** vengano compilati, è possibile scegliere il pulsante **Mappa testo a conto** nella pagina **Documenti in entrata** per definire che un determinato testo della fattura venga sempre mappato a un determinato conto dare o avere nella contabilità generale. Il campo **Descrizione** nelle righe del documento o di registrazione create da un documento elettronico per quel fornitore o cliente verrà compilato con il testo in questione e il campo **Nr.** (conto C/G) con il conto in questione.  
>   
>  Anziché il mapping a conto C/G, è possibile eseguire il mapping anche a un conto corrente bancario. Ciò risulta utile, ad esempio, per i documenti elettronici relativi alle spese che sono già state pagate in cui si desidera creare una riga registrazione COGE pronta per essere registrata in un conto corrente bancario.  

 Nella procedura riportata di seguito viene descritto come ricevere una fattura del fornitore e convertirla in una fattura di acquisto in [!INCLUDE[d365fin](includes/d365fin_md.md)]. La procedura è la stessa quando si converte una fattura del fornitore in una riga registrazioni COGE.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>Per ricevere e convertire una fattura elettronica in fattura di acquisto  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Documenti in entrata** e quindi scegliere il collegamento correlato.  

2.  Selezionare la riga per il record del documento in arrivo che rappresenta una nuova fattura elettronica in entrata, quindi scegliere l'azione **Modifica**.  

     Nella pagina **Scheda documenti in arrivo** viene allegato il file XML correlato e la maggior parte dei campi viene precompilata con le informazioni della fattura elettronica. Per ulteriori informazioni, vedere [Creare i record di documenti in entrata](across-how-create-income-document-records.md).  

3.  Nel campo **Tipo scambio dati** scegliere **PEPPOL - Fattura** oppure **OCR - Fattura**, a seconda dell'origine del documento elettronico.  

4.  Per mappare il testo della fattura del fornitore in un conto di addebito specifico, nella scheda **Azioni**, nel gruppo **Generale**, selezionare **Mappa testo a conto** e inserire i dati nella pagina **Foglio di lavoro Mappatura testo a conto**.  

5.  Selezionare l'azione **Crea documento**.  

     Verrà creata una fattura di acquisto in [!INCLUDE[d365fin](includes/d365fin_md.md)] basata sulle informazioni contenute nel documento elettronico.  

     Tutti gli errori di convalida, in genere correlati a dati mancanti o errati in [!INCLUDE[d365fin](includes/d365fin_md.md)], verranno visualizzati nella Scheda dettaglio **Messaggi di errore**.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Documenti in entrata](across-income-documents.md)  
[Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Scambio di dati in modalità elettronica](across-data-exchange.md)   
[Funzionalità aziendali generali](ui-across-business-areas.md)  
