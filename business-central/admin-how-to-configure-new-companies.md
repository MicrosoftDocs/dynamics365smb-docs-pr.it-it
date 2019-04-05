---
title: Configurazione di nuove società | Documenti Microsoft
description: È possibile configurare e personalizzare una nuova società creata. Per definire i dettagli dell'implementazione, occorre eseguire tre fasi per completare la configurazione.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: b1c953b0a5e1247115b26a8984a632478f80cdda
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "802360"
---
# <a name="configure-new-companies"></a>Configurare nuove società
Per configurare una nuova società nell'implementazione della soluzione, in genere occorre seguire tre fasi. La prima fase prevede di importare il pacchetto di configurazione, ovvero un file .rapidstart con informazioni sulla configurazione. Nella seconda fase vengono modificate le informazioni sulla configurazione e collegate alla nuova società. La fase finale consiste nell'analisi e nella correzione degli eventuali errori.  

Le procedure riportate di seguito presuppongono che sia stato creato e salvato un pacchetto di configurazione. Per ulteriori informazioni, vedere [Preparazione di un pacchetto di configurazione](admin-how-to-prepare-a-configuration-package.md).  

Le procedure riportate di seguito presuppongono che la nuova società sia stata inizializzata e aperta e che si stia utilizzando la Gestione ruolo utente Implementatore di RapidStart Services.

## <a name="to-import-a-configuration-package"></a>Per importare un pacchetto di configurazione  
1. Aprire la nuova società nel database di [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Pacchetti di configurazione** e quindi selezionare il collegamento correlato.  
3. Scegliere l'azione **Importa pacchetto**.  
4. Accedere alla posizione in cui si è stato salvato il file del pacchetto di configurazione .rapidstart, quindi scegliere il pulsante **Apri**.  
5. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Informazioni società** e quindi scegliere il collegamento correlato. Immettere le informazioni relative alla società nella scheda Informazioni società. Includere le informazioni, ad esempio le coordinate bancarie. È inoltre possibile inserire il logo della società.  

Vengono importate tutte le tabelle selezionate per l'inserimento nella nuova società. A questo punto, è possibile collegare i dati del pacchetto al database o rettificare e modificare i dati della tabella in base alle specifiche indicate dai clienti.  

## <a name="to-apply-package-data"></a>Per collegare i dati dei del pacchetto  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Foglio di lavoro configurazione** e quindi selezionare il collegamento correlato.  
2. Selezionare una tabella per cui si intende modificare i dati, quindi scegliere l'azione **Collega dati**. Scegliere il pulsante **Sì** per confermare il collegamento.
3. Per confermare che i dati siano ora contenuti nel database e che il collegamento sia riuscito, tornare alla pagina **Foglio di lavoro configurazione** e scegliere l'azione **Dati dabase**.  

> [!NOTE]  
>  Dopo il collegamento i dati possono essere visualizzati solo nel database. Non si trova più nel pacchetto.  

## <a name="to-modify-and-apply-package-data"></a>Per modificare e collegare i dati del pacchetto  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Foglio di lavoro configurazione** e quindi selezionare il collegamento correlato.  
2. Selezionare una tabella per cui si intende modificare i dati, quindi scegliere l'azione **Dati pacchetto**.  
3. Nella pagina **Record pacchetto di configurazione**, apportare le modifiche. Ad esempio, è possibile eliminare le opzioni non applicabili.  
4. Scegliere l'azione **Collega dati**, quindi scegliere il pulsante **OK**.  
5. Per confermare che i dati siano ora contenuti nel database e che il collegamento sia riuscito, tornare alla pagina **Foglio di lavoro configurazione** e scegliere l'azione **Dati dabase**.  

## <a name="to-locate-and-identify-a-configuration-error"></a>Per individuare e identificare un errore di configurazione  
Possono verificarsi alcuni tipi di errore quando si collegano dati a un database. L'errore più comune consiste nella mancata inclusione delle tabelle correlate richieste. È possibile correggere tali errori nel foglio di lavoro configurazione.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Pacchetti di configurazione** e quindi selezionare il collegamento correlato.  
2. Scegliere il pacchetto che si intende esaminare, quindi scegliere l'azione **Modifica**.  

    Vengono evidenziate tutte le tabelle contenenti errori. Il numero di errori del pacchetto viene visualizzato nel campo **Nr. errori del pacchetto**.  

3. Selezionare il campo **Nr. errori pacchetto** per aprire la pagina **Record pacchetto di configurazione**, che elenca i record con errori.  

### <a name="to-fix-an-error"></a>Per correggere un errore  
1. Aprire la società su cui è stato basato il pacchetto di configurazione.  
2. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Foglio di lavoro configurazione** e quindi selezionare il collegamento correlato.  
3. Correggere gli errori, ad esempio aggiungere le tabelle correlate mancanti al foglio di lavoro.  
4. Aggiungere le tabelle al pacchetto di configurazione esistente o creare un nuovo pacchetto che include soltanto le nuove tabelle. Per ulteriori informazioni, vedere [Preparazione di un pacchetto di configurazione](admin-how-to-prepare-a-configuration-package.md).  
5. Riaprire la nuova società per la quale si sta implementando la configurazione.  
6. Importare il pacchetto di configurazione.  

    > [!NOTE]  
    >  Se si importa nuovamente lo stesso pacchetto, è possibile sovrascrivere tutte le modifiche apportate ai dati precedentemente effettuate. Per questo motivo, è possibile aggiungere tutte le nuove tabelle a nuovo pacchetto e importarlo.  

7. Collegare i dati al database, come descritto nella sezione [Per modificare e collegare i dati del pacchetto](admin-how-to-configure-new-companies.md#to-modify-and-apply-package-data).

## <a name="see-also"></a>Vedi anche  
[Applicazione della configurazione a nuove società](admin-apply-configuration-to-new-companies.md)  
[Impostare una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)
