---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418374"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Извлекает строку на основе ее позиции в таблице. 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>Параметры

 _ulRowNumber_
  
> [in] Номер строки, для которой возвращаются свойства. Значением в параметре  _ulRowNumber_ может быть любое значение от 0, которое указывает первую строку в таблице, до n - 1, которое указывает последнюю строку в таблице. 
    
 _lppSRow_
  
> [out] Указатель на указатель на структуру [SRow,](srow.md) которая описывает целевую строку. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строка была успешно извлечена или строка для номера строки, указанного параметром  _ulRowNumber,_ не существует. 
    
## <a name="remarks"></a>Примечания

Метод **ITableData::HrEnumRow** извлекает строку на основе последовательного числа. Это число представляет порядок вставки (0 указывает на первую строку, а число строк минус 1 указывает на последнюю строку). MAPI поддерживает этот хронологический порядок вставки строк в течение всего времени существования объекта данных таблицы. 
  
Если номер, указанный в  _ulRowNumber,_ не соответствует строке в таблице, **HrEnumRow** возвращает S_OK и устанавливает для параметра  _lppSRow_ nULL. 
  
MAPI выделяет память для возвращаемой **структуры SRow** с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) при создании объекта данных таблицы. Вызываемая система должна освободить эту память, вызывая [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
Чтобы извлечь строки из таблицы в порядке их вставки, пользователи объекта данных таблицы вызывали **метод HrEnumRow.** 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

