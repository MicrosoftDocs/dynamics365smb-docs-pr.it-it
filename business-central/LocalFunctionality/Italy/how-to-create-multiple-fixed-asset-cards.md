---
title: 'Come creare più schede cespite [IT]'
description: In questo argomento viene spiegato come puoi creare automaticamente più schede cespite durante la registrazione delle fatture di acquisto.
services: project-madeira
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/18/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-multiple-fixed-asset-cards-in-the-italian-version"></a>Creare più schede cespite nella versione italiana
Durante la registrazione delle fatture di acquisto è possibile creare automaticamente più schede cespite. Se ad esempio la società acquista 200 computer dello stesso tipo dallo stesso fornitore, non è necessario creare manualmente una scheda cespite per ogni computer, ma tali schede possono essere create automaticamente.  

## <a name="to-create-multiple-fixed-asset-cards"></a>Per creare più schede cespite

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cespiti**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Liste**, quindi l'azione **Cespiti**.  
3.  Nella pagina **Lista cespiti**, scegliere l'azione **Nuovo**.  
4.  Compilare i campi della pagina **Scheda cespite**.  

    Verrà utilizzato il valore del campo **Nr.** quando successivamente si generano i cespiti residui.  

5.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
6.  Creare un nuovo ordine di acquisto o aprire l'ordine di acquisto esistente.  
7.  Espandere la Scheda dettaglio **Righe**.  
8.  Compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo**|Selezionare **Cespite**.|  
    |**Nr.**|Specificare il numero del cespite.<br /><br /> **NOTA:** deve corrispondere al numero di cespite immesso nell'elenco **Cespite**.|  
    |**Nr. di schede cespite**|Specificare il numero di duplicati corrispondente per il cespite.<br /><br /> **NOTA:** durante la registrazione della fattura vengono automaticamente generate schede cespite duplicate, che vengono aggiunte all'elenco di cespiti. L'unica differenza tra le varie schede cespite duplicate è il numero assegnato a ciascun cespite.|  

9. Scegliere il pulsante **OK**.  

## <a name="see-also"></a>Vedere anche
 [Cespiti](../../fa-manage.md)  
 [Cespiti italiani](italian-fixed-assets.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
