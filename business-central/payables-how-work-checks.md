---
title: 'Emettere, stampare e annullare un assegno'
description: Descrive come emettere o stampare assegni tramite le registrazioni dei pagamenti e annullare movimenti contabili degli assegni in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment journal, print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256, 404,'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Effettuare pagamenti tramite assegno

È possibile emettere assegni elettronici e manuali in [!INCLUDE[prod_short](includes/prod_short.md)]. In entrambi i metodi vengono utilizzate le registrazioni pagamenti per emettere assegni ai fornitori. È inoltre possibile annullare assegni e visualizzare movimenti contabili assegni.

La seguente procedura mostra come pagare un fornitore con un assegno automatico applicando il pagamento alla fattura del fornitore pertinente, stampando l'assegno e quindi registrando il pagamento come pagato. Questa operazione determina la registrazione di movimenti contabili fornitori positivi, collegati a movimenti contabili negativi della banca e ad assegni fisici per l'elaborazione della banca.

È possibile pagare con due tipi di assegni. Per entrambi i tipi, il campo **Tipo contropartita** o **Tipo conto** deve contenere **Conto bancario**.

- **Assegno automatico**: selezionare questa opzione per stampare un assegno relativo all'importo specificato nella riga di registrazione pagamenti. È necessario stampare gli assegni prima di poter registrare le righe di registrazione.
- **Assegno manuale**: selezionare questa opzione se è stato creato un assegno manualmente e si desidera creare un corrispondente movimento contabile per questo importo. Selezionare questa opzione, non è possibile stampare l'assegno.

> [!NOTE]  
> Per assicurarsi che la banca compensi solo gli assegni e gli importi convalidati, è possibile inviarle un file che contenga informazioni sul fornitore, l'assegno e il pagamento. Per ulteriori informazioni, vedere [Esportare un file Positive Pay](finance-how-positive-pay.md).

> [!IMPORTANT]
> La stampante deve essere configurata per i moduli di assegni e deve essere definito il layout dell'assegno da utilizzare. Per ulteriori informazioni, vedere [Selezionare un layout degli assegni](finance-how-define-check-layouts.md). In alternativa, è possibile inviare l'assegno come file PDF, ad esempio.  

È possibile stampare fino a 10 fatture in una pagina per una matrice. Se un assegno si applica a più di 10 fatture, quando si stampa la matrice l'assegno viene annullato alla prima pagina e viene stampata la parola ANNULLATO sull'assegno. Quindi si stampa il resto delle fatture e l'importo totale degli assegni nella seconda pagina.

## Per pagare una fattura fornitore con un assegno automatico

Di seguito viene descritto come pagare un fornitore tramite assegno. I passaggi sono simili al rimborso dei clienti tramite assegno.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni pagamenti**, quindi scegli il collegamento correlato.
2. Compilare le righe di registrazione pagamenti. Per ulteriori informazioni, vedere [Registrare pagamenti e rimborsi](payables-how-post-payments-refunds.md).
3. Nel campo **Codice metodo di pagamento** selezionare **Assegno**.
4. Nel campo **Tipo pagamento banca** selezionare **Assegno automatico**.
5. Scegliere l'azione **Stampa assegno**.
6. Nella pagina **Assegno** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Se la stampante è configurata per la stampa di assegni, selezionare il pulsante **Stampa**. In caso contrario, scegliere il pulsante **Invia a**, selezionare l'opzione **Documento PDF** quindi scegliere il pulsante **OK** e stampare il documento PDF.

    Gli assegni fisici possono ora essere inviati ai fornitori per l'elaborazione. Passare alla registrazione del pagamento come collegato al fornitore e pertanto pagato nel sistema.
8. Scegliere l'azione **Registra**.

Vengono creati movimenti contabili fornitori collegati completamente e movimenti contabili bancari.

> [!NOTE]  
> Se si desidera stampare e pagare gli assegni provenienti da vari conti correnti bancari utilizzando più di una valuta, eseguire un singolo processo batch **Stampa assegno** per ogni valuta, specificando il conto corrente bancario appropriato.

## Per annullare assegni stampati che non sono registrati

È possibile annullare gli assegni non registrati dopo che sono stati stampati utilizzando l'azione **Annullo assegno** della pagina **Registrazioni pagamenti**.

1. Nella pagina **Registrazioni pagamenti** scegliere **Annullo assegno**, quindi scegliere gli assegni da annullare.

## Per annullare gli assegni

Una volta che i pagamenti tramite assegno sono stati registrati, è possibile annullare gli assegni dai movimenti contabili bancari risultanti.

> [!IMPORTANT]
> Se l'assegno viene applicato a una fattura, annullare prima l'assegno in modo che la fattura possa essere rimborsata, quindi annullare l'assegno. Se l'assegno è stato stampato e non ha pagato la fattura, scegliere **Annullo solo assegno** come descritto in questa sezione.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Selezionare il conto corrente bancario appropriato, scegliere l'azione **Modifica**, quindi scegliere l'azione **Mov. contabili assegni**.
3. Nella pagina **Mov. contabili assegni** scegliere l'azione **Annullo assegno**.
4. Selezionare la casella di controllo **Annullo solo assegno**.
5. Scegliere il pulsante **OK**.

## Per visualizzare un riepilogo degli assegni registrati

Se si desidera verificare gli assegni registrati, ad esempio per verificare più assegni pagati a un fornitore, è possibile utilizzare il report **C/C bancario - Dettaglio assegni**.
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **C/C bancario - Dettaglio assegni**, quindi scegli il collegamento correlato.
2. Impostare i filtri desiderati quindi scegliere il pulsante **Anteprima**.

## Vedere anche

[Effettuare i pagamenti](payables-make-payments.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Esportare un file Positive Pay](finance-how-positive-pay.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
