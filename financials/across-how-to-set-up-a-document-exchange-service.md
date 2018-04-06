---
title: Come impostare un servizio di scambio documenti | Microsoft Docs
description: Utilizzare un provider di servizi esterno per scambiare documenti elettronici con i partner commerciali.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ac95d7b05eefdb71e9a7da9025c83e50466ad13a
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-a-document-exchange-service"></a>Impostare un servizio di scambio documenti
Utilizzare un provider di servizi esterno per scambiare documenti elettronici con i partner commerciali. Per ulteriori informazioni, vedere [Scambio di dati in modalità elettronica](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Per impostare un servizio di Exchange per documenti  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup servizio scamb. doc.**, quindi scegliere il collegamento correlato.  
2. Compilare i campi come indicato nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Agente utente**|Immettere un testo che può essere utilizzato per identificare la società nei processi di scambio documenti.|  
    |**ID tenant scamb. doc.**|Immettere il tenant nel servizio di Exchange per documenti che rappresenta la società. Questa chiave viene fornita dal provider di servizi di scambio documenti.|  
    |**Abilitato**|Specificare se il servizio è abilitato. **Nota:** Non appena si abilita il servizio, vengono creati almeno due movimenti della coda processi per elaborare il traffico dei documenti elettronici in entrata e in uscita di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Quando si disabilita il servizio, i movimenti della coda processi vengono eliminati.|  
    |**URL iscrizione**|Specificare la pagina Web a cui viene effettuata l'iscrizione per il servizio di Exchange per documenti.|  
    |**URL servizio**|Specificare l'indirizzo del servizio di Exchange per documenti che verrà chiamato quando si inviano e ricevono documenti elettronici.|  
    |**URL accesso**|Specificare la pagina di accesso del servizio di Exchange per documenti, cioè il punto in cui si immettono il nome utente della società e la password per accedere al servizio.|  
    |**Chiave cliente**|Immettere la chiave OAuth basata su transazioni a tre per la chiave del cliente. Questa chiave viene fornita dal provider di servizi di scambio documenti.|  
    |**Domanda segreta cliente**|Immettere il segreto che protegge la chiave del cliente. Questa chiave viene fornita dal provider di servizi di scambio documenti.|  
    |**Token**|Immettere la chiave OAuth basata su transazioni a tre per il token. Questa chiave viene fornita dal provider di servizi di scambio documenti.|  
    |**Domanda segreta token**|Immettere il segreto che protegge il token. Questa chiave viene fornita dal provider di servizi di scambio documenti.|  

> [!NOTE]  
>  Si consiglia di proteggere le informazioni di accesso immesse nella finestra **Setup servizio VAN**. È possibile crittografare dati nel server generando nuove chiavi di crittografia o importando quelle esistenti che vengono abilitate nell'istanza del server che collega al database. Questa funzionalità è descritta nella procedura seguente.  

## <a name="to-encrypt-your-logon-information"></a>Per crittografare le informazioni di accesso  
1. Nella finestra **Setup servizio VAN** scegliere l'azione **Gestione crittografia**.  
2. Nella finestra **Gestione crittografia dati** abilitare la crittografia dei dati. <!--For more information, see [Manage Data Encryption](../manage-data-encryption.md).-->  

## <a name="see-also"></a>Vedi anche  
[Impostazione dello scambio di dati](across-set-up-data-exchange.md)  
[Scambio di dati in modalità elettronica](across-data-exchange.md)

