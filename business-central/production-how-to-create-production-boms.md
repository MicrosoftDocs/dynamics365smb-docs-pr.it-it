---
title: Creare le distinte base di produzione
description: 'Scopri come creare una distinta base di produzione (DB), nuove versioni di una DB di produzione e come utilizzare la formula di calcolo della quantità.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'production bom, bills of material,'
ms.search.form: '911, 912, 917, 9287, 99000786, 99000787, 99000788, 99000789, 99000795, 99000797, 99000800, 99000809, 99000811, 99000812, 99000818'
ms.date: 06/22/2021
ms.author: bholtorf
---
# <a name="create-production-boms"></a><a name="create-production-boms"></a><a name="create-production-boms"></a>Creare le distinte base di produzione

Una distinta base (DB) di produzione contiene i dati master che descrivono i componenti e i sottoassemblaggi utilizzati nella produzione di un articolo padre. Dopo la creazione di un ordine di produzione per l'articolo padre, la relativa DB di produzione determinerà il calcolo delle richieste di materiale come rappresentato nella pagina **Componenti ordine produzione** .

[!INCLUDE[prod_short](includes/prod_short.md)] supporta anche le DB di assemblaggio. Utilizzare gli ordini di assemblaggio per la creazione di articoli finali dai componenti in un semplice processo che può essere svolto da una o più risorse di base, che non sono centri di lavoro o aree di produzione, né privi di risorse. Ad esempio, un processo di assemblaggio potrebbe consistere nel prelevare due bottiglie di vino e un pacchetto di caffè, quindi di imballarli come articolo da regalo. Per ulteriori informazioni, vedere [DB di assemblaggio o DB di produzione](inventory-how-work-boms.md#assembly-boms-or-production-boms).  

> [!TIP]
> L'app **Dati demo Contoso Coffee** include prodotti dimostrativi per una varietà di scenari di distinta base di produzione che possono essere utilizzati in un ambiente di test, anche durante una versione di valutazione. Scopri come configurare i dati di Contoso Coffee e trovare procedure dettagliate per diversi scenari in [Introduzione ai dati demo Contoso Coffee](contoso-coffee/contoso-coffee-intro.md).

Prima di poter configurare un ciclo, è necessario verificare quanto segue:  

- Aver creato schede articolo per gli articoli padre inclusi nella produzione. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).
- Sono state impostate le risorse di produzione. Per ulteriori informazioni, vedere [Impostare aree di produzione e centri di lavoro](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-production-bom"></a><a name="to-create-a-production-bom"></a><a name="to-create-a-production-bom"></a>Per creare una DB di produzione

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **DB produzione**, quindi seleziona il collegamento correlato.  
2. Scegli l'azione **Nuovo**.  
3. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Per modificare la distinta base di produzione, impostare il campo **Stato** su **Nuova** o **In sviluppo**. Per attivarla, impostare lo **Stato** su **Certificato**.  

    Compilare le righe della DB di produzione.
5. Nel campo **Tipo** specificare se l'articolo visualizzato in questa riga della distinta base è un articolo normale o una distinta base di produzione. In tal caso, è necessario che esista già come distinta base di produzione certificata.  
6. Nel campo **Nr.** cercare e selezionare l'articolo o la distinta base di produzione desiderata oppure immetterla nel campo.  
7. Specifica nel campo **Quantità per** il numero di unità di articolo da utilizzare per l'articolo padre, ad esempio quattro ruote per un'automobile.  
8. Nel campo **% scarto** è possibile specificare una percentuale fissa di componenti che verrà scartata nel processo di produzione. Quando i componenti sono pronti per l'utilizzo in un ordine di produzione rilasciato, questa percentuale verrà aggiunta alla quantità prevista, specificata nel campo **Quantità consumi**, nelle registrazioni di produzione. Per ulteriori informazioni, vedere [Registrare consumi e output](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Questa percentuale di scarto rappresenta i componenti scartati durante la produzione, quando si effettua il prelievo dal magazzino, mentre la percentuale di scarto nelle righe ciclo rappresenta l'output scartato, prima dell'inserimento in magazzino.  

9. Nel campo **Cod. legame ciclo-DB**, immettere un codice per connettere il componente a un'operazione specifica. Per ulteriori informazioni, vedere [Per creare collegamenti ciclo](production-how-to-create-routings.md#to-create-routing-links).
10. Per copiare righe di una DB di produzione esistente, scegliere l'azione **Copia DB** per selezionare le righe esistenti.  
11. Certificare la distinta base di produzione.  
12. È ora possibile associare la nuova distinta base di produzione alla scheda dell'articolo padre desiderato. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).  

> [!NOTE]  
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)] Per ricalcolare il costo standard dell'articolo dalla scheda articolo, scegliere l'azione **Produzione**, quindi l'azione **Calc. costo standard**.  

## <a name="to-create-a-new-version-of-a-production-bom"></a><a name="to-create-a-new-version-of-a-production-bom"></a><a name="to-create-a-new-version-of-a-production-bom"></a>Per creare una nuova versione delle DB di produzione

