---
title: Gestire le interazioni con i contatti
description: 'È possibile gestire tutti i tipi di comunicazioni o interazioni che intercorrono tra la società e i contatti, ad esempio comunicazioni via lettera, fax, e-mail, telefono, riunioni e così via.'
author: jswymer
ms.author: jswymer
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5082,'
ms.date: 04/01/2021
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="record-interactions-with-contacts"></a>Registrare interazioni con contatti

La registrazione delle interazioni con contatti aziendali prevede le seguenti attività:

* Impostazione di modelli di interazione  
* Creazione di interazioni per i contatti e i segmenti  
* Visualizzazione e gestione delle interazioni registrate  

## <a name="set-up-interaction-templates"></a>Impostazione modelli interazione

Prima di poter registrare le interazioni, devi impostare modelli interazione. Il termine modello di interazione indica uno schema che definisce le caratteristiche di base di un'interazione. Quando registri un'interazione, specifichi i modelli interazione su cui si basa. Impostazioni come la modalità di comunicazione utilizzata, chi ha avviato l'interazione e il relativo costo vengono trasferiti all'interazione.

Nella pagina **Modello Interazioni** è possibile impostare un modello di interazione.

Quando imposti un modello interazione, puoi aggiungere un allegato. Ad esempio, potresti allegare un documento Microsoft Word che contiene gli appunti di una riunione. Per ulteriori informazioni sugli allegati, vedi [Allegati per interazioni](marketing-interaction-attachments.md). Ripetere tali passaggi per impostare altri modelli interazione.  

## <a name="create-interactions"></a>Creare interazioni

Esistono due modi di registrare interazioni:

* È possibile creare manualmente interazioni collegate a un singolo contatto o segmento. Per ulteriori informazioni, vedere [Creare interazioni per i contatti e i segmenti](marketing-how-create-interactions.md).  
* È possibile fare in modo che le interazioni vengano registrate automaticamente nell'applicazione quando si eseguono azioni specifiche, ad esempio la stampa di una fattura o di un'offerta. Per ulteriori informazioni, vedere [Registrazione automatica delle interazioni con i contatti](marketing-auto-record-interactions.md).

## <a name="view-and-manage-recorded-interactions"></a>Visualizzazione e gestione delle interazioni registrate

È possibile visualizzare tutte le interazioni registrate non rimosse nella pagina **Mov. Log Interazione**. È possibile aprire la pagina per:

* Utilizzare l'icona **Cerca pagina o report** per cercare in **Movimenti log interazione**.
* Scegliere l'azione **Movimenti log interazione** in un contatto o un segmento.

  La pagina **Movimenti log interazione** contiene le interazioni create manualmente e le interazioni che [!INCLUDE [prod_short](includes/prod_short.md)] registra automaticamente.

Utilizza la pagina Movimenti log interazione per visualizzare lo stato delle interazioni e annullarle.

È possibile eliminare i movimenti log interazione che sono stati annullati. Per eliminare i movimenti log interazione, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Elimina movimenti log interazione annullati**, quindi scegli il collegamento correlato e compila le informazioni.

## <a name="see-also"></a>Vedi anche

[Gestione dei contatti](marketing-contacts.md)  
[Gestione delle opportunità di vendita](marketing-manage-sales-opportunities.md)  
[Utilizzare Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
