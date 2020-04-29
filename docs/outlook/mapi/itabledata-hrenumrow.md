---
title: итабледатахренумров
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

 _улровнумбер_
  
> возврата Номер строки, для которой возвращаются свойства. Значение параметра _улровнумбер_ может быть любым значением от 0, которое указывает первую строку в таблице, до n – 1, что указывает на последнюю строку в таблице. 
    
 _лппсров_
  
> вышли Указатель на указатель на структуру [сров](srow.md) , которая описывает целевую строку. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строка была получена успешно, или строка для номера строки, заданная параметром _улровнумбер_ , не существует. 
    
## <a name="remarks"></a>Примечания

Метод **итабледата:: хренумров** извлекает строку на основе порядкового номера. Это значение представляет порядок вставки (0 означает первую строку, а число строк минус 1 указывает на последнюю строку). MAPI поддерживает этот хронологический порядок вставки строк в течение всего времени существования объекта данных таблицы. 
  
Если номер, указанный в _улровнумбер_ , не соответствует строке в таблице, **хренумров** возвращает S_OK и задает для параметра _лппсров_ значение null. 
  
MAPI выделяет память для возвращенной структуры **сров** с помощью функции [мапиаллокатебуффер](mapiallocatebuffer.md) при создании объекта данных таблицы. Вызывающая сторона должна освободить эту память, вызвав функцию [мапифрибуффер](mapifreebuffer.md) . 
  
Чтобы получить строки из таблицы в порядке вставки, пользователь объекта данных таблицы вызывает метод **хренумров** . 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

