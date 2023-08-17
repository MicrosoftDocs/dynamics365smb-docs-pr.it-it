---
title: Rivalutazione dei cespiti
description: 'Informazioni su come rettificare il valore dei cespiti, registrando i nuovi importi come svalutazione o rivalutazione e registrare i costi di acquisto aggiuntivi.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5628, 5629, 5633'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="revalue-fixed-assets"></a>Rivalutazione dei cespiti

La rivalutazione dei cespiti può essere costituita da rivalutazioni, svalutazioni o rettifiche dei valori generali.

Quando il valore di un cespite è aumentato, si registra una riga di registrazione con un importo più elevato, una rivalutazione, nel registro beni ammortizzabili. Il nuovo importo viene registrato come rivalutazione in base all'impostazione di registrazione del cespite.

Quando il valore di un cespite è diminuito, si registra una riga di registrazione con un importo inferiore, una svalutazione, nel registro beni ammortizzabili. Il nuovo importo viene registrato come svalutazione in base all'impostazione di registrazione del cespite.

L'indicizzazione consente di correggere i valori di più cespiti, ad esempio le modifiche generali a livello di prezzo. Il processo batch **Indice cespiti** consente di modificare vari importi quali gli importi di svalutazione e di rivalutazione.

## <a name="to-post-an-appreciation-from-the-fixed-asset-gl-journal"></a>Per registrare una rivalutazione tramite Registrazioni Cespiti in C/G

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni cespiti in C/G**, quindi scegli il collegamento correlato.  
2. Creare una riga di registrazione iniziale e compilare i campi in base alle esigenze.
3. Nel campo **Tipo reg. cespite** scegliere **Rivalutazione**.
4. Scegliere l'azione **Inserisci conto cespiti**. Una seconda riga di registrazione viene creata per la contropartita impostata per la registrazione della rivalutazione.

    > [!NOTE]  
    >   Il passaggio 4 funziona solo se è stato impostato quanto segue: nella pagina **Scheda Cat. Reg. Cespite** della categoria di registrazione del cespite, il campo **Conto rivalutazioni** contiene il conto di addebito contabilità generale e il campo **Contropartita rivalutazione** contiene il conto C/G in cui si desidera registrare i movimenti di contropartita per la rivalutazione. Per ulteriori informazioni, vedere [Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Scegliere l'azione **Registra**.

## <a name="to-post-a-write-down-from-the-fixed-asset-gl-journal"></a>Per registrare una svalutazione tramite Registrazioni Cespiti in C/G

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni cespiti in C/G**, quindi scegli il collegamento correlato.  
2. Creare una riga di registrazione iniziale e compilare i campi in base alle esigenze.
3. Nel campo **Tipo reg. cespite** scegliere **Svalutazione**.
4. Scegliere l'azione **Inserisci conto cespiti**. Una seconda riga di registrazione viene creata per la contropartita impostata per la registrazione della svalutazione.

    > [!NOTE]  
    >   Il passaggio 4 funziona solo se è stato impostato quanto segue: nella pagina **Scheda Cat. Reg. Cespite** della categoria di registrazione del cespite, il campo **Conto svalutazioni** contiene il conto di credito contabilità generale e il campo **Conto spese svalutazione** contiene il conto C/G in cui si desidera registrare i movimenti di contropartita per le svalutazioni. Per ulteriori informazioni, vedere [Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Scegliere l'azione **Registra**.

## <a name="to-perform-general-revaluation-of-fixed-assets"></a>Per eseguire la rivalutazione generali dei cespiti

L'indicizzazione consente di correggere i valori di più cespiti, ad esempio le modifiche generali a livello di prezzo. Il processo batch **Indice cespiti** consente di modificare vari importi quali gli importi di svalutazione e di rivalutazione. La casella di controllo **Permetti indicizzazione** nella pagina **Registro beni ammortizzabili** deve essere selezionata.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Indice cespiti**, quindi scegli il collegamento correlato.  
2. Compilare i campi, se necessario.
3. Scegliere il pulsante **OK**.

    Le righe di rivalutazione vengono create in base alle impostazioni del passaggio 2. Le righe vengono create nella registrazione cespiti o nella registrazione cespiti in C/G, a seconda dell'impostazione del batch e del modello nella pagina **Setup registrazioni cespiti**. Per ulteriori informazioni, vedere [Impostare i valori generali per i cespiti](fa-how-setup-general.md).
4. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni cespiti in C/G**, quindi scegli il collegamento correlato.  
5. Selezionare la registrazione con i cespiti da rivalutare, quindi scegliere l'azione **Movimenti contabili**.  
6. Controllare i movimenti creati quindi scegliere l'azione **Registra** per eseguire la registrazione.

    > [!TIP]  
    >   Se i numeri dell'indice servono soltanto a fini di simulazione, è possibile creare un registro beni ammortizzabili in cui archiviarli. In tal modo i movimenti non avranno alcun effetto sugli altri registri beni ammortizzabili.

## <a name="to-post-additional-acquisition-costs"></a>Per registrare i costi di acquisto aggiuntivi

I costi aggiuntivi di acquisto di un cespite vengono registrati allo stesso modo dei costi di acquisto originali: da una fattura d'acquisto o da una registrazione cespiti. Per ulteriori informazioni, vedere [Acquisire i cespiti](fa-how-acquire.md).  

Se l'ammortamento del cespite è già stato calcolato, selezionare la casella di controllo **Amm. costi di Acq.** affinché la differenza tra costo aggiuntivo di acquisto e il valore di realizzo venga ammortizzata proporzionalmente all'importo di ammortamento del cespite precedente. Questa impostazione garantisce che il periodo di ammortamento non venga modificato.  

La percentuale di ammortamento viene calcolata in base a:  

*P = (ammortamento totale x 100) / base ammortizzabile*

*Importo di ammortamento = (P/100) x (costo aggiuntivo di acquisto – valore di realizzo)*  

Ricordarsi di selezionare la casella di controllo **Ammort. alla Data Reg. Cespite** nella fattura, nelle registrazioni cespiti in C/G o nelle righe delle registrazioni cespiti al fine di assicurarsi che venga calcolato l'ammortamento dall'ultima data di registrazione cespiti alla data di registrazione del costo di acquisto aggiuntivo.

### <a name="example---posting-additional-acquisition-costs"></a>Esempio: registrazione di costi di acquisto aggiuntivi

In data 1° agosto 2000 viene acquistato un macchinario. Il costo di acquisto è 4.800. L'ammortamento viene calcolato in base al metodo a quote costanti in quattro anni.

Il 31 agosto 2000 viene eseguita il processo batch **Calcola ammortamento**. L'ammortamento viene calcolato come segue:

*valore contabile x numero di giorni di ammortamento / numero totale di giorni di ammortamento = 4800 x 30 / 1440 = 100*  

Il 15 settembre 2000 viene registrata una fattura per la verniciatura della macchina. L'importo della fattura è 480.

Se, prima di registrare la fattura, è stata selezionata la casella di controllo **Ammort. alla data reg. cespite**, verrà effettuato il seguente calcolo:  

15 giorni di ammortamento (dal 01/09/00 al 15/09/00) vengono calcolati come segue:

*valore contabile x numero di giorni di ammortamento / numero rimanente di giorni di ammortamento = (4800 - 100) x 15 / 1410 = 50*

Se, prima di registrare la fattura, è stata selezionata la casella di controllo **Amm. costi di acq.**, verrà effettuato il seguente calcolo:  

*il costo di acquisto aggiuntivo viene ammortizzato in base al risultato della seguente formula: ((150 x 100) / 4800) / 100 x 480 = 15*

La base ammortizzabile diventa *5280 = (4800 + 480)*, mentre l'ammortamento maturato è *165 = (100 + 50 + 15)*, equivalente a 45 giorni di ammortamento del costo totale di acquisto. Ciò significa che il cespite viene ammortizzato completamente nel periodo previsto di quattro anni.  

Il 30/09/00 viene effettuata il processo batch **Calcola Ammortamento**. Viene effettuato il seguente calcolo:  

*la durata residua dell'ammortamento corrisponde a 3 anni, 10 mesi e 15 giorni = 1395 giorni*  

*il valore contabile è (5280 - 165) = 5115*  

*l'importo di ammortamento per il mese di settembre 2000 è: 5115 x 15 / 1395 = 55,00*  

*Totale ammortamento = 165 + 55 = 220*  

Se non è stata selezionata la casella di controllo **Ammort. alla data reg. cespite**, vengono persi 15 giorni di ammortamento perché eseguendo il processo batch **Calcolo ammortamento** il 30/09/00 verrebbe calcolato l'ammortamento dal 15/09/00 al 30/09/00. Ciò significa che se il processo batch **Calcolo ammortamento** viene eseguito il 30/09/00, il calcolo è il seguente:  

*la durata residua dell'ammortamento corrisponde a 3 anni, 10 mesi e 15 giorni = 1395 giorni*  

*il valore contabile corrisponde a (4800 + 480 - 100 - 15) = 5165*

*l'importo di ammortamento per il mese di settembre 2000 è: 5165 x 15 / 1395 = 55,54*  

*totale ammortamento = 100 + 15 + 55,54 = 170,54*

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/paths/manage-advanced-fixed-assets-transactions/)

## <a name="see-also"></a>Vedere anche

[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Finanze](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
