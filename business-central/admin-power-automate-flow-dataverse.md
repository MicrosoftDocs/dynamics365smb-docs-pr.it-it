---
title: Usare un flusso Power Automate per gli avvisi in caso di modifiche alle entità
description: Scopri come creare un flusso in Power Automate che ti avviserà quando un'entità viene modificata in un ambiente Dataverse.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power Automate, Flow, Dataverse'
ms.search.form: null
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="use-a-power-automate-flow-for-alerts-to-dataverse-entity-changes" />Usare un flusso Power Automate per gli avvisi in caso di modifiche alle entità Dataverse

Gli amministratori possono creare un flusso automatizzato in Power Automate che notifica [!INCLUDE[prod_short](includes/prod_short.md)] in caso di modifiche ai record nell'organizzazione [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

> [!NOTE]
> Questo articolo presuppone che tu abbia collegato la tua versione online di [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE [cds_long_md](includes/cds_long_md.md)] e pianificato la sincronizzazione tra le due applicazioni.

## <a name="import-the-flow-template" />Importare il modello del flusso

> [!TIP]
> Per semplificare l'impostazione del flusso, abbiamo creato un modello che definirà il trigger del flusso e la condizione del flusso per te. Per utilizzare il modello, segui i passaggi in questa sezione. Per creare tu stesso il flusso, salta questa sezione e inizia con i passaggi in [Definire l'attivazione del flusso](#define-the-flow-trigger).

1. Accedi a [Power Automate](https://powerautomate.microsoft.com).
2. Scegli **Modelli**, quindi cerca **Informa Business Central**.

:::image type="content" source="media/power-automate-import-template.png" alt-text="Parole chiave per trovare il modello di flusso.":::
3. Scegli il modello **Informa Business Central quando viene modificato un account**.
4. Continua con i passaggi nella sezione [Informa Business Central di una modifica](#notify-business-central-about-a-change).

## <a name="define-the-flow-trigger" />Definire l'attivazione del flusso

1. Accedi a [Power Automate](https://flow.microsoft.com).
2. Crea un flusso cloud automatizzato che inizia quando una riga per un'entità [!INCLUDE [cds_long_md](includes/cds_long_md.md)] viene aggiunta, modificata o eliminata. Per ulteriori informazioni, vedi [Attivare flussi quando una riga viene aggiunta, modificata o eliminata](/power-automate/dataverse/create-update-delete-trigger). Questo esempio usa l'entità **Conti**. L'immagine seguente mostra le impostazioni per il primo passaggio nella definizione di un trigger di flusso.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Impostazioni per il trigger del flusso":::
3. Utilizzare il pulsante **AssistEdit (...)** nell'angolo in alto a destra per aggiungere la connessione al tuo ambiente [!INCLUDE [cds_long_md](includes/cds_long_md.md)].
4. Scegliere **Mostra opzioni avanzate** e nel campo **Filtra righe**, immetti **customertypecode eq 3** o **customertypecode eq 11** e **statecode eq 0**. Questi valori indicano che il trigger reagirà solo quando vengono apportate modifiche agli account attivi del tipo **cliente** o **fornitore**.

## <a name="define-the-flow-condition" />Definire la condizione del flusso

I dati sono sincronizzati tra [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE [cds_long_md](includes/cds_long_md.md)] tramite un account dell'utente di integrazione. Per ignorare le modifiche apportate dalla sincronizzazione, crea un passaggio di condizione nel flusso che escluda le modifiche apportate dall'account dell'utente di integrazione.  

1. Aggiungere un passaggio **Recupera una riga tramite ID da Dataverse** dopo l'attivazione del flusso con le seguenti impostazioni. Per ulteriori informazioni, vedi [Recupera una riga tramite ID da Dataverse](/power-automate/dataverse/get-row-id).

    1. Nel campo **Nome tabella**, scegli **Utenti**
    2. Nel campo **ID riga**, scegli **Modificato da (valore)** dal trigger del flusso.  

2. Aggiungi un passaggio di condizione le seguenti impostazioni **or** per identificare l'account dell'utente di integrazione.
    1. L'utente **Indirizzo email principale** contiene **contoso.com**
    2. Il **Nome completo** contiene **[!INCLUDE[prod_short](includes/prod_short.md)]**.

3. Aggiungi un controllo Termina per interrompere il flusso se l'entità è stata modificata dall'account utente di integrazione.

L'immagine seguente mostra come definire il trigger di flusso e la condizione di flusso.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Panoramica del trigger del flusso e delle impostazioni delle condizioni":::

## <a name="notify-business-central-about-a-change" />Informare Business Central di una modifica

Se il flusso non viene interrotto dalla condizione, è necessario avvisare [!INCLUDE[prod_short](includes/prod_short.md)] che è stata apportata una modifica. Utilizzare il connettore [!INCLUDE[prod_short](includes/prod_short.md)] per farlo.

1. Nel fork **No** del passaggio della condizione, aggiungi un'azione e cerca **Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]**. Scegli l'icona del connettore nell'elenco.
2. Seleziona l'azione **Crea record (V3)**.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="Impostazioni del connettore [!INCLUDE[prod_short](includes/prod_short.md)]":::

3. Utilizzare il pulsante **Assist-edit (...)** nell'angolo in alto a destra per aggiungere la connessione al tuo ambiente [!INCLUDE[prod_short](includes/prod_short.md)].
4. Una volta connesso, compila i campi **Nome dell'ambiente** e **Nome società**.
5. Nel campo **Categoria API**, immetti **microsoft/dataverse/v1.0**.
6. Nel campo **Nome tabella** immetti **dataverseEntityChanges**.
7. Nel campo **entityName**, immetti **account**.
8. Salva il flusso.

La seguente immagine mostra come dovrebbe essere il flusso.

:::image type="content" source="media/power-automate-flow-dataverse-summary.png" alt-text="Panoramica di tutte le impostazioni per il flusso":::

Quando aggiungi, elimini o modifichi un account nel tuo ambiente [!INCLUDE [cds_long_md](includes/cds_long_md.md)], questo flusso eseguirà le seguenti azioni:

1. Chiama l'ambiente [!INCLUDE[prod_short](includes/prod_short.md)] specificato nel connettore [!INCLUDE[prod_short](includes/prod_short.md)].
2. Utilizza l'API [!INCLUDE[prod_short](includes/prod_short.md)] per inserire un record con **entityName** impostato su **account** nella tabella **Modifica immissione Dataverse**. Questo parametro è il nome esatto dell'entità Dataverse per cui stai creando il flusso.
3. [!INCLUDE[prod_short](includes/prod_short.md)] avvierà il movimento della coda dei lavori che sincronizza i clienti con gli account.

## <a name="see-also" />Vedi anche

[Utilizzare Business Central nei flussi Power Automate](across-how-use-financials-data-source-flow.md)  
[Configurare flussi di lavoro automatizzati](/business-central/dev-itpro/powerplatform/automate-workflows)  
[Integrazione con Microsoft Dataverse](admin-common-data-service.md)  
[Sincronizzazione di dati in Business Central con Microsoft Dataverse](admin-synchronizing-business-central-and-sales.md)  
