---
title: Gestione della configurazione della società in un foglio di lavoro | Documenti Microsoft
description: Il foglio di lavoro configurazione è la posizione centrale in cui è possibile pianificare, tenere traccia ed eseguire le operazioni di configurazione. È possibile creare un prospetto per ogni società in uso o creare un foglio di lavoro configurazione standard che può essere utilizzato per la configurazione di più società dello stesso tipo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3b4be28dda5e01656f8e91fe813c01969115100
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378250"
---
# <a name="manage-company-configuration-in-a-worksheet"></a>Gestione della configurazione della società in un foglio di lavoro
Il foglio di lavoro configurazione è la posizione centrale in cui è possibile pianificare, tenere traccia ed eseguire le operazioni di configurazione. È possibile creare un foglio di lavoro per ogni società in uso o creare un foglio di lavoro configurazione standard che può essere utilizzato per la configurazione di più società dello stesso tipo.  

La prima fase per la preparazione di un pacchetto di configurazione consiste nel selezionare una società che è già stata impostata e modificata in base alle esigenze specifiche della soluzione. Questa società costituisce un riferimento per le operazioni di configurazione di nuove società. Nel prospetto è possibile definire le tabelle che si desidera controllare e gestire tramite la configurazione. Poiché la maggior parte delle tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] presenta relazioni e dipendenze con altre tabelle, è possibile includere tali tabelle correlate in base alle proprie esigenze. Insieme, queste tabelle costituiranno la struttura relative su cui creare una nuova società. I passaggi successivi spiegano come creare il pacchetto di configurazione e implementarlo.  

Per agevolare il monitoraggio e la revisione del proprio lavoro, utilizzare il Dettaglio informazioni **Tabella pacchetto di configurazione** per visualizzare le informazioni relative ai record. Utilizzare il Dettaglio informazioni **Tabelle correlate a configurazione** per verificare le relazioni tra tabelle.  

Nelle procedure riportate di seguito viene illustrato come aggiungere e personalizzare le informazioni della tabella per la configurazione.  

## <a name="to-open-the-configuration-worksheet"></a>Per aprire il foglio di lavoro configurazione.  
1.  In [!INCLUDE[prod_short](includes/prod_short.md)] aprire la società che costituisce il modello di riferimento per la configurazione, quindi la Gestione ruolo utente Implementatore di RapidStart Services.  
2.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Foglio di lavoro configurazione** e quindi scegliere il collegamento correlato.  

## <a name="to-add-a-table-to-the-worksheet"></a>Per aggiungere una tabella al foglio di lavoro  
1.  Nella pagina **Foglio di lavoro configurazione**, scegliere l'azione **Modifica lista**.  
2.  Nella prima riga, nel campo **Tipo riga**, selezionare **Tabella**.  
4.  Nel campo **ID tabella** selezionare la tabella che si desidera aggiungere alla configurazione.  
5.  Nel campo **ID pagina** immettere l'ID della pagina associata alla tabella. Per le tabelle standard, questo valore viene compilato automaticamente. Per le tabelle personalizzate, occorre immettere l'ID.
6.  Nel campo **Riferimento** immettere l'URL di una pagina di documentazione, ad esempio della Guida, che fornisce procedure consigliate o istruzioni su come impostare la tabella.  
7.  Per aggiungere le tabelle correlate, scegliere l'azione **Ottieni tabelle correlate**.  

    > [!NOTE]  
    > Le tabelle correlate non verranno aggiunte con l'azione **Ottieni tabelle correlate** se una delle seguenti condizioni è vera:
    > - La relazione è condizionale.  
    > Esempio: se si ottengono le tabelle correlate per la tabella **Cliente**, la tabella **Ubicazione** non verrà aggiunta poiché è correlata solo in modo condizionale alla tabella **Cliente**, ovvero se il campo **Codice ubicazione** nella tabella **Cliente** è compilato.  
    > - La tabella correlata è filtrata.  
    > Esempio: un campo nella tabella relativa dispone di una clausola WHERE. Il motivo è che le informazioni sulle relazioni implicate vengono archiviate nella tabella di sistema **Campo**, che non è completamente accessibile all'applicazione.  
    > È necessario aggiungere tali tipi di tabelle manualmente seguendo il passaggio 4 della procedura.  

8.  Per modificare la lista delle tabelle risultante, selezionare una tabella che si desidera rimuovere, quindi scegliere l'azione **Elimina**.  
9. Ripetere i passaggi per ogni tabella che si desidera aggiungere alla configurazione.  
10. Per rimuovere le informazioni di tabella duplicate, che possono risultare dall'utilizzo dell'azione **Ottieni tabelle correlate**, scegliere l'azione **Elimina righe duplicate**. Ciò rimuoverà le tabelle duplicate con lo stesso codice pacchetto.  

