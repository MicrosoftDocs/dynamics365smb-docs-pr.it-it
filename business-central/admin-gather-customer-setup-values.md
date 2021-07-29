---
title: Raggruppare i valori di setup del cliente
description: Il questionario di configurazione aiuta a ridurre l'implementazione semplificando la creazione di nuove società e offrendo ai clienti un file Excel o XML.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: d38074c1ba42377707503fc87f242ad483552c93
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443895"
---
# <a name="gather-customer-setup-values"></a>Raggruppare i valori di setup del cliente
Utilizzare il questionario di configurazione per consentire la riduzione del carico di lavoro di implementazione semplificando i task di impostazione della nuova società. È possibile generare il questionario di configurazione in [!INCLUDE[prod_short](includes/prod_short.md)] e fornirlo al cliente come file di Excel o file XML.  

È possibile modificare tutti i valori di default in un questionario in modo che corrispondano il più possibile alle esigenze del cliente.  

> [!TIP]  
>  Per ulteriori informazioni sulla definizione dei valori di setup nei campi relativi alla pianificazione dell'approvvigionamento, vedere [Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md).  

Quando il cliente completa il questionario, importare il file nella nuova società [!INCLUDE[prod_short](includes/prod_short.md)] del cliente. L'azienda e il cliente convalidano le risposte del questionario prima di applicarle alla società.

## <a name="to-create-a-configuration-questionnaire"></a>Per creare un questionario di configurazione
È possibile utilizzare il questionario in modo da determinare l'ambito e le esigenze della configurazione. È possibile creare un nuovo questionario o modificarne uno esistente aggiungendo nuove domande o aree domande.  

<!-- A configuration questionnaire has the following structure
* The name of the questionnaire itself
* Question Areas that group questions about a similar subject. For example, you might create a question area that focuses on entering company informtion. Typically, configuration questionnaires have many question groups
* Questions that are closed ended, meaning that the customer must choose an answer, and can choose only one. -->

 È possibile creare questionari solo per le tabelle di tipo setup. Ad esempio, è possibile utilizzare lo strumento per inserire informazioni nelle pagine seguenti:  

-   Informazioni società  
-   Setup cespiti  
-   Setup contabilità generale  
-   Setup magazzino  
-   Setup assemblaggio
-   Setup manufacturing  
-   Setup contabilità fornitori  
-   Setup marketing  
-   Setup assistenza  
-   Setup contabilità clienti  
-   Setup warehouse  

> [!NOTE]  
>  Per visualizzare un elenco completo delle tabelle di configurazione, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup**, quindi scegli il collegamento correlato. Per determinare l'ambito di migrazione dei dati dei record, utilizzare la funzionalità di migrazione. Per ulteriori informazioni, vedere [Migrazione dei dati dei clienti](admin-migrate-customer-data.md).  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Questionari di configurazione**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.   
3. Nella pagina **Questionari di configurazione**, nel campo **Codice**, immettere... 
<!--4. In the **Name** field, enter...
5. Choose the **Question Areas** action. .
6. On the **Config. Question Areas** page, in the **Code** field, enter...
  
    > [!Note]  
    > The code is alphanumeric, and must start with a letter of the alphabet.
7. In the Table ID field, choose the table to which to apply the answer to the question. Your selection will determine the fields that are available for the questions, and thereby the answer selections.
  
    > [!Tip]
    > The list of table objects is long. If you know the name of the table, use **Search** in the upper left to find it in the list.
8. In the **Description** field, enter text that indicates the subject of the question group.
9. In the **No.** field, enter a number to define where the question appears in the sequence of questions.
10. In the **Field ID** field, choose the field the the customer's answer will be applied to. You can choose from the fields on the table you chose in the **Table ID** field.
  
    When you choose a field, [!INCLUDE[prod_short](includes/prod_short.md)] provides a suggestion in the **Question** field. You can edit the question if needed.
11. To add more questions to the questionnaire, repeat steps seven through 10.

> [!Tip]
> If at some point you change a question, or add a new one, choose the **Update Questions** action to update the list.

-->

3. Scegliere l'azione **Aree domande**. Verrà aperta la pagina **Aree domande**.  
4. Scegliere l'azione **Nuovo**. Verrà aperta la pagina **Area domande su configurazione**.  
5. Nel campo **ID tabella** scegliere l'ID della tabella per cui si desidera raccogliere le informazioni. Il campo **Nome tabella** viene compilato automaticamente.  
6. Scegliere l'azione **Aggiorna domande**. Ogni campo della tabella viene aggiunto al questionario con un punto interrogativo dopo la relativa etichetta.

È possibile immettere nuovamente l'etichetta per indicare chiaramente come si deve rispondere alla domanda. Ad esempio, se il campo è denominato "Nome", è possibile modificarlo per indicare "Qual è il nome di <data being collected>". È inoltre possibile fornire istruzioni nel campo **Riferimento**, incluso un URL a una pagina che fornisce informazioni aggiuntive.  

È anche possibile eliminare qualsiasi domanda che non si desidera includere nel questionario.  

> [!NOTE]  
>  Nel campo **Opzione risposta** viene indicato il tipo e il formato della risposta dei dati appropriati. Nel campo **Risposta** sono contenute informazioni fornite dall'utente.  
>   
>  In base alle esigenze, è possibile definire anche risposte di default nel campo **Risposta**. Tali valori vengono utilizzati di default per il setup personalizzato. Tuttavia, la persona che compila il questionario può modificare e aggiornare la risposta.  

