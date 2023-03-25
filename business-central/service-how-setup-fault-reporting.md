---
title: Impostare il reporting dei guasti in Gestione assistenza
description: Il reporting dei guasti consente di stabilire degli standard per registrare le informazioni relative ai guasti per gli articoli in assistenza con codici guasto e altro.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---

# Impostare il reporting dei guasti
Il reporting dei guasti consente di stabilire degli standard per registrare le informazioni relative ai guasti per gli articoli in assistenza. Ad esempio, è possibile specificare il tipo di problema, gli indizi osservati, il motivo del problema e in che modo risolverlo.  

I codici dei guasti descrivono i guasti tipici degli articoli in assistenza o le azioni che vengono intraprese su di essi. In base al livello di reporting di guasto nella propria azienda, potrebbe anche essere necessario impostare codici area guasto e codici indizio prima di impostare i codici guasto. Le aree guasto descrivono le aree dei guasti negli articoli in assistenza. I codici causa guasto descrivono il motivo dei guasti negli articoli in assistenza e, se necessario, specificano se escludere gli sconti di garanzia e contratto. Ad esempio, si potrebbe richiedere di escludere gli sconti di garanzia e contratto se il cliente è stato in qualche modo responsabile del guasto nell'articolo in assistenza. I codici causa guasto vengono assegnati agli ordini di assistenza. Per ulteriori informazioni, vedere [Utilizzare i compiti di assistenza](service-how-to-work-on-service-tasks.md).  

## Per specificare il livello globale di reporting dei guasti
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup assistenza**, quindi scegli il collegamento correlato.
2. Nel campo **Livello di reporting guasto** scegliere una delle opzioni descritte nella seguente tabella.  

    |**Livello guasto**|**Description**|  
    |------------|-------------|  
    |Nessuno | Non vengono utilizzati codici di reporting.|  
    |Guasto | I codici sono elencati nella tabella **Codici guasto**. Tali codici identificano i guasti degli articoli in assistenza o le azioni da intraprendere su di essi. È possibile raggruppare i codici correlati nei raggruppamenti **Codice area guasto**.|  
    |Guasto + Indizio | L'utente specifica una combinazione di codici nelle tabelle **Codici guasto** e **Codici indizio**. I codici indizio tipici includono degli indicatori che un cliente potrebbe utilizzare per descrivere un problema, ad esempio un rumore o una qualità.|  
    |Guasto + Indizio + Area | I codici guasto, indizio e area guasto vengono utilizzati come implementazione del sistema di codifica internazionale delle riparazioni (IRIS, International Repair Coding System).|  

Per completare l'impostazione del reporting dei guasti, è anche possibile specificare quali riparazioni o risoluzioni sono associate a un guasto o a un difetto. Esegui l'impostazione nella pagina **Relaz. cod. guasto/risoluzione**, in cui sono state impostate le combinazioni di codici per il gruppo a cui appartiene l'articolo in assistenza da cui hai effettuato l'accesso alla finestra e il numero di occorrenze per ciascuno di essi.

## Per creare relazioni codici guasto e risoluzione
<!--this needs to go in a working with topic-->
 Al fine di visualizzare le modalità più comuni di riparazione di particolari guasti nell'articolo durante l'assistenza, occorre impostare informazioni relative a relazioni codici guasto/risoluzione. Utilizzare il processo batch **Inser. relaz. cod. guasti/risol.** per trovare tutte le combinazioni di codici di guasto e di risoluzione negli ordini di assistenza registrati e registrarle nella pagina **Relazioni codici guasto/risoluzione**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Inser. relaz. cod. guasti/risol.**, quindi seleziona il collegamento correlato.  
2. Immettere le date per definire il periodo che si desidera includere nel processo batch.  
3. Per raggruppare le relazioni in base al gruppo di articoli in assistenza, scegliere la casella di controllo **Relaziona in base a Gruppo art. in ass.**.  
4. Per mantenere i record già inseriti manualmente nella pagina **Relazioni codici guasto/risoluzione**, scegliere la casella di controllo **Mantieni record inseriti manualm.**  

## Vedere anche
[Impostazione della gestione assistenza](service-setup-service.md)  
[Gestione assistenza](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]