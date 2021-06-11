---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430597"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет полезные методы работы со столами. MAPI предоставляет объекты или объекты данных таблиц, которые реализуют **ITableData,** чтобы помочь поставщикам услуг выполнять обслуживание таблиц. Чтобы получить объект данных таблицы, поставщики услуг называют [функцию CreateTable.](createtable.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Подвергается:  <br/> |Объекты данных таблицы  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPITableData  <br/> |
|Тип указателя:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Создает представление таблицы, возвращая указатель в [реализацию IMAPITable.](imapitableiunknown.md)  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Вставляет новую строку таблицы, возможно, заменив существующую строку.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Удаляет строку таблицы.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Извлекает строку таблицы.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Извлекает строку в зависимости от ее положения в таблице.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Отправляет уведомление для строки таблицы.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Вставляет строку таблицы.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Вставляет несколько строк таблицы, возможно, заменяя существующие строки.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Удаляет несколько строк таблицы.  <br/> |
   
## <a name="remarks"></a>Примечания

Реализация MAPI **ITableData** работает со таблицами, удерживая все данные и связанные ограничения в памяти, что делает его непригодным для использования с очень большими таблицами. Большие ограничения и сложные операции, такие как классификация, не поддерживаются. 
  
Объекты данных таблиц определяют строки с помощью столбца индекса, свойства, которое гарантированно имеет уникальное значение для каждой строки. Большинство поставщиков услуг используют **свойство** [PR_INSTANCE_KEY (PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)в качестве столбца индекса. Свойства с несколькими значениями не могут использоваться в качестве столбца индекса.
  
Объекты данных таблицы создают одно уведомление независимо от количества строк, затронутых изменением или удалением. Если целевая строка в операции не существует, добавляется строка.
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

