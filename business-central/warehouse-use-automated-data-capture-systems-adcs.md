---
title: Utilizzare i sistemi di acquisizione automatica dei dati (ADCS, Automatic Data Capture System)
description: Puoi utilizzare il tuo sistema di acquisizione automatica dei dati (ADCS) per registrare il movimento degli articoli nella warehouse e per registrare alcune attività di registrazione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: barcode
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: f1e2c24717d9c481f95d2572ee2e1f50b681b0a0
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442931"
---
# <a name="use-automated-data-capture-systems-adcs"></a>Utilizzare i sistemi di acquisizione automatica dei dati (ADCS, Automatic Data Capture System)

> [!NOTE]
> La soluzione Automated Data Capture System (ADCS) offre una modo per [!INCLUDE[prod_short](includes/prod_short.md)] per comunicare con dispositivi portatili tramite servizi Web. È necessario contattare un partner Microsoft in grado di fornire il collegamento tra il servizio Web e il dispositivo portatile specifico. 

È possibile utilizzare il sistema di acquisizione automatica dei dati (ADCS, Automatic Data Capture System) per registrare il movimento degli articoli nella warehouse e alcune attività di registrazione, ad esempio le rettifiche delle quantità nella registrazioni articoli di warehouse e gli inventari fisici. ADCS in genere comporta la scansione di un codice a barre.

Per utilizzare ADCS, è necessario assegnare a ciascun articolo nella warehouse un identificativo articolo. È inoltre necessario impostare i miniform, le funzioni per l'utilizzo dei palmari, i parametri per lo scambio di dati e specificare le impostazioni per i campi che controllano ADCS. Se è possibile specificare l'utilizzo di ADCS nella scheda Ubicazione di una warehouse.

In base alle esigenze della warehouse, nel setup del miniform per il computer palmare specifico è possibile definire la quantità di informazioni visualizzate. Di seguito sono descritti alcuni esempi di informazioni che è possibile visualizzare:  

- Dati dalle tabelle all'interno di [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio un elenco dei documenti di prelievo che l'utente può selezionare.  
- Informazioni testuali.  
- Messaggi per visualizzare le conferme o gli errori sulle attività eseguite e registrate dall'utente del palmare.

## <a name="to-enable-web-services-for-adcs"></a>Per abilitare i servizi Web per ADCS
Per utilizzare il sistema di acquisizione automatica dei dati, è necessario abilitare il servizio Web ADCS.  

## <a name="to-enable-and-publish-the-adcs-web-service"></a>Per abilitare e pubblicare il servizio Web ADCS  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Servizi Web**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.  
3. Nella pagina **Servizi Web**, inserire le seguenti informazioni su una nuova riga:  

    |Campo|Valore|  
    |---------------------------------|-----------|  
    |**Tipo oggetto**|Codeunit|  
    |**ID oggetto**|7714|  
    |**Nome servizio**|ADCS **Importante:** è necessario denominare il servizio **ADCS**.|  

5. Selezionare la casella di controllo **Pubblicato**.  
6. Scegliere il pulsante **OK**.  

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Per impostare una warehouse per l'utilizzo di ADCS  
Per utilizzare ADCS, è necessario specificare quali ubicazione della warehouse utilizzano la tecnologia.  

> [!NOTE]  
>  È consigliabile non impostare l'utilizzo di ADCS per una warehouse se per la stessa sono impostati anche criteri capacità collocazione.

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni**, e quindi scegli il collegamento correlato.
2.  Selezionare una warehouse dall'elenco per cui si desidera abilitare i sistemi ADCS, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda ubicazione**, selezionare la casella di controllo **Usa ADCS**.  

## <a name="to-specify-an-item-to-use-adcs"></a>Per specificare un articolo per utilizzare il sistema ADCS  
A ogni articolo di warehouse che si desidera utilizzare con ADCS deve essere assegnato un codice identificativo per collegarlo al numero dell'articolo. Ad esempio, è possibile utilizzare il codice a barre dell'articolo come codice identificativo. Un articolo può anche avere più codici identificativo. Può essere utile qualora un articolo sia disponibile in diverse unità di misura, ad esempio pezzi e pallet. In questo caso, assegnare un codice identificativo a ognuno.    

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.  
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

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Utenti ADCS**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3.  Nel campo **Nome** immettere un nome per l'utente. Il nome non può includere più di 20 caratteri, inclusi gli spazi.  
4.  Immettere una password nel campo **Password**. La password è mascherata.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Per specificare che un impiegato warehouse è un utente ADCS  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Impiegati warehouse**, quindi scegli il collegamento correlato.  
2.  Se necessario, aggiungere un nuovo impiegato warehouse. Per ulteriori informazioni, vedere [Impostare impiegati warehouse](warehouse-how-to-set-up-warehouse-employees.md).  
3.  Scegliere l'azione **Modifica lista**.  
4.  Selezionare un impiegato warehouse dall'elenco. Nel campo **Utente ADCS** fare clic sulla freccia rivolta verso il basso e selezionare il nome di un utente ADCS dall'elenco.  

> [!NOTE]  
>  La warehouse di default per l'impiegato dede utilizzare ADCS.

## <a name="to-create-and-customize-miniforms"></a>Per creare e personalizzare miniform
Utilizzare i miniform per descrivere le informazioni che si desidera visualizzare in un palmare. Ad esempio, è possibile creare miniform per supportare l'attività di warehouse di prelievo articoli. Dopo aver creato un miniform, è possibile aggiungervi funzioni per le azioni comuni effettuate dall'utente con i palmari, ad esempio spostarsi su o giù di una riga.  

> [!NOTE] 
> Per implementare o modificare la funzionalità di una funzione miniform, è necessario creare una nuova codeunit per il campo **Codeunit per la gestione** per eseguire l'azione o la risposta richiesta. È possibile ottenere ulteriori informazioni sulla funzionalità ADCS esaminando le codeunit, come 7705, 7706, 7712 e 7713.  

### <a name="to-create-a-miniform-for-adcs"></a>Per creare un miniform per ADCS  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Miniform**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3.  Nel campo **Codice** inserire un codice per il miniform. Facoltativamente, è possibile inserire valori in tutti gli altri campi.  

    Selezionare la casella di controllo **Avvia miniform** per indicare che il miniform è il primo form visualizzato dall'utente modifica all'accesso  

4.  Nella Scheda dettaglio **Righe** definire i campi visualizzati nel miniform. L'ordine in cui vengono immesse le righe corrisponde all'ordine di visualizzazione delle righe nel palmare.  

Dopo avere creato un miniform, i passaggi successivi consistono nel creare funzioni e associare funzionalità per i diversi input da tastiera.  

### <a name="to-customize-miniform-functions"></a>Per personalizzare le funzioni del miniform  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Miniform**, quindi scegli il collegamento correlato.  
2.  Selezionare un miniform dalla lista, quindi scegliere l'azione **Modifica**.  
3.  Scegliere l'azione **Funzioni**.  
4.  Nell'elenco a discesa **Codice funzione** selezionare un codice per rappresentare la funzione che si desidera associare al miniform. Ad esempio, è possibile scegliere il pulsante ESC, che associa la funzionalità alla pressione del tasto ESC.  

## <a name="see-also"></a>Vedere anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]