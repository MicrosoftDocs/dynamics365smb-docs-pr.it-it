---
title: Impostare l&quot;estensione dei codici postali GetAddress.io per il Regno Unito | Documenti Microsoft
description: Descrive come installare e configurare il servizio di codici postali per l&quot;importazione di indirizzi del Regno Unito
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/16/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 29b3b551e3ea8e8dfd52a3846332eec47f9346ce
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="set-up-the-getaddressio-uk-postcodes-extension"></a>Impostare l'estensione dei codici postali GetAddress.io per il Regno Unito
Questa estensione semplifica l'inserimento di indirizzi del Regno Unito per entità come clienti, contatti, dipendenti, fornitori, conti bancari e così via. 

L'estensione dei codici postali GetAddress.io per il Regno Unito utilizza l'API getAddress per trovare gli indirizzi nei codici postali del Regno Unito. Per utilizzare l'estensione, è necessario disporre di un piano e una chiave API per l'API getAddress. Questa operazione è semplice e può essere effettuata quando si imposta l'estensione dei codici postali GetAddress.io per il Regno Unito. I piani sono basati sull'utilizzo, o ciò che viene talvolta detto "chiamate". In questo caso, una chiamata si verifica quando [!INCLUDE[d365fin](includes/d365fin_md.md)] visualizza un elenco di indirizzi per un codice postale. In base alla frequenza con cui si aggiungono gli indirizzi, scegliere il piano migliore in base alle esigenze. Se si sceglie **Ottieni chiave API** nella pagina, si utilizzerà il piano **Gratuito** che consente di aggiungere 20 indirizzi al giorni e che è valido per 30 giorni. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>Per impostare l'estensione dei codici postali GetAddress.io per il Regno Unito 
1. Nell'angolo superiore destro scegliere l'icona **Ricerca della pagina o del report** ![Ricerca della pagina o del report](media/ui-search/search_small.png "icona Ricerca della pagina o del report"), inserire **Connessioni servizio**, quindi scegliere il collegamento correlato.  
2. Nel finestra **Connessioni servizio** scegliere **Servizio CAP UK**.
3. Nella pagina **Configurazione fornitore codice postale** scegliere **Disabilitata**.
4. Nella finestra **Selezione servizio CAP**, scegliere **GetAddress.io**.
5. Nella finestra **Config GetAddress.io** selezionare **Ottieni chiave API** per aprire la pagina **Piani** nel sito Web dell'API getAddress.  

    **Nota**: potrebbe essere necessario disabilitare i pop-up nel browser.
6. Acquistare un piano o scegliere **Ottieni chiave API** e immettere il proprio indirizzo e-mail.
7. Aprire l'e-mail da getAddress.io e copiare la chiave il codice API. La chiave si trova sotto l'intestazione **La tua chiave API**.
8. Nella finestra **Config GetAddress.io** incollare la chiave API nel campo **Chiave API** e scegliere **OK**.
9. Nella pagina **Connessioni servizio** verificare che il campo **Fornitore indirizzo** mostri **GetAddress.io**. Se così, il servizio è abilitato.

## <a name="see-also"></a>Vedi anche
[Utilizzare i codici postali GetAddress.io per il Regno Unito](ui-extensions-getaddressio.md) [Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
