---
title: Assemblaggio su ordine e assemblaggio per magazzino
description: Informazioni sull'assemblaggio di articoli da usare per ordini di vendita o da tenere in magazzino per vendite future.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock" />Assemblaggio su ordine e assemblaggio per magazzino

[!INCLUDE [prod_short](includes/prod_short.md)] consente di fornire articoli di assemblaggio nei seguenti due modi:

* Assemblaggio su ordine  
* Assemblaggio per magazzino  

## <a name="assemble-to-order" />Assemblaggio su ordine

Utilizza il processo di assemblaggio su ordine per gli articoli che non vuoi immagazzinare. Ad esempio, per i seguenti motivi:

* Personalizzerai gli articoli in base alle esigenze del cliente.
* Vuoi ridurre al minimo il costo dell'inventario disponibile.

L'elenco seguente descrive alcuni dei vantaggi del processo di assemblaggio su ordine:  

* Personalizzare gli articoli di assemblaggio quando si accetta un ordine di vendita.  
* Panoramica della disponibilità dell'articolo di assemblaggio e dei relativi componenti.  
* Impegnare i componenti di assemblaggio immediatamente per garantire l'evasione dell'ordine.  
* Determinare la redditività dell'ordine personalizzato eseguendo il roll up di prezzo e costo.  
* Integrato nella warehouse per facilitare assemblaggio e spedizione.  
* Usare l'assemblaggio su ordine quando crei un'offerta di vendita o un ordine di vendita programmato.  
* Combinare le quantità di magazzino con le quantità per l'assemblaggio su ordine.  

Nel processo di assemblaggio su ordine, si assemblano gli articoli per un ordine di vendita. Esiste un collegamento uno a uno tra l'ordine di assemblaggio e l'ordine di vendita.  

