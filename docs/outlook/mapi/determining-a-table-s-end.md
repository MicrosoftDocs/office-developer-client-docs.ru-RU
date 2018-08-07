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
ms.openlocfilehash: 7cbf11f16948d582ba36a0b4d20411549b723b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808287"
---
# <a name="determining-a-tables-end"></a>Определение окончания таблицы

  
  
**Относится к**: Outlook 
  
 Распространенные ошибки — это предполагается, что конец таблицы достигнут когда: 
  
- [IMAPITable::QueryRows](imapitable-queryrows.md) вызван в цикле с конца цикла определяется число строк, возвращаемых [IMAPITable::GetRowCount](imapitable-getrowcount.md). Число, которое возвращает **GetRowCount** не всегда представляет точное количество строк в таблице. Это приблизительное число. 
    
- **QueryRows** вызван с заданное количество строк и возвращенных меньшего числа строк. Это не до **QueryRows** возвращает набор с число строк, равное нулю, нет несколько строк для извлечения строк. 
    
> [!IMPORTANT]
> Единственный случай, когда Звонящий можно допустить, что курсор расположен в конце таблицы для число строк положительное или в начале таблицы для количество отрицательных строк — при возвращении значение S_OK и нуль строк. Никогда не возвращается значение MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

