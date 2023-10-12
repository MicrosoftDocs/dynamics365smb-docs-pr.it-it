---
title: Pianificare una nuova domanda ordine per ordine
description: 'È possibile eseguire questa attività di pianificazione nella pagina Pianificazione ordini, in cui viene visualizzata tutta la nuova domanda, oltre alle informazioni sulla disponibilità e ai suggerimenti sulla fornitura, inclusa la sostituzione di articoli.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5522, 5524, 5526'
ms.date: 07/29/2021
ms.author: bholtorf
---
# <a name="plan-for-new-demand-order-by-order"></a>Pianificare una nuova domanda ordine per ordine

È possibile eseguire questa attività di pianificazione nella pagina **Pianificazione Ordini**, in cui viene visualizzata tutta la nuova domanda, oltre alle informazioni sulla disponibilità e ai suggerimenti sulla fornitura. In questa finestra sono disponibili la visualizzazione e gli strumenti necessari per una pianificazione efficace della domanda dalle righe di vendita e dalle righe di componenti e per la creazione diretta di diversi tipi di ordini di approvvigionamento.  

È possibile accedere alla pagina **Pianificazione ordini** in due modi: da un ordine che si desidera pianificare in modo specifico oppure in modalità batch per pianificare tutte le nuove domande.  


## <a name="to-plan-for-new-production-order-demand"></a>Per pianificare la domanda di un nuovo ordine di produzione

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini di produzione confermati**, quindi seleziona il collegamento correlato. È possibile effettuare tali passaggi per ordini di produzione pianificati, confermati o rilasciati.
2. Aprire l'ordine di produzione che si desidera pianificare, quindi scegliere l'azione **Pianificazione**.  
3. Nella pagina **Pianificazione ordini** scegliere l'azione **Calcola piano**.  

Le righe di pianificazione appaiono nella pagina in base al filtro di visualizzazione **Domanda produzione**, che consente di mostrare le righe componente non completate di tutti gli ordini di produzione esistenti. Non viene deliberatamente mostrata la domanda solo per l'ordine di produzione selezionato poiché è necessario pianificare un ordine di produzione con una sintesi della domanda relativa a eventuali righe componente precedenti. Le righe di pianificazione relative all'ordine di produzione selezionato vengono espanse.  

## <a name="to-plan-for-any-new-demand"></a>Per pianificare qualunque nuova domanda

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Pianificazione ordini**, quindi scegli il collegamento correlato.  
2. Nella pagina **Pianificazione ordini** scegliere l'azione **Calcola piano**.
3. Fare clic sul pulsante **Espandi** davanti alla data del campo **Data uscita** per visualizzare le righe di pianificazione sottostanti, che rappresentano le righe di domanda con disponibilità insufficiente.  
4. Per ogni riga di pianificazione estesa, ovvero riga di domanda, i valori dei campi relativi alle informazioni sono visualizzati nella parte inferiore della pagina.  

    |Opzione|Description|  
    |----------------------------------|---------------------------------------|  
    |**Qtà in altre ubicazioni**|Mostra se l'articolo esiste in un'altra ubicazione. È quindi possibile cercarlo e selezionarlo.|  
    |**Esistono sostitutivi**|Mostra se viene creato un elemento sostitutivo per l'elemento specificato. È quindi possibile cercarlo e selezionarlo. Si noti che questa funzionalità è applicabile solo ai componenti, ovvero a righe di domanda di tipo **Produzione**.|  
    |**Quantità disponibile**|Mostra la disponibilità totale dell'articolo, cioè, la disponibilità calcolata.|  
    |**Prima data disponibile**|Mostra la data di arrivo di un ordine di approvvigionamento in entrata in grado di coprire la quantità necessaria in corrispondenza di una data successiva a quella di uscita.|  

5. Selezionare nel campo **Sistema di rifornimento** il tipo di ordine di approvvigionamento da creare.  

    Il valore di default corrisponde a quello specificato nella scheda articolo o scheda USK, ma è possibile modificarlo selezionando una delle tre opzioni seguenti:  

    |Opzione|Description|  
    |----------------------------------|---------------------------------------|  
    |**Acquisto**|Crea un ordine di acquisto.|  
    |**Trasferimento**|Crea ordine per trasferimenti.|  
    |**Ordine Produzione**|Crea un ordine di produzione.|  

    Nel campo **Approvvigionamento Da** è necessario selezionare un valore in base al sistema di rifornimento specificato.  

    > [!NOTE]  
    >  Se il campo non viene compilato, verrà visualizzato automaticamente un messaggio di errore durante l'utilizzo della funzione **Crea ordini approvvigionamento** e non verrà creato alcun ordine di approvvigionamento per la riga di pianificazione selezionata. Questo criterio non viene applicato quando il sistema di rifornimento è **Ordine di produzione**.  

