---
title: Impostare i metodi preferiti per l'invio dei documenti di vendita | Documenti Microsoft
description: "Descrive come impostare il metodo preferito di ogni cliente per l'invio dei documenti di vendita, ad esempio e-mail, PDF, documento elettronico, e così via."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9c73a6ed721cd8deda48cd2fa8a3470733b9f672
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-document-sending-profiles"></a>Impostare profili di invio documenti
È possibile impostare per ogni cliente un metodo preferito di invio documenti di vendita, in modo da non dover selezionare un'opzione di invio ogni volta che si sceglie l'azione **Registra e invia**.

Nella finestra **Profili di invio documenti** si impostano differenti profili di vendita che è possibile selezionare dal campo **Profilo di invio documenti** nella scheda cliente. È possibile selezionare la casella di controllo **Default** per specificare che il profilo di invio documenti è il profilo predefinito per tutti i clienti, eccetto per quelli per i quali il campo **Profilo di invio documenti** è compilato con un altro profilo di invio.

Se si sceglie l'azione **Registra e invia** in un documento di vendita, nella finestra di dialogo **Registra e invia conferma** viene visualizzato anche il profilo di invio utilizzato, cioè quello impostato per il cliente o quello predefinito per tutti i clienti. Nella finestra di dialogo è possibile modificare il profilo di invio per il documento di vendita. Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md).

## <a name="to-set-up-a-document-sending-profile"></a>Per impostare un profilo di invio documenti
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Profili di invio documenti**, quindi scegliere il collegamento correlato.
2. Nella finestra **Profili di invio documenti** scegliere l'azione **Nuovo**.
3. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Per specificare un profilo di invio in una scheda cliente
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Clienti**, quindi scegliere il collegamento correlato.
2. Aprire la scheda del cliente per cui si desidera impostare un profilo di invio.
3. Nel campo **Profilo di invio documenti** selezionare un profilo che è stato impostato secondo la procedura descritta in precedenza.

## <a name="see-also"></a>Vedi anche
[Setup Vendite](sales-setup-sales.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

