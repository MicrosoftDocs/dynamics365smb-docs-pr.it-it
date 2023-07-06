---
title: Impostare la valutazione magazzino e i costi
description: 'Per assicurarsi che i costi di magazzino vengano registrati correttamente, è necessario impostare vari campi e pagine prima di iniziare a effettuare transazioni di articoli.'
author: SorenGP
ms.topic: conceptual
ms.search.keywords: null
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="setting-up-inventory-valuation-and-costing"></a><a name="setting-up-inventory-valuation-and-costing"></a><a name="setting-up-inventory-valuation-and-costing"></a>Impostazione della valutazione magazzino e i costi

Per assicurarsi che i costi di magazzino vengano registrati correttamente, è necessario impostare vari campi e pagine prima di iniziare a effettuare transazioni di articoli. In genere, le aziende scelgono un metodo di determinazione dei costi specifico e lo applicano agli articoli di magazzino, ad esempio, per aiutarle a tenere traccia del valore degli articoli in magazzino.  

> [!TIP]
> Per un'introduzione alla determinazione dei costi in [!INCLUDE [prod_short](includes/prod_short.md)], vedere [Informazioni sul costing di magazzino](finance-learn-about-costing.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

|**Per**|**Vedere**|  
|------------|-------------|
|Specificare un metodo di costing predefinito per la società in modo da definire come verrà utilizzato il relativo costo in entrata per valutare il valore di magazzino e il costo delle merci vendute.|[Impostare le informazioni generali di magazzino](inventory-how-setup-general.md)|  
|Specificare un metodo di determinazione dei costi per i singoli articoli se richiedono un metodo di determinazione dei costi diverso.|[Registrare nuovi articoli](inventory-how-register-new-items.md)|  
|Assicurarsi che il costo venga registrato automaticamente nella contabilità generale ogni volta che viene contabilizzata una transazione di magazzino.|Campo **Reg. automatica costi** nella pagina **Setup magazzino**|  
|Assicurarsi che i costi previsti siano registrati nella contabilità generale per visualizzare, dai conti C/G provvisori, una stima degli importi residui e il costo degli articoli trattati, prima dell'effettiva fatturazione.|Campo **Reg. costi previsti in C/G** nella pagina **Setup magazzino**|  
|Impostare il sistema affinché venga effettuata la rettifica automatica delle eventuali modifiche dei costi ogni volta che si registrano transazioni di magazzino.|[Rettifica costi articolo](inventory-how-adjust-item-costs.md)|  
|Definire se il costo medio deve essere calcolato solo per articolo o per articolo per ogni unità di stockkeeping e per ogni variante dell'articolo.|Campo **Tipo calcolo costo medio** nella pagina **Setup magazzino**|  
|Selezionare il periodo di tempo che si desidera venga utilizzato dall'applicazione per calcolare il costo medio ponderato degli articoli per i quali è utilizzato il metodo di costing Medio.|Campo **Costo medio periodo** nella pagina **Setup magazzino**|  
|Definire i periodi di magazzino per controllare il valore di magazzino nel tempo, disabilitando la registrazione delle transazioni nei periodi di magazzino chiusi.|[Utilizzare periodi di magazzino](finance-how-to-work-with-inventory-periods.md)|  
|Assicurarsi che i resi di vendita vengano applicati alla transazione in uscita originale per mantenere il valore di magazzino.|Campo **Storno esatto costo obblig.** nella pagina **Contabilità clienti**|  
|Assicurarsi che i resi di acquisto vengano applicati alla transazione in entrata originale per mantenere il valore di magazzino.|Campo **Storno esatto costo obblig.** nella pagina **Contabilità fornitori**|
|Impostare le regole di arrotondamento da applicare quando i prezzi degli articoli e i costi standard vengono rettificati o suggeriti.|Pagina **Metodo di arrotondamento**|  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Impostare le informazioni generali di magazzino](inventory-how-setup-general.md)  
[Riconciliare i costi di magazzino con la contabilità generale](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Impostare le procedure ottimali: metodo di costing](setup-best-practices-costing-method.md)  
[Dettagli di progettazione: determinazione dei costi di inventario](design-details-inventory-costing.md)  
[Dettagli di progettazione: modifica dei metodi di costing per gli articoli](design-details-changing-costing-methods.md)  
[Utilizzare Business Central](ui-work-product.md)  
[Finanze](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
