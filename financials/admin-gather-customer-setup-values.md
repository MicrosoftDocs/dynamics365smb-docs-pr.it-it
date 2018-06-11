---
title: Raggruppare i valori di setup del cliente | Documenti Microsoft
description: "Utilizzare il questionario di configurazione per consentire la riduzione del carico di lavoro di implementazione semplificando i task di impostazione della nuova società. È possibile generare il questionario di configurazione in Business Central e fornirlo al cliente come file di Excel con estensione (.xls) o file XML."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cab3117811ccaca1aca985818a7c2145858beb97
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="gather-customer-setup-values"></a>Raggruppare i valori di setup del cliente
Utilizzare il questionario di configurazione per consentire la riduzione del carico di lavoro di implementazione semplificando i task di impostazione della nuova società. È possibile generare il questionario di configurazione in [!INCLUDE[d365fin](includes/d365fin_md.md)] e fornirlo al cliente come file di Excel o file XML.  

È possibile modificare tutti i valori di default in un questionario in modo che corrispondano il più possibile alle esigenze del cliente.  

> [!TIP]  
>  Per ulteriori informazioni sulla definizione dei valori di setup nei campi relativi alla pianificazione dell'approvvigionamento, vedere [Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md).  

Quando il cliente completa il questionario, importare il file nella nuova società [!INCLUDE[d365fin](includes/d365fin_md.md)] del cliente. L'azienda e il cliente convalidano le risposte del questionario prima di applicarle alla società.

## <a name="to-create-a-configuration-questionnaire"></a>Per creare un questionario di configurazione
È possibile utilizzare il questionario in modo da determinare l'ambito e le esigenze della configurazione. È possibile creare un nuovo questionario o modificarne uno esistente aggiungendo nuove domande o aree domande.  

 È possibile creare questionari solo per le tabelle di tipo setup. Ad esempio, è possibile utilizzare lo strumento per inserire informazioni nelle finestre seguenti:  

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
>  Per visualizzare una lista completa di tabelle di setup, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup**, quindi scegliere il collegamento correlato. Per determinare l'ambito di migrazione dei dati dei record, utilizzare la funzionalità di migrazione. Per ulteriori informazioni, vedere [Migrazione dei dati dei clienti](admin-migrate-customer-data.md).  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Questionario di configurazione**, quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Viene visualizzata la finestra **Questionario su configurazione**.  
3. Scegliere l'azione **Aree domande**. Verrà aperta la finestra **Aree domande**.  
4. Scegliere l'azione **Nuovo**. Verrà aperta la finestra **Area domande su configurazione**.  
5. Nel campo **ID tabella** scegliere l'ID della tabella per cui si desidera raccogliere le informazioni. Il campo **Nome tabella** viene compilato automaticamente.  
6. Scegliere l'azione **Aggiorna domande**. Ogni campo della tabella viene aggiunto al questionario con un punto interrogativo dopo la relativa etichetta.

È possibile immettere nuovamente l'etichetta per indicare chiaramente come si deve rispondere alla domanda. Ad esempio, se il campo è denominato "Nome", è possibile modificarlo per indicare "Qual è il nome di <data being collected>". È inoltre possibile fornire istruzioni nel campo **Riferimento**, incluso un URL a una pagina che fornisce informazioni aggiuntive.  

È anche possibile eliminare qualsiasi domanda che non si desidera includere nel questionario.  

> [!NOTE]  
>  Nel campo **Opzione risposta** viene indicato il tipo e il formato della risposta dei dati appropriati. Nel campo **Risposta** sono contenute informazioni fornite dall'utente.  
>   
>  In base alle esigenze, è possibile definire anche risposte di default nel campo **Risposta**. Tali valori vengono utilizzati di default per il setup personalizzato. Tuttavia, la persona che compila il questionario può modificare e aggiornare la risposta.  

## <a name="to-complete-the-configuration-questionnaire"></a>Per completare il questionario di configurazione
Utilizzare il questionario di configurazione per organizzare e documentare una discussione dettagliata relativa alle esigenze specifiche del cliente. Utilizzarlo anche per raccogliere i dati di setup dal cliente allo scopo di configurare le tabelle di setup [!INCLUDE[d365fin](includes/d365fin_md.md)], quali, ad esempio, contabilità generale, magazzino e clienti.  

> [!NOTE]  
>  È anche possibile creare il proprio questionario di configurazione per soddisfare le proprie esigenze.  

