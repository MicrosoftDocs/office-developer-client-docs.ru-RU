---
title: IMAPITableQuerySortOrder
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
  
Извлекает текущий порядок сортировки для таблицы.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Параметры

 _lppSortCriteria_
  
> [out] Указатель на указатель на структуру [SSortOrderSet, удерживая](ssortorderset.md) текущий порядок сортировки. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Текущий порядок сортировки был успешно возвращен.
    
MAPI_E_BUSY 
  
> В настоящее время идет другая операция, которая препятствует запуску операции и получения порядка сортировки. Либо операция должна быть завершена, либо она должна быть остановлена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::QuerySortOrder** извлекает текущий порядок сортировки для таблицы. Заказы сортировки описываются в структуре [SSortOrderSet.](ssortorderset.md) 
  
- Для **члена cSorts** структуры **SSortOrderSet** можно установить нулевое значение, если: 
    
- Таблица не отсортна.
    
- Сведения о сортировке таблицы не имеются.
    
- Структура **SSortOrderSet** не подходит для описания порядка сортировки. 
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

При вызове метода [IMAPITable::SortTable](imapitable-sorttable.md) со структурой **SSortOrderSet,** содержащей ноль столбцов в ключе сортировки, удалите текущий порядок сортировки и примените порядок по умолчанию, если он существует. В последующих вызовах **QuerySortOrder** можно выбрать, возвращать ли ноль или больше столбцов для ключа сортировки. Вы можете вернуть больше столбцов, чем в настоящем представлении.
  
Дополнительные сведения о сортировке см. в [теме "Сортировка и классификация".](sorting-and-categorization.md)
  
## <a name="see-also"></a>См. также



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

