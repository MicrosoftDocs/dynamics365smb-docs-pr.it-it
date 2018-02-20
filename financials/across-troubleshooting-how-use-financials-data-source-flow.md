---
title: Risoluzione dei problemi di integrazione con Microsoft Flow | Documenti Microsoft
description: Risolvere i problemi per rendere disponibili i dati di Financials come origine dati e specificare un URL OData dei service Web per creare un workflow automatizzato.
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4c28b5b6dce6152399cf599877180e806227b5ef
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a>Risoluzione dei problemi di integrazione con Microsoft Flow - Richiesta di URL troppo lungo
È possibile utilizzare i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come parte di un flusso di lavoro in Microsoft Flow.  

> [!NOTE]  
>   È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con Flow.  

Se si sta creando un Microsoft Flow utilizzando il connettore [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile ricevere un messaggio di errore indicante che l'URL richiesto è troppo lungo dopo la creazione del flusso, ad esempio: **RequestUriTooLong**.

## <a name="cause"></a>Causa
Quando si attiva un flusso viene eseguita la ricerca delle modifiche ai dati. Nel determinare se i dati sono stati modificati, i connettori confrontano i dati memorizzati nella cache con i nuovi dati richiesti dall'origine.  

Quando la richiesta dei dati crea un URL troppo lungo l'esito è negativo. Le cause comuni possono includere:
- Generalmente, qualsiasi tabella di origine con più di 250 righe
- Tabelle di origine che contengono diverse migliaia di record

## <a name="workaround"></a>Soluzione alternativa
Utilizzare questa procedura come soluzione alternativa.
1. Scegliere di modificare il flusso che ha restituito l'esito negativo.
2. Espandere **Mostra opzioni avanzate** nel trigger del flusso.
3. Nel campo **Ignora numero** immettere il numero dei record da ignorare.  
Ad esempio, se la tabella utilizzata come origine dati contiene 4.000 record, immettere 4.000 come numero di record da ignorare.
4. Aggiornare il flusso.

> [!NOTE]  
> Il connettore è attualmente in Beta. Gli aggiornamenti alla modalità di modifica dei dati vengono inclusi in una versione futura.


## <a name="see-also"></a>Vedi anche
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in un workflow automatizzato](across-how-use-financials-data-source-flow.md)  
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importazione dei dati aziendali da altri sistemi contabili](upload-data.md)  
[Gestire utenti e autorizzazioni](ui-how-users-permissions.md)    
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanze](finance.md)  

