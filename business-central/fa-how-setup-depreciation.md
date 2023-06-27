---
title: Impostare l'ammortamento cespiti
description: Esistono diversi metodi di ammortamento. In Business Central puoi definire il metodo di ammortamento di un cespite nella pagina **Scheda cespite**.
author: edupont04
ms.topic: conceptual
ms.search.keywords: write down
ms.date: 06/28/2021
ms.author: edupont
---

# <a name="set-up-fixed-asset-depreciation" />Impostare l'ammortamento dei cespiti

È possibile utilizzare diversi metodi di ammortamento per la preparazione di estratti conto finanziari e dichiarazioni dei redditi. Molte grandi aziende utilizzano il metodo di ammortamento nei loro estratti conto finanziari, in quanto generalmente consente di dichiarare più utili. Altre aziende invece utilizzano il metodo di ammortamento accelerato ai fini del calcolo dell'imposta sul reddito, ad esempio l'ammortamento a quote decrescenti. Definire il metodo di ammortamento di un cespite con il campo **Metodo ammortamento** nella pagina **Scheda cespite**. Per ulteriori informazioni su ciò che fanno i diversi metodi, vedere [Metodi di ammortamento](fa-depreciation-methods.md).

Impostare i registri beni ammortizzabili, dove si definiscono i diversi modi di calcolo dell'ammortamento per vari tipi di cespiti. Ciascun registro beni ammortizzabili specifica singoli termini di ammortamento. È possibile ad esempio specificare che un cespite debba essere ammortizzato in un periodo di tre anni in un registro e in un periodo di cinque anni in un altro.

Una volta creati i registri beni ammortizzabili necessari, assegnare almeno un registro ad ogni cespite. Un registro assegnato a un cespite è detto registro beni ammortizzabili. È possibile impostare un numero illimitato di registri beni ammortizzabili per un cespite.  

## <a name="to-create-a-depreciation-book" />Per creare un registro beni ammortizzabili

In un registro beni ammortizzabili cespiti, viene specificato come i cespiti vengono ammortizzati. Per facilitare i diversi metodi di ammortamento è possibile impostare diversi registri beni ammortizzabili.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registri beni ammortizzabili**, quindi scegli il collegamento correlato.
2. Nella pagina **Lista registri beni ammortizzabili** scegliere l'azione **Nuovo**.
3. Nella pagina **Scheda registro beni ammortizz.** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > È possibile registrare le transazioni dei cespiti nella pagina **Reg. cespiti in G/L** o **Registraz. cespiti**, a seconda se le transazioni sono per la creazione di rendiconti finanziari o per la gestione interna. Attenersi al seguente passaggio per definire il tipo di registrazione da utilizzare per le diverse attività cespiti per default.
4. Nella Scheda dettaglio **Integrazione**, selezionare la casella di controllo per ogni attività di cespite di cui si desidera registrare le transazioni utilizzando la pagina **Registrazioni cespiti in C/G**.
5. Ripetere i passaggi da 2 a 4 per ogni metodo di ammortamento o di registrazione che si desidera assegnare ai cespiti come registro beni ammortizzabili.

> [!IMPORTANT]
> Scegliere il campo **Usa arrot. in amm. periodico** per arrotondare a numeri interi gli importi di ammortamento periodici calcolati. Ad esempio, se la società utilizza anche l'arrotondamento fattura a numeri interi nella pagina **Setup contabilità generale**, l'arrotondando degli importi di ammortamento ai numeri interi può contribuire a fornire trasparenza.

Se ad esempio viene eseguita la cessione di cespiti laddove il registro beni ammortizzabili non specifica l'arrotondamento, ma il setup contabilità generale della propria società richiede l'arrotondamento, al momento della cessione dei cespiti verrà visualizzato un messaggio di errore che indica che un importo deve essere arrotondato su un movimento contabile.  

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset" />Per assegnare un registro dei beni ammortizzabili a un cespite

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Selezionare il cespite per il quale si desidera impostare un registro beni ammortizzabili.
3. Nella Scheda dettaglio **Registro beni ammortizzabili** compilare i campi secondo le necessità.
4. Se è necessario assegnare più di un registro beni ammortizzabili al cespite, scegliere l'azione **Aggiungi più registri beni ammortizzabili**.
5. In alternativa, scegliere l'azione **Registri beni ammortizz.** per specificare uno o più registri beni ammortizzabili cespiti.

    > [!NOTE]  
    >   Quando si utilizza il metodo di ammortamento manuale, è necessario inserire manualmente l'ammortamento nelle registrazioni cespiti in C/G. La funzione **Calcolo ammortamento** non considera i cespiti che utilizzano il metodo di ammortamento manuale. È possibile utilizzare questo metodo per i cespiti che non sono soggetti ad ammortamento, ad esempio i terreni.

    > [!NOTE]  
    > Quando usi il metodo di ammortamento definito dall'utente, assegni il registro beni ammortizzabili in un modo diverso. Per ulteriori informazioni, vedi [Impostare il metodo di ammortamento definito dall'utente](fa-how-setup-user-defined-depreciation-method.md).

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job" />Per assegnare un registro beni ammortizzabili a più cespiti tramite un processo batch