Quando immetti un articolo assemblaggio su ordine in una riga dell'ordine di vendita, un ordine di assemblaggio viene automaticamente creato. L'ordine di assemblaggio è basato sulla riga di vendita e le righe sono basate sulla DBA di assemblaggio dell'articolo. La quantità di componenti nella distinta base di assemblaggio viene moltiplicata per la quantità dell'ordine. La pagina **Righe assemblaggio su ordine** mostra i dettagli sulle righe dell'ordine di assemblaggio collegate. I dettagli possono aiutarti a personalizzare l'articolo di assemblaggio. La data di consegna è basata sulla disponibilità dei componenti. Per ulteriori informazioni sull'assemblaggio degli articoli per ordini di vendita, vai a [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
> Benché non rientri nel processo predefinito, è possibile vendere le quantità di magazzino e le quantità di assemblaggio su ordine nello stesso ordine di vendita. Per ulteriori informazioni sulla combinazione di articoli in stock e assemblaggio su ordinazione, vai a [Vendere gli articoli di magazzino nei flussi da assemblare su ordine](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

Per specificare che un articolo è assemblato su ordinazione, nel campo **Criteri di assemblaggio** della pagina **Scheda articolo** per l'articolo, scegli **Assemblaggio su ordine**.  

## <a name="assemble-to-stock" />Assemblaggio per magazzino

Utilizza il processo di assemblaggio per magazzino per gli articoli che si assemblano e si immagazzinano per vendite future. Gli articoli assemblaggio per magazzino sono articoli standard, come i kit confezionati, che non si personalizzano. È inoltre possibile consumare questi articoli come componenti di sottoassemblaggio. Gli articoli vengono prelevati ed elaborati come singoli articoli e trattati come articoli finiti di produzione. Per ulteriori informazioni sugli articoli di assemblaggio, vai a [Articoli di assemblaggio](assembly-how-to-assemble-items.md).  

Quando specifichi un articolo con assemblaggio per magazzino in una riga vendita, l'articolo viene trattato come qualsiasi altro articolo venduto da magazzino. Ad esempio, [!INCLUDE [prod_short](includes/prod_short.md)] controlla la disponibilità solo per l'articolo assemblato e non per i suoi componenti.  

> [!NOTE]  
> Benché non rientri del processo predefinito, è possibile assemblare un articolo su ordine anche se è impostato per l'assemblaggio per magazzino. Per ulteriori informazioni vedi [Vendere articoli di assemblaggio su ordine e articoli di magazzino insieme](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Per specificare che un articolo è assemblato per magazzino, nel campo **Criteri di assemblaggio** della pagina **Scheda articolo** per l'articolo, scegli **Assemblaggio per magazzino**.  

## <a name="combination-scenarios" />Scenari di combinazione

Quando le quantità di assemblaggio su ordine e per magazzino vengono combinate in un ordine di vendita, le quantità di assemblaggio su ordine devono essere spedite per prime.  

Se un ordine di assemblaggio è collegato a una riga ordine di vendita, il valore del campo **Qtà per assemblaggio su ordine** nella riga ordine di vendita viene copiato nel campo **Quantità da assemblare** tramite il campo **Quantità** nell'intestazione dell'ordine di assemblaggio. Per ulteriori informazioni vedi [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).  

Il valore nel campo **Quantità da assemblare** è correlato al campo **Qtà. da spedire** nella riga ordine di vendita. Questa relazione gestisce la modalità di spedizione di quantità parziali e complete da assemblare su ordine:

* Quando l'intera quantità nella riga ordine di vendita viene assemblata su ordine
* In scenari di combinazione in cui una parte della quantità è assemblata su ordine e un'altra parte viene spedita dal magazzino.

Lo scenario di combinazione consente flessibilità per le spedizioni parziali. Puoi utilizzare il campo **Quantità da assemblare** per specificare la quantità da spedire parzialmente dal magazzino e dall'assemblaggio all'ordine.  

Se la quantità completa della riga di vendita deve essere assemblata su ordine e spedita, il valore del campo **Qtà da spedire** viene copiato nel campo **Quantità da assemblare** nell'ordine di assemblaggio collegato quando si modifica la quantità da inviare. Questo aggiornamento garantisce che la quantità spedita sia totalmente fornita dalla quantità per l'assemblaggio su ordine.  

Tuttavia, negli scenari di combinazione, il valore completo del campo **Qtà da spedire** non viene copiato nel campo **Quantità da assemblare** nell'ordine di assemblaggio. Viene invece inserito un valore predefinito nel campo **Quantità da assemblare**. Il valore è calcolato dal campo **Qtà. da spedire** per garantire che le quantità da assemblare su ordine vengano spedite per prime.

Per deviare da questa impostazione predefinita, ad esempio perché vuoi assemblare solo una quantità maggiore o minore di quella specificata nel campo **Qtà da spedire**, puoi modificare il campo **Quantità da assemblare** in base a regole predefinite, come illustrato di seguito.  

Un esempio del motivo per cui è consigliabile modificare la quantità da assemblare è la possibilità di registrare parzialmente la spedizione di quantità di magazzino prima che possa essere spedito l'output di assemblaggio.  

Le seguenti tabelle illustrano le regole che definiscono i valori minimo e massimo che è possibile immettere nel campo **Quantità da assemblare** per deviare dal valore di default in uno scenario di combinazione. La tabella viene visualizzata in uno scenario di combinazione in cui il campo **Qtà da spedire** nella riga ordine di vendita collegato viene modificato da 7 a 4 e nel campo **Quantità da assemblare** viene immesso di default il valore 4.  

**Riga ordine vendita**

|                | **Quantità** | **Qtà da spedire** | **Qtà per assemblaggio su ordine** | **Quantità spedita** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Valore iniziale**| 10          | 7                | 7                             | 0                    |
|**Modifica**      |              | 4                |                               |                      |

**Testata ordine di assemblaggio**

|                | **Quantità** | **Qtà da spedire** | **Qtà per assemblaggio su ordine** | **Quantità spedita** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Valore iniziale**| 7           | 7                | 0                             | 7                    |
|**Modifica**      |              | 4 (immesso di default)|                         |                      |

Sulla base di questo esempio, è possibile modificare il campo **Quantità da assemblare** come segue:  

* La quantità minima che è possibile immettere è 1. È necessario assemblare almeno un'unità per poter vendere le quattro unità, presupponendo che le tre restanti siano disponibili in magazzino.  
* La quantità massima che è possibile immettere è 4. Questo limite garantisce di non assemblare più articoli di quelli necessari per la vendita.  

## <a name="see-related-microsoft-training" />Vedi il relativo [training Microsoft](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also" />Vedere anche

[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare le distinte base assemblaggio](assembly-how-work-assembly-boms.md)  
[Magazzino](inventory-manage-inventory.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
