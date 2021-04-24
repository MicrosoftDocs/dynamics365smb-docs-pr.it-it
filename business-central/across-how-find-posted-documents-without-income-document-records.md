---
title: Cercare i documenti senza allegati| Documenti Microsoft
Description: È possibile cercare i movimenti di contabilità generale per i documenti di vendita e di acquisto registrati che non presentano documenti elettronici in entrata, quali fatture importate.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b4a72567f470771b8f158f62bd70ef78d41408d6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775999"
---
# <a name="find-posted-documents-without-incoming-document-records"></a>Trovare documenti registrati senza record di documenti in entrata
Nelle pagine **Piano dei conti** e **Movimenti C/G** è possibile utilizzare una funzione di ricerca per trovare movimenti di contabilità generale per documenti di vendita e di acquisto registrati che non hanno record di documenti in entrata e successivamente collegarli centralmente a record esistenti o crearne di nuovi con file di documento allegati.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>Per trovare documenti registrati senza record di documenti in entrata
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti** e quindi scegliere il collegamento correlato.
2. Selezionare una riga relativa a un conto CO/GE per quei movimenti di contabilità generale di cui si desidera vedere i documenti di vendita e di acquisto registrati senza record di documenti in entrata. Quindi scegliere l'azione **Documenti registrati senza documento in entrata**.
3. In alternativa, scegliere l'azione **Movimenti contabili**.
4. Nella pagina **Movimenti C/G**, scegliere l'azione **Documenti registrati senza documenti in entrata**.

Viene visualizzata la pagina **Documenti registrati senza documento in entrata** che mostra i documenti di vendita e di acquisto registrati senza i record di documenti in entrata rappresentati dai movimenti di contabilità generale nel conto COGE per il quale è stata aperta la pagina. La pagina può visualizzare un massimo di 1.000 righe. Per impostazione predefinita, il campo **Filtro data** contiene quindi un filtro che limita la visualizzazione ai movimenti con date di registrazione dall'inizio del periodo contabile alla data del lavoro.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Per connettere i documenti trovati a record di documento in entrata esistenti
1. Nella pagina **Documenti registrati senza documento in entrata** selezionare la riga relativa a un documento registrato che si desidera connettere a un record di documento in entrata esistente, quindi scegliere l'azione **Documenti registrati senza documento in entrata**.
2. Nella pagina **Documenti in entrata** selezionare il record di documento in entrata che si desidera connettere al documento registrato trovato, quindi scegliere **OK**.
3. Nella pagina **Documenti registrati senza documento in entrata**, il record di documento in entrata selezionato è ora connesso al documento registrato, come indicato nel Dettaglio informazioni **File documento in entrata**.

Se nella pagina **Documenti in entrata** non è presente un record di documento in entrata adeguato, è possibile crearlo. Per ulteriori informazioni, vedere [Creare i record di documenti in entrata](across-how-create-income-document-records.md).

## <a name="see-also"></a>Vedi anche
[Elaborare i documenti in entrata](across-process-income-documents.md)  
[Documenti in entrata](across-income-documents.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]