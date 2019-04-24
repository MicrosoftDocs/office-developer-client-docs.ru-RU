---
title: Группировка и ограничения таблиц в поставщиках хранилищ сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299414"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Группировка и ограничения таблиц в поставщиках хранилищ сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения часто позволяют пользователям управлять способом отображения содержимого папки. Как правило, пользователи могут группировать сообщения в соответствии со значением одного или нескольких свойств сообщения или могут исключать сообщения, соответствующие определенным условиям. Это делается с помощью интерфейса [IMAPITable: IUnknown](imapitableiunknown.md) . Клиентские приложения могут запрещать строкам, возвращаемым из таблицы, любые критерии, заданные пользователем. Поэтому поставщику хранилища сообщений необходимо реализовать следующие методы **IMAPITable** . 
  
|Метод IMAPITable * * * *|**Описание**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Возвращает строки таблицы, которые отвечают заданным условиям.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Возвращает набор столбцов в таблице или набор столбцов, используемых в текущий момент.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Возвращает одну или несколько строк из таблицы, начиная с заданной позиции.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |ПриМеняет ограничение к таблице, чтобы последующие вызовы метода **FindRow** возвращали только строки, соответствующие ограничению.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Указывает, какие столбцы должны возвращаться при извлечении строк из таблицы.  <br/> |
   
Ограничения могут быть сложными для реализации; более подробную информацию можно узнать в статье [ограничения](about-restrictions.md). Дополнительные сведения о реализации таблиц содержатся в статье [MAPI Tables](mapi-tables.md).
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

