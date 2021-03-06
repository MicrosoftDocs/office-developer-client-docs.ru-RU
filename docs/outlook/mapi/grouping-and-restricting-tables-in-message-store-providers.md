---
title: Группировка и ограничение таблиц в поставщиках магазинов сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428986"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Группировка и ограничение таблиц в поставщиках магазинов сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения часто позволяют пользователям контролировать отображение содержимого папки. Обычно пользователь может выбрать группу сообщений в соответствии со значением одного или более свойств сообщений или исключить сообщения, которые соответствуют определенным критериям. Это делается с помощью [интерфейса IMAPITable : IUnknown.](imapitableiunknown.md) Клиентские приложения могут ограничить строки, возвращаемые из таблицы, любыми критериями, указанными пользователем. Поэтому поставщику магазина сообщений необходимо реализовать следующие **методы IMAPITable.** 
  
|IMAPITable** метод**|**Описание**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Возвращает строки таблиц, которые соответствуют указанным критериям.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Возвращает набор столбцов в таблице или набор используемых в настоящее время столбцов.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Возвращает одну или несколько строк из таблицы, начиная с данной позиции.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Применяет ограничение к таблице, чтобы последующие вызовы **в FindRow возвращали** только строки, которые соответствуют этому ограничению.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Указывает, какие столбцы должны быть возвращены при извлечении строк из таблицы.  <br/> |
   
Ограничения могут быть сложными для реализации; дополнительные сведения см. [в см. в руб. Об ограничениях.](about-restrictions.md) Дополнительные сведения о реализации таблиц см. в [таблице MAPI Tables.](mapi-tables.md)
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

