---
title: 'Procedura: Trasferire fondi bancari | Documenti Microsoft'
description: 'Procedura: Trasferire fondi bancari'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 03/32/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e2e3642d08428367fac1dd5845013e14627fe6ed
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-transfer-bank-funds"></a>Procedura: Trasferire fondi bancari
Talvolta, può anche essere necessario effettuare un bonifico da un conto corrente bancario ad un altro. A tale scopo, è necessario registrare una transazione nelle registrazioni COGE. L'attività varia a seconda se i conti correnti bancari utilizzano la stessa valuta o valute diverse.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Per registrare un bonifico tra conti correnti bancari con lo stesso codice valuta
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazione COGE**, quindi scegliere il collegamento correlato.
2. In una riga di registrazione compilare i campi **Data di registrazione** e **Nr. documento**. .
3. Nel campo **Tipo conto** selezionare **Conti C/C bancari**.
4. Nel campo **Nr. conto** selezionare la banca da cui si desidera trasferire i fondi.
5. Immettere l'importo da traferire nel campo **Importo**.
6. Nel campo **Tipo contropartita** selezionare **Conti C/C bancari**.
7. Nel campo **Contropartita** selezionare il conto bancario da cui si desidera trasferire i fondi.
8. Effettuare la registrazione.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Per registrare un bonifico tra conti correnti bancari con codici valuta diversi
Per trasferire i fondi tra conti correnti bancari che utilizzano valute diverse, è necessario inserire due righe di registrazioni COGE.

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazione COGE**, quindi scegliere il collegamento correlato.
2. Creare due righe di registrazione e compilare i campi **Data di registrazione** e **Nr. documento**. .
3. Nella prima riga di registrazioni selezionare **C/C bancario** nel campo **Tipo conto**.
4. Nel campo **Nr. conto** selezionare il conto bancario a cui si desidera trasferire i fondi.
5. Nel campo **Importo** immettere la quantità nella valuta del conto corrente bancario. Immettere gli importi in Avere con un segno meno (-). Immettere gli importi in Dare senza il segno meno (-).
6. Nel campo **Tipo contropartita** selezionare **Conti C/C bancari**.
7. Nel campo **Contropartita** selezionare il conto bancario da cui si desidera trasferire i fondi.
8. Nella seconda riga di registrazioni selezionare **C/C bancario** nel campo **Tipo conto**.
9. Nel campo **Nr. conto** selezionare il conto bancario da cui si desidera trasferire i fondi.
10. Nel campo **Importo** immettere la quantità nella valuta del conto corrente bancario. Immettere gli importi in Avere con un segno meno (-). Immettere gli importi in Dare senza il segno meno (-).
11. Nel campo **Tipo contropartita** selezionare **Conti C/C bancari**.  
12. Nel campo **Contropartita** selezionare il conto bancario a cui si desidera trasferire i fondi.

    **Nota**: se i tassi di cambio utilizzati nelle registrazioni sono diversi dai tassi riportati nella finestra **Tassi di cambio valuta**, compilare una terza riga per il guadagno o la perdita nel tasso di cambio. Immettere **Conto C/G** nel campo **Tipo conto**. Nel campo **Nr. conto** immettere il numero di conto C/G per i guadagni o le perdite nel tasso di cambio . Immettere utile o perdita in **Importo** campo con o senza un segno meno per i crediti e debiti rispettivamente.
13. Effettuare la registrazione.

## <a name="see-also"></a>Vedi anche
[Gestione di conti correnti bancari](bank-manage-bank-accounts.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

