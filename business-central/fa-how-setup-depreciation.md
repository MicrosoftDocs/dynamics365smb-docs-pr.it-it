---
title: Impostare l'ammortamento cespiti| Documenti Microsoft
description: Specificare in un registro beni ammortizzabili la modalità di ammortamento o svalutazione dei cespiti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c9eea613db52d327caa1c3d5449864900fc867d1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749271"
---
# <a name="set-up-fixed-asset-depreciation"></a>Impostare l'ammortamento dei cespiti
 È possibile utilizzare diversi metodi di ammortamento per la preparazione di estratti conto finanziari e dichiarazioni dei redditi. Molte grandi aziende utilizzano il metodo di ammortamento nei loro estratti conto finanziari, in quanto generalmente consente di dichiarare più utili. Altre aziende invece utilizzano il metodo di ammortamento accelerato ai fini del calcolo dell'imposta sul reddito, ad esempio l'ammortamento a quote decrescenti. Definire il metodo di ammortamento di un cespite con il campo **Metodo ammortamento** nella pagina **Scheda cespite**. Per ulteriori informazioni su ciò che fanno i diversi metodi, vedere [Metodi di ammortamento](fa-depreciation-methods.md).

 Nei registri beni ammortizzabili si definiscono i diversi modi di calcolo dell'ammortamento per i diversi cespiti. In ogni registro è possibile specificare i singoli termini di ammortamento. È possibile ad esempio specificare che un cespite debba essere ammortizzato in un periodo di tre anni in un registro e in un periodo di cinque anni in un altro.

 Una volta creati i registri beni ammortizzabili necessari, assegnare almeno un registro ad ogni cespite. Un registro assegnato a un cespite è detto registro beni ammortizzabili. È possibile impostare un numero illimitato di registri beni ammortizzabili per un cespite. 

## <a name="to-create-a-depreciation-book"></a>Per creare un registro beni ammortizzabili
In un registro beni ammortizzabili cespiti, viene specificato come i cespiti vengono ammortizzati. Per facilitare i diversi metodi di ammortamento è possibile impostare diversi registri beni ammortizzabili.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registri beni ammortizzabili** e quindi scegliere il collegamento correlato.
2. Nella pagina **Lista registri beni ammortizzabili** scegliere l'azione **Nuovo**.
3. Nella pagina **Scheda registro beni ammortizz.** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   È possibile registrare le transazioni dei cespiti nella pagina **Reg. cespiti in G/L** o **Registraz. cespiti**, a seconda se le transazioni sono per la creazione di rendiconti finanziari o per la gestione interna. Attenersi al seguente passaggio per definire il tipo di registrazione da utilizzare per le diverse attività cespiti per default.
4. Nella Scheda dettaglio **Integrazione**, selezionare la casella di controllo per ogni attività di cespite di cui si desidera registrare le transazioni utilizzando la pagina **Registrazioni cespiti in C/G**.
5. Ripetere i passaggi da 2 a 4 per ogni metodo di ammortamento o di registrazione che si desidera assegnare ai cespiti come registro beni ammortizzabili.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Per assegnare un registro dei beni ammortizzabili a un cespite
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cespiti** e quindi scegliere il collegamento correlato.
2. Selezionare il cespite per il quale si desidera impostare un registro beni ammortizzabili.
3. Nella Scheda dettaglio **Registro beni ammortizzabili** compilare i campi secondo le necessità.
4. Se è necessario assegnare più di un registro beni ammortizzabili al cespite, scegliere l'azione **Aggiungi più registri beni ammortizzabili**.
5. In alternativa, scegliere l'azione **Registri beni ammortizz.** per specificare uno o più registri beni ammortizzabili cespiti.

    > [!NOTE]  
    >   Quando si utilizza il metodo di ammortamento manuale, è necessario inserire manualmente l'ammortamento nelle registrazioni cespiti in C/G. La funzione **Calcolo ammortamento** non considera i cespiti che utilizzano il metodo di ammortamento manuale. È possibile utilizzare questo metodo per i cespiti che non sono soggetti ad ammortamento, ad esempio i terreni.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Per assegnare un registro beni ammortizzabili a più cespiti tramite un processo batch
