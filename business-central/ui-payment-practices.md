---
title: Report Procedure di pagamento
description: Scopri come creare facilmente il report Procedure di pagamento per fornitori e clienti.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment, practices, vendor, customer, report'
ms.search.form: '686, 687, 689'
ms.date: 04/23/2024
ms.author: altotovi
--- 

# <a name="payment-practices-report"></a>Report Procedure di pagamento

Alcuni paesi/aree richiedono che le società generino report sui tempi di pagamento per i propri fornitori come definiti dalle autorità locali. Questo reporting può basarsi su diverse fonti e può ordinare i fornitori in base alle loro dimensioni o ai termini di pagamento definiti, fornendo reporting ai fornitori per quanto segue, come richiesto dalle autorità locali:  

- Il periodo di pagamento pattuito medio.  
- Il periodo di pagamento effettivo medio.   
- La percentuale di fatture pagate dopo la fine del periodo di pagamento concordato. 

Gli utenti possono selezionare il periodo per il quale desiderano eseguire un calcolo e trovare i dettagli in base al raggruppamento scelto. Per ciascuno di questi raggruppamenti è possibile trovare i movimenti di origine. 

> [!NOTE]
> Questo reporting è attualmente obbligatorio in alcuni paesi, ma si tratta di una funzionalità globale e può essere utilizzata ovunque. Attualmente, ogni anno le società svedesi con 250 e più dipendenti devono comunicare all'Ufficio svedese di registrazione delle imprese quali tempi di pagamento hanno per gli acquisti da società più piccole di loro. Atti simili esistono nel Regno Unito, in Australia e in Nuova Zelanda.  

## <a name="generate-the-report"></a>Generare il report

Per eseguire il report **Procedure di pagamento**, procedi nel seguente modo:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Procedure di pagamento**, quindi seleziona il collegamento correlato. 
2. Seleziona **Nuovo**.
3. Immetti i valori nei seguenti campi della Scheda dettaglio **Generale**:

   | Campo | Descrizione |
   |---------|-----------------------------------|
   | Nr. | Specifica il numero del movimento o del record per il report. |
   | Tipo di aggregazione | Specifica la modalità di aggregazione dei dati. Se scegli l'opzione **Periodo** il report sarà basato su periodi diversi, ma se scegli l'opzione **Dimensioni società** il report viene creato in base alle dimensioni della società configurate nel campo **Codice dimensioni società** nella scheda **Fornitore**. |
   | Tipo di testata | Specifica la fonte per i movimenti nella procedura di pagamento ed è possibile scegliere Fornitori, Clienti o entrambi. |
   | Data di inizio | Specifica la data di inizio della procedura di pagamento. |
   | Data di fine | Specifica la data di fine della procedura di pagamento. |

> [!NOTE]
> Se decidi di utilizzare l'opzione **Dimensioni società**, devi prima creare movimenti nella pagina **Dimensioni società** e aggiungerli a tutti i fornitori che desideri monitorare con questo metodo.

4. Una volta compilati tutti i campi nell'intestazione, devi eseguire l'azione **Genera** per generare dati nelle righe e statistiche per il tipo di reporting selezionato.
5. In base al **Tipo di aggregazione** otterrai righe diverse. Puoi modificare alcuni valori manualmente, ma in questo caso ciascuna riga modificata e l'intero report verranno contrassegnati come **Modificato manualmente**.
6. Da tutti i campi calcolati, puoi andare più in profondità per vedere come è stato calcolato questo risultato, aprendo la pagina **Lista dati procedura di pagamento**.
7. Se desideri stampare il documento, puoi farlo eseguendo l'azione **Stampa**.

## <a name="see-also"></a>Vedere anche

[Report finanziari](finance-reports.md)  
[Analisi dei rendiconti finanziari in Microsoft Excel](finance-analyze-excel.md)  
[Report di contabilità clienti e analisi](receivables-reports.md)  
[Report di contabilità fornitori e analisi](payables-reports.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Dati finanziari](finance.md)  
[Panoramica delle funzionalità locali](about-localization.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
