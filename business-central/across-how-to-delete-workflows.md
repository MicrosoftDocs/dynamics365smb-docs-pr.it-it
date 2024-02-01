---
title: Come eliminare i workflow di approvazione
description: È possibile eliminare un flusso di lavoro che non si desidera utilizzare più. Lo stato di tutte le istanze dei passaggi del flusso di lavoro che sono definite nel flusso di lavoro deve essere impostato su **Completato**.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '1500,'
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="delete-approval-workflows"></a>Eliminare i workflow di approvazione

È possibile eliminare un workflow che non si desidera utilizzare più. Lo stato di tutte le istanze delle fasi del workflow nel workflow devono avere stato **Completato**.

> [!CAUTION]
> Quando si elimina un flusso di lavoro, tutte le informazioni in esso contenute vengono perse.

Nella pagina **Workflow** crea un workflow elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi del flusso di lavoro compilando i campi delle righe del flusso di lavoro in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione. Ulteriori informazioni in [Creare workflow di approvazione](across-how-to-create-workflows.md).

## <a name="delete-a-workflow"></a>Eliminare un flusso di lavoro

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.
2. Selezionare il flusso di lavoro che si desidera eliminare.
3. Scegliere l'azione **Elimina**.
4. In alternativa, aprire il flusso di lavoro che si desidera eliminare.
5. Nella pagina **Workflow** scegliere l'azione **Elimina**.

> [!NOTE]
> L'eliminazione di un flusso di lavoro richiede che sia disabilitato. Per disabilitare un flusso di lavoro, aprilo nella pagina **Workflow**, quindi disattiva l'interruttore **Abilitato**.

## <a name="see-also"></a>Vedere anche

[Creare workflow di approvazione](across-how-to-create-workflows.md)  
[Abilitare i workflow di approvazione](across-how-to-enable-workflows.md)  
[Utilizzare i workflow di approvazione](across-use-workflows.md)  
[Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Configurare i flussi di lavoro di approvazione](across-set-up-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
