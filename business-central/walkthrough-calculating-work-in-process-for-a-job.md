---
title: 'Procedura dettagliata: Calcolo del valore WIP per un progetto'
description: 'Scopri come tenere traccia di consumo di ore di lavoro del personale, ore macchina, articoli a magazzino e altri tipi di utilizzo durante l''esecuzione di un progetto.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: null
ms.date: 12/13/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Procedura dettagliata: Calcolo del valore WIP per un progetto

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Con un progetto, è possibile pianificare l'impiego delle risorse dell'azienda e tenere traccia dei vari costi connessi all'impiego delle risorse in un progetto specifico. Un progetto implica il consumo di ore di lavoro del personale, ore macchina, articoli a magazzino e altri tipi di utilizzo che devono essere monitorati durante l'esecuzione del progetto. Se un progetto si protrae per lungo tempo, potrebbe essere opportuno trasferire questi costi a un conto WIP (Work in Process, ovvero semilavorati) nel conto patrimoniale fino al completamento del progetto. Sarà possibile riconoscere conti e vendite nel conto economico quando opportuno.  

## Informazioni sulla procedura dettagliata

 In questa procedura dettagliata sono illustrati i task seguenti:  

-   Calcolo del WIP  
-   Selezione di un metodo di calcolo del WIP  
-   Esclusione dal WIP di parte di un progetto.  
-   Registrazione del WIP nella contabilità generale.  
-   Storno di una registrazione WIP  

 In ogni fase della procedura viene calcolato il valore del WIP e le transazioni del progetto sono trasferite alla contabilità generale. Le fasi di calcolo e registrazione sono state separate per consentire all'utente di rivedere i dati e apportarvi modifiche prima di procedere alla registrazione nella contabilità generale. Pertanto, dopo aver eseguito i processi batch di calcolo e prima di effettuare i processi batch di registrazione, è necessario controllare che tutti i dati siano corretti.  

## Ruoli

 Questa procedura dettagliata è svolta da un membro del team (Cinzia Di Marco).  

## Prerequisiti

 Prima di svolgere le attività di questa procedura dettagliata, è necessario installare [!INCLUDE[prod_short](includes/prod_short.md)].  

## Scenario

 Questa procedura dettagliata è incentrata su CRONUS International Ltd., una società che si occupa di progettazione, consulenza e installazione di nuove infrastrutture, ad esempio aule conferenze e uffici, complete di mobilia e accessori. La maggior parte di lavoro in CRONUS è svolto sulla base di un progetto e Cinzia, un membro del team di progetto, utilizza il progetto per avere una panoramica dei progetti in corso avviati da CRONUS e di quelli completati. Una parte del progetto può risultare lunga e può durare mesi. Cinzia può utilizzare un conto WIP per registrare i semilavorati e per tenere traccia dei costi in varie parti del progetto.  

## Calcolo del WIP

 CRONUS ha preso in carico un lungo progetto che si sta estendendo su più periodi contabili. Cinzia, un membro del team di progetto, calcola il WIP per garantire l'accuratezza del rendiconto finanziario della società.  

 Durante la procedura, Cinzia seleziona uno specifico gruppo di task da includere nel calcolo del WIP. Nella pagina **Righe attività di progetto** Cinzia può specificare queste righe nella colonna **WIP-Totale**.  

 Nella seguente tabella vengono illustrate tre opzioni.  

|Campo|Descrizione|  
|-------------------------------------|---------------------------------------|  
|**\<blank\>**|Lasciare vuota se l'attività di progetto fa parte di un gruppo di attività.|  
|**Totale**|Definisce l'intervallo o il gruppo di task incluso nel calcolo di WIP e corrispettivo. Qualsiasi attività di progetto nel gruppo con **Tipo di attività di progetto** impostato su **Registrazione** verrà incluso nel totale WIP, a meno che il relativo campo **WIP-Totale** sia impostato su **Escluso**.|  
|**Escluso**|Si applica solo a un'attività con **Tipo di attività di progetto** impostato su **Registrazione**. Il task non viene incluso in caso di calcolo di WIP e corrispettivo.|  

 Nella seguente procedura dettagliata, Cinzia applica il metodo Valore costo, lo standard della società, per calcolare il WIP. Cinzia specifica la parte del progetto da includere nel calcolo WIP assegnando dei valori WIP-Totale a varie righe di attività di progetto.  

