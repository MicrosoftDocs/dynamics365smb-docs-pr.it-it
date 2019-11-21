---
title: Creare oggetti XMLport basati su schemi XML | Microsoft Docs
description: Utilizzare gli schemi XML per impostare il framework del servizio di scambio documenti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0d028206d1e17c7a1093cf2b93da02894909deb5
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554448"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a>Utilizzare gli schemi XML per preparare le definizioni di scambio dati
Per abilitare l'importazione/esportazione di dati in file XML attraverso il framework di scambio dati in [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile usare gli schemi XML per definire quali elementi di dati si desidera scambiare con [!INCLUDE[d365fin](includes/d365fin_md.md)]. È possibile effettuare questa attività nella pagina **Visualizzatore schema XML** caricando il file di schema XML, selezionando gli elementi dati pertinenti e quindi inizializzando una definizione di scambio dati o un oggetto XMLport.  

 Dopo avere definito gli elementi dati da includere in base allo schema XML, è possibile utilizzare l'azione **Genera XMLport** per creare l'oggetto XMLport.  

 In alternativa, è possibile utilizzare l'azione **Genera definizione scambio dati** per inizializzare una definizione di scambio di dati in base agli elementi dati selezionati, che poi può essere completata nella struttura di scambio di dati. Viene creato un record nella pagina **Registrazione definizioni di scambio** dove si continua il processo definendo il mapping tra gli elementi del file e i campi in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).  

 In questo argomento sono contenute le seguenti procedure:  

-   Per caricare un file di schema XML  

-   Per selezionare o rimuovere i nodi in uno schema XML  

-   Per generare una definizione di scambio di dati basata su uno schema XML  

-   Per generare un oggetto XMLport per il file basato su uno schema XML  

-   Per importare un oggetto XMLport in Object Designer  

### <a name="to-load-an-xml-schema-file"></a>Per caricare un file di schema XML  

1.  Assicurarsi che il file schema XML pertinente sia disponibile. L'estensione del file è .xsd.  

2.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Schemi XML** e quindi scegliere il collegamento correlato.  

3.  Scegliere l'azione **Nuovo**.  

4.  Compilare i campi come indicato nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Codice**|Specificare un codice per identificare lo Schema XML.|  
    |**Description**|Specificare una descrizione dello Schema XML.|  

     Il campo **Spazio dei nomi di destinazione** specifica lo spazio dei nomi nel file schema XML che è stato caricato dalla riga.  

5.  Scegliere l'azione **Carica schema**, quindi selezionare il file di schema XML.  

     Quando il file viene caricato, i campi rimanenti nella riga vengono compilati con informazioni provenienti dal file e viene selezionata la casella di controllo **Schema caricato**.  

    > [!NOTE]  
    >  La struttura ad albero dello schema XML caricato è compressa per impostazione predefinita. Ogni nodo può essere espanso scegliendo il pulsante **+** accanto al nodo desiderato. Per espandere tutti i nodi, selezionare **Espandi tutto** nella barra multifunzione.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Per selezionare o rimuovere i nodi in uno schema XML  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Visualizzatore schema XML** e quindi scegliere il collegamento correlato.  

2.  Compilare i campi nell'intestazione come descritto nella tabella riportata di seguito.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Codice schema XML**|Specificare il file schema XML che è stato caricato nel passaggio 5 nella sezione "Per caricare un file schema XML".|  
    |**Nuovo nr. XMLport**|Specificare il numero dell'oggetto XMLport che viene creato da questo schema XML quando si sceglie l'azione **Genera XMLport**.|  

     Le righe sono ora compilate con nodi che rappresentano tutti gli elementi nello Schema XML. I nodi per gli elementi obbligatori secondo lo Schema XML vengono selezionati per impostazione predefinita.  

3.  Nella prima riga, nella colonna **Nome nodo**, espandere il nodo **Documento**, quindi espandere gradualmente i nodi sottostanti che si desidera esaminare.  

     In alternativa, fare clic con il pulsante destro del mouse su un nodo, quindi selezionare **Espandi tutto**.  

