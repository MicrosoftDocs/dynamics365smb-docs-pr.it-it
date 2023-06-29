---
title: Registrare il consumo e l'output per l'ordine di produzione
description: Questo argomento spiega come registrare il consumo e l'output per una riga ordine di produzione rilasciata visualizzata nella pagina Registrazioni di produzione.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5510
ms.date: 03/08/2023
ms.author: edupont
---
# <a name="register-consumption-and-output-for-one-released-production-order-line"></a><a name="register-consumption-and-output-for-one-released-production-order-line"></a>Registrare i consumi e l'output relativi a una singola riga dell'ordine di produzione rilasciato

Questa attività viene eseguita nella pagina **Registrazioni di produzione**. Le registrazioni combinano le funzioni delle registrazioni consumi e registrazioni output separate. Alle registrazioni combinate è possibile accedere direttamente da un ordine di produzione rilasciato. Lo scopo principale è la registrazione manuale del consumo di componenti, la quantità di articoli finali prodotti e il tempo impiegato nelle operazioni. I valori vengono registrati nei movimenti contabili nell'ordine di produzione rilasciato. Le quantità di produzione sono registrate come movimenti contabili articoli negativi, le quantità di output vengono registrate come movimenti contabili positivi e il tempo speso viene registrato come movimento contabile capacità. Tali valori immessi possono essere anche visualizzati nella parte inferiore della finestra come quantità effettive.  

> [!NOTE]  
> Poiché i dati relativi al consumo vengono elaborati insieme ai dati di output, questa registrazione consente di visualizzare le operazioni e i componenti collegati in una struttura di processo logica. I componenti vengono indentati sotto la relativa operazione. Questo richiede l'utilizzo di codice legame tra ciclo e distinta base.  

> [!NOTE]  
> i componenti privi di codici di legame tra ciclo e distinta base vengono elencati per primi in questa finestra.  

## <a name="to-register-consumption-and-output"></a><a name="to-register-consumption-and-output"></a>Per registrare consumi e output

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini di produzione rilasciati**, quindi scegli il collegamento correlato.  
2. Aprire una riga dell'ordine di produzione rilasciato pronta per la registrazione e nella Scheda dettaglio **Righe** scegliere l'azione **Riga**, quindi scegliere l'azione **Registrazioni di produzione**.  

    La pagina **Registrazioni di produzione** si apre mostrando le righe di registrazione per la riga ordine di produzione in base alle pagine **Componenti ordini produzione** e **Cicli ordini produzione** . Le righe hanno origine dalla distinta base di produzione e il ciclo assegnati all'articolo che deve essere prodotto. Per ulteriori informazioni, vedere [Creare distinte base di produzione](production-how-to-create-routings.md).  

3. Nel campo **Data di registrazione** nella parte superiore della registrazione, specificare una data di registrazione da applicare a tutte le righe. Viene immessa come predefinita la data del lavoro. Il campo consente di allineare rapidamente le date di registrazione su tutte le righe, se necessario.  

    > [!NOTE]  
    >  Le date di registrazione immesse nelle singole righe sovrascriveranno questo campo.  

4. Nel campo **Metodo consuntivazione** nella parte superiore della finestra è possibile scegliere di visualizzare anche il consumo e l'output registrati automaticamente in base ai metodi di consuntivazione definiti rispettivamente per l'articolo e per la risorsa. Per ulteriori informazioni vedere [Attivare la consuntivazione dei componenti in base all'output dell'operazione](production-how-to-flush-components-according-to-operation-output.md).

5. Immettere le quantità desiderate nei campi modificabili, specificando consumo e output.  
  
    In ogni tipo di riga di registrazione, vengono visualizzati solo i campi rilevanti. Gli altri sono vuoti e protetti da scrittura.  

    All'apertura della finestra sono già disponibili le quantità da registrare. Se non è stato ancora registrato alcun valore, per impostazione predefinita le quantità previste verranno visualizzate in tutti i campi relativi alla quantità, come specificato nell'ordine di produzione. Se sono state effettuate registrazioni parziali, nei campi relativi alla quantità delle righe verranno visualizzate le quantità residue. Le quantità e gli orari già registrati per l'ordine sono visualizzati nella parte inferiore della finestra come movimenti effettivi.  

    Nel caso delle quantità disponibili nel campo **Quantità di output**, è possibile configurare i valori da preimpostare alla prima apertura della finestra. A tale scopo, aprire la pagina **Setup manufacturing** e utilizzare il campo **Quantità predefinita output** della Scheda dettaglio **Generale**.

    > [!NOTE]  
    >  Si noti che solo la quantità di output nell'ultima riga di registrazione del tipo di movimento **Output** rettificherà il livello di magazzino durante la registrazione. Occorre quindi evitare di contabilizzare le registrazioni, con la quantità di output prevista preimpostata nell'ultima riga di output, fino alla produzione effettiva di tutti gli articoli finali.  

6. Selezionare il campo **Completato** delle righe di output per indicare che l'operazione è terminata. Questo campo è correlato al campo **Stato del ciclo** di una riga cicli di un ordine di produzione.  
7. Scegliere l'azione **Registra** per registrare le quantità immesse, quindi chiudere le registrazioni.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    Se occorre registrare altri valori, le registrazioni li conterranno alla successiva apertura. I valori immessi vengono visualizzati come valori effettivi nella parte inferiore delle registrazioni.  

    > [!NOTE]  
    >   se un articolo in fase di utilizzo viene bloccato, le quantità di consumo per tale articolo non verranno registrate. Se viene bloccato un centro di lavoro o un'area di produzione, le quantità di output o i tempi di processo per la riga di output interessata non verranno registrati.  

    > [!NOTE]  
    > se si chiudono le registrazioni senza contabilizzarle, le modifiche andranno perse.  

> [!WARNING]  
> La pagina **Registrazioni di produzione** non può essere utilizzata simultaneamente da due utenti. Ciò significa che se l'utente 2 apre la pagina e immette i dati quando l'utente 1 già lavora nella pagina, è possibile che l'utente 2 perda i dati quando l'utente 1 chiude la pagina.  

## <a name="see-also"></a><a name="see-also"></a>Vedi anche

[Manufacturing](production-manage-manufacturing.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Pianif.](production-planning.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