## <a name="to-complete-the-configuration-questionnaire"></a>Per completare il questionario di configurazione
Utilizzare il questionario di configurazione per organizzare e documentare una discussione dettagliata relativa alle esigenze specifiche del cliente. Utilizzarlo anche per raccogliere i dati di setup dal cliente allo scopo di configurare le tabelle di setup [!INCLUDE[prod_short](includes/prod_short.md)], quali, ad esempio, contabilità generale, magazzino e clienti.  

> [!NOTE]  
>  È anche possibile creare il proprio questionario di configurazione per soddisfare le proprie esigenze.  

1. Aprire la società per cui si intende completare il questionario.
2. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Questionari di configurazione**, quindi scegli il collegamento correlato.  
3. Selezionare il questionario per la società, quindi scegliere l'azione **Esporta in Excel**, facoltativamente l'azione **Esporta in XML**.
4. Far completare il questionario di configurazione al cliente immettendo le risposte nella cartella di lavoro di Excel. Esistono prospetti per ciascuna area domande creata per il questionario.   
5. Salvare la cartella di lavoro di Excel come *Dati XML*. Scegliere l'azione **Importa da XML** e selezionare il file .xml con le risposte del cliente.
6. Scegliere l'azione **Aree domande** per avviare il processo di convalida e di applicazione delle risposte al questionario di configurazione.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Per completare un questionario dal foglio di lavoro configurazione  
Nella procedura descritta di seguito viene fornita una modalità alternativa per accedere ai questionari di configurazione. Presuppone che il pacchetto di configurazione fornito includa i questionari.  

1. Dopo avere importato un pacchetto di configurazione, aprire il foglio di lavoro configurazione.  
2. Per ogni tabella per cui è presente un'area domande, scegliere l'azione **Domande**. Viene aperta la pagina del questionario.  
3. Rispondere alle domande, quindi scegliere l'azione **Applica risposte**.  
4. Scegliere il pulsante **OK** per chiudere il questionario.

## <a name="to-validate-the-configuration-questionnaire"></a>Per convalidare il questionario di configurazione
È importante convalidare il questionario di configurazione prima di applicarlo al formato di [!INCLUDE[prod_short](includes/prod_short.md)]. È anche un modo per mantenere la formattazione dei dati durante l'importazione da Excel.  

Un'operazione di convalida comune consiste nel verificare che stringhe di testo non vengano immesse nei campi data. Il processo di revisione è necessario perché il formato della risposta nel questionario non viene convalidato automaticamente durante l'esecuzione della funzione **Applica risposte**.  

> [!NOTE]  
>  In generale, la convalida del questionario di configurazione è un processo manuale. Esistono, tuttavia, controlli per le incoerenze di formattazione regionali. Inoltre, si verificheranno degli errori se la struttura del database di [!INCLUDE[prod_short](includes/prod_short.md)] non corrisponde alla struttura del database di migrazione.  

1. Nella pagina **Questionari di configurazione**, selezionare il questionario appropriato e quindi scegliere l'azione **Aree domande**.  
2. Aprire l'area domande appropriata.  
3. Per ogni domanda, confermare che il valore nel campo **Risposta** corrisponde al formato fornito nel campo **Opzione risposta**. Confermare ad esempio che l'indirizzo di una società è in formato testo.  
4. Se si rivelano degli errori, è possibile risolverli e apportare rettifiche in Excel esportando il questionario e quindi importandolo nuovamente. In alternativa, è anche possibile risolvere gli errori direttamente in [!INCLUDE[prod_short](includes/prod_short.md)] mentre si rivedono le risposte nella pagina **Area domande su configurazione**.  
5. Ripetere questi passaggi per ogni area domande.  

Dopo avere completato la convalida, i dati sono pronti per essere collegati al database.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Per applicare le risposte di un questionario di configurazione
Dopo aver importato e convalidato le informazioni da un questionario di configurazione, è possibile trasferire oppure applicare i dati di setup alle tabelle corrispondenti nel database di [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Questionari di configurazione**, quindi scegli il collegamento correlato. Viene visualizzata la pagina **Questionario su configurazione**.  
2. Selezionare un questionario di configurazione dall'elenco e scegliere l'azione **Modifica lista**.  
3. È possibile applicare le risposte in uno dei due modi seguenti.  

- Per applicare l'intero questionario, scegliere l'azione **Applica risposte**.  
- Per applicare le risposte solo per un'**area domande** specifica, scegliere l'azione **Aree domande**, selezionare un'**area domande** nell'elenco, quindi, scegliere l'azione **Applica risposte**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Per verificare che la risposta sia stata applicata correttamente  
1. Controllare le pagine di setup per le diverse aree funzionali di [!INCLUDE[prod_short](includes/prod_short.md)]. Per individuare la pagina, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere il nome della pagina di setup e quindi scegliere il collegamento correlato.  
2. Verificare che i campi siano stato compilati con i dati appropriati provenienti da diverse aree domande del questionario di configurazione.  

A questo punto è stato configurato il setup con le informazioni aziendali e regole del cliente.

## <a name="see-also"></a>Vedere anche  
[Impostazione di una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]