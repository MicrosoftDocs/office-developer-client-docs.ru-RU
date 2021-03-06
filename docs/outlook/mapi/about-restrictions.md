---
title: Об ограничениях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433110"
---
# <a name="about-restrictions"></a>Об ограничениях

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Ограничение — это способ ограничить количество строк в представлении только теми строками со значениями для столбцов, которые соответствуют определенным критериям. Существует множество различных возможностей для использования ограничений со таблицами. Клиентские приложения могут использовать ограничения, например, для фильтрации таблицы контента для сообщений, отправленных конкретным лицом, для поиска строк, которые либо не поддерживают свойство, либо устанавливают свойство к определенному значению, либо для поиска дублирующих получателей в сообщении. 
  
Методы [IMAPITable:::Restrict](imapitable-restrict.md) и [IMAPITable::FindRow](imapitable-findrow.md) используются для набора ограничений на таблице. **Ограничение** применяет ограничение к таблице, не ирисовываясь ни одной строки. Чтобы получить только те строки, которые соответствуют ограничению, требуется последующий вызов [iMAPITable::QueryRows](imapitable-queryrows.md) или аналогичный метод. **FindRow** применяет ограничение и извлекает первую строку в таблице, которая соответствует критериям. **FindRow** применяет временное ограничение, которое существует только на время вызова, в то время как **Ограничение** применяет более постоянное ограничение. 
  
Некоторые клиенты могут создать ограничение с помощью столбцов, которые не находятся в текущем наборе столбцов. Поддержка такого ограничения необязательна, и реализутели таблиц, поддерживающие его, добавляют значение, особенно для таблиц контента. Не поддержав ее, реализутели таблицы могут вернуть  MAPI_E_TOO_COMPLEX из вызова Ограничение или MAPI_E_NOT_FOUND из **вызова FindRow.** 
  
Клиенты должны знать, что даже если поставщик поддерживает ограничения столбцов, не в текущем наборе столбцов, они получат более лучшую производительность, указав столбцы, которые они намерены использовать в своих ограничениях с [IMAPITable::SetColumns](imapitable-setcolumns.md).
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