## <a name="to-add-multiple-tables-to-the-configuration-worksheet"></a>Per aggiungere più tabelle al foglio di lavoro configurazione  
1. Scegliere l'azione **Ottieni tabelle**. Viene visualizzata la pagina con il processo batch **Ottieni tabelle di configurazione**.  
2. Nella Scheda dettaglio **Opzioni**, specificare i tipi di tabelle da aggiungere alla configurazione, come descritto nella tabella seguente.

    |Opzione|Description|  
    |----------------------------------|---------------------------------------|  
    |**Includi solo elementi con dati**|Selezionare la casella di controllo per includere solo le tabelle contenenti dati. Ad esempio, può essere necessario includere una tabella che definisce già le condizioni di pagamento tipiche supportate dalla soluzione in uso.|  
    |**Includi tabelle correlate**|Selezionare la casella di controllo per includere tutte le tabelle correlate. Per aggiungere un sottoinsieme di tabelle correlate, vedere il passaggio 3 di questa procedura.|  
    |**Includi tabelle di dimensioni**|Selezionare la casella di controllo per includere le tabelle di dimensioni.|  
    |**Includi solo tabelle con licenza**|Selezionare la casella di controllo per includere solo le tabelle per le quali è presente una licenza per la creazione del prospetto che consente l'accesso.|

