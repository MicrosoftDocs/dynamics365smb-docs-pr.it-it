---
author: edupont04
ms.topic: include
ms.date: 03/15/2022
ms.author: edupont
---
Con l'espandersi delle attività delle società in un numero sempre maggiore di paesi/aree geografiche, diventa essenziale poter vendere e riportare dati finanziari in più di una valuta. La valuta locale (VL) è definita nella pagina **Setup contabilità generale** come descritto nell'articolo [Informazioni sulla contabilità generale e sul piano dei conti](../finance-general-ledger.md). Una volta che la valuta locale (LCY) è stata definita, sarà rappresentata come una valuta vuota, quindi quando il campo **Valuta** è vuoto, significa che è LCY.  

Successivamente, è necessario impostare i codici valuta per ogni valuta che utilizzi se acquisti o vendi in valute diverse da quella locale (LCY). Anche i conti bancari possono essere creati utilizzando le valute. È possibile registrare transazioni Co.Ge. in valute diverse, tuttavia, la transazione Co.Ge. verrà sempre registrata nella valuta locale (LCY).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

La contabilità generale è impostata per utilizzare la valuta locale (VL) ma è anche possibile impostarla per l'uso di un'altra valuta con un tasso di cambio della valuta assegnato. Se si imposta una seconda valuta come valuta contabile addizionale, [!INCLUDE[prod_short](prod_short.md)] registra automaticamente gli importi nella valuta locale e in questa valuta di dichiarazione aggiuntiva in ogni movimento C/G e altri movimenti, ad esempio i movimenti IVA. Per ulteriori informazioni, vedi [Impostare una valuta contabile addizionale](../finance-how-setup-additional-currencies.md). La valuta di rendicontazione aggiuntiva viene spesso utilizzata per facilitare la rendicontazione finanziaria ai proprietari che risiedono in paesi/aree geografiche che utilizzano valute diverse dalla valuta locale (LCY).  

> [!IMPORTANT]
> Se desideri utilizzare una valuta aggiuntiva per i report finanziari, assicurati di aver compreso le limitazioni. Per ulteriori informazioni, vedi [Impostare una valuta contabile addizionale](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Quando esegui la registrazione in C/G utilizzando un codice valuta, ad esempio per registrare una spesa in un giornale di registrazione generale utilizzando un codice valuta, la transazione viene convertita in VL utilizzando il tasso di cambio della valuta per la data di registrazione. Il movimento C/G non conterrà informazioni relative alla valuta utilizzata, ma solo il valore in VL. Per tenere traccia della valuta originale, ad esempio per una fattura, è necessario utilizzare i documenti di vendita e acquisto nonché i conti correnti bancari che memorizzano le informazioni sul codice valuta per i movimenti.
