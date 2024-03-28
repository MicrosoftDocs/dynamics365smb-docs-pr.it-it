---
title: Associazione e sincronizzazione (video)
description: La sincronizzazione del mapping della tabella di integrazione consente la sincronizzazione di dati in tutti i record in una tabella in Business Central e in una tabella in Dynamics 365 Sales che sono associate.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'crm, sales, couple, decouple, synchronize'
ms.search.form: '6250,'
ms.service: dynamics-365-business-central
---

# <a name="couple-and-synchronize-records-between-dataverse-and-business-central"></a>Associare e sincronizzare record tra Dataverse e Business Central

In questo argomento viene descritto come associare uno o più record in [!INCLUDE[prod_short](includes/prod_short.md)] a record in Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)]. L'associazione di record consente di visualizzare le infomazioni di Dataverse da [!INCLUDE[prod_short](includes/prod_short.md)] e viceversa. L'associazione consente inoltre di sincronizzare dati tra i record. È possibile associare i record esistenti, oppure creare e associare nuovi record.

> [!NOTE]
> L'associazione e la sincronizzazione dei dati è disponibile solo se l'amministratore di sistema ha creato una connessione tra [!INCLUDE[prod_short](includes/prod_short.md)] e Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)]. Un modo rapido di verificare è di aprire la scheda **Cliente** e di cercare l'azione **Imposta associazione**. Se l'azione è disponibile, le app sono collegate.

## <a name="video-example"></a>Esempio di video

