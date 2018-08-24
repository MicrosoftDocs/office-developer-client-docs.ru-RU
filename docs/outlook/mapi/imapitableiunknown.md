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
ms.openlocfilehash: a5504711bdeac4ef94cbe47395ceb8163b60ad68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584333"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит сведения о таблицы только для чтения. **IMAPITable** используется клиентами и поставщиков услуг для работы с внешний вид таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Список таблиц  <br/> |
|Реализованный:  <br/> |Поставщиков услуг и MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения, поставщиков услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPITable  <br/> |
|Тип указателя:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения о предыдущем ошибки в таблице.  <br/> |
|[Уведомить](imapitable-advise.md) <br/> |Регистрация для получения уведомлений о влияния на таблице указанных событий.  <br/> |
|[Unadvise](imapitable-unadvise.md) <br/> |Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода **IMAPITable::Advise** .  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Возвращает состояние в таблице и тип.  <br/> |
|[Метода SetColumns](imapitable-setcolumns.md) <br/> |Определяет конкретного свойства и порядок свойств в виде столбцов в таблице.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Возвращает список столбцов для таблицы.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Возвращает общее число строк в таблице.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Перемещение курсора в определенное место в таблице.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Перемещение курсора в приблизительно, например дробная позицию в таблице.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Получает текущую позицию строки в таблице курсора на основании дробное значение.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Находит следующую строку в таблице, которая соответствует определенным условиям поиска.  <br/> |
|[Ограничить](imapitable-restrict.md) <br/> |Применение фильтра к таблице, уменьшение строки, задайте значение только строк, соответствующих определенным условиям.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Помечает текущую позицию в таблице.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Освобождает память, связанную с закладку.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Упорядочивает строки в таблице, на основе критерия сортировки.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Получает текущий порядок сортировки для таблицы.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Возвращает один или несколько строк из таблицы, начиная с текущей позиции курсора.  <br/> |
|[Прервать](imapitable-abort.md) <br/> |Останавливает асинхронной операции в данный момент для таблицы.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |При развертывании категории свернутые таблицы, добавление конечные строки, относящегося к категории, которую требуется в табличном представлении.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Сворачивание категорию расширенной таблицы, удаление конечные строки, относящегося к категории из в табличном представлении.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Приостанавливает работу до завершения одного или нескольких асинхронной операции выполняется в таблице.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Возвращает данные, необходимые для перестроения текущего свернут или развернут состояние форматирование таблицы.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Заново создает текущее развернутое или свернутое состояние форматирование таблицы с использованием данных, сохраненный во время предыдущего вызова метода **IMAPITable::GetCollapseState** .  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