Se si desidera assegnare un registro beni ammortizzabili a diversi cespiti è possibile utilizzare il processo batch **Crea registro beni amm. cespiti** per creare registri beni ammortizzabili relativi ai cespiti.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cespiti** e quindi scegliere il collegamento correlato.
2. Selezionare il cespite per cui si desidera impostare l'assegnazione di un registro beni ammortizzabili, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda registro beni ammortizz.**, scegliere l'azione **Crea registro beni amm. cespiti**.
4. Nella pagina **Crea registro beni amm. cespiti**, compilare il campo **Registro beni ammortizzabili**.
5. Scegliere il campo **Copia da nr. cespite**, quindi selezionare il numero di cespite che si desidera utilizzare come base per la creazione di nuovi registri beni ammortizzabili.

    Se si compila questo campo, nei campi relativi all'ammortamento dei nuovi registri beni ammortizzabili cespiti saranno contenute le stesse informazioni dei corrispondenti campi presenti nel registro dal quale vengono copiati i dati. Se si desidera creare nuovi registri beni ammortizzabili cespiti con i campi relativi all'ammortamento vuoti, lasciare il campo vuoto.  
6. Nella Scheda dettaglio **Cespite** è possibile impostare un filtro per selezionare i cespiti per cui verranno creati i registri beni ammortizzabili cespiti.
7. Scegliere il pulsante **OK**.

## <a name="to-set-up-depreciation-posting-types"></a>Per impostare i tipi di registrazione dell'ammortamento
Per ogni registro beni ammortizzabili, è necessario impostare le modalità di gestione dei diversi tipi di registrazione in [!INCLUDE[prod_short](includes/prod_short.md)]. ad esempio se la registrazione debba essere in dare o in avere e se il tipo di registrazione debba essere incluso nella base ammortizzabile.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registri beni ammortizzabili** e quindi scegliere il collegamento correlato.  
2. Selezionare il registro beni ammortizzabili da impostare, quindi scegliere l'azione **Setup tipo reg. cespiti**.
3. Nella pagina **Setup tipo reg. cespiti** compilare i campi in base alle esigenze.

    > [!NOTE]  
    >   Non è possibile inserire né eliminare la pagina **Setup tipo reg. cespiti**. È possibile tuttavia soltanto modificare le righe esistenti.

Si consiglia di evitare di modificare l’impostazione dei registri beni ammortizzabili per cui siano già stati registrati dei movimenti. Le modifiche non verrebbero infatti applicate ai movimenti già registrati e le statistiche del registro beni ammortizzabili risulterebbero pertanto fuorvianti.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Per impostare modelli e batch di default per l'ammortamento dei cespiti
Per ogni registro beni ammortizzabili viene determinato un setup di default delle definizioni e dei batch. Questi default vengono utilizzati per la duplicazione di righe da una registrazione all'altra, per la creazione di righe di registrazione tramite il processo batch **Calcolo ammortamento** o **Indice cespiti** o per la duplicazione dei costi di acquisizione nelle registrazioni assicurazioni.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registri beni ammortizzabili** e quindi scegliere il collegamento correlato.  
2. Selezionare il registro beni ammortizzabili di cui si desidera definire le registrazioni di default, quindi scegliere l'azione **Setup registrazioni cespiti**.  
3. Affinché ogni utente disponga di un'impostazione di default, scegliere il campo **ID utente** da selezionare nella pagina **Utenti**.  
4. Negli altri campi, selezionare la definizione o il batch registrazioni che deve essere utilizzato per default.  

## <a name="see-also"></a>Vedi anche
[Impostazione di cespiti](fa-setup.md)  
[Cespiti](fa-manage.md)  
[Finanze](finance.md)  
[Introduzione](product-get-started.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
