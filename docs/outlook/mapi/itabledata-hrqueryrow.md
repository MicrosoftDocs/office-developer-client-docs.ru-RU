---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ef0dc212a6a6f761cd8dd0cae5312c548c02ae50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583822"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает строку таблицы.
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>Параметры

 _lpSPropValue_
  
> [in] Указатель на структуру значение свойства, с описанием столбца индекса для строки нужно вернуть. Член **ulPropTag** структуры значение свойства должны содержать один и тот же свойство тег параметра- _ulPropTagIndexColumn_ вызов функции [CreateTable](createtable.md) , которая обращается к реализации [ITableData](itabledataiunknown.md) . 
    
 _lppSRow_
  
> [out] Указатель на указатель извлеченных строк. 
    
 _lpuliRow_
  
> [in, out] На ввод допустимый указатель или значение NULL, который означает необходимость сведения не должно быть возвращено. Выходные данные, допустимый указатель, указывающий на номер строки строки, порядковый номер, идентифицирующий положение строки в таблице.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строка был успешно извлечен.
    
MAPI_E_INVALID_PARAMETER 
  
> [SPropValue](spropvalue.md) структуры, указывающего _lpSPropValue_ не содержит свойство column индекса. 
    
## <a name="remarks"></a>Замечания

Метод **ITableData::HrQueryRow** получает все свойства для строки, которая имеет столбец индекса, который соответствует значению индекса столбца в структуре свойство, которое указывает _lpSPropValue_. **HrQueryRow** также возвращает номер строки, если вызывающий объект запрашивает его, указывающее положение строки в таблице. 
  
Так как **HrQueryRow** не изменяет структуру **SPropValue** , на который указывает _lpSPropValue_, вызывающие необходимо освободить структура при возврате **HrQueryRow** . Вызывающие объекты также необходимо освободить **SRow** структуры, содержащей извлеченные строки. 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

