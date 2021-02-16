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
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407062"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Приостанавливать обработку до завершения одной или более асинхронных операций в таблице.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> Зарезервировано; должно быть нулем.
    
 _ulTimeout_
  
> [in] Максимальное количество миллисекунд для ожидания завершения асинхронной операции. Чтобы неопределенное время ждать завершения, установите  _для ulTimeout_ 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [in, out] При вводе допустимый указатель или NULL. При выходе, если  _lpulTableStatus_ является допустимым указателем, он указывает на последнее состояние таблицы. Если  _lpulTableStatus_ имеет NULL, сведения о состоянии не возвращаются. Если **WaitForCompletion** возвращает неудачное значение HRESULT,  _содержимое lpulTableStatus_ будет неопределенным. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция ожидания прошла успешно.
    
MAPI_E_NO_SUPPORT 
  
> Таблица не поддерживает ожидание завершения асинхронных операций.
    
MAPI_E_TIMEOUT 
  
> Асинхронная операция или операции не были завершены в указанное время.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::WaitForCompletion** приостанавливать обработку до завершения всех асинхронных операций, которые в настоящее время проводятся для таблицы. **WaitForCompletion** позволяет выполнить асинхронные операции полностью или в течение определенного количества миллисекунд, как указано  _в ulTimeout,_ перед прерыванием. Чтобы обнаружить асинхронные операции, вызовите метод [IMAPITable::GetStatus.](imapitable-getstatus.md) 
  
## <a name="see-also"></a>См. также



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

