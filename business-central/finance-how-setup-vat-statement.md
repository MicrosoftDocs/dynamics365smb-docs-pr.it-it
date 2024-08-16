---
title: Impostare una dichiarazione IVA
description: In questo articolo viene spiegato come impostare un modello di dichiarazione IVA e i nomi delle dichiarazioni IVA per soddisfare i requisiti mutevoli delle autorità fiscali.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '317, 318, 320, 474'
ms.date: 08/13/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Imposta modelli di dichiarazione IVA e nomi di dichiarazione IVA

Le autorità fiscali possono e devono modificare i requisiti per la registrazione dell'IVA. Definizioni di dichiarazione IVA e di nomi delle dichiarazioni IVA consentono di prepararsi per eventuali modifiche e a effettuare una transizione graduale ai nuovi requisiti. È possibile utilizzare i modelli di dichiarazione IVA per impostare diversi report quando si sceglie di stampare la dichiarazione. Ogni modello di dichiarazione IVA può avere più nomi di dichiarazione IVA, che a loro volta definiscono i calcoli; è possibile creare un nuovo nome di dichiarazione IVA quando cambiano i requisiti. Ad esempio, un nome potrebbe calcolare l'IVA per quest'anno in base ai requisiti correnti e un altro potrebbe calcolare l'IVA in base ai requisiti per l'anno successivo. I nomi sono inoltre un metodo per conservare una cronologia dei formati delle dichiarazioni IVA, ad esempio, ad esempio, per poter verificare come è stata calcolata l'IVA negli anni precedenti.

## Per definire dichiarazioni IVA

Una dichiarazione IVA consente di calcolare l'importo di liquidazione dell'IVA per un certo periodo, ad esempio un trimestre.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Dichiarazioni IVA**, quindi scegli il collegamento correlato.  
2. Scegliere il campo **Nome**, quindi **Nuovo** nella pagina **Nomi dichiarazione IVA**.
3. Compilare i campi necessari. Di solito si desidera avere un'impostazione per ciascuna combinazione di Cat. Reg. Business IVA e Cat. reg. art./serv. IVA. Per i numeri di riga ha senso utilizzare numeri o codici equivalenti a quelli presenti nella dichiarazione IVA ufficiale [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> È possibile filtrare le informazioni che la dichiarazione includerà, a seconda di ciò che viene scelto nel campo **Tipo**. **Totale conto** è utile quando si desidera ottenere l'IVA di un conto specifico.
**Totale Mov. IVA** ottiene l'IVA da conti assegnati alle selezioni in **Tipo reg. gen.**, **Cat. reg. business IVA** e/o i campi **Cat. reg. art./serv. IVA**. **Totale Riga** consente di immettere un valore o filtrare rapidamente il campo **Totale Riga**. Per ulteriori informazioni sulla ricerca e l'applicazione di filtri, vedere [Ricerca, filtro e ordinamento di dati](ui-enter-criteria-filters.md). **Descrizione** è spesso utilizzato aggiungere una nota alla dichiarazione. Ad esempio, potrebbe essere utilizzata come intestazione quando si utilizza il totale riga.

## Per visualizzare in anteprima la dichiarazione IVA

Una volta definita una dichiarazione IVA, è possibile visualizzarla in anteprima per assicurarsi che soddisfi le proprie esigenze.
> [!Tip]
> È consigliabile disporre di una sezione della dichiarazione IVA utilizzando il **tipo** **Totale movimenti IVA** e un'altra sezione usando il **tipo** **Totale conto** per riconciliare gli importi in base alla tabella **Movimento IVA** rispetto all'importo in **Conti G/L**. È possibile anche usare il report **C/G - Riconciliazione IVA** per questo scopo.

1. Scegliere **Anteprima**.
2. Immettere un filtro data per limitare la dichiarazione a un periodo specifico. Per ulteriori informazioni su come personalizzare la pagina per visualizzare il filtro data, vedere [Ricerca, filtro e ordinamento di dati](ui-enter-criteria-filters.md)..
3. È possibile selezionare varie opzioni per specificare il tipo di movimenti IVA da includere nella dichiarazione.
4. Per le righe il cui campo **Tipo** contiene il valore **Totale movimenti IVA** è possibile visualizzare un elenco dei movimenti IVA selezionando l'importo nel campo **Importo colonna**.
5. È possibile utilizzare la personalizzazione per mostrare più campi nelle righe. Ad esempio, l'importo base non realizzato e l'importo IVA non realizzata, se si utilizza l'IVA non realizzata.

## Vedere anche

[Impostare l'imposta sul valore aggiunto](finance-setup-vat.md)    
[Impostazione dell'imposta sul valore aggiunto non realizzata](finance-setup-unrealized-vat.md)    
[Segnalare l'IVA all'autorità fiscale](finance-how-report-vat.md)    
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)    
[Funzionalità locale in Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
