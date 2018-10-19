---
title: Come creare collegamenti a informazioni o programmi esterni nei record | Microsoft Docs
description: Aggiungere un collegamento ipertestuale a un documento o un sito Web in un record specifico, ad esempio, un cliente o un documento.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c2e70ad534a28cf5062e9e54a2dfbd3af6afaa39
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a>Aggiunta di collegamenti a siti Web, documenti o programmi nei record
In un record specifico, ad esempio un cliente, un documento o un ordine di vendita, è possibile aggiungere un collegamento a un sito Web, programma o documento esterno. In alternativa, è possibile creare un collegamento che apre un nuovo messaggio e-mail vuoto a un cliente specifico quando lo si seleziona. La pagina schede di alcuni record, ad esempio schede clienti e fornitori, includono un campo **Home page** in cui è possibile immettere un indirizzo Internet (URL). Per includere altri collegamenti, è possibile utilizzare il metodo descritto in questo articolo.

Un altro esempio potrebbe essere quando si ricevono fatture stampate dai fornitori. È possibile digitalizzarle e salvarle come file .pdf in un sito SharePoint. È quindi possibile creare un collegamento da una fattura di acquisto in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] alla fattura corrispondente in SharePoint. In alternativa, è possibile creare un collegamento da una scheda articolo nella pagina corrispondente nel catalogo in linea del fornitore.

## <a name="to-add-a-link-on-a-record"></a>Per aggiungere un collegamento in un record   

1.  Aprire il record a cui si desidera associare il collegamento, ad esempio una scheda cliente o un ordine di vendita. Se si desidera associare il collegamento a una riga specifica, ad esempio una riga di registrazione, selezionare la riga.  

2.  Scegliere l'azione **Collegamenti** per aprire la finestra **Collegamenti** in cui vengono visualizzati tutti i collegamenti correnti aggiunti al record.

3. Per aggiungere un nuovo collegamento, scegliere **Nuovo**.

4.  Nel campo **Indirizzo collegamento**, immettere

    -   Per creare un collegamento a un file nel computer o in rete, immettere il percorso completo e il nome di file, ad esempio **C:Documenti\Fattura1.doc**.
    -   Per creare un collegamento a un sito Web, immettere l'indirizzo Internet (URL), ad esempio **www.microsoft.com**.
    -   Per creare un collegamento a un sito Web, immettere l'indirizzo Internet (URL), ad esempio **www.microsoft.com**.
    -   Per creare un collegamento a un programma, immettere una stringa specifica per aprire il programma. Ad esempio, per aprire OneNote con una pagina specifica, immettere **onenote:///C:Documenti\test.one**. Oppure per aprire Outlook con una nuova e-mail vuota a un alias specifico, immettere **mailto:testalias**.  

5.  Nel campo **Descrizione** inserire informazioni relative al collegamento.  

6.  Fare clic sul pulsante **Salva**.  

## <a name="to-delete-a-link-from-a-record"></a>Per eliminare un collegamento da un record  

Per eliminare un collegamento, nella finestra **Collegamenti**, è possibile selezionare **…** e quindi **Elimina**.

Se si elimina un unico record, ad esempio una riga dell'ordine di vendita, un ordine di vendita o una scheda cliente, tutti i collegamenti associati al record vengono eliminati. Tuttavia, se si eliminano dei record utilizzando un processo batch, ad esempio **Elimina ord. vendita fatturati**, i collegamenti sono ancora archiviati nel database. Per eliminare i collegamenti dal database, eseguire la codeunit **Elimina collegamenti record orfani**. A tale scopo, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina collegamenti record orfani** e quindi scegliere il collegamento correlato.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  In the **Data Deletion** window, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Vedi anche  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

