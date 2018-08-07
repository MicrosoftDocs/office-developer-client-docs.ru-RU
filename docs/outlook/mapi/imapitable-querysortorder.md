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
ms.openlocfilehash: b5eb671be022a6c3aa22e66f68386691fe23b275
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809219"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**Относится к**: Outlook 
  
Получает текущий порядок сортировки для таблицы.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Параметры

 _lppSortCriteria_
  
> [out] Указатель на указатель на структуру [SSortOrderSet](ssortorderset.md) , содержащую текущий порядок сортировки. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Порядок сортировки успешно возвращен.
    
MAPI_E_BUSY 
  
> В, не позволяющей операции извлечения порядок сортировки запуск выполняется другой операции. В процессе выполнения операции должны выполнить либо должна быть остановлена.
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::QuerySortOrder** получает текущий порядок сортировки для таблицы. Порядок сортировки, описаны в структуру [SSortOrderSet](ssortorderset.md) . 
  
- Член **cSorts** структуры **SSortOrderSet** можно задать нулевое значение, если: 
    
- В таблице приведен без сортировки.
    
- Нет информации о порядок сортировки таблицы.
    
- Структура **SSortOrderSet** не подходит для описания порядка сортировки. 
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вызывается метод [IMAPITable::SortTable](imapitable-sorttable.md) с структуру **SSortOrderSet** , содержащую ноль столбцов в ключ сортировки, удалите текущий порядок сортировки и применить порядок по умолчанию, если он существует. В последующие вызовы **QuerySortOrder**можно выбрать, нужно ли возвращать ноль или больше столбцов для ключа сортировки. Можно вернуть больше столбцов, чем в наличии представления.
  
Дополнительные сведения о сортировке см [категоризации](sorting-and-categorization.md).
  
## <a name="see-also"></a>См. также



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

