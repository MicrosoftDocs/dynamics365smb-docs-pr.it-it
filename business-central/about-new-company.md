---
title: "Creare una nuova società utilizzando una Guida setup assistito | Microsoft Docs"
description: "Creare una nuova società vuota in Business Central è facile. Una Guida setup assistito fornisce le istruzioni nei vari passaggi e consente di importare i dati aziendali esistenti."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 03/02/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: ce2fd5c5027fc54c92bf5ffc63b70c84d81f26b3
ms.contentlocale: it-it
ms.lasthandoff: 05/17/2018

---
# <a name="creating-new-companies-in-included365finincludesd365finmdmd"></a>Creazione di nuove società in [!INCLUDE[d365fin](includes/d365fin_md.md)]
In [!INCLUDE[d365fin](includes/d365fin_md.md)] i contenitori per i dati aziendali che appartengono alla Business Unit o alla persona giuridica vengono indicati con il termine *società*. Quando ci si iscrive a [!INCLUDE[d365fin](includes/d365fin_md.md)], vengono fornite una società dimostrativa e una società vuota denominata *La mia azienda*. Il passaggio tra le aziende è facile; basta accedere a **Impostazioni personali**e passare all'altra azienda. È tuttavia possibile anche creare nuove aziende in [!INCLUDE[d365fin](includes/d365fin_md.md)] in base alle esigenze aziendali. Quando si crea una nuova azienda una guida setup assistito aiuta ad applicare le nozioni di base. Successivamente è possibile importare i dati rilevanti dal sistema legacy o un'altra azienda in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="create-new-company"></a>Crea nuova società
Se si decide di aggiungere un'azienda a [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile utilizzare il setup guidato assistito **Crea nuova società** per iniziare. Il setup guidato è disponibile dalla finestra **Società** e tramite la ricerca nel campo **Società** in **Impostazioni personali**.  

Il setup guidato offre tre modelli:

-   **Valutazione - Dati di esempio**  
    Crea una società che è simile alla società di dimostrazione con i dati di esempio e i dati di setup.  
-   **Produzione - Solo dati setup**  
    Crea una società che è simile a **La mia società** con i dati di setup ma senza i dati di esempio.
-   **Valutazione avanzata - Completa dati di esempio** Crea una società con i dati di setup e dati di esempio completi per tutte le funzionalità, incluse Manufacturing e Gestione assistenza.
-   **Crea nuovo - Senza dati**  
    Crea una società vuota senza dati di setup.  

Se si desidera iniziare in modo semplice con una società nuova, scegliere **Produzione - Solo dati setup** e quindi importare i dati della propria azienda, ad esempio i clienti, gli articoli e i fornitori. Scegliere il modello **Nuovo** se si desidera impostare tutto da zero. È possibile in tal caso utilizzare la guida al setup assistito **Setup società** per istruzioni su come iniziare con i dati di setup di base.  

> [!NOTE]  
>   La creazione di una nuova società richiede alcuni minuti prima che sia possibile accedervi in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lo stato del setup nella finestra **Società** mostra quando la nuova società è pronta. È quindi possibile passare alla nuova società utilizzando **Impostazioni personali**.  

Nella versione di valutazione di 30 giorni è possibile creare un numero qualsiasi di nuove società, ma saranno disponibili solo nel periodo di prova. Per altre informazioni, contattare il partner [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="company-setup"></a>Setup società
Quando si accede a una nuova società, la procedura guidata **Setup società** si avvia automaticamente e fornisce le istruzioni per iniziare. Verranno richieste le informazioni sulla società, ad esempio l'indirizzo, i dati bancari e il metodo di calcolo dei costi di magazzino. Queste informazioni servono da base per molte aree di [!INCLUDE[d365fin](includes/d365fin_md.md)] che non dovranno quindi più essere impostate manualmente un momento successivo.  

L'indirizzo della società, ad esempio, è incluso nelle fatture e in altri documenti e i dati bancari vengono utilizzati per i pagamenti. Il metodo di calcolo dei costi viene utilizzato per calcolare i prezzi, nonché valutare il magazzino.  

Dopo che sono state impostate le informazioni di base, è possibile impostare le restanti aree fondamentali. È a questo punto possibile aggiungere i dati aziendali, ad esempio i clienti e i fornitori. Per ulteriori informazioni, vedere [Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md).  

## <a name="see-also"></a>Vedi anche
[Personalizzazione di Business Central](ui-customizing-overview.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Modifica delle impostazioni di base](ui-change-basic-settings.md)  
[Introduzione](product-get-started.md)  