Se si desidera assegnare un registro beni ammortizzabili a diversi cespiti è possibile utilizzare il processo batch **Crea registro beni amm. cespiti** per creare registri beni ammortizzabili relativi ai cespiti.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Selezionare il cespite per cui si desidera impostare l'assegnazione di un registro beni ammortizzabili, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda registro beni ammortizz.**, scegliere l'azione **Crea registro beni amm. cespiti**.
4. Nella pagina **Crea registro beni amm. cespiti**, compilare il campo **Registro beni ammortizzabili**.
5. Scegliere il campo **Copia da nr. cespite**, quindi selezionare il numero di cespite che si desidera utilizzare come base per la creazione di nuovi registri beni ammortizzabili.

    Se si compila questo campo, nei campi relativi all'ammortamento dei nuovi registri beni ammortizzabili cespiti saranno contenute le stesse informazioni dei corrispondenti campi presenti nel registro dal quale vengono copiati i dati. Se si desidera creare nuovi registri beni ammortizzabili cespiti con i campi relativi all'ammortamento vuoti, lasciare il campo vuoto.  
6. Nella Scheda dettaglio **Cespite** è possibile impostare un filtro per selezionare i cespiti per cui verranno creati i registri beni ammortizzabili cespiti.
7. Scegliere il pulsante **OK**.

## <a name="to-set-up-depreciation-posting-types" />Per impostare i tipi di registrazione dell'ammortamento

Per ogni registro beni ammortizzabili, è necessario impostare le modalità di gestione dei diversi tipi di registrazione in [!INCLUDE[prod_short](includes/prod_short.md)]. ad esempio se la registrazione debba essere in dare o in avere e se il tipo di registrazione debba essere incluso nella base ammortizzabile.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registri beni ammortizzabili**, quindi scegli il collegamento correlato.  
2. Selezionare il registro beni ammortizzabili da impostare, quindi scegliere l'azione **Setup tipo reg. cespiti**.
3. Nella pagina **Setup tipo reg. cespiti** compilare i campi in base alle esigenze.

    > [!NOTE]  
    >   Non è possibile inserire né eliminare la pagina **Setup tipo reg. cespiti**. È possibile tuttavia soltanto modificare le righe esistenti.

Si consiglia di evitare di modificare l’impostazione dei registri beni ammortizzabili per cui siano già stati registrati dei movimenti. Le modifiche non verrebbero infatti applicate ai movimenti già registrati e le statistiche del registro beni ammortizzabili risulterebbero pertanto fuorvianti.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation" />Per impostare modelli e batch di default per l'ammortamento dei cespiti

Per ogni registro beni ammortizzabili viene determinato un setup di default delle definizioni e dei batch. Questi default vengono utilizzati per la duplicazione di righe da una registrazione all'altra, per la creazione di righe di registrazione tramite il processo batch **Calcolo ammortamento** o **Indice cespiti** o per la duplicazione dei costi di acquisizione nelle registrazioni assicurazioni.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registri beni ammortizzabili**, quindi scegli il collegamento correlato.  
2. Selezionare il registro beni ammortizzabili di cui si desidera definire le registrazioni di default, quindi scegliere l'azione **Setup registrazioni cespiti**.  
3. Affinché ogni utente disponga di un'impostazione di default, scegliere il campo **ID utente** da selezionare nella pagina **Utenti**.  
4. Negli altri campi, selezionare la definizione o il batch registrazioni che deve essere utilizzato per default.  

## <a name="fiscal-year-365-days-field-depreciation" />Ammortamento e campo Anno fiscale 365 giorni

Quando viene eseguito il processo batch Calcolo ammortamento, il calcolo è basato normalmente su un anno standard di 360 giorni in cui ciascuno dei 12 mesi ha 30 giorni.

Se selezioni questo campo, il processo batch applica invece il calendario da 365 giorni, in cui ogni mese è calcolato con lo stesso numero di giorni del calendario. L'unica eccezione è febbraio negli anni bisestili, che verrà considerato di 28 giorni anziché di 29. Di conseguenza, anche l'anno bisestile verrà considerato di 365 giorni e non di 366.

## <a name="see-related-microsoft-training" />Vedi il relativo [training Microsoft](/training/modules/configure-depreciation-books/)

## <a name="see-also" />Vedere anche

[Impostazione di cespiti](fa-setup.md)  
[Cespiti](fa-manage.md)  
[Finanze](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
