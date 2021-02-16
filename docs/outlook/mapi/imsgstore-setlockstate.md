---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423631"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Блокирует или разблокирует сообщение. ���� ����� ���������� ������ ����������� ������� MAPI.
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>Параметры

 _lpMessage_
  
> [in] Указатель на сообщение для блокировки или разблокировки.
    
 _ulLockState_
  
> [in] Значение, которое указывает, следует ли заблокировать или разблокировать сообщение. Допустимо одно из следующих значений:
    
MSG_LOCKED 
  
> Сообщение должно быть заблокировано. 
    
MSG_UNLOCKED 
  
> Сообщение должно быть разблокировано.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние блокировки сообщения успешно установлено.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::SetLockState** блокирует или разблокирует сообщение. **SetLockState** может быть вызван только пулером MAPI во время отправки сообщения. 
  
Обычно, когда пулер MAPI вызывает **SetLockState** для блокировки сообщения, он блокирует только самое старое сообщение (то есть следующее сообщение, поставленное в очередь для отправки пулом MAPI). Если самое старое сообщение в очереди ожидает временно недоступного поставщика транспорта, а следующее сообщение в очереди использует другого поставщика транспорта, то пулер MAPI может начать обработку следующего сообщения. Обработка начинается с блокировки сообщения с помощью **SetLockState.**
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

После того как пулер MAPI вызывает **SetLockState** с параметром  _ulLockState,_ установленным в MSG_LOCKED, вызов метода [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) для отмены передачи сообщения должен быть неудачным. 
  
Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения в реализации **SetLockState,** чтобы сохранить все изменения, внесенные в сообщение до получения вызова **SetLockState.** 
  
## <a name="see-also"></a>См. также



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

