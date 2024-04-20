---
title: Esportare i dati di Business Central in Excel
description: È possibile esportare i report finanziari e i dati di Business Intelligence da Business Central in Excel o aprire i dati di Business Central in Excel.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'analysis, reporting, financial report, business intelligence, BI, Excel'
ms.search.form: 9901
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="export-your-business-data-to-excel"></a>Esportare i dati di Business Central in Excel

Excel è un potente strumento per lavorare con i dati. È possibile aprire qualsiasi lista in Excel da [!INCLUDE[prod_short](includes/prod_short.md)]. Puoi persino modificare i dati in Excel e quindi inviarli di nuovo a [!INCLUDE [prod_short](includes/prod_short.md)]. La stessa funzionalità ti consente di portare facilmente i tuoi dati con te se decidi di annullare l'abbonamento.

## <a name="opening-lists-in-excel"></a>Aprire gli elenchi in Excel

È possibile visualizzare i dati in Excel da qualsiasi registrazione, elenco o foglio di lavoro. Aprire la pagina che si desidera quindi scegliere **Apri in Excel**. Ad esempio, aprire l'elenco dei clienti (cercare **Clienti**) quindi scegliere **Apri in Excel**. Il browser chiederà conferma dell'apertura o del salvataggio della cartella di lavoro di Excel generata.  

> [!NOTE]
> Utilizzare questa opzione se non si desidera apportare modifiche e pubblicare di nuovo tali modifiche su [!INCLUDE[prod_short](includes/prod_short.md)].  

Ogni elenco include alcune colonne. L'esportazione in Excel include tutte le colonne presenti nella visualizzazione corrente. Modifica le colonne aprendo il menu di scelta rapida per una colonna e quindi specificando quali colonne desideri visualizzare. L'elenco delle colonne è diverso per la maggior parte degli elenchi. Le colonne riflettono la struttura nel database che memorizza i tuoi dati. Se non sei sicuro del tipo di dati che contiene una determinata colonna, aggiungilo alla tua visualizzazione. Puoi sempre rimuoverlo.  

### <a name="edit-data-in-excel"></a>Modifica dei dati in Excel

L'esperienza [!INCLUDE[prod_short](includes/prod_short.md)] include un componente aggiuntivo per Excel in modo da poter modificare i dati in Excel. Per ulteriori informazioni, vedere [Analisi dei rendiconti finanziari in Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Esportare i dati in altri sistemi contabili

Se si decide di annullare la sottoscrizione a [!INCLUDE[prod_short](includes/prod_short.md)], è possibile esportare i dati in Excel e averli a disposizione nel sistema finanziario.  

È possibile esportare tutte le pagine, ma potrebbe essere più di quanto effettivamente necessario. Prendere in considerazione di esportare le seguenti pagine essenziali e ricordarsi di aggiungere tutte le colonne come descritto in precedenza:  

* Piano dei conti  
* Clienti  
* Fornitori  
* Banche  
* Articoli  

Se si desidera esportare anche tutte le transazioni finanziarie, ovvero una grande quantità di dati, l'esportazione richiede un tempo superiore. Le transazioni finanziarie sono visualizzate nella pagina **Movimenti C/G**.  

È consigliabile anche esportare i dati dalle pagine seguenti:  

* Movimenti contabili clienti  
* Movimenti contabili fornitori  
* Mov. contabili C/C bancari  
* Mov. contabili articoli  
* Setup registrazioni COGE  
* Cat. reg. clienti  
* Cat. reg. fornitori  
* Cat. reg. articoli  
* Cat. reg. bancarie  
* Budget C/G  
* Movimenti budget C/G  
* Offerte vendita  
* Fatture vendite  
* Fatture di acquisto  
* Contatti  
* Agenti  

> [!NOTE]  
> Se è stata impostata più di uno società in [!INCLUDE[prod_short](includes/prod_short.md)], è necessario esportare i dati relativi a ogni società.

> [!NOTE]
> È necessario disporre di almeno una delle seguenti autorizzazioni per aprire o modificare i dati in Excel:
>
> * Set di autorizzazioni *D365 Azione esportazione Excel*  
> * Autorizzazione di sistema 6110 *Consenti l'azione Esporta in Excel*.  

Per ulteriori informazioni, vedere [Per ottenere una sintesi delle autorizzazioni di un utente](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-also"></a>Vedi anche
[Annullamento della sottoscrizione per [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Analisi dei rendiconti finanziari in Microsoft Excel](finance-analyze-excel.md)  
[Finanze](finance.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
