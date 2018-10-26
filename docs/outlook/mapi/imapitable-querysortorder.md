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
ms.openlocfilehash: 48ca692779fb53cab386d8a18b5f0a50e11d531c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569437"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает текущий порядок сортировки для таблицы.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Параметры

 _lppSortCriteria_
  
> [out] Указатель на указатель на структуру [SSortOrderSet](ssortorderset.md) , содержащую текущий порядок сортировки. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Порядок сортировки успешно возвращен.
    
MAPI_E_BUSY 
  
> В, не позволяющей операции извлечения порядок сортировки запуск выполняется другой операции. В процессе выполнения операции должны выполнить либо должна быть остановлена.
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::QuerySortOrder** получает текущий порядок сортировки для таблицы. Порядок сортировки, описаны в структуру [SSortOrderSet](ssortorderset.md) . 
  
- Член **cSorts** структуры **SSortOrderSet** можно задать нулевое значение, если: 
    
- В таблице приведен без сортировки.
    
- Нет информации о порядок сортировки таблицы.
    
- Структура **SSortOrderSet** не подходит для описания порядка сортировки. 
    
## <a name="notes-to-implementers"></a>Примечания для реализующих

Если вызывается метод [IMAPITable::SortTable](imapitable-sorttable.md) с структуру **SSortOrderSet** , содержащую ноль столбцов в ключ сортировки, удалите текущий порядок сортировки и применить порядок по умолчанию, если он существует. В последующие вызовы **QuerySortOrder**можно выбрать, нужно ли возвращать ноль или больше столбцов для ключа сортировки. Можно вернуть больше столбцов, чем в наличии представления.
  
Дополнительные сведения о сортировке см [категоризации](sorting-and-categorization.md).
  
## <a name="see-also"></a>См. также



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

