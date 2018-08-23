---
title: IMAPITableWaitForCompletion
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
ms.openlocfilehash: a3343381709b7ce3370ba481ad8dbb935c7d4165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586951"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Приостанавливает работу до завершения одного или нескольких асинхронной операции выполняется в таблице.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> Зарезервировано; должно быть равно нулю.
    
 _ulTimeout_
  
> [in] Максимальное число миллисекундах время ожидания для асинхронной операции или операции для выполнения. До начала неопределенное время до завершения, значение _ulTimeout_ 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [in, out] На выходе — допустимый указатель или значение NULL. В выходных данных Если _lpulTableStatus_ является допустимым указателем, он указывает самое последнее состояние таблицы. Если _lpulTableStatus_ имеет значение NULL, возвращаются сведения о состоянии. Если **WaitForCompletion** возвращает значение HRESULT неудачно, содержимое _lpulTableStatus_ не определено. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Операция ожидания прошла успешно.
    
MAPI_E_NO_SUPPORT 
  
> Таблицы не поддерживает ожидание завершения асинхронной операции.
    
MAPI_E_TIMEOUT 
  
> Асинхронной операции или операции не завершена в указанное время.
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::WaitForCompletion** приостанавливает работу до завершения любой асинхронной операции в настоящее время на правильном пути для таблицы. **WaitForCompletion** можно разрешить асинхронной операции, либо полностью полный или для запуска некоторых количество миллисекунд, как указано в _ulTimeout_, прежде чем прерывания. Для обнаружения в процессе выполнения асинхронной операции, вызовите метод [IMAPITable::GetStatus](imapitable-getstatus.md) . 
  
## <a name="see-also"></a>См. также



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

