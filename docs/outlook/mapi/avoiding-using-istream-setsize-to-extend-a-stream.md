---
title: Избегание использования IStreamSetSize для расширения потока
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428916"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Избегание использования IStream::SetSize для расширения потока

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
При записи в потоки иногда необходимо увеличить их, так как их первоначального размера уже недостаточно. Используйте метод OLE **IStream::Write,** чтобы выполнить это, а не **IStream::SetSize**. **IStream::Write** автоматически расширяет поток, что делает ** IStream::SetSize ** ненужным. Вызов **IStream::Write** без **IStream::SetSize** может быть в три раза быстрее, чем сделать **вызов SetSize** до **записи**.
  

