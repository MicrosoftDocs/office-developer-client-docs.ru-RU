---
title: Группировка и ограничение таблиц в поставщиках store сообщений
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
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Группировка и ограничение таблиц в поставщиках store сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения часто позволяют пользователям контролировать отображение содержимого папки. Как правило, пользователь может выбрать группу сообщений в соответствии со значением одного или более свойств сообщения или исключить сообщения, которые соответствуют определенным критериям. Для этого используется интерфейс [IMAPITable : IUnknown.](imapitableiunknown.md) Клиентские приложения могут ограничить строки, возвращенные из таблицы, любыми критериями, заданными пользователем. Поэтому поставщику store сообщений необходимо реализовать следующие методы **IMAPITable.** 
  
|Метод IMAPITable** **|**Описание**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Возвращает строки таблиц, которые соответствуют заданным условиям.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Возвращает набор столбцов в таблице или набор используемых в настоящее время столбцов.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Возвращает одну или несколько строк из таблицы, начиная с заданной позиции.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Применяет ограничение к таблице, чтобы последующие вызовы **FindRow** возвращали только строки, которые соответствуют ограничению.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Указывает, какие столбцы должны возвращаться при извлечении строк из таблицы.  <br/> |
   
Реализация ограничений может быть сложной; дополнительные сведения [см. в сведениях об ограничениях.](about-restrictions.md) Дополнительные сведения о реализации таблиц см. в [таблицах MAPI.](mapi-tables.md)
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

