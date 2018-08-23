---
title: Предотвращение использования с помощью IStreamSetSize для расширения потока
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9245d4913c2832b8c942093e65cf088643a1947c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592082"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Расширение потока без использования IStream::SetSize

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
При создании потоков, это необходимо увеличить размер, так как их исходный размер больше не достаточно. Используйте метод OLE **IStream::Write** для этого вместо **IStream::SetSize**. **IStream::Write** автоматически расширяет потока, что ** IStream::SetSize ** ненужных. Вызов **IStream::Write** без **IStream::SetSize** может быть до трех раз быстрее, чем внесения **SetSize** звонков до **записи**.
  

