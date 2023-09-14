---
title: Trasferimento di fondi bancari
description: 'È possibile trasferire gli importi da un conto corrente bancario a un altro, incluse le valute diverse, tramite la registrazione della transazione nelle registrazioni COGE.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bank account transfer, multiple currencies'
ms.search.form: 39
ms.date: 04/29/2021
ms.author: bholtorf
---
# Trasferimento di fondi bancari

Talvolta, può anche essere necessario effettuare un bonifico da un conto corrente bancario in [!INCLUDE[prod_short](includes/prod_short.md)] a un altro. A tale scopo, è necessario registrare la transazione nella pagina **Registrazioni COGE**. L'attività varia a seconda se i conti correnti bancari utilizzano la stessa valuta o valute diverse.

## Per registrare un bonifico tra conti correnti bancari con lo stesso codice valuta

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni COGE**, quindi scegli il collegamento correlato.
2. In una riga di registrazioni compilare i campi **Data di registrazione** e **Nr. documento**.
3. Nel campo **Tipo conto** selezionare **Conti C/C bancari**.
4. Nel campo **Nr. conto** selezionare la banca da cui si desidera trasferire i fondi.
5. Immettere l'importo da traferire nel campo **Importo**.

    Successivamente, è necessario specificare il conto di contropartita. Se non riesci a visualizzare i campi pertinenti, scegli l'azione **Mostra più colonne** per visualizzare tutti i campi disponibili.
6. Nel campo **Tipo contropartita** selezionare **Conti C/C bancari**.
7. Nel campo **Nr. contropartita** selezionare il conto bancario a cui si desidera trasferire i fondi.
8. Effettuare la registrazione.

## Per registrare un bonifico tra conti correnti bancari con codici valuta diversi

Per trasferire i fondi tra conti correnti bancari che utilizzano valute diverse, è necessario inserire due righe di registrazioni COGE.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni COGE**, quindi scegli il collegamento correlato.
2. Creare due righe di registrazione e compilare i campi **Data di registrazione** e **Nr. documento**.
3. Nella prima riga di registrazioni selezionare **C/C bancario** nel campo **Tipo conto**.
4. Nel campo **Nr. conto** selezionare il conto bancario da cui si desidera trasferire i fondi.
5. Nel campo **Importo** immettere la quantità nella valuta del C/C bancario con o senza un segno meno.

    > [!TIP]
    > Un importo senza segno è un debito e un importo con un segno meno è un credito.

    > [!NOTE]
    > Alcune società preferiscono effettuare trasferimenti tra conti su righe di registrazione separate. Altre società preferiscono registrare tutto su una riga di registrazione utilizzando un conto di contropartita. Se non sai cosa fare, rivolgiti al tuo esperto locale.
    >
    > Se la tua società preferisce utilizzare un conto di contropartita, imposta il campo **Tipo contropartita** su **Conto bancario** e imposta il campo **Nr contropartita** sul C/C bancario su cui desideri trasferire i fondi. Quindi procedi al passaggio 9 o 10.
    >
    > Se la tua società preferisce utilizzare una riga di registrazione separata, vai al passaggio successivo.
6. Nella seconda riga di registrazioni selezionare **C/C bancario** nel campo **Tipo conto**.
7. Nel campo **Nr. conto** selezionare il conto bancario a cui si desidera trasferire i fondi.
8. Nel campo **Importo** immettere la quantità nella valuta del C/C bancario con o senza un segno meno.

    > [!TIP]
    > Un importo senza segno è un debito e un importo con un segno meno è un credito.
9. Se i tassi di cambio utilizzati nelle registrazioni sono diversi da quelli riportati nella pagina **Tassi di cambio valuta**, compila una nuova riga di registrazione per le perdite o gli utili di conversione.  

    1. Immettere **Conto C/G** nel campo **Tipo conto**.  

    2. Nel campo **Nr. conto** immettere il numero di conto C/G per i guadagni o le perdite nel tasso di cambio.  

    3. Immettere le perdite o gli utili di conversione nel campo **Importo** con o senza segno meno.

    > [!TIP]
    > Un importo senza segno è un debito e un importo con un segno meno è un credito.
10. Effettuare la registrazione.

## Vedere anche

[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]