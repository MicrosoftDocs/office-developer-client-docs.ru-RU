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
ms.openlocfilehash: 140efe0b2d1b428a94b5bb2919d461779613932a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564684"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Получает строку на основе его расположения в таблице. 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>Параметры

 _ulRowNumber_
  
> [in] Количество строк, для которого возвращаются свойства. Значение параметра _ulRowNumber_ может быть любое значение от 0, что указывает на первую строку в таблице, через n - 1, которое указывает на последнюю строку в таблице. 
    
 _lppSRow_
  
> [out] Указатель на указатель на структуру [SRow](srow.md) , описывающий строки целевое значение. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Был успешно извлечен строку или строки по максимальному числу строк, указанного с помощью параметра _ulRowNumber_ не существует. 
    
## <a name="remarks"></a>Замечания

Метод **ITableData::HrEnumRow** извлекает строки на основании порядковый номер. Это значение указывает порядок вставки (0 указывает на первую строку и число строк минус 1 указывает последнюю строку). MAPI поддерживает этот порядке вставки строки в течение времени жизни объекта данных в таблице. 
  
Если число указано в _ulRowNumber_ не соответствует строки в таблице, **HrEnumRow** возвращает значение S_OK и параметру _lppSRow_ присваивается значение NULL. 
  
MAPI выделение памяти для возвращаемых **SRow** структуры с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) при создании объекта данных в таблице. Вызывающий объект должен освободить память путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Для извлечения строк из таблицы в том порядке, в том, что они были добавлены, пользователи объектов данных в таблице вызовите метод **HrEnumRow** . 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

