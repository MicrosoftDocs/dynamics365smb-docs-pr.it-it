---
title: 'Aggiungere allegati, collegamenti e note nei record'
description: 'Aggiungi un collegamento ipertestuale a un documento o un sito Web in un record specifico, ad esempio, un cliente o un documento.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: how-to
ms.date: 09/15/2023
ms.custom: bap-template
ms-service: dynamics-365-business-central
---
# Gestire allegati, collegamenti e note in schede e documenti

Nella maggior parte delle pagine elenco, delle schede e dei documenti, puoi allegare file, aggiungere collegamenti e scrivere note nella scheda **Allegati** del riquadro **Dettaglio informazioni**. Il numero nel titolo della scheda indica quanti file, collegamenti o note allegati esistono per la scheda o il documento.

Nella scheda dettaglio **Righe** puoi anche utilizzare l'azione **Allegati** per allegare documenti a una riga specifica. Ad esempio, potresti voler allegare specifiche di progettazione a un articolo su una fattura di acquisto.

Allegati, collegamenti e note rimangono allegati alla scheda o al documento mentre viene elaborato in altri stati. Ad esempio, da un ordine di vendita in corso a una fattura di vendita registrata. Tuttavia, nessuno dei tipi di allegato viene generato dal sistema, ad esempio durante la stampa o il salvataggio in un file.

Puoi anche aggiungere allegati alle email che invii da [!INCLUDE [prod_short](includes/prod_short.md)]. Quando invii un'e-mail direttamente da un documento, ad esempio un'offerta di vendita, l'azione **Aggiungi file dal documento di origine** ti consente di scegliere i file da allegare. Puoi scegliere solo i file allegati al documento. Non puoi scegliere i file allegati alle righe.

> [!NOTE]
> Quando si spedisce e si fattura parzialmente una fattura di vendita o un ordine di acquisto, l'allegato verrà collegato solo alla fattura finale di quell'ordine. Allo stesso modo, quando si fattura utilizzando Differimenti, l'allegato viene collegato ai movimenti C/G per il documento, ma non per i movimenti di differimento.
>
> Se elimini un ordine prima che venga fatturato, viene rimosso anche l'allegato.
>
> Quando si usa l'azione **Ottieni righe di carico** da una fattura di acquisto, l'allegato del relativo ordine di acquisto non viene aggiunto alla fattura di acquisto.

## Per allegare un file a una fattura acquisto

È possibile allegare un qualsiasi tipo di file, ad esempio testo, immagini o video, a una scheda, a un documento o a una riga di un documento. Ciò è utile, ad esempio, quando si desidera archiviare la fattura di un fornitore come file PDF nella relativa fattura acquisto in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> I file allegati con la funzione Documenti in entrata non sono inclusi nella scheda **Allegati**. Per ulteriori informazioni, vedi [Documenti in entrata](across-income-documents.md). Lo stesso vale per i file allegati alle righe dei documenti.

La seguente procedura è basata su una fattura di acquisto. I passaggi sono simili per tutti gli altri documenti e schede supportati.

> [!TIP]
> Se il tuo allegato è specifico per una riga di un documento, puoi allegarlo alla riga. Seleziona la riga e scegli l'azione **Allegati**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture di acquisto**, quindi scegli il collegamento correlato.
2. Apri la fattura di acquisto a cui vuoi allegare un file.
3. Nel riquadro **Dettaglio informazioni**, apri la scheda **Allegati**.
4. Scegliere il valore dietro il campo **Documenti**, ad esempio "0".
5. Nella pagina **Documenti allegati**, nel campo **Allegato**.
6. Nella finestra di dialogo **Allega un documento**, esegui una delle seguenti operazioni per allegare un file:

   [!INCLUDE[file-upload](includes/file-upload.md)]

Il file è ora allegato alla fattura acquisto.

## Per visualizzare il file allegato

1. Nel riquadro Dettaglio informazioni, apri la scheda **Allegati**.
2. Scegliere il valore dietro il campo **Documenti**, ad esempio "1".
3. Nella pagina **Documenti allegati** scegliere l'azione **Anteprima**.
4. Aprire il file scaricato.

## Per salvare un documento come allegato PDF

Ogni volta che è necessario salvare un documento come file, è possibile utilizzare l'azione **Allega come PDF** per acquisire il contenuto del documento corrente come file PDF allegato al riquadro Dettaglio informazioni del documento. Ciò è utile, ad esempio, quando i documenti seguono più passaggi in un processo, come un processo di vendita o un flusso di lavoro di approvazione, e si desidera fare riferimento a una stampa del passaggio precedente.

La seguente procedura è basata su un ordine di vendita. I passaggi sono simili per tutti i documenti supportati.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Selezionare un ordine di vendita programmato quindi scegliere l'azione **Allega come PDF**.

Un file PDF con il contenuto corrente dell'ordine cliente viene aggiunto alla scheda **Allegati** nel riquadro Dettaglio informazioni.

## Per aggiungere un collegamento da una scheda articolo

È possibile aggiungere un link da una scheda o da un documento a qualsiasi URL. Ciò è utile, ad esempio, quando si desidera collegare una scheda articolo al catalogo articoli del fornitore.

La procedura seguente è basata su una scheda articolo. I passaggi sono simili per tutti gli altri documenti e schede supportati.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.
2. Selezionare l'articolo da cui si desidera aggiungere un collegamento, quindi scegliere la scheda **Allegati** nel riquadro Dettaglio informazioni.
3. In **Collegamenti**, scegliere l'icona **+**.
4. Nel campo **Indirizzo collegamento**, immettere il collegamento.

    Il collegamento deve essere un URL Internet o Intranet.

5. Nel campo **Descrizione** immettere le informazioni relative al collegamento.  
6. Scegliere il pulsante **OK**.

Il collegamento è ora allegato alla scheda articolo.  

## Per scrivere una nota in un ordine cliente

È possibile scrivere una nota in un documento o una scheda, ad esempio, per comunicare istruzioni speciali ad altri utenti del documento o della scheda. È possibile includere URL e collegamenti a file nelle note.

> [!NOTE]
> Le note nella scheda **Allegati** non sono correlate alla funzionalità Note interne, utilizzata principalmente per la comunicazione tra utenti del flusso di lavoro. Per ulteriori informazioni, vedere [Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md).

La seguente procedura è basata su un ordine di vendita. I passaggi sono simili per tutti gli altri documenti e schede supportati.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Selezionare l'ordine di vendita in cui si desidera scrivere una nota, quindi scegliere la scheda **Allegati** nel riquadro Dettaglio informazioni.
3. Nella sezione **Note**, scegliere l'icona **+**.
4. Nel campo **Nota**, scrivere un testo qualsiasi, ad esempio "Questo è un ordine urgente".
5. Scegli il pulsante **OK**.

La nota è ora allegata all'ordine cliente.

## Vedere anche  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Documenti in entrata](across-income-documents.md)  
[Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
