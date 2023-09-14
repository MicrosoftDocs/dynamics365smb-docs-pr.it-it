---
title: Impostare condizioni interessi finanziari
description: Informazioni su come impostare Business Central in modo da poter informare i clienti degli addebiti aggiuntivi inviando note addebito interessi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge'
ms.search.form: '6, 494'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Impostare condizioni interessi finanziari

Quando un cliente non effettua il pagamento entro la data di scadenza, è possibile fare in modo che gli addebiti per interessi vengano calcolati automaticamente e aggiunti agli importi insoluti nel conto del cliente. È possibile informare i clienti degli interessi aggiunti mediante l'invio di note di addebito interessi. Tuttavia, impostare dapprima un codice che rappresenta ogni calcolo di addebito interessi. Immettere quindi questo codice nel campo Codice condizioni di addebito interessi nelle schede cliente.  

## Condizioni interessi finanziari

È necessario impostare le condizioni interessi finanziari per ogni calcolo di addebito interessi e quindi assegnare le condizioni nel campo **Codice condizioni di addebito interessi** nella pagina **Cliente**.

È possibile calcolare gli addebiti interessi utilizzando il metodo del saldo giornaliero medio oppure il metodo del saldo dovuto.

* Saldo giornaliero medio  
  
  Viene considerato il numero di giorni che il pagamento è dovuto:  
  *Metodo Saldo giornaliero medio* - *Addebito interessi* = *Importo insoluto* x *(Giorni in arretrato / Periodo di interesse)* x *(Tasso di interesse/100)*

* Saldo scaduto  
  
  L'addebito interessi è una percentuale dell'importo insoluto:  
  *Metodo del saldo dovuto* - *Addebito interessi* = *Importo insoluto* x *(Tasso di interesse / 100)*

Inoltre ogni condizione nella tabella Condiz.Interessi Finanziari è collegata a una sottotabella, detta tabella Testi addebiti interessi. Per ciascun gruppo di condizioni interessi finanziari, è possibile creare un testo iniziale e/o uno finale da includere nella nota di addebito degli interessi.

### Per impostare le condizioni di addebito degli interessi

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Condiz. interessi finanziari**, quindi scegli il collegamento correlato.  
2. Compilare i campi, se necessario.
3. Per utilizzare più di una combinazione di condizioni interessi finanziari, impostare un codice per ciascuno di essi.

    Per ogni condizione di interessi finanziari, è possibile specificare singole condizioni, tra cui oneri addizionali sia in VL sia in valuta estera. È possibile definire oneri addizionali in valuta estera per ogni condizione nella pagina **Condiz. interessi finanziari**.
4. Scegliere l'azione **Valute**.
5. Nella pagina **Valute per addebito interessi**, specificare per ogni termine un codice valuta e un onere addizionale.

    > [!NOTE]  
    > Creando addebiti di interessi in una valuta estera, le condizioni per la valuta estera impostate qui verranno utilizzate per creare note di addebito interessi. Se non sono state impostate condizioni interessi finanziari in valuta estera, verranno utilizzate le condizioni interessi finanziari in valuta locale specificate nella pagina **Condiz. interessi finanziari** e quindi convertite nella relativa valuta.

    Per ciascuna condizione di interessi finanziari è possibile specificare il testo che sarà stampato prima (**Testo Iniziale**) o dopo (**Testo Finale**) nei movimenti nella nota di addebito di interessi.  
6. Scegliere rispettivamente le azioni **Testo iniziale** o **Testo finale** e compilare la pagina **Testi addebiti interessi**.
7. Per inserire automaticamente i relativi valori nel testo di addebito di interessi risultante, fornire seguenti segnaposti nel campo **Testo**.

|Segnaposto|Valore|  
|-----------------|-----------|  
|%1|Contenuto del campo **Data documento** della testata della nota di addebito interessi|  
|%2|Contenuto del campo **Data scadenza** della testata della nota di addebito interessi|  
|%3|Contenuto del campo **Tasso di interesse** nelle condizioni di addebito degli interessi finanziari correlate|  
|%4|Contenuto del campo **Importo residuo** della testata della nota di addebito interessi|  
|%5|Contenuto del campo **Importo interessi** della testata della nota di addebito interessi|  
|%6|Contenuto del campo **Onere addizionale** della testata della nota di addebito interessi|  
|%7|Importo totale del sollecito|  
|%8|Contenuto del campo **Codice valuta** della testata della nota di addebito interessi|  
|%9|Contenuto del campo **Data reg.** della testata della nota di addebito interessi|  

## Vedi il relativo [training Microsoft](/training/modules/send-memos-dynamics-365-business-central/)

## Vedere anche

[Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md)  
[Impostare i termini e i livelli di sollecito](finance-setup-reminders.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
