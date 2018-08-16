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
ms.openlocfilehash: 92540159386e6f37d93684aff037b235071010f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809608"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**Относится к**: Outlook 
  
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
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
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
