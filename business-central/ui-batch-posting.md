---
title: Come registrare più documenti contemporaneamente | Microsoft Docs
description: Anziché registrare un singolo documento alla volta, è possibile selezionare più documenti non registrati in un elenco per la registrazione batch, per una registrazione immediata o programmata, ad esempio, per la fine della giornata.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1fd25f8b07a359414f62ef4757162f8a73889c27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912723"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Registrare più documenti contemporaneamente

Anziché registrare un singolo documento alla volta, è possibile selezionare più documenti non registrati in un elenco per una registrazione immediata o una registrazione batch programmata, ad esempio, per la fine della giornata. Ciò può essere utile se solo un supervisore può registrare documenti creati da altri utenti o per evitare problemi di prestazioni del sistema dovuti alla registrazione durante l'orario di lavoro.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Per registrare immediatamente più ordini di acquisto

La seguente procedura descrive come registrare immediatamente più ordini di acquisto. I passaggi sono simili per tutti i documenti di acquisto e vendita.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e quindi scegliere il collegamento correlato.
2. Nella pagina **Ordini acquisto**, selezionare tutti gli ordini da registrare:
3. Nel campo **Nr.** selezionare i tre punti verticali per aprire il menu di scelta rapida, quindi scegliere il l'azione **Seleziona più elementi**.
4. Selezionare la casella di controllo per tutte le righe che rappresentano gli ordini che si desidera registrare contemporaneamente.
5. Scegliere l'azione **Registrazione** e quindi l'azione **Registra**.
6. Scegliere il pulsante **Sì** nel messaggio di conferma.

## <a name="to-batch-post-multiple-purchase-orders"></a>Per eseguire registrazioni batch di ordini di acquisto

La seguente procedura descrive come eseguire registrazioni batch di ordini di acquisto. I passaggi sono simili per tutti i documenti di acquisto e vendita in cui l'azione **Registra batch** è disponibile.

> [!NOTE]
> La registrazione in batch dei documenti avviene in background. [!INCLUDE [prodshort](includes/prodshort.md)] online include processi predefiniti per la registrazione in background e la registrazione in batch. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Ordini acquisto**, selezionare tutti gli ordini da registrare:
3. Nel campo **Nr.** selezionare i tre punti verticali per aprire il menu di scelta rapida, quindi scegliere il l'azione **Seleziona più elementi**.
4. Selezionare la casella di controllo per tutte le righe che rappresentano gli ordini che si desidera registrare contemporaneamente.
5. Scegliere l'azione **Registrazione** e quindi l'azione **Registra batch**.
6. Nella pagina **Aggior. batch ordini acquisto**, riempire i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Scegliere il pulsante **OK**.
8. Per visualizzare potenziali problemi verificatisi durante la registrazione batch di documenti, aprire la pagina **Registro messaggi di errore**.

Gli ordini di acquisto verranno ora aggiunti a un movimento coda processi dedicato, che definisce quando i documenti vengono registrati. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

Se si seleziona **PDF** nel campo **Tipo di output report**, gli ordini di acquisto registrati correttamente saranno disponibili nella parte **Report elaborati** in Gestione ruolo utente.

## <a name="see-also"></a>Vedere anche

[Contabilizzazione dei documenti e delle registrazioni](ui-post-documents-journals.md)  
[Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md)  
[Modificare i documenti registrati](across-edit-posted-document.md)  
[Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
