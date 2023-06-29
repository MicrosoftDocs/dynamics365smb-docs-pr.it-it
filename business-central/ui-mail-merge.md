---
title: Utilizzo di modelli Word per comunicazioni in blocco
description: I modelli di Word possono semplificare la creazione di massa di documenti personalizzati per entità specifiche.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/01/2023
ms.custom: bap-template
ms.search.forms: '9989, 13,'
---

# <a name="use-word-templates-for-bulk-communication"></a><a name="use-word-templates-for-bulk-communication"></a>Utilizzare modelli Word per comunicazioni in blocco

Microsoft Word i modelli possono rendere più facile la comunicazione di massa in stampa o via e-mail con entità come contatti, clienti e venditori. Ad esempio puoi creare:

* Brochure per avvisare i clienti di una campagna di vendita
* Lettere per informare i venditori su un nuovo criterio di acquisto
* Inviti per attirare i contatti a un evento imminente

> [!NOTE]
> Quando configuri i modelli di Word, è necessario utilizzare un dispositivo con Microsoft Word 2019 o versione successiva e il sistema operativo Windows installato.

## <a name="set-up-the-source-of-data"></a><a name="set-up-the-source-of-data"></a>Configurare l'origine dei dati

Usa le entità in [!INCLUDE[prod_short](includes/prod_short.md)] come origine dei dati per il modello e aggiungi campi unione per personalizzare i documenti per ciascuna entità. I campi di unione provengono dall'entità in [!INCLUDE[prod_short](includes/prod_short.md)]. Quando si applica un modello di Word a un'entità, i dati dei campi di unione vengono inseriti nel documento.

Nella pagina **Modelli di Word** , quando crei un nuovo modello, una guida al setup assistito ti aiuterà nei seguenti passaggi:

1. Scegli una o più entità da utilizzare come origine dei dati. Ad esempio, se desideri creare una brochure per una campagna di vendita, probabilmente sceglieresti l'entità Cliente come origine.
2. Scegli altre entità come origini dei dati aggiuntive. Scopri di più in [Aggiungere voci correlate o non correlate all'entità di origine](#add-entries-that-are-related-or-unrelated-to-the-source-entity).
3. Scaricare un modello vuoto. Puoi impostare subito il modello in Word oppure puoi caricare il modello vuoto e completare la guida. Quando il tuo modello è pronto, usa l'azione **Carica** nella pagina **Modelli di Word** per sostituire il modello vuoto con il modello finito. Per ulteriori informazioni, vedi [Impostare il modello di Word](#set-up-the-template-in-word).
4. Carica il modello che hai preparato.
5. Inserisci un codice e un nome che identifichi il modello.

Quando scarichi un modello, ottieni un file .zip che include due file.

|File  |Descrizione  |
|---------|---------|
|DataSource.xlsx     | Il file di origine dati fornisce i campi che si possono usare nel modello. Non modificare il file di origine dati. Puoi utilizzare solo il modello di Word e i file di origine dati che scarichi ed è necessario archiviare i file nella stessa posizione.     |
|Modello di Word     | Un file .docx da utilizzare come modello.        |

Per informazioni sull'impostazione di un modello in Word, vai a [Impostare il modello in Word](#set-up-the-template-in-word).

## <a name="add-entries-that-are-related-or-unrelated-to-the-source-entity"></a><a name="add-entries-that-are-related-or-unrelated-to-the-source-entity"></a>Aggiungere voci correlate o non correlate all'entità di origine

Puoi anche unire i dati di altre entità. Per aggiungere altre entità come origini dati, utilizza una delle seguenti azioni nella pagina **Modelli di Word** o quando utilizzi la guida al setup assistito:

|Azione  |Descrizione  |
|---------|---------|
|**Aggiungi entità correlata**  | Utilizza i dati di entità correlate all'entità di origine. Ad esempio, per l'entità Cliente puoi anche unire i dati dell'entità Contatto. Le entità sono correlate quando un campo su un'entità fa riferimento a un'altra. Un campo nell'entità Cliente fa riferimento a un campo nell'entità Contatto, quindi sono correlate. Il campo condiviso è spesso un identificatore come un nome, un codice o un ID.        |
|**Aggiungi entità non correlata**| Utilizza i dati di entità non correlate all'entità di origine. Ad esempio, stai creando un modello per l'entità Cliente. Puoi aggiungere l'entità Informazioni sulla società in modo da poter includere i tuoi dettagli di contatto. Un vantaggio fondamentale è che se modifichi le informazioni di contatto, queste vengono automaticamente aggiornate nel tuo modello. Dopo aver aggiunto un'entità non correlata, puoi aggiungere altre entità ad essa correlate.         |

Per le entità non correlate, scegli un record specifico. Poiché puoi aggiungere un'entità solo una volta, per utilizzare un record diverso devi eliminare l'entità e aggiungerla di nuovo con il nuovo record.

È possibile creare una gerarchia di entità, correlate e non correlate. La relazione è mostrata come una struttura ad albero. Il campo **Relazione entità** mostra anche informazioni sulla relazione. Per le entità non correlate, il campo mostra il record che crea la relazione.

Quando aggiungi le entità, utilizza il campo **Prefisso campo** per specificare un prefisso per i nomi dei campi. Successivamente, quando aggiunti i campi al modello, il prefisso può rendere più facile distinguere tra campi dell'entità di origine e di altre entità.

### <a name="select-the-fields-to-include"></a><a name="select-the-fields-to-include"></a>Selezionare i campi da includere

Per ogni entità, puoi specificare i campi che desideri siano disponibili per il modello. Scegli il numero nella colonna **Numero di campi selezionati** per accedere a un elenco di campi disponibili. Nella pagina **Selezione campo** utilizza la casella di controllo **Includi** per specificare i campi. Per alcune entità, i campi utilizzati in genere dalle aziende sono inclusi per impostazione predefinita. È possibile modificare l'elenco, ad esempio, per rimuovere i campi predefiniti. Le tue modifiche si applicano solo al modello su cui stai lavorando.

> [!NOTE]
> Il numero totale di campi che puoi aggiungere da tutte le entità è 250.

> [!NOTE]
> Tu o il tuo partner Microsoft potete aggiungere campi personalizzati alle entità. Quando lo fai, anteponiamo al nome dei campi il prefisso **CALC** e assegniamo il tipo di campo **Calcolato**. Il tipo di campo è chiamato calcolato per indicare che il campo può mostrare diversi tipi di valori, come testo, numeri, date e così via.

## <a name="to-create-a-word-template-in-business-central"></a><a name="to-create-a-word-template-in-business-central"></a>Per creare un modello Word in Business Central

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Modelli di Word**, quindi scegli il collegamento correlato.
2. Scegli **Nuovo**, poi **Crea un modello**, quindi segui i passi della guida all'impostazione assistita. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Si può anche creare un modello direttamente dalla pagina per un'entità scegliendo l'azione **Applica modello Word** per aprire la guida di configurazione assistita, e poi **Nuovo modello**. Quando lo fai, l'origine dei dati viene scelta per te in base al tipo di entità.

## <a name="set-up-the-template-in-word"></a><a name="set-up-the-template-in-word"></a>Impostare il modello in Word

Quando stai impostando un modello in Word, nella scheda **Posta** puoi aggiungere campi di unione scegliendo **Inserisci campo unione**. I campi unione provengono dal file di origine dati che hai scaricato per l'entità. Agiscono come segnaposto che dicono a Word dove mettere le informazioni sull'entità nel documento.

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Aggiungere campi unione in Microsoft Word":::

## <a name="apply-a-template"></a><a name="apply-a-template"></a>Collegare un modello

Quando il tuo modello di Word è pronto, nella pagina **Modelli di Word** puoi scegliere **Applica** per generare i documenti. Quando si applica un modello di Word a un'entità, i dati dei campi di unione vengono inseriti nel documento. Puoi creare un unico documento che contiene sezioni per ogni entità, oppure scegliere **Dividi** per creare un nuovo documento per ogni entità.

Puoi usare l'azione **Applica modelli di Word** per applicare i modelli a uno o più dello stesso tipo di entità, come un cliente, direttamente nel contesto della pagina per l'entità. Ad esempio, le pagine **Cliente** o **Fornitore**.

## <a name="use-word-templates-with-email"></a><a name="use-word-templates-with-email"></a>Usare i modelli di Word con la posta elettronica

È possibile utilizzare i modelli di Word per aggiungere contenuti ai messaggi di posta elettronica. Quando componi un'email, puoi scegliere l'azione **Usa modello Word** per applicare il contenuto di un modello al messaggio. È necessario aver creato i modelli per l'entità. Puoi usare un modello alla volta, e quando passi da un modello all'altro il messaggio cambia per riflettere il contenuto del modello scelto.

Inoltre, puoi usare l'azione **Aggiungi file da modello Word** per allegare il contenuto del modello all'email come file. Il file userà il formato che hai specificato per l'output del modello.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Opzioni per usare il contenuto di un modello Word in un'e-mail":::

## <a name="edit-a-word-template"></a><a name="edit-a-word-template"></a>Modificare un modello di Word

Puoi apportare le seguenti modifiche ai tuoi modelli di Word:

* Per modificare il corpo del testo o unire i campi inclusi nel modello, utilizza l'azione **Scarica**, apporta le modifiche, quindi utilizza l'azione **Carica**
* Per modificare le origini dei dati, utilizza l'azione **Modifica entità correlate**
* Per sostituire il modello Word con un nuovo modello, utilizza l'azione **Carica**
* Eliminare il modello

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Gestione dei layout di report e documenti](ui-manage-report-layouts.md)  
[Configurare la posta elettronica](admin-how-setup-email.md)  