### Per calcolare il WIP  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetto**, quindi scegli il collegamento correlato.  
2. Nell'elenco **Progetti** selezionare il progetto **Chernelli**, quindi scegliere l'azione **Modifica**. Viene visualizzata la Scheda progetto in modalità di modifica.  

     Il WIP può essere calcolato sulla base di valore del costo, valore delle vendite, costo del venduto, percentuale di completamento o contratto completato. Nell'esempio, CRONUS utilizza il metodo Valore costo.  

3. Selezionare il campo **Metodo WIP** della Scheda dettaglio **Registrazione**, quindi **Valore costo**.  
4. Scegliere l'azione **Righe attività di progetto** e impostare i valori elencati di seguito nel campo **WIP-Totale**.  

     Nella seguente tabella vengono illustrati i valori.  

    |Nr. attività di progetto|Campo WIP-Totale|  
    |------------------|----------------------|  
    |1130|Escluso|  
    |1190|Totale|  
    |1210|Escluso|  
    |1310|Escluso|  

5. Scegliere l'azione **WIP**, quindi scegliere l'azione **Calcola WIP**.  
6. Nella pagina **Progetto - Calcola WIP**, si seleziona un progetto per il quale calcolare il WIP. Nella Scheda dettaglio **Progetto** selezionare **Chernelli** nel campo **Nr.** .  
7. Nel campo **Data di registrazione** immettere una data successiva alla data di lavoro.
8. Nel campo **Nr. documento** , immettere **1**. Viene quindi creato un documento a cui è possibile fare riferimento in seguito per la tracciabilità.  
9. Scegliere **OK** per eseguire il processo batch. Viene visualizzato un messaggio. Fare clic sul pulsante **OK** per continuare. Chiudere la pagina **Righe attività di progetto**.  

    > [!NOTE]  
    >  Il messaggio indica che sono presenti avvisi associati al calcolo WIP. Gli avvisi verranno esaminati nella procedura successiva.  

10. Nella pagina **Scheda progetto**, espandere la Scheda dettaglio **WIP e corrispettivo** per vedere i valori calcolati. È inoltre possibile visualizzare la **Data di registrazione WIP** e i valori che sono stati registrati nella contabilità generale, se disponibile.  

 Si noti che il valore **Importo costi ricon.** è 215,60 nella colonna **Da registrare**. Ciò riflette i costi totali di due degli articoli nel gruppo di attività di progetto 1110 a 1130. Il terzo articolo è stato impostato su **Escluso** e quindi non è incluso nel calcolo del WIP.  

### Per esaminare gli avvisi WIP  

1.  Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Pannello di controllo WIP progetto**, quindi scegli il collegamento correlato.  
2.  Selezionare il progetto **Chernelli**, quindi scegliere l'azione **Mostra avvisi**.  
3.  Nella pagina **Avvisi WIP progetto** analizzare l'avviso associato al progetto.  

 Dopo il periodo contabile, Cinzia deve ricalcolare il WIP per includervi il lavoro completato finora.  

### Per ricalcolare il WIP  

1. Nella pagina **Scheda progetto**, scegliere l'azione **Movimenti WIP** per visualizzare il calcolo del WIP.  

     La pagina **Movimenti WIP progetto** riporta gli ultimi movimenti WIP calcolati per un progetto, anche se il WIP non è ancora stato registrato nella contabilità generale.  

2. È possibile utilizzare i passaggi nella procedura relativa a come calcolare il WIP per ricalcolare il WIP. Ogni volta che si ricalcola il WIP, viene creato un movimento nella pagina **Movimenti WIP progetto**.  
3. Chiudere la pagina.  

> [!NOTE]  
> Il WIP e il corrispettivo vengono calcolati ma non vengono registrati nella contabilità generale. A tale scopo, è necessario eseguire il processo batch **Registra WIP in C/G** dopo aver calcolato il WIP e il corrispettivo.

## Registrazione del WIP nella contabilità generale

 Ora che il WIP per il progetto è stato calcolato, è possibile registrarlo nella contabilità generale.  

### Per registrare il WIP nella contabilità generale  