4.  Scegliere una delle seguenti azioni per modificare quali nodi vengono visualizzati.  

    |**Azione**|Descrizione|  
    |----------------|---------------------------------------|  
    |**Mostra tutto**|Tutti i nodi vengono visualizzati.|  
    |**Nascondi voci non obbligatorie**|Solo i nodi che rappresentano gli articoli richiesti in base allo schema XML vengono visualizzati. Questi nodi sono in genere indicati da un **1** nel campo **MinOccurs**.<br /><br /> Selezionare **Mostra tutto** per stornare la visualizzazione.|  
    |**Nascondi voci non selezionate**|Solo i nodi in cui la casella di controllo **Selezionato** è selezionata vengono visualizzati.<br /><br /> Selezionare **Mostra tutto** per stornare la visualizzazione.|  

5.  Scegliere l'azione **Modifica**.  

6.  Con la casella di controllo **Selezionato** specificare per ciascun nodo se si desidera che l'elemento sia supportato nella definizione di scambio dati per il file della banca SEPA correlato.  

    > [!NOTE]  
    >  Quando si seleziona un nodo figlio obbligatorio, vengono selezionati anche tutti i relativi nodi padre.  

7.  Selezionare l'azione **Seleziona tutti gli elementi obbligatori** per selezionare nuovamente tutti i nodi che rappresentano gli elementi che sono richiesti in base allo Schema XML.  

8.  Selezionare l'azione **Deseleziona tutto** per annullare eventuali selezionare.  

     Il campo **Scelta** specifica che il nodo dispone di due o più nodi di pari livello che fungono da opzioni.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>Per generare una definizione di scambio di dati basata su uno schema XML  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Schemi XML** e quindi scegliere il collegamento correlato.  

2.  Selezionare lo schema XML rilevante e quindi scegliere l'azione **Apri visualizzatore schema XML**.  

3.  Assicurarsi che i nodi pertinenti siano selezionati. Per ulteriori informazioni, vedere la sezione "Per selezionare o rimuovere i nodi in uno schema XML".  

4.  Nella pagina **Visualizzatore schema XML** scegliere l'azione **Genera definizione scambio dati**.  

 Verrà creata una definizione di scambio dati nella pagina **Registrazione definizioni di scambio** che si potrà completare specificando gli elementi del file da mappare con i campi in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
>  È inoltre possibile utilizzare la funzione **Ottieni struttura file** della pagina **Registrazione definizioni di scambio** che utilizza la funzionalità della finestra **Visualizzatore schema XML** per precompilare la Scheda dettaglio **Definizioni colonne**.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>Per generare un oggetto XMLport basato su uno schema XML  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Schemi XML** e quindi scegliere il collegamento correlato.  

2.  Selezionare lo schema XML rilevante e quindi scegliere l'azione **Apri visualizzatore schema XML**.  

3.  Nel campo **Nuovo nr. XMLport** specificare il numero che il nuovo oggetto XMLport riceverà quando sarà generato.  

4.  Assicurarsi che i nodi pertinenti siano selezionati. Per ulteriori informazioni, vedere la sezione "Per selezionare o rimuovere i nodi in uno schema XML".  

5.  Scegliere l'azione **Genera XMLport**, quindi salvare l'oggetto come file con estensione TXT nel percorso appropriato.  

6. Importare il nuovo oggetto XMLport nell'ambiente di sviluppo di [!INCLUDE[d365fin](includes/d365fin_md.md)] e compilarlo.

## <a name="see-also"></a>Vedi anche  
[Impostare le definizioni di scambio dati](across-how-to-set-up-data-exchange-definitions.md)   
[Esportare pagamenti in un file della banca](payables-how-export-payments-bank-file.md)   
[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
[Informazioni sul framework di scambio dati](across-about-the-data-exchange-framework.md)
