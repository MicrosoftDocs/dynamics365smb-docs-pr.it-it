---
title: Dettagli di progettazione - Pagina righe tracciabilità articolo
description: Informazioni su come gestire il flusso dei numeri seriali e di lotto nel magazzino usando la pagina Righe tracciabilità articolo.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, inventory, item, tracking, serial number, lot number'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-lines-page"></a><a name="design-details-item-tracking-lines-page"></a>Dettagli di progettazione: Pagina righe tracciabilità articolo
I record di tracciabilità articolo e i record di impegno vengono creati nel sistema di impegno e la relativa disponibilità viene calcolata in modo dinamico. I dati che vengono immessi nella pagina **Righe tracciabilità articolo** vengono gestiti in una versione temporanea della tabella **Specifica tracciabilità**. Quando la pagina viene chiusa, viene eseguito il commit dei dati attivi alla tabella **Movimenti impegni** e viene eseguito il commit dei dati storici alla tabella **Specifica tracciabilità**. Per ulteriori informazioni, vedere [Dettagli di progettazione: Movimenti di tracciabilità articolo storici e attivi](design-details-active-versus-historic-item-tracking-entries.md).  
  
Le ricerche dai campi **Nr. seriale** e **Nr. lotto** mostrano la disponibilità in base sia alla tabella **Mov. contabili articoli** sia alla tabella **Movimenti impegni**, senza filtro di data. La matrice dei campi della quantità nell'intestazione della pagina **Righe tracciabilità articolo** visualizza in modo dinamico le quantità e le somme dei numeri di tracciabilità articolo che vengono immesse nelle righe della pagina. Le quantità devono corrispondere a quelle della riga documento, contraddistinta da **0** nei campi **Indefinito** nell'intestazione della pagina.  
  
Per coordinare il flusso dei numeri seriali e di lotto attraverso il magazzino, l'immissione dei dati nella pagina **Righe tracciabilità articolo** segue queste regole:  
  
* Per le righe di tracciabilità articolo in entrata e in uscita, non è possibile immettere un numero seriale, con o senza un numero di lotto, più di una volta nella stessa istanza della pagina **Righe tracciabilità articolo**. Se si tenta di immettere qualsiasi combinazione di numeri seriali o di lotto che sono già presenti nella pagina, un messaggio di errore bloccherà l'immissione dei dati.  
* Per le righe di tracciabilità articolo in entrata, non è possibile registrare il documento correlato se un articolo della stessa variante e con lo stesso numero seriale è già in magazzino. Se si tenta di registrare una riga positiva per un articolo di magazzino con la stessa variante e lo stesso numero seriale, un messaggio di errore bloccherà la registrazione. Tuttavia, per le righe di tracciabilità articoli sia in entrata che in uscita nei documenti aperti, è possibile avere la stessa combinazione di numeri seriali o di lotto correlati a righe di documenti di origine differenti, quindi che esistono in istanze differenti della pagina **Righe tracciabilità articolo**, fino a quando il documento correlato non viene registrato.  
* Se l'articolo è impostato per la tracciabilità specifica a un numero seriale o a un numero di lotto, non è possibile inserire una riga del documento in uscita a meno che in magazzino non esista un articolo con il numero seriale o di lotto definito. Se si tenta di registrare una riga di documento in uscita per un articolo con un numero seriale o di lotto non presente in magazzino, un messaggio di errore bloccherà la registrazione.  
  
Le regole per l'immissione dei dati nella pagina **Righe tracciabilità articolo** supportano anche i principi di associazione che regolano la tracciabilità ordine, la pianificazione e l'impegno. Per ulteriori informazioni, vedere [Dettagli di progettazione: Tracciabilità articolo e pianificazione](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a><a name="see-also"></a>Vedi anche
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
