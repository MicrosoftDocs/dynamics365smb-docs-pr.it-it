---
title: Importa transazioni retribuzioni
description: 'Per gestire lo stipendio, importare e registrare le transazioni finanziarie dal provider di retribuzioni nella contabilità generale, utilizzando un''estensione di retribuzione quale Ceridian.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Ceridian, Quickbooks, salary'
ms.search.form: '1660, 1661, 36601'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="importing-payroll-transactions"></a>Importazione delle transazioni retribuzioni

Per indicare i pagamenti di stipendio e le transazioni correlate, è necessario importare e registrare in contabilità generale le transazioni finanziarie trasformate dal provider di retribuzioni. A tale scopo, è necessario innanzitutto importare un file che si riceve dal provider di retribuzioni nella pagina **Contabilità generale**. Successivamente si esegue il mapping tra i conti esterni nel file retribuzioni e i conti C/G pertinenti. Infine, si registrano le transazioni retribuzioni in base alla mappatura dei conti.

> [!NOTE]  
> Per utilizzare questa funzione, è necessario installare e abilitare un'estensione per l'importazione delle retribuzioni. Il Registro paga di Ceridian e le estensioni per l'importazione del file retribuzioni di Quickbooks sono preinstallati in [!INCLUDE[prod_short](includes/prod_short.md)]. Per maggiori informazioni, vedere [Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Per importare un file delle retribuzioni

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni COGE**, quindi scegli il collegamento correlato.
2. Nel batch registrazioni COGE appropriato scegliere l'azione **Importa transazioni retribuzioni**. Si apre una guida al setup assistito.
3. Seguire i passaggi indicati nella pagina **Importa transazioni retribuzioni**.

    > [!TIP]  
    >   Nel passaggio relativo alla mappatura dei record di retribuzione esterni ai conti C/G, i mapping eseguiti verranno ricordati che la successiva importazione degli stessi record. In questo modo si risparmia tempo in quando non occorre compilare manualmente il campo **Nr. conto** nelle registrazioni COGE ogni volta che si importano transazioni retribuzioni periodiche.   

    Se si sceglie il pulsante **OK** nella guida al setup assistito, la pagina **Contabilità generale** viene popolata con le righe che rappresentano le transazioni che contiene il file retribuzioni e con i conti appropriati già precompilati nei campi **Conto C/G** in base ai mapping effettuati nella guida.
4. Modificare o registrare le righe delle registrazioni relative a tutte le altre le transazioni della contabilità generale. Per ulteriori informazioni, vedere [Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Vedere anche

[Finanze](finance.md)  
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
