---
title: Configurazione dei processi di produzione
description: 'Per convertire il materiale in articoli finali prodotti, è necessario configurare nel sistema le risorse di produzione, ad esempio distinte base, cicli, operatori macchina e macchinari.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000768, 99000779, 99000780, 99000866'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="setting-up-manufacturing"></a>Impostazione della produzione

Per convertire il materiale in articoli finali prodotti, è necessario configurare nel sistema le risorse di produzione, ad esempio distinte base, cicli, operatori macchina e macchinari.

Nel sistema operatori e macchine sono rappresentati come centri di lavoro che possono essere organizzati in aree di produzione e gruppi aree di produzione. Una volta definite queste risorse, è possibile caricarvi operazioni in base alla struttura dei processi e dei materiali (DB) definita per l'articolo, nonché alla capacità del centro di lavoro o dell'area di produzione. È inoltre possibile impostare la capacità di produzione delle singole risorse. La capacità viene definita dagli orari di lavoro disponibili nei centri di lavoro e nelle aree di produzione e viene gestita tramite calendari disponibili per ogni livello. In un calendario delle aree di produzione sono specificati i giorni e gli orari lavorativi, i turni, le ferie e le assenze che determinano la capacità lorda disponibile dell'area di produzione (in genere misurata in minuti). Tale capacità viene calcolata in base ai valori definiti di efficienza e capacità.  

Dopo l'impostazione della produzione, è possibile pianificare ed eseguire gli ordini di produzione. Per ulteriori informazioni, vedere [Pianificazione](production-planning.md) e [Manufacturing](production-manage-manufacturing.md).  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

|**Per**|**Vedere**|  
|------------|-------------|  
|Configurare le funzionalità di Manufacturing, ad esempio la definizione delle ore di lavoro del reparto e la selezione dei parametri di pianificazione.|La pagina **Setup manufacturing**.|
|Nella scheda **Pianificazione** della pagina **Setup manufacturing**, impostare i parametri di pianificazione globale che sovrascrivono i parametri impostati sulle singole schede articolo.|[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)|
|Definire una settimana lavorativa standard nel reparto di produzione in termini di ora di inizio e di fine di ogni giorno lavorativo e di turni lavorativi correlati.|[Creare calendari del reparto produzione](production-how-to-create-work-center-calendars.md)|  
|Organizzare i valori e i requisiti fissi di una risorsa di produzione come aree di produzione o centri di lavoro per gestirne l'output della produzione.|[Impostare aree di produzione e centri di lavoro](production-how-to-set-up-work-and-machine-centers.md)|
|Organizzare operazioni di produzione nell'ordine richiesto e assegnarle ad aree di produzione o centri di lavoro con i periodi lavorativi necessari.|[Creare cicli](production-how-to-create-routings.md)|
|Organizzare componenti o sottoassemblaggi di produzione in riferimento a un articolo padre prodotto e certificare la DB per l'esecuzione nelle aree di produzione.|[Creare le distinte base di produzione](production-how-to-create-production-boms.md)|
|Assicurarsi che l'esatta quantità di componenti sia disponibile quando gli articoli prodotti vengono stoccati in un'unità di misura, ma prodotti in un'altra.|[Utilizzare le unità di misura batch di produzione](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Definire famiglie di articoli di produzione con processi di lavorazione simili per ridurre i consumi. Ad esempio, è possibile che da una lamina vengano prodotti contemporaneamente quattro pezzi di un articolo e 10 pezzi di un altro articolo differente.|[Utilizzare famiglie di prodotti](production-how-work-family.md)|
|Utilizzare task standard per semplificare la creazione di cicli allegando rapidamente informazioni supplementari a operazioni periodiche.|[Impostare righe di ciclo standard](production-how-set-up-standard-routing-lines.md)|  
|Preparare le aree di produzione e i cicli per rappresentare le operazioni di produzione in conto lavoro.|[Gestire le attività di conto lavoro](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Vedere anche

[Manufacturing](production-manage-manufacturing.md)  
[Pianif.](production-planning.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