6. Nel campo **Approvvigionamento da** è possibile ricercare e selezionare la provenienza dell'approvvigionamento:  

    - Se il sistema di rifornimento è impostato su **Acquisto**, la ricerca sarà effettuata nella pagina **Catalogo articolo fornitori**.  
    - Se il sistema di rifornimento è impostato su **Trasferimento**, la ricerca sarà effettuata nella pagina **Lista ubicazioni**.  

    Se l'articolo è disponibile in un'altra ubicazione, nel campo **Qtà in altre ubicazioni** in basso verrà visualizzato un valore e sarà possibile cercare e selezionare l'ubicazione da cui l'articolo deve essere fornito durante la creazione dell'ordine di trasferimento.  

    Se esiste un articolo sostitutivo per l'articolo richiesto, nel campo **Esistono sostitutivi** verrà visualizzato il valore **Sì** e sarà possibile cercare nella pagina **Movimenti sostituzione articolo** e selezionare l'articolo sostitutivo desiderato.  

    > [!NOTE]  
    > Tieni presente che le sostituzioni non determinano automaticamente la sostituzione di un articolo con un altro articolo, ad esempio durante la creazione di un ordine di vendita o in una distinta base. Invece, sarai avvisato del fatto che un articolo sostitutivo è disponibile.

7. Selezionare la casella di controllo **Impegna** se si desidera impegnare l'ordine di approvvigionamento in fase di creazione e la riga di domanda per cui viene creato. Questo campo è vuoto per impostazione predefinita.  

    > [!NOTE]  
    >  È possibile selezionare solo questa casella di controllo se per l'articolo è stato selezionato il valore **Facoltativo** o **Sempre** nel campo **Impegna** nella scheda articolo relativa.  

8. Nel campo **Qtà da ordinare**, immettere la quantità per l'ordine di approvvigionamento che si sta creando.   
    Il valore di default è quello del campo **Quantità necessaria**. Ma è possibile decidere di ordinare una quantità diversa in base alle condizioni effettive della domanda. Se, ad esempio, nella pagina **Pianificazione ordini** si nota che più righe di domanda indipendenti sono per lo stesso articolo acquistato e la data di scadenza è approssimativamente la stessa, è possibile consolidarle immettendo la quantità totale necessaria nel campo **Qtà da ordinare** di una riga, quindi eliminare le altre righe di pianificazione obsolete per l'articolo.  

9. Nei campi **Data Scadenza** e **Data Ordine** è possibile specificare le date da applicare agli ordini di approvvigionamento creati.  

    L'interazione di questi due campi viene definita in base al campo **Lead time di sicurezza di default**, situato nella pagina **Setup manufacturing**. Per impostazione predefinita il valore di Data Scadenza corrisponde al valore di Data Uscita, ma è possibile modificarlo come desiderato.  

> [!NOTE]  
>  Se si immette una data successiva a quella di uscita, verrà visualizzato un messaggio di avviso.  

## <a name="to-make-supply-orders"></a>Per creare ordini di approvvigionamento

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini di produzione confermati**, quindi seleziona il collegamento correlato. È possibile effettuare tali passaggi per un ordine di produzione pianificato, confermato o rilasciato.  
2. Aprire l'ordine di produzione che si desidera pianificare, quindi scegliere l'azione **Pianificazione**.  
3. Posizionare il cursore nella riga di pianificazione desiderata, quindi scegliere l'azione **Crea ordini**.  
4. Nella pagina **Crea ordini approvvigionamento** , nella Scheda dettaglio **Pianificazione ordini**, campo **Crea ordini per** , selezionare una delle opzioni seguenti.  

    |Opzione|Description|  
    |----------------------------------|---------------------------------------|  
    |**La riga attiva**|Creare ordini di approvvigionamento solo per la riga in cui è posizionato il cursore.|  
    |**L'ordine attivo**|Crea ordini di approvvigionamento per tutte le righe dell'ordine in cui è posizionato il cursore.|  
    |**Tutte le righe**|Consentire la creazione di ordini approvvigionamento per tutte le righe nella pagina **Pianificazione Ordini**.|  

5. Definire nella Scheda dettaglio **Opzioni** il tipo di ordini di approvvigionamento o di righe di richiesta di approvvigionamento da creare.  

    > [!NOTE]  
    >  le impostazioni più recenti definite nella pagina **Crea Ordini Approvvigionamento** verranno salvate con l'ID dell'utente attivo, in modo da consentirne il caricamento alla successiva apertura della pagina.  

6. Scegliere **OK** per consentire al sistema di creare gli ordini di produzione suggeriti o le righe di richiesta di approvvigionamento.  

La pianificazione della domanda non soddisfatta è stata effettuata mediante la creazione di ordini di approvvigionamento specifici. Le informazioni dettagliate sui flussi di lavoro specifici relativi all'utilizzo della pagina **Pianificazione Ordini** dipendono dai criteri interni di ogni società.  

Al termine delle operazioni di pianificazione nella pagina **Pianificazione Ordini**, dopo avere ad esempio definito una modalità alternativa per l'approvvigionamento della quantità, è possibile passare alla creazione di ordini di approvvigionamento per una o più righe di pianificazione.  

> [!NOTE]  
> È possibile che gli ordini di approvvigionamento creati introducano una nuova domanda dipendente, ad esempio relativa a ordini di produzione sottostanti, e che sia quindi necessario scegliere nuovamente **Calcola piano** per individuare tali domande e risolverle prima di passare alle altre righe dell'elenco.  

## <a name="see-also"></a>Vedi anche

<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
[Pianif.](production-planning.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)  
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Registrare nuovi articoli](inventory-how-register-new-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
