---
title: Come impostare ubicazioni per l'utilizzo di collocazioni
description: Le collocazioni rappresentano la struttura di warehouse di base e vengono utilizzate per creare suggerimenti relativi al posizionamento degli articoli.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---

# <a name="set-up-locations-to-use-bins" />Impostare ubicazioni per l'utilizzo di collocazioni

Le collocazioni rappresentano la struttura di base del magazzino e possono suggerire dove riporre gli articoli. Dopo avere creato le collocazioni, puoi definire il contenuto o utilizzarle come collocazioni variabili, ovvero prive di contenuto specifico.

Per utilizzare la funzionalità di collocazione in una ubicazione, attiva l'interruttore **Collocazione obbligatoria** nella scheda **Ubicazione**. Dopo aver attivato l'interruttore, i campi **Codice collocazione** e **Codice zona** sono disponibili nei seguenti documenti:

* Testata carico warehouse
* Righe carico warehouse
* Righe stoccaggio warehouse
* Testata spedizione warehouse
* Righe spedizione warehouse
* Righe stoccaggio warehouse

Nel prossimo passaggio si progetta il flusso degli articoli nell'ubicazione specificando i codici di collocazione nei campi di setup che rappresentano i diversi flussi.  

> [!NOTE]  
> È necessario creare i codici collocazione prima di poterli specificare per l'ubicazione. Per ulteriori informazioni, vedere [Creare collocazioni](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins" />Per impostare un'ubicazione per l'utilizzo di collocazioni

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
2. Selezionare l'ubicazione in cui si desidera utilizzare le collocazioni.  
3. Scegliere l'azione **Modifica**.  
4. Nella Scheda Dettaglio **Warehouse** seleziona la casella di controllo **Collocazione obbligatoria**.  
5. Se non si utilizzano stoccaggi e prelievi guidati per l'ubicazione, nel campo **Selezione collocazioni predefinita** scegli il metodo che [!INCLUDE [prod_short](includes/prod_short.md)] deve utilizzare per assegnare una collocazione predefinita a un articolo.  
6. Aprire la scheda per l'ubicazione per cui si desidera impostare le collocazioni.
7. Nella Scheda dettaglio **Collocazioni**, seleziona le collocazioni da utilizzare come predefinite per i carichi, le spedizioni e le collocazioni di produzione in entrata, in uscita e aperte.  

    I codici delle collocazioni immessi vengono visualizzati automaticamente nelle testate e nelle righe dei vari documenti di warehouse. Le collocazioni di default definiscono le posizioni iniziali e finali degli articoli nella warehouse.  
8. Se usi stoccaggi e prelievi guidati, seleziona una collocazione per le rettifiche di warehouse. Il codice di collocazione nel campo **Codice collocazione rettifica** definisce la collocazione virtuale in cui vengono registrate le eventuali discrepanze rilevate nelle giacenze:

    * Quando si osservano le differenze registrate nelle registrazioni articoli warehouse
    * Differenze calcolate durante la registrazione di un inventario fisico della warehouse  
9. Facoltativo: compila i campi nella scheda dettaglio **Criteri collocazione**. I campi più importanti sono **Criteri capacità collocazione**, **Permettere breakbulk** e **Codice modello stoccaggio**.  
10. Nella Scheda dettaglio **Warehouse** compilare i campi **Tempo gest. uscita da whse.**, **Tempo gest. entrata in whse.** e **Codice calendario base**. Per ulteriori informazioni, vai a [Impostazione dei calendari di base](across-how-to-assign-base-calendars.md).

## <a name="fill-in-the-consumption-bin" />Rifornimento della collocazione di consumo

Il seguente diagramma di flusso illustra in che modo il campo **Cod. collocazione** nelle righe del componente dell'ordine di produzione viene compilato in base al setup dell'ubicazione.

:::image type="content" source="media/binflow.png" alt-text="Campo Codice collocazione nelle righe componenti dell'ordine di produzione.":::

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-bins-location" />Vedi il relativo [training Microsoft](/training/modules/configure-bins-location/)

## <a name="see-also" />Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
