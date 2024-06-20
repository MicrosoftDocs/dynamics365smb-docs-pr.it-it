---
title: Utilizzo di periodi contabili e anni fiscali
description: Informazioni su come utilizzare periodi contabili per stabilire quando la società genera report sulle prestazioni finanziarie.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '100,'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="work-with-accounting-periods-and-fiscal-years"></a>Usare periodi contabili e anni fiscali

I periodi contabili sono periodi di tempo per i quali una società o un'organizzazione crea report sulle prestazioni finanziarie, ad esempio, generando il relativo conto economico o conto patrimoniale. In genere, i periodi contabili fanno riferimento all'anno fiscale della società, che può contenere diversi periodi contabili, ad esempio mesi o trimestri.

Per molte società l'anno fiscale non coincide con l'anno solare, ad esempio quando l'anno fiscale termina il 30 giugno anziché il 31 dicembre. Per le società appena create, l'anno fiscale può anche essere in realtà più lungo di 12 mesi.  

[!INCLUDE[prod_short](includes/prod_short.md)] richiede periodi contabili solo se vuoi chiudere un conto economico o eseguire task di compressione dei dati.

Puoi usare i periodi contabili nei report ad esempio quando esamini i movimenti registrati nella pagina **Saldo/Budget** in cui è possibile specificare l'intervallo tra report. Una delle opzioni che è possibile specificare è la creazione di report per periodo contabile. È inoltre possibile creare un report finanziario che confronta i risultati per periodi contabili differenti.

## <a name="creating-a-new-fiscal-year"></a>Creazione di un nuovo anno fiscale

Puoi creare periodi contabili in blocco manualmente o utilizzando il processo batch **Crea anno fiscale**.

### <a name="how-to-create-accounting-periods-in-bulk"></a>Creazione di periodi contabili in blocco

Utilizzare il processo batch **Crea anno fiscale** per dividere un anno fiscale in periodi di uguale durata.  

1. Scegli l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report") immetti **Periodi contabili**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Crea anno nuovo**.
3. Nel campo **Data inizio**, immettere la data di inizio dell'anno fiscale.  
4. Nel campo **Nr. di periodi**, immettere il numero di periodi contabili in cui dividere l'anno fiscale. È possibile avere fino a 365 periodi in un anno.  
5. Nel campo **Durata periodo**, immettere una durata per ciascun periodo. Gli identificatori di durata sono 1M per un mese, 1T per un trimestre e 1A per un anno.  
6. Selezionare **OK**.  

### <a name="how-to-create-accounting-periods-manually"></a>Creazione manuale di periodi contabili

Se i periodi contabili nell'anno fiscale hanno durate differenti, ad esempio il calendario 4-4-5 utilizzato negli Stati Uniti nel settore del commercio al dettaglio, è possibile impostarli manualmente.  
  
1. Scegli l'icona ![Cerca pagina o report.](media/ui-search/search_small.png "Icona Cerca pagina o report") immetti **Periodi contabili**, quindi scegli il collegamento correlato.  
2. Nel campo **Data inizio**, immettere la data di inizio dell'anno fiscale. Nel campo **Nome** viene visualizzato il nome del mese.  
3. Scegliere la casella di controllo **Nuovo anno fiscale** per indicare che si tratta del primo periodo dell'anno. [!INCLUDE[prod_short](includes/prod_short.md)] utilizzerà questo periodo per determinare i periodi da chiudere a fine anno.
4. Ripetere i passaggi 2 e 3 per ogni altro periodo.  

## <a name="closing-a-fiscal-year"></a>Chiusura di un anno fiscale

La chiusura di un anno fiscale è una delle attività di chiusura dei libri. Dopo la chiusura dell'anno fiscale, le caselle di controllo **Chiuso** e **Data bloccata** sono selezionate per tutti i periodi dell'anno. Non è possibile riaprire un anno o deselezionare le caselle di controllo.

> [!NOTE]  
> È sempre necessario avere almeno un anno fiscale aperto. Quando si chiude un anno, verificare di aver creato un nuovo anno. Da notare inoltre che dopo aver chiuso un anno, non è possibile modificare la data iniziale di quello successivo.

1. Scegli l'icona ![Cerca pagina o report.](media/ui-search/search_small.png "Icona Cerca pagina o report") immetti **Periodi contabili**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Chiudi anno**.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a>Registrazione di movimenti in un anno fiscale chiuso

Anche se l'anno fiscale è stato chiuso, è possibile registrarvi dei movimenti C/G. In questo caso, i movimenti vengono contrassegnati come registrati in un anno fiscale chiuso e viene selezionata la casella di controllo **Mov. anno prec.** Per impostazione predefinita, la casella di controllo non è visualizzata nella pagina ma è possibile aggiungerla. I passaggi successivi consistono nel chiudere il conto economico e nel trasferire i risultati dell'anno a un conto nello stato patrimoniale. Ripetere questi passaggi ogni volta che si registrano movimenti in un anno fiscale chiuso.

## <a name="see-also"></a>Vedere anche

[Chiusura dei registri](year-close-books.md)  
[Chiusura di anni e periodi](year-close-years-periods.md)  
[Come utilizzare i report finanziari](bi-how-work-account-schedule.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
