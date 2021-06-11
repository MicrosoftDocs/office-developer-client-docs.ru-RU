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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает текущий порядок сортировки для таблицы.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Parameters

 _lppSortCriteria_
  
> [вышел] Указатель на указатель на [структуру SSortOrderSet](ssortorderset.md) с текущим порядком сортировки. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Текущий порядок сортировки был успешно возвращен.
    
MAPI_E_BUSY 
  
> В настоящее время продолжается еще одна операция, которая не позволяет начать операцию ирисовки сортировки. Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::QuerySortOrder** извлекает текущий порядок сортировки для таблицы. Заказы сортировки описываются со структурой [SSortOrderSet.](ssortorderset.md) 
  
- Член **cSorts** структуры **SSortOrderSet** может быть установлен до нуля, если: 
    
- Таблица несортовка.
    
- Сведений о сортировке таблицы нет.
    
- Структура **SSortOrderSet** не подходит для описания порядка сортировки. 
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вызов выполнен в [методе IMAPITable::SortTable](imapitable-sorttable.md) со структурой **SSortOrderSet,** содержащей нулевые столбцы в ключе сортировки, удалите текущий порядок сортировки и примените порядок по умолчанию, если он есть. В последующих вызовах **в QuerySortOrder** можно выбрать, возвращать ли ноль или больше столбцов для ключа сортировки. Вы можете вернуть больше столбцов, чем в настоящем представлении.
  
Дополнительные сведения о сортировке см. в [рубрике Сортировка и классификация.](sorting-and-categorization.md)
  
## <a name="see-also"></a>См. также



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

