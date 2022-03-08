---
title: Utilizzare sistemi ADCS (Automated Data Capture Systems) | Documenti Microsoft
description: È possibile utilizzare il sistema di acquisizione automatica dei dati (ADCS, Automatic Data Capture System) per registrare il movimento degli articoli nella warehouse e alcune attività di registrazione, ad esempio le rettifiche delle quantità nella registrazioni articoli di warehouse e gli inventari fisici.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: barcode
ms.date: 11/20/2019
ms.author: sgroespe
ms.openlocfilehash: 209bbe3539fb99c626376149c22c419b4b476608
ms.sourcegitcommit: e97e1df1f5d7b1d8af477580960a8737fcea4d16
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832337"
---
# <a name="use-automated-data-capture-systems-adcs"></a>Utilizzare i sistemi di acquisizione automatica dei dati (ADCS, Automatic Data Capture System)

> [!NOTE]
> Nella versione standard di [!INCLUDE[d365fin](includes/d365fin_md.md)], il sistema ADCS è utilizzato in distribuzioni locali. Tuttavia, un partner Microsoft può utilizzarlo in distribuzioni online utilizzando Power Apps o simili.

È possibile utilizzare il sistema di acquisizione automatica dei dati (ADCS, Automatic Data Capture System) per registrare il movimento degli articoli nella warehouse e alcune attività di registrazione, ad esempio le rettifiche delle quantità nella registrazioni articoli di warehouse e gli inventari fisici. ADCS in genere comporta la scansione di un codice a barre.

Per utilizzare ADCS, è necessario assegnare a ciascun articolo nella warehouse un identificativo articolo. È inoltre necessario impostare i miniform, le funzioni per l'utilizzo dei palmari, i parametri per lo scambio di dati e specificare le impostazioni per i campi che controllano ADCS. Se è possibile specificare l'utilizzo di ADCS nella scheda Ubicazione di una warehouse.

In base alle esigenze della warehouse, nel setup del miniform per il computer palmare specifico è possibile definire la quantità di informazioni visualizzate. Di seguito sono descritti alcuni esempi di informazioni che è possibile visualizzare:  

- Dati dalle tabelle all'interno di [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio un elenco dei documenti di prelievo che l'utente può selezionare.  
- Informazioni testuali.  
- Messaggi per visualizzare le conferme o gli errori sulle attività eseguite e registrate dall'utente del palmare.

Per ulteriori informazioni, vedere [Configurazione di un sistema di acquisizione automatica dei dati](/dynamics-nav/Configuring-Automated-Data-Capture-System) nella Guida per sviluppatori e professionisti IT.

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Per impostare una warehouse per l'utilizzo di ADCS  
Per utilizzare ADCS, è necessario specificare quali ubicazione della warehouse utilizzano la tecnologia.  

> [!NOTE]  
>  È consigliabile non impostare l'utilizzo di ADCS per una warehouse se per la stessa sono impostati anche criteri capacità collocazione.

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.
2.  Selezionare una warehouse dall'elenco per cui si desidera abilitare i sistemi ADCS, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda ubicazione**, selezionare la casella di controllo **Usa ADCS**.  

## <a name="to-specify-an-item-to-use-adcs"></a>Per specificare un articolo per utilizzare il sistema ADCS  
A ogni articolo di warehouse che si desidera utilizzare con ADCS deve essere assegnato un codice identificativo per collegarlo al numero dell'articolo. Ad esempio, è possibile utilizzare il codice a barre dell'articolo come codice identificativo. Un articolo può anche avere più codici identificativo. Può essere utile qualora un articolo sia disponibile in diverse unità di misura, ad esempio pezzi e pallet. In questo caso, assegnare un codice identificativo a ognuno.    

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.  
2.  Selezionare un articolo dall'elenco che fa parte della soluzione ADCS in uso, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda articolo** scegliere l'azione **Identificativi**.
4. Nella pagina **Identificativi articolo** scegliere l'azione **Nuovo**.
5. Nel campo **Codice**  specificare l'identificativo per l'articolo. Ad esempio, l'identificativo può essere il numero di codice a barre dell'articolo.  

    È inoltre possibile impostare **Cod. variante** e un codice **Unità di misura**.  

6. Se necessario, immettere più codici per ciascun articolo.
7. Scegliere il pulsante **OK**.  
8.  Per rivedere le informazioni, scegliere il campo **Codice identificativo** per aprire la pagina **Identificativi articolo**.

