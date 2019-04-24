---
title: Имапитаблеваитфоркомплетион
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328814"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
ПриОстанавливает обработку, пока не завершится одна или несколько асинхронных операций, выполняемых над таблицей.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> Резервирования должно быть равно нулю.
    
 _Ултимеаут_
  
> возврата Максимальное время ожидания завершения асинхронной операции или операций (в миллисекундах). Чтобы подождать неопределенное время до завершения, задайте для параметра _ултимеаут_ значение 0xFFFFFFFF. 
    
 _Лпултаблестатус_
  
> [вход, выход] Для входных данных — допустимый указатель или значение NULL. В выходных данных, если _лпултаблестатус_ является допустимым указателем, он указывает на Последнее состояние таблицы. Если _лпултаблестатус_ имеет значение null, сведения о состоянии не возвращаются. Если **ваитфоркомплетион** возвращает неудачное значение HRESULT, то содержимое _лпултаблестатус_ не определено. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция ожидания выполнена успешно.
    
МАПИ_Е_НО_СУППОРТ 
  
> Таблица не поддерживает ожидание завершения асинхронных операций.
    
МАПИ_Е_ТИМЕАУТ 
  
> Асинхронная операция или операции не завершились в указанное время.
    
## <a name="remarks"></a>Комментарии

Метод **IMAPITable:: ваитфоркомплетион** приостанавливает обработку до тех пор, пока не завершится выполнение всех асинхронных операций, выполняемых в данный момент для таблицы. **Ваитфоркомплетион** позволяет выполнять асинхронные операции как полностью полностью, так и в течение определенного числа миллисекунд, как указано в _ултимеаут_, до прерывания. Чтобы определить выполняемые асинхронные операции, вызовите метод [IMAPITable::/Status](imapitable-getstatus.md) . 
  
## <a name="see-also"></a>См. также



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

