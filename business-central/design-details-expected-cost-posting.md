---
title: Dettagli di progettazione - Registrazione del costo previsto
description: 'I costi previsti rappresentano, ad esempio, la stima del costo di un articolo acquistato registrato prima di ricevere la fattura per l''articolo.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 07/20/2021
ms.author: edupont
---
# <a name="design-details-expected-cost-posting"></a>Dettagli di progettazione: Registrazione del costo previsto
I costi previsti rappresentano, ad esempio, la stima del costo di un articolo acquistato registrato prima di ricevere la fattura per l'articolo.  

 I costi previsti possono venire registrati sia nell'inventario sia nella contabilità generale. Quando si registra una quantità che è solo ricevuta o spedita ma non fatturata, viene creato un movimento di valorizzazione con il costo previsto. Questo costo previsto influisce sul valore di magazzino ma non viene registrato nella contabilità generale a meno che non si imposti il sistema appositamente.  

> [!NOTE]  
>  I costi previsti vengono gestiti solo per le transazioni articoli. I costi previsti non sono per i tipi di transazione immateriali, ad esempio capacità e addebiti articolo.  

 Se è stata registrata solo la parte quantitativa di un aumento di magazzino, il valore di magazzino nella contabilità generale non cambierà a meno che non sia stata selezionata la casella di controllo **Reg. costi previsti in CG** nella pagina **Setup magazzino**. In questo caso, il costo previsto viene registrato nei conti provvisori al momento del carico. Dopo che il carico è stato completamente fatturato, i conti provvisori verranno quindi bilanciati e il costo effettivo viene registrato nel conto giacenza magazzino.  

 Per supportare il lavoro di riconciliazione e di tracciabilità, il movimento di valorizzazione fatturato mostra l'importo del costo previsto che è stato registrato per bilanciare i conti provvisori.  

## <a name="prerequisites-for-posting-expected-costs"></a>Prerequisiti per la registrazione dei costi previsti

Per rendere possibile la registrazione dei costi previsti è necessario effettuare le seguenti operazioni:
1. Nella pagina **Setup magazzino**, selezionare le caselle di controllo **Reg. automatica costi** e **Reg. costi previsti in CG**.
2. Impostare i conti provvisori da utilizzare durante il processo di registrazione dei costi previsti.  

  Nella pagina **Setup registrazione magazzino**, verificare i campi **Conto giac. magazzino** e **Conto giac. magazzino (prov.)** per l'impostazione **Codice ubicazione e codice cat. reg. magazzino** dell'articolo che si sta acquistando. Per maggiori informazioni su questi conti, vedere [Design Details - Dettagli di progettazione: Conti nella contabilità generale](design-details-accounts-in-the-general-ledger.md).
3. Nella pagina **Setup registrazioni COGE**, verificare il campo **Conto ratei magaz. (provvis.)** per i valori **Cat. Reg. Business** e **Cat. reg. articolo/servizio** che verranno utilizzati.
4. Quando si crea un ordine di acquisto, per impostazione predefinita il campo **Nr. fattura fornitore** è obbligatorio. È necessario deselezionarlo nella pagina **Setup contabilità fornitori** deselezionando il campo **Nr. doc. esterno obblig.**.

## <a name="example"></a>Esempio

> [!NOTE]  
> I numeri di conto utilizzati in questo esempio sono solo di riferimento e saranno diversi nel sistema in uso. Impostarli come indicato nei prerequisiti sopra.

Si registra un ordine di acquisto come ricevuto. Il costo previsto è di VL 95,00.  

 **Movimenti di valorizzazione**  

|Data di registrazione:|Tipo movimento|Importo costo (previsto)|Costo prev. registrato in C/G|Costo previsto|Nr. movimento cont. articolo|Nr. movimento|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|01-01-20|Costo Diretto|95,00|95,00|Sì|1|1|  

 **Movimenti di relazione nella C/G – Relazione Movimento Articolo**  

|Nr. movimento C/G|Nr. movimento valorizzazione|Nr. registro C/G|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  

 **Movimenti C/G**  

|Data di registrazione:|Conti C/G|Numero di conto (demo en-US)|Importo|Nr. movimento|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|Conto giac. magazzino (prov.)|5530|-95,00|2|  
|01-01-20|Conto giac. magazzino (prov.)|2131|95,00|1|  

 In una data successiva, registrare l'ordine di acquisto come fatturato. Il costo fatturato è di VL 100,00.  

 **Movimenti di valorizzazione**  

|Data di registrazione:|Importo costo (effettivo)|Importo costo (previsto)|Costo registrato in C/G|Costo previsto|Nr. movimento cont. articolo|Nr. movimento|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|01-15-20|100.00|-95,00|100.00|No|1|2|  

 **Movimenti di relazione nella C/G – Relazione Movimento Articolo**  

|Nr. movimento C/G|Nr. movimento valorizzazione|Nr. registro C/G|  
|--------------------|---------------------|-----------------------|  
|3|2|2|  
|4|2|2|  
|5|2|2|  
|6|2|2|  

 **Movimenti C/G**  

|Data di registrazione|Conti C/G|N. conto (solo esempi!)|Importo|Nr. movimento|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-15-20|Conto giac. magazzino (prov.)|5530|95,00|4|  
|01-15-20|Conto giac. magazzino (prov.)|2131|-95,00|3|  
|01-15-20|Conto costi diretti coll.|7291|-100|6|  
|01-15-20|Conto giac. magazzino|2130|100|5|  

## <a name="see-also"></a>Vedi anche
 [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)   
 [Dettagli di progettazione: Rettifica costo](design-details-cost-adjustment.md)   
 [Dettagli di progettazione: Riconciliazione con la contabilità generale](design-details-reconciliation-with-the-general-ledger.md)   
 [Dettagli di progettazione: Registrazione di magazzino](design-details-inventory-posting.md)   
 [Dettagli di progettazione: Scostamento](design-details-variance.md)  
 [Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
 [Finanze](finance.md)  
 [Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
