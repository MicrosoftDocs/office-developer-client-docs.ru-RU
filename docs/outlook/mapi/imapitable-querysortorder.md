---
title: имапитаблекуерисортордер
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407552"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает текущий порядок сортировки таблицы.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Параметры

 _лппсорткритериа_
  
> вышли Указатель на указатель на структуру [ссортордерсет](ssortorderset.md) , содержащую текущий порядок сортировки. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Текущий порядок сортировки успешно возвращен.
    
MAPI_E_BUSY 
  
> Выполняется другая операция, которая не позволяет запустить операцию извлечения порядка сортировки. Выполнение выполняемой операции должно быть разрешено или остановлено.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable:: куерисортордер** получает текущий порядок сортировки таблицы. Порядок сортировки описан в структуре [ссортордерсет](ssortorderset.md) . 
  
- Элемент **ксортс** структуры **ссортордерсет** может иметь нулевое значение, если: 
    
- Таблица не отсортирована.
    
- Нет сведений о том, как сортируется таблица.
    
- Структура **ссортордерсет** не подходит для описания порядка сортировки. 
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вызывается метод [IMAPITable:: сорттабле](imapitable-sorttable.md) с структурой **ссортордерсет** , содержащей нулевые столбцы в ключе сортировки, удалите текущий порядок сортировки и примените порядок по умолчанию, если таковой имеется. При последующих вызовах **куерисортордер**можно выбрать, возвращать ли ноль или больше столбцов для ключа сортировки. Можно вернуть больше столбцов, чем в указанном представлении.
  
Более подробную информацию о сортировке можно узнать в статье [Сортировка и категоризация](sorting-and-categorization.md).
  
## <a name="see-also"></a>См. также



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

