---
title: Cercare dati specifici
description: Puoi utilizzare la ricerca quando vuoi trovare un record specifico.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: data, search, record
ms.search.form: ''
ms.date: 09/20/2022
ms.author: bholtorf
ms.openlocfilehash: a97668a12b6571b11b21a56f0737a8aea9387b01
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: it-CH
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608401"
---
# <a name="search-for-a-record-in-your-data"></a>Cercare un record nei dati

Quando vuoi trovare un record o un valore particolare, usa la funzionalità **Cerca dati** per cercarlo. Avvia una ricerca in Gestione ruolo utente nei seguenti modi:

* Utilizza l'azione **Cerca dati**
* Usa la combinazione di tasti di scelta rapida CTRL+ALT+F.

## <a name="how-search-works"></a>Come funziona la ricerca

Dopo aver inserito le parole chiave, [!INCLUDE[prod_short](includes/prod_short.md)] avvia la ricerca in background e scorre ogni tabella una alla volta. I risultati della ricerca iniziano a comparire dopo aver terminato ogni tabella. 

Se inserisci più di una parola chiave, i risultati includeranno solo i record che contengono tutte le parole in uno qualsiasi dei campi selezionati.

La pagina dei risultati mostra i tre record aggiornati più di recente. Se ce ne sono più di tre, puoi scegliere **Mostra tutto** per visualizzarli.

Ogni volta che scegli un risultato di ricerca, aumenti la popolarità della tabella e apparirà più in alto nei risultati. Inoltre, il record verrà trovato più rapidamente se lo cerchi in futuro.

> [!NOTE]
> Le intestazioni sui documenti di vendita, acquisto e servizio rappresentano in realtà diversi tipi di documenti, come preventivi, fatture e ordini. Le intestazioni vengono trattate come se fossero tabelle. Se la tua parola chiave è stata trovata in una riga di uno di questi documenti, quando scegli il risultato della ricerca viene visualizzata la pagina del documento e non solo la riga.

## <a name="getting-started"></a>Introduzione

Puoi velocizzare i risultati scegliendo i campi delle tabelle che vuoi includere nelle tue ricerche. Le tabelle e i campi tra cui puoi scegliere variano a seconda della Gestione ruolo utente. Per impostazione predefinita, vengono scelte tutte le tabelle e i campi, il che può rallentare la ricerca. Ti consigliamo di escludere quante più tabelle e campi possibile.

## <a name="see-also"></a>Vedi anche

[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Immissione di dati](ui-enter-data.md)  