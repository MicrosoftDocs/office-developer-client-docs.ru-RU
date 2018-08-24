---
title: Определение окончания таблицы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f9979baf144b6106adcec416ee04439404e05d19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576346"
---
# <a name="determining-a-tables-end"></a>Определение окончания таблицы

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 Распространенные ошибки — это предполагается, что конец таблицы достигнут когда: 
  
- [IMAPITable::QueryRows](imapitable-queryrows.md) вызван в цикле с конца цикла определяется число строк, возвращаемых [IMAPITable::GetRowCount](imapitable-getrowcount.md). Число, которое возвращает **GetRowCount** не всегда представляет точное количество строк в таблице. Это приблизительное число. 
    
- **QueryRows** вызван с заданное количество строк и возвращенных меньшего числа строк. Это не до **QueryRows** возвращает набор с число строк, равное нулю, нет несколько строк для извлечения строк. 
    
> [!IMPORTANT]
> Единственный случай, когда Звонящий можно допустить, что курсор расположен в конце таблицы для число строк положительное или в начале таблицы для количество отрицательных строк — при возвращении значение S_OK и нуль строк. Никогда не возвращается значение MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

