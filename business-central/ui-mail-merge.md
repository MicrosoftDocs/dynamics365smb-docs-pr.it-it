---
title: Utilizzo di modelli Word per comunicazioni in blocco | Microsoft Docs
description: I modelli di Word possono semplificare la creazione di massa di documenti personalizzati per entità specifiche.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'document, mail, merge, Word, template, email'
ms.date: 04/01/2021
ms.author: bholtorf
---

# Utilizzare modelli Word per comunicazioni in blocco
Microsoft Word i modelli possono rendere più facile la comunicazione di massa in stampa o via e-mail con entità come contatti, clienti e venditori. Ad esempio, è possibile creare brochure per avvisare i clienti di una campagna di vendita, lettere per informare i fornitori su una nuova politica di acquisto o inviti per attirare contatti a un evento imminente.

> [!NOTE]
> Puoi utilizzare i modelli di Word solo su dispositivi con Microsoft Word 2019 e il sistema operativo Windows installati.

Puoi usare entità in [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati per il modello e aggiungi campi unione per personalizzare i documenti per ciascuna entità. I campi di unione provengono dall'entità in [!INCLUDE[prod_short](includes/prod_short.md)]. Quando si applica un modello di Word a un'entità, i dati dei campi unione vengono inseriti nel documento.

Nella pagina **Modelli di Word**, quando si crea un nuovo modello si usa una guida di configurazione assistita per scaricare un file ZIP che contiene un DataSource.xlsx e un file modello di Word per l'entità. Il file di origine dati fornisce i campi che si possono usare nel modello. Non modificare il file di origine dati. Puoi utilizzare solo il modello di Word e i file di origine dati che scarichi da [!INCLUDE[prod_short](includes/prod_short.md)] ed è necessario archiviare i file nella stessa posizione.

Dopo aver impostato il modello e aggiunto i campi unione, utilizza la stessa guida per caricare il modello.

## Impostare il modello in Word
Quando stai impostando un modello in Word, nella scheda **Posta** puoi aggiungere campi di unione scegliendo **Inserisci campo unione**. I campi unione disponibili provengono dal file di origine dati che hai scaricato per l'entità. Agiscono come segnaposto che dicono a Word dove mettere le informazioni sull'entità nel documento. 

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Aggiungere campi unione in Microsoft Word":::

## Aggiungere entità correlate
Oltre ad aggiungere dati per l'entità sorgente, cioè l'entità per la quale stai creando il modello, puoi anche unire i dati delle entità che sono collegate ad essa. Per esempio, se l'origine è l'entità Cliente, potete anche unire i dati dei campi dell'entità Cliente/Committente perché entrambe le entità hanno un campo in comune.

Le entità correlate condividono un campo, che spesso è un identificatore come un nome, un codice o un ID, con l'entità sorgente. Quando si imposta un modello ci sono opzioni semplici e avanzate per scegliere le entità correlate:

* Semplice - Aggiungi le relazioni conosciute che [!INCLUDE[prod_short](includes/prod_short.md)] rende disponibili di default.
* Avanzato - Aggiungi relazioni non standard, come quelle che sono state aggiunte da estensioni o personalizzazioni. Questo richiede che conosciate i campi che le entità condividono.

Quando aggiungi un'entità correlata, devi specificare un prefisso per il nome del campo. Quando si aggiungono campi al modello, il prefisso può rendere più facile distinguere tra campi dell'entità sorgente e campi di entità correlate.

## Per creare un modello Word in Business Central
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Modelli di Word**, quindi scegli il collegamento correlato.
2. Scegli **Nuovo**, poi **Crea un modello**, quindi segui i passi della guida all'impostazione assistita. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Si può anche creare un modello direttamente dalla pagina per un'entità scegliendo l'azione **Applica modello Word** per aprire la guida di configurazione assistita, e poi **Nuovo modello**. Quando lo fai, l'origine dei dati viene scelta per te in base al tipo di entità.

## Applicare un modello
Quando il tuo modello di Word è pronto, nella pagina **Modelli di Word** puoi scegliere **Applica** per generare i documenti. Quando si applica un modello di Word a un'entità, i dati dei campi di unione vengono inseriti nel documento. Puoi creare un unico documento che contiene sezioni per ogni entità, oppure scegliere **Dividi** per creare un nuovo documento per ogni entità.

Puoi applicare dei modelli a uno o più dello stesso tipo di entità, come un contatto, direttamente nel contesto di quella pagina, o dalla pagina Modelli di Word per applicare il modello a tutte le entità di quel tipo.

## Usare i modelli di Word con la posta elettronica
È possibile utilizzare i modelli di Word per aggiungere contenuti ai messaggi di posta elettronica. Quando componi un'email, puoi scegliere l'azione **Usa modello Word** per applicare il contenuto di un modello al messaggio. Questo richiede che tu abbia creato uno o più modelli per l'entità. Puoi usare un modello alla volta, e quando passi da un modello all'altro il messaggio cambia per riflettere il contenuto del modello scelto.

Inoltre, puoi usare l'azione **Aggiungi file da modello Word** per allegare il contenuto del modello all'email come file. Il file userà il formato che hai specificato per l'output del modello.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Opzioni per usare il contenuto di un modello Word in un'e-mail":::

## Vedere anche
[Gestione dei layout di report e documenti](ui-manage-report-layouts.md)  