1. Aprire la società per cui si intende completare il questionario.
2. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Questionario di configurazione**, quindi scegliere il collegamento correlato.  
3. Selezionare il questionario per la società, quindi scegliere l'azione **Esporta in Excel**, facoltativamente l'azione **Esporta in XML**.
4. Far completare il questionario di configurazione al cliente immettendo le risposte nella cartella di lavoro di Excel. Esistono prospetti per ciascuna area domande creata per il questionario.   
5. Scegliere l'azione **Importa da Excel** e selezionare il file .xlsx con le risposte del cliente.  
6. Scegliere l'azione **Aree domande** per avviare il processo di convalida e di applicazione delle risposte al questionario di configurazione.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Per completare un questionario dal foglio di lavoro configurazione  
Nella procedura descritta di seguito viene fornita una modalità alternativa per accedere ai questionari di configurazione. Presuppone che il pacchetto di configurazione fornito includa i questionari.  

1. Dopo avere importato un pacchetto di configurazione, aprire il foglio di lavoro configurazione.  
2. Per ogni tabella per cui è presente un'area domande, scegliere l'azione **Domande**. Viene aperta la pagina del questionario.  
3. Rispondere alle domande, quindi scegliere l'azione **Applica risposte**.  
4. Scegliere il pulsante **OK** per chiudere il questionario.

## <a name="to-validate-the-configuration-questionnaire"></a>Per convalidare il questionario di configurazione
È importante convalidare il questionario di configurazione prima di applicarlo al formato di [!INCLUDE[d365fin](includes/d365fin_md.md)]. È anche un modo per mantenere la formattazione dei dati durante l'importazione da Excel.  

Un'operazione di convalida comune consiste nel verificare che stringhe di testo non vengano immesse nei campi data. Il processo di revisione è necessario perché il formato della risposta nel questionario non viene convalidato automaticamente durante l'esecuzione della funzione **Applica risposte**.  

> [!NOTE]  
>  In generale, la convalida del questionario di configurazione è un processo manuale. Esistono, tuttavia, controlli per le incoerenze di formattazione regionali. Inoltre, si verificheranno degli errori se la struttura del database di [!INCLUDE[d365fin](includes/d365fin_md.md)] non corrisponde alla struttura del database di migrazione.  

1. Nella finestra **Questionari di configurazione**, selezionare il questionario appropriato e quindi scegliere l'azione **Aree domande**.  
2. Aprire l'area domande appropriata.  
3. Per ogni domanda, confermare che il valore nel campo **Risposta** corrisponde al formato fornito nel campo **Opzione risposta**. Confermare ad esempio che l'indirizzo di una società è in formato testo.  
4. Se si rivelano degli errori, è possibile risolverli e apportare rettifiche in Excel esportando il questionario e quindi importandolo nuovamente. In alternativa, è anche possibile risolvere gli errori direttamente in [!INCLUDE[d365fin](includes/d365fin_md.md)] mentre si rivedono le risposte nella finestra **Area domande su configurazione**.  
5. Ripetere questi passaggi per ogni area domande.  

Dopo avere completato la convalida, i dati sono pronti per essere collegati al database.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Per applicare le risposte di un questionario di configurazione
Dopo aver importato e convalidato le informazioni da un questionario di configurazione, è possibile trasferire oppure applicare i dati di setup alle tabelle corrispondenti nel database di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Questionario di configurazione**, quindi scegliere il collegamento correlato. Viene visualizzata la finestra **Questionario su configurazione**.  
2. Selezionare un questionario di configurazione dall'elenco e scegliere l'azione **Modifica lista**.  
3. È possibile applicare le risposte in uno dei due modi seguenti.  

- Per applicare l'intero questionario, scegliere l'azione **Applica risposte**.  
- Per applicare le risposte solo per un'**area domande** specifica, scegliere l'azione **Aree domande**, selezionare un'**area domande** nell'elenco, quindi, scegliere l'azione **Applica risposte**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Per verificare che la risposta sia stata applicata correttamente  
1. Controllare le finestre di setup per le diverse aree funzionali di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per trovare la finestra, selezionare l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere il nome della finestra di setup, quindi scegliere il collegamento correlato.  
2. Verificare che i campi siano stato compilati con i dati appropriati provenienti da diverse aree domande del questionario di configurazione.  

A questo punto è stato configurato il setup con le informazioni aziendali e regole del cliente.

## <a name="see-also"></a>Vedi anche  
[Impostare una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)
