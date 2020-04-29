---
title: итабледатахркуериров
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
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434769"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает строку таблицы.
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>Параметры

 _лпспропвалуе_
  
> возврата Указатель на структуру значения свойства, которая описывает столбец индекса для извлекаемой строки. Элемент **улпроптаг** структуры значения свойства должен содержать тот же тег свойства, что и параметр _улпроптагиндексколумн_ , из вызова функции [креатетабле](createtable.md) , которая получает доступ к реализации [итабледата](itabledataiunknown.md) . 
    
 _лппсров_
  
> вышли Указатель на указатель на извлеченную строку. 
    
 _лпулиров_
  
> [вход, выход] В поле input — допустимый указатель или значение NULL, которое указывает, что никакие сведения не требуется возвращать. В выходных данных — допустимый указатель, указывающий на номер строки строки, порядковый номер, который определяет положение строки в таблице.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строка была успешно получена.
    
MAPI_E_INVALID_PARAMETER 
  
> Структура [спропвалуе](spropvalue.md) , на которую указывает _лпспропвалуе_ , не содержит свойство столбца index. 
    
## <a name="remarks"></a>Примечания

Метод **итабледата:: хркуериров** извлекает все свойства для строки, содержащей столбец индекса, который соответствует значению столбца индекса, включенному в структуру свойства, на которую указывает _лпспропвалуе_. **Хркуериров** также возвращает номер строки, если вызывающая сторона запрашивает ее, которая определяет положение строки в таблице. 
  
Так как **хркуериров** не изменяет структуру **спропвалуе** , на которую указывает _лпспропвалуе_, вызывающие объекты должны освобождать структуру при возврате **хркуериров** . Вызывающие также должны освободить структуру **сров** , содержащую извлеченную строку. 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

