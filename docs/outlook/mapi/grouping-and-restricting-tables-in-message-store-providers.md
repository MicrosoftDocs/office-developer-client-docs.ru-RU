---
title: Группировка и ограничение таблиц в поставщиках хранилищ сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ec1c07a8d2c88680ebd94cf8ecd6901ed86ad100
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578789"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Группировка и ограничение таблиц в поставщиках хранилищ сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения часто позволяют пользователям управлять способ отображения содержимого папки. Как правило пользователь можно выбрать для сообщений, сгруппированных по значение одного или нескольких свойств сообщения или исключить сообщения, которые соответствуют определенным условиям. Это делается с помощью [IMAPITable: IUnknown](imapitableiunknown.md) интерфейса. Клиентские приложения можно ограничить строк, возвращенных из таблицы для любой пользователь вводит условия. Таким образом сообщение хранилища поставщика необходимо реализовать следующие методы **IMAPITable** . 
  
|IMAPITable ** метод **|**Описание**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Возвращает таблицы строк, которые соответствуют определенным условиям.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Возвращает набор столбцов в таблице или наборы столбцов, используемых в настоящее время.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Возвращает один или несколько строк из таблицы, начиная с заданной позиции.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Применяет ограничение в таблицу, чтобы последующие вызовы **FindRow** возвращать только строки, соответствующие ограничение.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Указывает, какие столбцы должны возвращаться при строки извлекаются из таблицы.  <br/> |
   
Ограничения может быть сложной для реализации; Для получения дополнительных сведений обратитесь к разделу [О ограничения](about-restrictions.md). Дополнительные сведения о реализации таблицы [MAPI](mapi-tables.md)см.
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