1. Nell'elenco **Progetti** selezionare il progetto **Chernelli**.  
2. Scegliere l'azione **WIP**, quindi scegliere l'azione **Registra WIP in C/G**.  
3. Nella Scheda dettaglio **Progetti** della pagina **Progetto - Registra WIP in C/G** selezionare **Chernelli** nel campo **Nr.** .  
4. Inserire **1** nel campo **Nr. documento storno** della Scheda dettaglio **Opzioni**.  
5. Scegliere **OK** per registrare il WIP nella contabilità generale.  
6. Fare clic sul pulsante **OK** per chiudere la pagina di conferma.  

     Dopo avere completato la registrazione, è possibile visualizzare le informazioni di registrazione nella pagina **Movimenti C/G WIP**.  

7.  Nell'elenco **Progetti** selezionare il progetto **Chernelli**, quindi scegliere l'azione **Movimenti C/G WIP**.  

     Nella pagina **Movimenti C/G WIP progetto** verificare che il WIP sia stato registrato nella contabilità generale.  

8. Chiudere la pagina.  
9. Aprire la pagina **Scheda progetto** per il progetto **Chernelli**.  
10. Nella Scheda dettaglio **WIP e corrispettivo**, si noti che nella colonna **Registrato** il campo **Importo C/G costi ricon.** ora è compilato, il che indica che il WIP è stato correttamente registrato nella contabilità generale.  
11. Scegliere il pulsante **OK** per chiudere la scheda.  

## Storno di una registrazione WIP

 Cinzia si accorge che le attività di progetto escluse dal calcolo del WIP avrebbero dovuto essere calcolate nel WIP. Cinzia può stornare le registrazioni errate senza dover contabilizzare nuove registrazioni WIP.  

### Per stornare una registrazione WIP  

1. Nell'elenco **Progetti** selezionare il progetto **Chernelli**.  
2. Scegliere l'azione **WIP**, quindi scegliere l'azione **Registra WIP in C/G**.  
3. Nella Scheda dettaglio **Progetto** della pagina **Progetto - Registra WIP in C/G** selezionare **Chernelli** nel campo **Nr.** .  
4. Inserire **1** nel campo **Nr. documento storno** della Scheda dettaglio **Opzioni**.  
5. Nel campo **Data registrazione storno**, inserire la data di registrazione originale. I dati dovrebbero essere gli stessi utilizzati per calcolare il WIP la prima volta.  
6. Selezionare la casella di controllo **Storna solo**. In questo modo il WIP precedentemente registrato viene stornato senza una nuova registrazione nella contabilità generale.  
7. Selezionare il pulsante **OK** per eseguire il processo batch e fare clic sul pulsante **OK** per chiudere la pagina di conferma.  
8. Aprire la pagina **Scheda progetto** per il progetto **Chernelli**.  
9. Nella Scheda dettaglio **WIP e corrispettivo** verificare che non vi siano movimenti WIP registrati.  
10. Chiudere questa pagina.  
11. Nell'elenco **Progetti** selezionare il progetto **Chernelli**, scegliere l'azione **WIP**, quindi scegliere l'azione **Movimenti C/G WIP**. I movimenti WIP hanno la casella di controllo **Stornato** selezionata.  
12. Chiudere questa pagina.  
13. Aprire **Righe attività di progetto** per il progetto, includere nel calcolo del WIP le parti del progetto necessarie, ricalcolare il WIP e registrare il nuovo valore nella contabilità generale.  

    > [!NOTE]  
    >  Si supponga che Cinzia abbia calcolato e registrato il WIP per un progetto con date errate. Seguendo il metodo che è stato discusso in precedenza, Cinzia può stornare le registrazioni errate, correggerne le date e registrarle nuovamente nella contabilità generale.  

## Passaggi successivi

 In questa procedura dettagliata sono stati svolti i passaggi del calcolo del WIP in [!INCLUDE[prod_short](includes/prod_short.md)]. In progetti più grandi, potrebbe essere utile trasferire periodicamente i costi a un conto WIP fino al completamento del progetto. In questa procedura dettagliata è stato illustrato come escludere le righe di task dal calcolo. È stato inoltre illustrato quando è necessario ricalcolare. Infine, è stato descritto come registrare il WIP nella contabilità generale. Inoltre è incluso un esempio di come stornare una registrazione WIP nella contabilità generale.  

## Vedere anche

 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  
 [Procedura dettagliata: Gestione dei progetti](walkthrough-managing-projects-with-jobs.md)  
 [Metodi WIP](projects-understanding-wip.md)  
 [Monitoraggio di progressi e performance](projects-how-monitor-progress-performance.md)  
 [Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
