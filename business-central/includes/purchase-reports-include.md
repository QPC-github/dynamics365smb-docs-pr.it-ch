---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ae96e5a3fc1cc7f4b17e5ef208650248cbe0b3c2
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: it-CH
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104419"
---
La tabella seguente descrive alcuni dei report di acquisto chiave.

|Report |ID oggetto|Descrizione  |
|---------|---------|---------|
|**Statistiche acquisti**|312|[!INCLUDE [reports-purchase-statistics](reports-purchase-statistics.md)]|
|**Fornitore - Lista primi 10**|311|Mostra informazioni sugli acquisti dai fornitori in un determinato periodo. È possibile scegliere il numero di fornitori da includere nel report.<br>I fornitori sono ordinati secondo l'importo ed è possibile scegliere se ordinarli per importo acquisto o saldo. Il report offre una panoramica dei fornitori da cui si acquista di più o di cui si è maggiormente debitori.|
|**Catalogo degli articoli del venditore** o **Catalogo articolo/fornitore**|320 oppure 720|Visualizza un elenco dei fornitori per gli articoli selezionati o gli articoli per i fornitori selezionati. Per ciascuna combinazione articolo/fornitore vengono indicati il costo unitario diretto, il calcolo del lead time e il numero articolo del fornitore.<br>Negli Stati Uniti, in Canada e in Messico, questo report non è disponibile. Invece, usa il report **Catalogo articolo/fornitore** (10164).|
|**Acquisti fornitore/articolo**|313|Viene visualizzata una lista di movimenti articoli per ogni fornitore in un determinato periodo. Il report contiene informazioni su quantità fatturata, importo e possibili sconti. Può essere utilizzato, ad esempio, per analizzare gli acquisti articoli adottati da una società e per indicare se esiste una relazione tra gli sconti e gli acquisti dell'articolo.|
|**Costo magazzino e listino prezzi**|716|Visualizza una lista di informazioni relative ai prezzi degli articoli o delle unità di stockkeeping selezionati: costo unitario diretto, ultimo costo diretto, prezzo unitario, percentuale di profitto e profitto.|
|**Magazzino - Piano disponibilità**|707|Se desideri avere una panoramica su articoli/unità di stoccaggio specifici e sulla loro disponibilità. Questo report mostrerà i valori cumulati come i fabbisogni lordi, le entrate pianificate e pianificate, l'inventario e così via. |
|**Acquisti fornitore inventario**|714|Visualizza una lista dei fornitori dai quali sono stati acquistati degli articoli in un determinato periodo. Le informazioni visualizzate riguardano le quantità fatturate, gli importi e gli sconti. Il report può essere utilizzato per un'analisi degli acquisti in relazione a singoli articoli.|
|**Ordini acquisto magazzino**|709|Visualizza un elenco degli articoli contenuti in ordini fornitore. Viene inoltre indicata la data di consegna prevista, nonché la quantità e l'importo di ordini in ritardo. Ad esempio, utilizzare questo report per verificare la data di consegna prevista per gli articoli ordinati e per decidere l'emissione di eventuali solleciti per gli ordini in ritardo.|
|**Disponibilità impegno acquisto**|409|Mostra la disponibilità di articoli da spedire sui documenti di acquisto, ad esempio gli ordini di reso. È possibile stabilire che nel report venga indicato lo stato di ciascun documento o di ciascuna riga di acquisto. <br>Quando si stampa il report, la quantità disponibile per la spedizione può essere automaticamente immessa nel campo **Qtà da Ricevere** delle righe acquisti. Nelle note credito acquisto e nelle righe negative degli ordini di acquisto, il campo **Qtà da Ricevere** è indicata la quantità da spedire. Il report può quindi essere utilizzato per determinare quali documenti spedire. **Nota** : questo report non è disponibile per la funzionalità di warehouse avanzata.|
<!--|**Dettaglio scadenziario fornitori**|11006| DACH specifico: un report che potrebbe essere utilizzato dal capo squadra del reparto acquistato così come la contabilità. Qui avrai una panoramica delle fatture fornitore non pagate, comprese le date di scadenza, le valute e gli importi. La base sono i movimenti contabili fornitori aperti.| -->
