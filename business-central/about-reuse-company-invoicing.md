---
title: Usare la fatturazione e Business Central
description: Soluzione alternativa per l'accesso a Microsoft Invoicing dopo aver effettuato l'iscrizione a Dynamics 365 Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Invoicing, Microsoft 365'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="use-the-same-microsoft-365-account-in--and-microsoft-invoicing"></a><a name="use-the-same-microsoft-365-account-in--and-microsoft-invoicing"></a>Utilizzare lo stesso account di Microsoft 365 in [!INCLUDE[prod_short](includes/prod_long.md)] e Microsoft Invoicing
Quando si effettua l'iscrizione per una versione di valutazione con [!INCLUDE[prod_short](includes/prod_short.md)], è possibile passare a una fase di valutazione di 30 giorni, effettuare una sottoscrizione oppure interrompere l'utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]. In tutti i casi, ad un certo punto potrebbe essere stato visualizzato un riquadro chiamato **Microsoft Invoicing** e potrebbe essere stato fatto clic su di esso. Era un'app che faceva parte di quello che ora è Microsoft 365 Business Standard ed era precedentemente noto come abbonamento Microsoft 365 Business Premium, quindi non tutti avranno visto quel riquadro nella propria esperienza di Microsoft 365.  

Microsoft Invoicing non è più disponibile, ma se fosse necessario accedere a Invoicing per recuperare i dati, è possibile che venga visualizzato un messaggio in cui non è possibile accedere a Microsoft Invoicing poiché l'account è utilizzato in [!INCLUDE[prod_short](includes/prod_short.md)].  

Un messaggio simile viene visualizzato se si installa l'app mobile per Invoicing.  

## <a name="workaround"></a><a name="workaround"></a>Soluzione alternativa
Invoicing e [!INCLUDE[prod_short](includes/prod_short.md)] dispongono di una piattaforma condivisa. Di conseguenza, quando l'utente fa clic su Invoicing nell'interfaccia di amministrazione di Microsoft 365, viene riconosciuto come un utente esistente di [!INCLUDE[prod_short](includes/prod_short.md)]. Ciò si verifica perché Invoicing non può utilizzare la stessa società in uso in [!INCLUDE[prod_short](includes/prod_short.md)].  

Sarà necessario accedere a [!INCLUDE[prod_short](includes/prod_short.md)], rinominare la società esistente, quindi creare una nuova società che potrà essere utilizzata in Invoicing. Nessun dato viene spostato né sovrascritto durante questa soluzione alternativa.

### <a name="to-rename-your-company"></a><a name="to-rename-your-company"></a>Per rinominare la società
1. Accedi a [!INCLUDE[prod_short](includes/prod_short.md)].
2. Nell'angolo superiore destro scegli l'icona **Impostazioni** ![Impostazioni](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente"), quindi scegli l'azione **Impostazioni personali**.
3. Nel campo **Società**, scegliere un'altra società.
4. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Società**, quindi scegli il collegamento correlato.  
5. Nella pagina **Società**, scegliere **Modifica lista**.  
6. Modificare il nome dell'elemento *La mia società* inserendo una denominazione diversa.  

    Attendere alcuni minuti. Apporteremo alcune modifiche nel database sottostante e tale operazione richiede del tempo.
7.  Quando il sistema è nuovamente pronto all'uso, scegliere il pulsante **Crea nuova società**.  
8.  Nella finestra di dialogo visualizzata, specificare il nome come *La mia società*, quindi scegliere l'opzione **Produzione - Solo dati setup**.  

Anche tale operazione richiede alcuni minuti. Al completamento del processo, sarà possibile accedere a Invoicing come parte dell'esperienza Microsoft 365 Business Standard. Ma solo per esportare i dati poiché l'app Invoicing è obsoleta.  

### <a name="what-about-my-data"></a><a name="what-about-my-data"></a>Quali modifiche vengono apportate ai miei dati?
Quando si rinomina l'elemento originale in La mia società, le tabelle del database in cui sono memorizzati i dati [!INCLUDE[prod_short](includes/prod_short.md)] esistenti vengono rinominate, ma i dati stessi non subiscono alcuna modifica.  

Se si utilizza sia Invoicing che [!INCLUDE[prod_short](includes/prod_short.md)], i dati vengono memorizzati in due contenitori diversi (le due società). Nessun elemento viene condiviso, quindi sarà necessario gestire i clienti e gli articoli in entrambe le società.  

## <a name="see-also"></a><a name="see-also"></a>Vedere anche
[Domande frequenti](across-faq.yml)  
[Amministrazione](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
