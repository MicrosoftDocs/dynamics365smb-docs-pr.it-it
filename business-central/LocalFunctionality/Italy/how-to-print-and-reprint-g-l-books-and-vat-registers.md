---
title: 'Stampare e ristampare libri giornale e registri IVA [IT]'
description: 'Le autorità fiscali richiedono l''invio di due report fiscali che elencano tutti i movimenti contabili registrati, i report Libro giornale - Stampa e Registro IVA - Stampa.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '12141, 12143, 12149, 12150'
ms.date: 11/29/2023
ms.author: bholtorf
ms.custom: bap-template
---
# Stampare e ristampare libri giornale e registri IVA nella versione italiana

Le autorità fiscali richiedono l'invio di due report fiscali che elencano tutti i movimenti contabili registrati, i report **Libro giornale - Stampa** e **Registro IVA - Stampa**. Ogni pagina stampata deve avere un proprio numero progressive e pertanto è necessario aggiornare [!INCLUDE[prod_short](../../includes/prod_short.md)] con il numero dell'ultima pagina stampata prima di eseguire nuovamente il report.  

Di seguito viene descritto come stampare o ristampare il report **Libro giornale - Stampa**, ma gli stessi passaggi si applicano per la stampa o la ristampa del report **Registro IVA - Stampa**.  

## Per stampare il report libro giornale  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Libro giornale - Stampa**, quindi scegli il collegamento correlato.  
2. Compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo report**|Selezionare il tipo di report da creare.<br /><br /> Se si seleziona **Ristampa**, il campo **Da Nr. progressivo** si abilita automaticamente.|  
    |**Data Inizio**|Immettere la data iniziale del periodo a partire dal quale i movimenti registrati vengono visualizzati.|  
    |**Data Fine**|Immettere la data finale del periodo a partire dal quale i movimenti registrati vengono visualizzati.|  
    |**Da Nr. progressivo**|Indica il numero progressivo del report.|  
    |**Stampa informazioni società**|Selezionare per stampare le informazioni della società nel report.<br /><br /> I campi restanti sono popolati in base alla pagina **Informazioni società**.|  

    Quando si stampa il report, viene visualizzato un promemoria per aggiornare la pagina **Setup contabilità generale** con il numero dell'ultima pagina.  

    > [!IMPORTANT]  
    >  [!INCLUDE[prod_short](../../includes/prod_short.md)] non salva automaticamente il numero di pagina quando si esegue il report. Una volta eseguito il report Libro giornale - Stampa o il report Registro IVA - Stampa, è necessario aggiornare [!INCLUDE[prod_short](../../includes/prod_short.md)] con il numero dell'ultima pagina stampata.  

3. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.  

    Per impostare il numero dell'ultima pagina stampata per il report registro IVA, cercare **Registro IVA** e scegliere il collegamento per la pagina in **Categorie reg. IVA**.  

4. Nella Scheda dettaglio **Stampe Fiscali**, nel campo **Ultima pag. libro giornale stampata**, specificare il numero dell'ultima pagina del report **Libro giornale - Stampa** appena stampato.  

Entrambi i report ufficiali possono essere ristampati. Quando si ristampa un report, la prima pagina del report deve avere lo stesso numero di pagina del report stampato la prima volta. Se si desidera ristampare uno di questi report e il numero di pagina non è corretto, modificare le informazioni di ristampa per il report  

Di seguito viene descritto come visualizzare o modificare la numerazione della pagina per le versioni precedentemente stampate del report **Libro giornale - Stampa**, ma gli stessi passaggi si applicano per il report **Registro IVA - Stampa**.  

## Per visualizzare o modificare i numeri di pagina per la ristampa del report libro contabile  

1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Modifica informazioni ristampa libro giornale** . Nella pagina **Informazioni ristampa libro giornale**, il campo **Numero prima pagina** indica il numero della prima pagina dei report precedentemente stampati.  

Quando si aggiorna la pagina **Setup contabilità generale** o **Registri IVA** con il numero dell'ultima pagina del report stampato, accertarsi di specificare il numero di pagina corretto. Se il report ristampato inizia con il numero di pagina non corretto, le autorità fiscali non lo accetteranno. La pagina **Informazioni ristampa libro giornale** e **Informazioni ristampa registro IVA** facilitano l'identificazione del numero corretto di pagina.  

## Vedere anche  

[Funzionalità locale per l'Italia](italy-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]