## <a name="to-add-an-adcs-user"></a>Per aggiungere un utente ADCS  
È possibile aggiungere qualsiasi utente come utente di un sistema di acquisizione automatica dei dati (ADCS, Automatic Data Capture System). In questo caso, l'utente deve inoltre immettere una password. In alternativa, è anche possibile fornire una connessione che identifichi l'utente ADCS come impiegato warehouse. La password dell'utente ADCS può essere diversa dalla password dell'utente per l'accesso a Windows. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti ADCS** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3.  Nel campo **Nome** immettere un nome per l'utente. Il nome non può includere più di 20 caratteri, inclusi gli spazi.  
4.  Immettere una password nel campo **Password**. La password è mascherata.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Per specificare che un impiegato warehouse è un utente ADCS  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impiegati warehouse** e quindi scegliere il collegamento correlato.  
2.  Se necessario, aggiungere un nuovo impiegato warehouse. Per ulteriori informazioni, vedere [Impostare impiegati warehouse](warehouse-how-to-set-up-warehouse-employees.md).  
3.  Scegliere l'azione **Modifica lista**.  
4.  Selezionare un impiegato warehouse dall'elenco. Nel campo **Utente ADCS** fare clic sulla freccia rivolta verso il basso e selezionare il nome di un utente ADCS dall'elenco.  

> [!NOTE]  
>  La warehouse di default per l'impiegato dede utilizzare ADCS.

## <a name="to-create-and-customize-miniforms"></a>Per creare e personalizzare miniform
Utilizzare i miniform per descrivere le informazioni che si desidera visualizzare in un palmare. Ad esempio, è possibile creare miniform per supportare l'attività di warehouse di prelievo articoli. Dopo aver creato un miniform, è possibile aggiungervi funzioni per le azioni comuni effettuate dall'utente con i palmari, ad esempio spostarsi su o giù di una riga.  

Per implementare o modificare la funzionalità di una funzione miniform, è necessario creare una nuova codeunit o modificarne una esistente per eseguire l'azione o la risposta richiesta. È possibile ottenere ulteriori informazioni sulla funzionalità ADCS esaminando le codeunit, ad esempio la 7705, ovvero la codeunit di gestione per la funzionalità di accesso. La codeunit 7705 mostra il funzionamento di un miniform di tipo scheda.  

### <a name="to-create-a-miniform-for-adcs"></a>Per creare un miniform per ADCS  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Miniform** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3.  Nel campo **Codice** inserire un codice per il miniform. Facoltativamente, è possibile inserire valori in tutti gli altri campi.  

    Selezionare la casella di controllo **Avvia miniform** per indicare che il miniform è il primo form visualizzato dall'utente modifica all'accesso  

4.  Nella Scheda dettaglio **Righe** definire i campi visualizzati nel miniform. L'ordine in cui vengono immesse le righe corrisponde all'ordine di visualizzazione delle righe nel palmare.  

Dopo avere creato un miniform, i passaggi successivi consistono nel creare funzioni e associare funzionalità per i diversi input da tastiera.  

### <a name="to-add-support-for-a-function-key"></a>Per aggiungere il supporto per un tasto funzione  
1.  Aggiungere codice simile al seguente esempio a file con estensione xsl per il plug-in. Viene creata una funzione per il tasto **F6**. Le informazioni sulla sequenza di tasti possono essere ottenute dal produttore del dispositivo.  
    ```xml  
    <xsl:template match="Function[.='F6']">  
      <Function Key1="27" Key2="91" Key3="49" Key4="55" Key5="126" Key6="0"><xsl:value-of select="."/></Function>  
    </xsl:template>  
    ```  
2.  Nell'ambiente di sviluppo di [!INCLUDE[d365fin](includes/d365fin_md.md)] aprire la tabella 7702 e aggiungere un codice che rappresenti il nuovo tasto. Nell'esempio, creare un tasto denominato **F6**.  
3.  Aggiungere il codice C/AL alla funzione della codeunit specifica del miniform per gestire il tasto funzione.  

### <a name="to-customize-miniform-functions"></a>Per personalizzare le funzioni del miniform  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Miniform** e quindi scegliere il collegamento correlato.  
2.  Selezionare un miniform dalla lista, quindi scegliere l'azione **Modifica**.  
3.  Scegliere l'azione **Funzioni**.  
4.  Nell'elenco a discesa **Codice funzione** selezionare un codice per rappresentare la funzione che si desidera associare al miniform. Ad esempio, è possibile scegliere il pulsante ESC, che associa la funzionalità alla pressione del tasto ESC.  

Nell'ambiente di sviluppo di [!INCLUDE[d365fin](includes/d365fin_md.md)] modificare il codice del campo **Codeunit per la gestione** per creare o modificare il codice in modo che venga eseguita la richiesta o la risposta necessaria.

Per ulteriori informazioni, vedere [Configurazione di un sistema di acquisizione automatica dei dati](/dynamics-nav/Configuring-Automated-Data-Capture-System) nella Guida per sviluppatori e professionisti IT.

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