3. Nella Scheda dettaglio **Oggetto** impostare i filtri appropriati per specificare i tipi di tabelle da includere o escludere.  
4. Scegliere il pulsante **OK**. Le tabelle di [!INCLUDE[prod_short](includes/prod_short.md)] vengono aggiunte al prospetto. Per ogni movimento nella lista è presente un tipo di riga **Tabella**.  
5. Per rimuovere le informazioni di tabella duplicate, che possono risultare dall'utilizzo dell'azione **Ottieni tabelle**, scegliere l'azione **Elimina righe duplicate**. Ciò rimuoverà le tabelle duplicate con lo stesso codice pacchetto.  
6. È possibile aggiungere al prospetto tabelle collegate a una tabella selezionata dall'utente. Esaminare le informazioni nel dettaglio informazioni **Tabelle correlate** per controllare se vi sono tabelle mancanti. Per aggiungere le tabelle correlate a una tabella specifica, selezionare la tabella nella lista, quindi scegliere l'azione **Ottieni tabelle correlate**.  

    > [!NOTE]  
    > Le tabelle correlate non verranno aggiunte con l'azione **Ottieni tabelle correlate** se una delle seguenti condizioni è vera:
    > - La relazione è condizionale.  
    > Esempio: se si ottengono le tabelle correlate per la tabella **Cliente**, la tabella **Ubicazione** non verrà aggiunta poiché è correlata solo in modo condizionale alla tabella **Cliente**, ovvero se il campo **Codice ubicazione** nella tabella **Cliente** è compilato.  
    > - La tabella correlata è filtrata.  
    > Esempio: un campo nella tabella relativa dispone di una clausola WHERE. La ragione è che le informazioni implicate di relazioni vengono archiviate nella tabella virtuale **Campo** e non sono disponibili nelle pagine quali il prospetto di configurazione per i motivi di prestazione.  
    > È necessario aggiungere le tabelle correlate caratterizzate da relazioni particolarmente complesse manualmente seguendo il passaggio 4 nella sezione [Per aggiungere una tabella al foglio di lavoro](admin-how-to-manage-company-configuration-in-a-worksheet.md#to-add-a-table-to-the-worksheet).

7. Per eliminare tabelle dalla lista delle tabelle risultante, selezionare una tabella da rimuovere, quindi scegliere l'azione **Elimina**.  

Attenersi alla procedura descritta di seguito per specificare i campi della tabella da includere. Dopo la creazione di questa specifica, è possibile esportare la tabella in Excel e utilizzare la struttura della tabella come modello per la raccolta dei dati relativi ai clienti. Per ulteriori informazioni, vedere [Preparare la migrazione dei dati dei clienti](admin-use-templates-to-prepare-customer-data-for-migration.md).  

## <a name="to-specify-a-set-of-fields-and-records-for-a-configuration-table"></a>Per specificare un insieme di campi e di record per una tabella di configurazione  
1. Selezionare una tabella dalla lista delle tabelle di configurazione, quindi scegliere l'azione **Modifica lista**.  
2. Selezionare una tabella in cui si desidera specificare le informazioni relative ai campi, quindi scegliere l'azione **Campi**.  
3. Per selezionare solo i campi da includere, scegliere l'azione **Cancella campo Incluso**. Per aggiungere tutti i campi, scegliere l'azione **Imposta campo incluso**.  
4. Per specificare che i dati di un campo non devono essere convalidati, deselezionare la casella di controllo **Convalida campo** del campo.  
5. Scegliere il pulsante **OK**.  
6. Per filtrare un determinato set di record da includere nel foglio di lavoro configurazione, scegliere l'azione **Filtri** e specificare i valori di filtro appropriati.

È possibile creare aree di funzionalità e gruppi di tabelle nel prospetto in modo da raggruppare le funzionalità simili. Ad esempio, per impostare il piano dei conti per la configurazione, è possibile decidere di creare un gruppo di tabelle per la registrazione. In genere, le aree vengono utilizzate per raggruppare una serie di tabelle che corrispondono a un'area funzionale. Ogni area può contenere gruppi. Un gruppo può essere utilizzato per ordinare le tabelle che presentano una funzione comune.  

Nella procedura riportata di seguito viene descritto come aggiungere designazioni di gruppi e aree dopo che è stata creata la lista di tabelle iniziale. Dopo l'aggiunta di queste categorie, è possibile continuare ad aggiungere tabelle e modificare la relativa lista.  

## <a name="to-categorize-and-group-functionality-in-the-worksheet"></a>Per classificare e per raggruppare le funzionalità del prospetto  
1. All'inizio di un area, inserire una nuova riga nel foglio di lavoro.  
2. Nel campo **Tipo riga**, scegliere **Area**. Nel campo **Nome** immettere un nome per l'area.  
3. All'inizio di un raggruppamento di tabelle, inserire una nuova riga nel foglio di lavoro.  
4. Nel campo **Tipo riga**, scegliere **Gruppo**. Nel campo **Nome** immettere un nome per l'area. Il nome del gruppo viene automaticamente indentato.  
5. Per spostare le tabelle nella categoria appropriata, selezionare una tabella da spostare quindi scegliere l'azione **Vai su** o **Vai giù**. In alternativa, è possibile eliminare una riga del prospetto e inserire nuovamente la tabella nell'ubicazione richiesta.  

Alcune tabelle di [!INCLUDE[prod_short](includes/prod_short.md)] sono standard e i dati in esse contenuti è probabile che restino invariati nelle diverse implementazioni. Di conseguenza, per consentire al cliente di concentrarsi meglio, è possibile rimuovere queste tabelle dal prospetto dopo che sono state incluse nel pacchetto di configurazione. Una volta aggiunte, le tabelle rimangono parte del pacchetto di configurazione.  

## <a name="to-remove-a-standard-table-in-the-worksheet"></a>Per rimuovere una tabella standard del prospetto  
Dopo aver aggiunto tutte le tabelle necessarie a un pacchetto di configurazione, stabilire quali tabelle non richiederanno l'attenzione del cliente.  
1.  Selezionare le tabelle da eliminare scegliendo l'azione **Elimina**.  

    > [!NOTE]  
    >  Le tabelle rimangono nel pacchetto anche se vengono eliminate dal foglio di lavoro.  

## <a name="to-review-and-customize-existing-database-data"></a>Per esaminare e personalizzare dati nei database esistenti
Quando si crea un pacchetto di configurazione per una soluzione, è possibile visualizzare e personalizzare i dati del database disponibili per adattarli alle esigenze del cliente. Alla tabella del database deve essere associata una pagina.  

## <a name="to-customize-data-in-the-database"></a>Per personalizzare i dati nel database  

1.  Nella pagina **Foglio di lavoro configurazione**, individuare le tabelle di cui si desidera visualizzare o modificare i dati.  

    > [!NOTE]  
    >  Assicurarsi che a ogni tabella sia stato assegnato un ID pagina. Per le tabelle [!INCLUDE[prod_short](includes/prod_short.md)], il valore viene compilato automaticamente. Per le tabelle personalizzate occorre immettere l'ID.  

2.  Scegliere l'azione **Dati database**.  

     Viene visualizzata la pagina di [!INCLUDE[prod_short](includes/prod_short.md)] relativa alla pagina.  

3.  Esaminare le informazioni disponibili. Modificare in base alle esigenze eliminando i record non pertinenti o aggiungendone di nuovi.

## <a name="see-also"></a>Vedere anche  
[Impostare la configurazione della società](admin-set-up-company-configuration.md)  
[Impostazione di una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]