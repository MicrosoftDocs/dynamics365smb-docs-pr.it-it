---
title: Aggiungere allegati, collegamenti e note nei record | Microsoft Docs
description: Aggiungere un collegamento ipertestuale a un documento o un sito Web in un record specifico, ad esempio, un cliente o un documento.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 447012a66e75e1acf03f2aff1ba6b6922164312f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918565"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Gestire allegati, collegamenti e note in schede e documenti

Nel riquadro Dettaglio informazioni della maggior parte di schede e documenti, è possibile allegare file, aggiungere collegamenti e scrivere note. Per collegamenti e note, è anche possibile eseguire queste operazioni nella pagina elenco selezionando dapprima la riga correlata.

Per visualizzare o modificare uno di questi tipi di informazioni allegate, è necessario dapprima aprire la scheda **Allegati** nel riquadro Dettaglio informazioni. Il numero dietro il titolo della scheda indica quanti file, collegamenti o note allegati esistono per la scheda o il documento.

Allegati, collegamenti e note rimangono allegati durante il passaggio ad altri stati della scheda o del documento, ad esempio da un ordine di vendita in corso a una fattura di vendita registrata. Tuttavia, nessuno dei tipi di allegato viene generato dal sistema, ad esempio durante la stampa o il salvataggio in un file.

> [!NOTE]
> Quando si spedisce e si fattura parzialmente un ordine di vendita o un ordine di acquisto, l'allegato verrà collegato solo alla fattura finale di quell'ordine. Allo stesso modo, quando si fattura utilizzando la funzione Differimenti, l'allegato viene collegato solo ai movimenti C/G per il documento, ma non per i movimenti di differimento.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Per allegare un file a una fattura acquisto
È possibile allegare un qualsiasi tipo di file, contenente testo, immagini o video, a una scheda o a un documento. Ciò è utile, ad esempio, quando si desidera archiviare la fattura di un fornitore come file PDF nella relativa fattura acquisto in [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> I file allegati con la funzione Documenti in entrata non sono inclusi nella scheda **Allegati**. Per ulteriori informazioni, vedere [Documenti in entrata](across-income-documents.md).

La seguente procedura è basata su una fattura di acquisto. I passaggi sono simili per tutti gli altri documenti e schede supportati.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture acquisto** e quindi scegliere il collegamento correlato.
2. Aprire l'ordine di vendita a cui desidera allegare un file.
3. Nel riquadro Dettaglio informazioni, aprire la scheda **Allegati**.
4. Scegliere il valore dietro il campo **Documenti**, ad esempio "0".
5. Nella pagina **Documenti allegati**, nel campo **Allegato**, scegliere l'azione **Seleziona file**.
5. Selezionare un file in qualsiasi posizione, quindi scegliere il pulsante **Apri**.

Il file è ora allegato alla fattura acquisto.

## <a name="to-view-an-attached-file"></a>Per visualizzare il file allegato
1. Nel riquadro Dettaglio informazioni, aprire la scheda **Allegati**.
2. Scegliere il valore dietro il campo **Documenti**, ad esempio "1".
3. Nella pagina **Documenti allegati** scegliere l'azione **Anteprima**.
4. Aprire il file scaricato.

## <a name="to-save-a-document-as-a-pdf-attachment"></a>Per salvare un documento come allegato PDF
Ogni volta che è necessario salvare un documento come file, è possibile utilizzare l'azione **Allega come PDF** per acquisire il contenuto del documento corrente come file PDF allegato al riquadro Dettaglio informazioni del documento. Ciò è utile, ad esempio, quando i documenti seguono più passaggi in un processo, come un processo di vendita o un flusso di lavoro di approvazione, e si desidera fare riferimento a una stampa del passaggio precedente.

La seguente procedura è basata su un ordine di vendita. I passaggi sono simili per tutti i documenti supportati.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.
2. Selezionare un ordine di vendita programmato quindi scegliere l'azione **Allega come PDF**.

Un file PDF con il contenuto corrente dell'ordine cliente viene aggiunto alla scheda **Allegati** nel riquadro Dettaglio informazioni.

## <a name="to-add-a-link-from-an-item-card"></a>Per aggiungere un collegamento da una scheda articolo
È possibile aggiungere un collegamento da una scheda o documento a qualsiasi URL o percorso. Ciò è utile, ad esempio, quando si desidera collegare una scheda articolo al catalogo articoli del fornitore.

La procedura seguente è basata su una scheda articolo. I passaggi sono simili per tutti gli altri documenti e schede supportati.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.
2. Selezionare l'articolo da cui si desidera aggiungere un collegamento, quindi scegliere la scheda **Allegati** nel riquadro Dettaglio informazioni.
3. In **Collegamenti**, scegliere l'icona **+**.
4. Nel campo **Indirizzo collegamento**, immettere il collegamento.

    Il collegamento deve essere un URL Internet o Intranet.

5. Nel campo **Descrizione** immettere le informazioni relative al collegamento.  
6. Scegliere il pulsante **OK**.

Il collegamento è ora allegato alla scheda articolo.  

## <a name="to-write-a-note-on-a-sales-order"></a>Per scrivere una nota in un ordine cliente
È possibile scrivere una nota in un documento o una scheda, ad esempio, per comunicare istruzioni speciali ad altri utenti del documento o della scheda. È possibile includere URL e collegamenti a file nelle note.

> [!NOTE]
> Le note nella scheda **Allegati** non sono correlate alla funzionalità Note interne, utilizzata principalmente per la comunicazione tra utenti del flusso di lavoro. Per ulteriori informazioni, vedere [Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md).

La seguente procedura è basata su un ordine di vendita. I passaggi sono simili per tutti gli altri documenti e schede supportati.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.
2. Selezionare l'ordine di vendita in cui si desidera scrivere una nota, quindi scegliere la scheda **Allegati** nel riquadro Dettaglio informazioni.
3. Nella sezione **Note**, scegliere l'icona **+**.
4. Nel campo **Nota**, scrivere un testo qualsiasi, ad esempio "Questo è un ordine urgente".
5. Scegliere il pulsante **OK**.

La nota è ora allegata all'ordine cliente.

## <a name="see-also"></a>Vedere anche  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Documenti in entrata](across-income-documents.md)  
[Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)  