Questo video mostra l'associazione e la sincronizzazione dei dati nel contesto di un'integrazione con [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Per associare un record

1. In [!INCLUDE[prod_short](includes/prod_short.md)], aprire la scheda del record da associare. Ad esempio, la scheda Cliente o Contatto.  

    È inoltre possibile aprire la pagina elenco e selezionare il record che si desidera associare.  

2. Scegliere l'azione **Imposta associazione**.  
3. Compilare i campi e scegliere **OK**.  

## <a name="to-synchronize-a-single-record"></a>Per sincronizzare un singolo record

1. In [!INCLUDE[prod_short](includes/prod_short.md)], aprire la scheda del record da associare. Ad esempio, la scheda Cliente o Contatto.  
2. Scegliere l'azione **Sincronizza adesso**.  
3. Se un record può essere sincronizzato in una direzione, selezionare l'opzione che specifica la direzione di aggiornamento dei dati e scegliere **OK**.  

## <a name="to-synchronize-a-single-record-from-"></a>Per sincronizzare un singolo record da [!INCLUDE[crm_md](includes/crm_md.md)]

1. In [!INCLUDE[crm_md](includes/crm_md.md)], aprire il modulo del record da associare. Ad esempio, la scheda Account o il modulo scheda Contatto.  
2. Scegli l'azione **[!INCLUDE[prod_short](includes/prod_short.md)]** nella barra multifunzione per aprire e associare automaticamente il record.

    > [!Note]
    > È possibile sincronizzare automaticamente un singolo record da [!INCLUDE[crm_md](includes/crm_md.md)] solo quando l'opzione **Sinc. solo record associati** è disabilitata e la direzione di sincronizzazione è impostata su **Bidirezionale** o **Da tabella di integrazione** nella pagina **Mapping tabella integrazione** per il record. Per ulteriori informazioni, vedere [Mappatura delle tabelle e dei campi da sincronizzare](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>Per accoppiare più record usando l'accoppiamento basato sulla corrispondenza

Specifica i dati da sincronizzare per un'entità, come un cliente o un contatto, accoppiando i record in base alle corrispondenze. Raffina le corrispondenze rendendo la ricerca sensibile alle maiuscole e assegnando una priorità per ogni corrispondenza. Se non viene trovata alcuna corrispondenza, si può anche specificare che si vuole creare l'entità in Dataverse. Per maggiori informazioni, vedi [Personalizzare l'accoppiamento basato sulla corrispondenza](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

> [!NOTE]
> Il processo di associazione basata su corrispondenza ignora i record che sono già stati abbinati. Per includere questi record quando esegui l'associazione basata su corrispondenza, annulla l'associazione dei record e riprova. Per saperne di più sull'annullamento dell'associazione dei record, vai a [Annullare l'associazione di record](#uncoupling-records).

1. In [!INCLUDE[prod_short](includes/prod_short.md)], aprire la pagina elenco per il record, ad esempio le pagine elenco Clienti o Contatti.
2. scegli l'azione **Accoppiamento basato su corrispondenza** .
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>Per sincronizzare più record

1. In [!INCLUDE[prod_short](includes/prod_short.md)], apri la pagina elenco per il record, ad esempio le pagine Clienti o Contatti.  
2. Selezionare i record che si intende sincronizzare, quindi scegliere **Sincronizza adesso**.  
3. Se i record possono essere sincronizzati in una direzione, selezionare l'opzione che specifica la direzione e scegliere **OK**.  

## <a name="bulk-insert-and-couple-records"></a>Inserire e associare record in blocco

Se hai un numero elevato di entità Dataverse che corrispondono ai record in [!INCLUDE [prod_short](includes/prod_short.md)], puoi inserirle e associarle in blocco. Ad esempio, potresti voler inserire e associare in blocco i record quando imposti la sincronizzazione per la prima volta.

Utilizzerai la **procedura guidata per l'importazione di dati** nell'**interfaccia di amministrazione di Microsoft Power Platform**.

L'esempio seguente descrive come inserire e associare in blocco clienti ad account in Dataverse. Utilizza lo stesso processo per altri tipi di entità, come fornitori, articoli e risorse.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , immetti **Clienti**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Apri in Excel** per aprire i dati del cliente in Excel. <!--Don't they need to choose the customers that they want to import to Dataverse?-->
3. Per mappare e importare dati nell'entità **Account** in Dataverse, segui i passaggi descritti in [Importare i dati (tutti i tipi di record ) da più origini](/power-platform/admin/import-data-all-record-types).  

    Se l'entità Account include una colonna **bcbi_companyid**, quando esegui il mapping delle colonne di dati assicurati che l'importazione assegni l'ID azienda appropriato nella colonna per ogni record importato. Per trovare l'ID azienda in [!INCLUDE [prod_short](includes/prod_short.md)], procedi come segue:

    1. Apri la pagina **Mapping tabella integrazione**.
    2. Scegli il mapping **CLIENTE**, quindi scegli **Modifica lista**.
    3. Scorri verso destra e scegli il pulsante di modifica assistita :::image type="icon" source="media/assist-edit-icon.png" border="false"::: nel campo **Filtro tabella integrazione**. Viene visualizzato il filtro predefinito per il mapping dei clienti che contiene l'ID azienda. L'ID azienda è la prima parte del valore. Copia solo quella parte e ignora gli 0. L'esempio seguente evidenzia la parte da copiare.

    :::image type="content" source="media/dataverse-company-id-guid.png" alt-text="Mostra la parte dell'ID azienda da copiare.":::

    > [!NOTE]
    > Non tutti i nomi delle entità Dataverse e i record di Business Central corrispondono. A seconda di ciò che stai importando, verifica che le seguenti colonne contengano i seguenti valori dopo l'importazione:
    >
    >* Per i clienti, la colonna **CustomerTypeCode** deve contenere **Cliente**.
    >* Per i fornitori, la colonna **CustomerTypeCode** deve contenere **Fornitori**. 
    >* Per gli articoli, la colonna **ProductTypeCode** deve contenere **Inventario vendite**.
    >* Per le risorse, la colonna **ProductTypeCode** deve contenere **Servizio**.
 
4. Dopo aver importato i dati nell'ambiente Dataverse, in [!INCLUDE [prod_short](includes/prod_short.md)], segui i passaggi [Per associare più record usando l'associazione basata su corrispondenza](#to-couple-multiple-records-using-match-based-coupling) per associare le entità Dataverse con record [!INCLUDE [prod_short](includes/prod_short.md)]. 

## <a name="uncoupling-records"></a>Annullare l'associazione di record

È possibile annullare l'associazione di uno o più record nelle pagine di elenco o nella pagina **Errori di sincronizzazione dati associati** scegliendo una o più righe e quindi **Elimina associazione**. È inoltre possibile rimuovere tutte le associazioni per una o più mapping di tabella nella pagina **Mapping tabella integrazione**.

## <a name="see-also"></a>Vedi anche

[Utilizzare Dynamics 365 Sales da Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
