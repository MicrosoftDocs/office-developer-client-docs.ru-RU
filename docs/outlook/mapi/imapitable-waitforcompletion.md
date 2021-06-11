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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Приостановка обработки до завершения одной или более асинхронных операций в таблице.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> Зарезервировано; должно быть нулевой.
    
 _ulTimeout_
  
> [in] Максимальное количество миллисекунд для ожидания завершения асинхронной операции. Чтобы дождаться завершения, установите  _ulTimeout_ на 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [in, out] На входе допустимый указатель или NULL. На выходе,  _если lpulTableStatus_ является допустимым указателем, он указывает на последний статус таблицы. Если  _lpulTableStatus_ является NULL, сведения о состоянии не возвращаются. Если **в WaitForCompletion** возвращается неудачное значение HRESULT, содержимое  _lpulTableStatus_ неопределяется. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция ожидания прошла успешно.
    
MAPI_E_NO_SUPPORT 
  
> В таблице не поддерживается ожидание завершения асинхронных операций.
    
MAPI_E_TIMEOUT 
  
> Асинхронная операция или операции не были завершены в указанное время.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::WaitForCompletion** приостанавливать обработку до завершения всех асинхронных операций, которые в настоящее время проводятся для таблицы. **WaitForCompletion** может разрешить асинхронные операции либо полностью завершить, либо выполнить определенное количество миллисекунд, как  _указывается в ulTimeout,_ прежде чем прерываться. Чтобы обнаружить асинхронные операции, позвоните по методу [IMAPITable::GetStatus.](imapitable-getstatus.md) 
  
## <a name="see-also"></a>См. также



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

