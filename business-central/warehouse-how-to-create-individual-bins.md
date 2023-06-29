---
title: Creare collocazioni
description: 'Genera gruppi di collocazioni simili nel foglio di lavoro per la creazione di collocazioni, crea le collocazioni singolarmente nella scheda ubicazione o automaticamente nel foglio di lavoro per la creazione di collocazioni.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7368, 7369, 7370, 7371, 7372, 7373'
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="create-bins"></a><a name="create-bins"></a>Creare collocazioni

Il metodo più efficace per creare le collocazioni della warehouse consiste nel generare gruppi di collocazioni simili nel prospetto di creazione collocazioni. È tuttavia possibile creare le collocazioni singolarmente dalla scheda ubicazione. È inoltre possibile utilizzare una funzione nella pagina **Prospetto creaz. collocazione** per creare automaticamente le collocazioni.  

## <a name="to-create-a-bin-from-the-location-card"></a><a name="to-create-a-bin-from-the-location-card"></a>Per creare una collocazione nella scheda ubicazione

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, e quindi scegli il collegamento correlato.  
2.  Selezionare l'ubicazione da cui si desidera creare una collocazione e scegliere l'azione **Collocazioni**.  
3. Scegliere l'azione **Nuovo**.
4. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="the-dedicated-field"></a><a name="the-dedicated-field"></a>Campo Dedicata

Il campo **Dedicata** nella pagina **Collocazioni** specifica che le quantità nella collocazione sono protette dal prelievo per altre domande. Tuttavia, le quantità nelle collocazioni dedicate possono comunque essere impegnate. Di conseguenza, le quantità nelle collocazioni dedicate sono incluse nel campo **Quantità totale disponibile** della pagina **Impegno**.

La creazione di una collocazione dedicata risulta in una funzionalità simile nelle attività di warehouse di base all'utilizzo di tipi di collocazione, disponibile solo nella gestione warehouse avanzata. Per ulteriori informazioni, vedere [Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md).

### <a name="example"></a><a name="example"></a>Esempio

Un'area di produzione impostata con un codice collocazione nel campo **Cod. coll. art. per produzione**. Le righe componenti di ordini di produzione con il codice collocazione che necessitano di componenti prelevati a priori vengono posizionate in quel punto. Tuttavia, fino a quando i componenti vengono utilizzati da tale collocazione, in seguito alle domande di altri componenti è possibile prelevare o utilizzare questi ultimi da tale collocazione perché sono ancora considerati contenuti della collocazione disponibili. Per verificare che il contenuto della collocazione sia disponibile solo per la domanda di componenti che utilizza la collocazione articoli per produzione, è necessario selezionare il campo **Dedicata** sulla riga per tale codice collocazione.

> [!Caution]
> Gli articoli nelle collocazioni dedicate non sono protetti quando vengono prelevati e utilizzati come componenti di produzione o di assemblaggio tramite la pagina **Prelievo magazzino**. Per ulteriori informazioni, vedere [Prelevare per produzione o assemblaggio in configurazioni di warehouse di base](warehouse-how-to-pick-for-production.md).

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a><a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Per creare singole collocazioni nel prospetto di creazione delle collocazioni

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetto creaz. collocazione**, e seleziona il collegamento correlato.  
2.  In ciascuna riga, compilare i campi necessari per assegnare un nome e caratteristiche specifiche alle collocazioni che si sta creando.  
3.  Scegliere l'azione **Crea collocazioni**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a><a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Per creare collocazioni automaticamente nel prospetto di creazione collocazioni

Prima di avviare la creazione automatica delle collocazioni, è necessario individuare i generi di collocazione essenziali per le operazioni da eseguire, nonché determinare il percorso più efficiente per il flusso degli articoli attraverso la struttura fisica della warehouse.  

> [!NOTE]  
> Dopo aver utilizzato una collocazione, non sarà possibile eliminarla a meno che non sia vuota. Se tuttavia si desidera utilizzare un altro sistema di denominazione delle collocazioni, è possibile utilizzare la registrazione di riclassificazione per trasferire gli articoli in un nuovo sistema di collocazioni. Poiché questo processo viene eseguito manualmente e richiede molto tempo, si consiglia di impostare le collocazioni in modo corretto sin dall'inizio.  

Per utilizzare la pagina **Prospetto creaz. collocazione**, è necessario essere impostato come impiegato warehouse nell'ubicazione in cui si trovano le collocazioni. Per ulteriori informazioni, vedere [Impostare impiegati warehouse](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetto creaz. collocazione**, e quindi seleziona il collegamento correlato.  
2.  Scegliere l'azione **Calcola collocazioni**.
3. Nella pagina **Calcola collocazioni**, nel campo **Codice modello collocazione**, quindi selezionare il modello da utilizzare per le collocazioni che si stanno creando.
4.  Immettere una descrizione per le collocazioni in fase di creazione.  
5.  Per creare i codici di collocazione, compilare i campi **Dal nr.** e **A nr.** delle tre categorie visualizzate nella pagina: **Scaffalatura**, **Sezione** e **Livello**. Il codice di collocazione può contenere un massimo di 20 caratteri.  

    > [!NOTE]  
    >  Il numero di caratteri immesso nei singoli campi per le tre categorie, ad esempio i caratteri immessi nei tre campi **Dal nr.**, più gli eventuali separatori di campo, devono essere 20 o meno.  

     Nel codice è possibile utilizzare lettere per ottenere una combinazione di identificazione alfanumerica, ma in tal caso è necessario immettere le stesse lettere nei campi **Dal nr.** e **A nr.** . È ad esempio possibile definire la parte Scaffalatura del codice come **Dal nr. A01** e **A nr. A10**. L'applicazione non è impostato per la generazione di codici con sequenze di lettere, ad esempio da A01 a F05.  

6.  Se si desidera utilizzare un carattere, ad esempio il trattino (-), per separare le parti del codice collocazione definite nei campi relativi alle categorie, immettere tale carattere nel campo **Separatore Campo**.  
7.  Se si desidera che non venga automaticamente creata una riga per una collocazione già esistente, selezionare il campo **Controllo su collocazione esistente**.  
8. Al termine della compilazione dei campi, scegliere **OK**.

    Verrà automaticamente creata una riga per ciascuna collocazione nel prospetto. A questo punto, è possibile eliminare alcune collocazioni,ad esempio nel caso in cui si disponga di una scaffalatura con un passaggio attraverso i primi due livelli di una coppia di sezioni.  

9. Dopo avere eliminato tutte le collocazioni non necessarie, scegliere l'azione **Crea collocazioni**. Verranno create automaticamente le collocazioni per ciascuna riga del prospetto.  

Ripetere la procedura per un altro gruppo di collocazioni finché non sono state create tutte le collocazioni desiderate per la warehouse.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/create-new-bins/)

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
