---
author: brentholtorf
ms.topic: include
ms.date: 03/04/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Se la tua azienda opera in più di un paese o area, probabilmente è importante poter svolgere operazioni commerciali in più di una valuta. Puoi definire la tua valuta locale (VL) nella pagina **Setup contabilità generale**. Successivamente, la valuta locale verrà rappresentata come valuta vuota in documenti e transazioni. Quando il campo **Valuta** è vuoto, la valuta è VL.

Il video seguente spiega come impostare la valuta locale.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1iM1n]

Successivamente, è necessario impostare i codici valuta per ogni valuta che utilizzi se acquisti o vendi in valute diverse da quella locale (LCY). Anche i conti bancari possono essere creati utilizzando le valute. È possibile registrare transazioni Co.Ge. in valute diverse, tuttavia, la transazione Co.Ge. verrà sempre registrata nella valuta locale (LCY).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

La contabilità generale è impostata per utilizzare la valuta locale (VL) ma è anche possibile impostarla per l'uso di un'altra valuta con un tasso di cambio della valuta assegnato. Se si imposta una seconda valuta come valuta contabile addizionale, [!INCLUDE[prod_short](prod_short.md)] registra automaticamente gli importi nella valuta locale e nella valuta contabile addizionale in ogni movimento C/G e altri movimenti, ad esempio quelli IVA. Per ulteriori informazioni, vedi [Impostare una valuta contabile addizionale](../finance-how-setup-additional-currencies.md). La valuta di rendicontazione aggiuntiva viene spesso utilizzata per facilitare la rendicontazione finanziaria ai proprietari che risiedono in paesi/aree geografiche che utilizzano valute diverse dalla valuta locale (LCY).  

> [!IMPORTANT]
> Se desideri utilizzare una valuta aggiuntiva per i report finanziari, assicurati di aver compreso le limitazioni. Per ulteriori informazioni, vedi [Impostare una valuta contabile addizionale](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Quando si eseguono registrazioni nella contabilità generale utilizzando una valuta estera, [!INCLUDE [prod_short](prod_short.md)] converte la transazione in VL utilizzando il tasso di cambio della data di registrazione. Il movimento C/G non conterrà informazioni relative alla valuta utilizzata, ma solo il valore in VL. Per tenere traccia della valuta originale, è necessario utilizzare i documenti di acquisto nonché i conti correnti bancari che includono le informazioni sulla valuta per i movimenti.
