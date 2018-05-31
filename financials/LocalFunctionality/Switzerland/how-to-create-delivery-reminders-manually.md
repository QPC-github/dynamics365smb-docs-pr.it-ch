---
title: Come creare solleciti di consegna manualmente
description: In ADD INCLUDE<!--[!INCLUDE[navnow](../../includes/how-to-generate-delivery-reminders.md).
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 7e82038dc676da036419b47f9685b3678ce8d06e
ms.contentlocale: it-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-delivery-reminders-manually"></a>Creare solleciti di consegna manualmente
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], è possibile creare solleciti di consegna quando un acquisto non è stato consegnato come previsto. È possibile creare un singolo sollecito di consegna manualmente o generare solleciti di consegna per tutte le consegne scadute. Per ulteriori informazioni, vedere [Generare solleciti di consegna](how-to-generate-delivery-reminders.md).

> [!NOTE]
> Per creare solleciti di consegna, è necessario impostare le proprietà relative. Per ulteriori informazioni, vedere [Impostare solleciti di consegna](how-to-set-up-delivery-reminders.md).

## <a name="to-create-a-delivery-reminder-manually"></a>Per creare un sollecito di consegna manualmente  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Sollecito di consegna**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Nella Scheda dettaglio **Generale** della finestra **Sollecito di consegna** compilare i campi come descritto nella tabella seguente.  

    |Campo|Descrizione|  
    |---------------------------------|---------------------------------------|  
    |**Nr.**|Numero di identificazione univoco del sollecito di consegna.|  
    |**N. fornitore**|Numero del fornitore per cui si desidera registrare il sollecito di consegna.<br /><br /> Quando si seleziona il numero fornitore, i campi **Nome**, **Indirizzo**, **NPA/Città** e **Contatto** vengono compilati automaticamente.|  
    |**Data di Registrazione**|Data di registrazione per il sollecito di consegna. Tale data viene copiata in tutti i movimenti contabili relativi al sollecito di consegna.|  
    |**Data Documento**|Data del documento per il sollecito di consegna. Questa data è utilizzata anche per calcolare la data di scadenza per il sollecito di consegna. Se necessario, è possibile modificare la data di registrazione.|  
    |**Livello di sollecito**|Livello del sollecito di consegna. Questo valore si basa sul numero di solleciti di consegna già inviati. Per ulteriori informazioni, vedere [Impostare termini, livelli e testo dei solleciti di consegna](how-to-set-up-delivery-reminder-terms-levels-and-text.md).|  
    |**Cod. termini di sollecito**|Specifica il codice dei termini del sollecito di consegna impostato per il fornitore.|  
    |**Data scad.**|Data di scadenza per il sollecito di consegna.|  

4.  Scegliere l'azione selezionare **Suggerisci riga sollecito**  

    Se per il fornitore specificato sono presenti consegne scadute, queste vengono aggiunte al sollecito di consegna.  

5.  Scegliere il pulsante **OK**.  

    Il sollecito di consegna viene creato. È ora possibile emettere e stampare il sollecito di consegna.  

## <a name="see-also"></a>Vedi anche  
 [Solleciti consegna](delivery-reminders.md)   
 [Generare solleciti di consegna](how-to-generate-delivery-reminders.md)   
 [Impostare solleciti di consegna](how-to-set-up-delivery-reminders.md)   
 [Impostare i termini, i livelli e i testi di sollecito di consegna](how-to-set-up-delivery-reminder-terms-levels-and-text.md)   
 [Assegnare codici di solleciti di consegna ai fornitori](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [Emettere solleciti di consegna](how-to-issue-delivery-reminders.md)   
 [Stampare report di test per i solleciti di consegna](how-to-print-test-reports-for-delivery-reminders.md)
