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
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434769"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Извлекает строку таблицы.
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>Параметры

 _lpSPropValue_
  
> [in] Указатель на структуру значения свойства, которая описывает столбец индекса для извлекаемой строки. Член **ulPropTag** структуры значения свойства должен содержать тот же тег свойства, что и параметр _ulPropTagIndexColumn_ из вызова функции [CreateTable,](createtable.md) которая имеет доступ к реализации [ITableData.](itabledataiunknown.md) 
    
 _lppSRow_
  
> [out] Указатель на указатель на извлеченную строку. 
    
 _lpuliRow_
  
> [in, out] При вводе допустимый указатель или NULL, который указывает, что не требуется возвращать сведения. При выходе допустимый указатель, который указывает на номер строки строки, последовательное число, определяя положение строки в таблице.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строка успешно извлечена.
    
MAPI_E_INVALID_PARAMETER 
  
> Структура [SPropValue,](spropvalue.md) на которую  _указывает lpSPropValue,_ не содержит свойство столбца индекса. 
    
## <a name="remarks"></a>Примечания

Метод **ITableData::HrQueryRow** извлекает все свойства строки со столбцом индекса, который соответствует значению столбца индекса, включенного в структуру свойств, на которую указывает _lpSPropValue._ **HrQueryRow** также возвращает номер строки, если вызываемая строка запрашивает его, что определяет положение строки в таблице. 
  
Так **как HrQueryRow** не изменять **структуру SPropValue,** на который указывает  _lpSPropValue,_ при возвращении **HrQueryRow** вызывателям необходимо освободить структуру. Вызыватели также должны освободить **структуру SRow,** которая содержит извлеченную строку. 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

