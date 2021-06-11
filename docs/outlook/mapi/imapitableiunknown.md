---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420117"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет представление таблицы только для чтения. **IMAPITable** используется клиентами и поставщиками услуг для управления тем, как отображается таблица. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |Объекты таблицы  <br/> |
|Реализовано в:  <br/> |Поставщики услуг и MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения, поставщики услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPITable  <br/> |
|Тип указателя:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |Возвращает [структуру MAPIERROR, содержащую](mapierror.md) сведения о предыдущей ошибке в таблице.  <br/> |
|[Консультирование](imapitable-advise.md) <br/> |Регистры для получения уведомления о указанных событиях, влияющих на таблицу.  <br/> |
|[Unadvise](imapitable-unadvise.md) <br/> |Отменяет отправку уведомлений, ранее настроенных с помощью вызова метода **IMAPITable::Advise.**  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Возвращает состояние и тип таблицы.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Определяет конкретные свойства и порядок свойств, которые будут отображаться в качестве столбцов в таблице.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Возвращает список столбцов для таблицы.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Возвращает общее количество строк в таблице.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Перемещает курсор в определенное положение в таблице.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Перемещает курсор в приблизительное дробное положение в таблице.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Извлекает текущее положение строки таблицы курсора на основе дробного значения.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Находит следующую строку в таблице, которая соответствует определенным критериям поиска.  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |Применяет фильтр к таблице, уменьшая набор строк только к тем строкам, которые соответствуют указанным критериям.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Отмечает текущее положение таблицы.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Освобождает память, связанную с закладкой.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Заказы строк таблицы на основе критериев сортировки.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Извлекает текущий порядок сортировки для таблицы.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Возвращает одну или несколько строк из таблицы, начиная с текущей позиции курсора.  <br/> |
|[Прервать](imapitable-abort.md) <br/> |Останавливает любые асинхронные операции, которые в настоящее время ведутся для таблицы.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Расширяет категорию обрушения таблицы, добавляя строки листа, принадлежащие этой категории, к представлению таблицы.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Разрушает расширенную категорию таблицы, удаляя строки листа, принадлежащие этой категории, из представления таблицы.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Приостановка обработки до завершения одной или более асинхронных операций в таблице.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Возвращает данные, необходимые для восстановления текущего рухнувшего или расширенного состояния классифицизированной таблицы.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Восстановление текущего расширенного или свернутого состояния таблицы категорий с помощью данных, которые были сохранены при предварительном вызове метода **IMAPITable::GetCollapseState.**  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