Vengono utilizzate nuove versioni della distinta base, ad esempio nel caso in cui un articolo viene sostituito oppure quando un cliente fa richiesta di una versione particolare del prodotto. Il principio di versione consente di gestire varie versioni di una distinta base di produzione. La struttura della versione della distinta base di produzione corrisponde alla struttura delle distinte base di produzione. La differenza basilare sta nel tempo di validità delle versioni. La validità viene definita dalla data di inizio.  

La data di inizio indica l'inizio del periodo di validità della versione. Costituisce inoltre un elemento che funge da filtro per calcoli e valutazioni. La versione della distinta base è valida fino alla data di entrata in vigore di quella nuova.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **DB produzione**, quindi seleziona il collegamento correlato.  
2. Seleziona la DB di produzione da copiare quindi scegli l'azione **Versioni**.  
3. Scegli l'azione **Nuovo**.  
4. Compila i campi in base alle esigenze.
5. Nel campo **Cod. versione** immettere il codice identificativo univoco della versione. Nel campo è possibile inserire qualsiasi combinazione di numeri o di lettere.  

    Alla versione appena creata viene assegnato automaticamente lo stato **Nuovo**.
6. Quando la versione della DB è completata, scegliere **Certificata** nel campo **Stato**.  

La validità temporale della versione viene specificata nel campo **Data di Inizio**.  

> [!NOTE]  
> Selezionare l'opzione **Articolo** contenuta nel campo **Tipo** per utilizzare un articolo dai dati master della distinta base di produzione. Se l'articolo dispone anche di una DB di produzione, quando vengono inserite informazioni nel campo **Nr. DB di produzione** nella scheda articolo, viene presa in considerazione questa distinta base di produzione.  
>
> Selezionare l'opzione **DB produzione** se si desidera utilizzare una distinta base di produzione fantasma sulla riga.  
>
> Le distinte base fantasma vengono utilizzate per strutturare i prodotti. Questo tipo di distinta base di produzione non dà origine ad alcun prodotto finito, ma viene usata esclusivamente per determinare la domanda dipendente. Le distinte base fantasma non hanno dati principali propri.

## <a name="quantity-calculation-formula-on-production-boms"></a><a name="quantity-calculation-formula-on-production-boms"></a><a name="quantity-calculation-formula-on-production-boms"></a>Formula di calcolo della quantità nelle DB di produzione

La quantità viene calcolata tenendo conto delle diverse dimensioni che sono anch'esse immesse nelle righe delle DB di produzione. Le dimensioni fanno riferimento a un'unità d'ordine per l'articolo corrispondente. È possibile immettere anche lunghezza, larghezza, profondità e peso come dimensioni.  

Le colonne Formula di Calcolo, Lunghezza, Larghezza, Profondità e Peso non vengono visualizzate in quanto utilizzate solo da pochi utenti. Per calcolare la quantità, è necessario prima visualizzare queste colonne.  

La relazione dei singoli componenti viene definita dalla formula di calcolo. Sono disponibili le seguenti formule di calcolo:  

- **Vuoto** - Le dimensioni non vengono considerate. (Quantità = Quantità per)  
- **Lunghezza** - Quantità = Quantità per * Lunghezza  
- **Lunghezza x Larghezza** - Quantità = Quantità per * Lunghezza x Larghezza  
- **Lunghezza x Larghezza x Profondità** - Quantità = Quantità per x Lunghezza x Larghezza x Profondità  
- **Peso** - Quantità = Quantità per x Peso  
- **Quantità fissa** - Quantità = Quantità per

> [!NOTE]
> La formula di calcolo **Quantità fissa** garantisce che il consumo di un componente sia sempre lo stesso, indipendentemente dalle quantità in uscita o di scarto. Per i componenti dell'ordine di produzione, quando il campo **Formula di calcolo** è impostato su **Quantità fissa**, il valore del campo **Quantità prevista** è sempre uguale al campo **Quantità per**. La percentuale di scarto definita sulla stessa riga viene ignorata. La quantità fissa è rispettata dal report **Disponibilità per distinta base**. Il report mostrerà l'articolo come collo di bottiglia se la quantità disponibile è inferiore alla quantità nel campo **Quantità per elemento padre**. I campi **In grado di fare l'elemento padre** e **In grado di fare l'articolo principale** sono sempre vuoti, indipendentemente dalla quantità disponibile. Anche la quantità fissa è inclusa nei calcoli per i costi standard. La dimensione del lotto per l'articolo prodotto incide sul costo allocato per un articolo.

### <a name="example"></a><a name="example"></a><a name="example"></a>Esempio

Una distinta base richiede 70 parti metalliche con le dimensioni Lunghezza = 0,20 m e Larghezza = 0,15 m. I valori vengono immessi come segue: Formula di Calcolo = Lunghezza x Larghezza, Lunghezza = 20, Larghezza = 15, Quantità per = 70. La quantità è data da Quantità per x Lunghezza * Larghezza, ovvero Quantità = 70 x 0,20 m x 0,15 m = 2,1 m2.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Creare cicli](production-how-to-create-routings.md)  
[Gestire le varianti di prodotto](inventory-item-variants.md)  
[Procedura dettagliata: varianti](contoso-coffee/manufacturing/variants.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)  
[Pianif.](production-planning.md)  
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  
[Utilizzare le distinte base assemblaggio](assembly-how-work-assembly-boms.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
