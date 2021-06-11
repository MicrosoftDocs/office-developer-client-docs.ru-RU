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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Блокирует или разблокирует сообщение. ���� ����� ���������� ������ ����������� ������� MAPI.
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in] Указатель на сообщение для блокировки или разблокировки.
    
 _ulLockState_
  
> [in] Значение, которое указывает, должно ли сообщение быть заблокировано или разблокировано. Допустимо одно из следующих значений:
    
MSG_LOCKED 
  
> Сообщение должно быть заблокировано. 
    
MSG_UNLOCKED 
  
> Сообщение должно быть разблокировано.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние блокировки сообщения было успешно установлено.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::SetLockState** блокирует или открывает сообщение. **SetLockState** может быть вызван только шпалером MAPI во время отправки сообщения. 
  
Обычно, когда шпалер MAPI вызывает **SetLockState** для блокировки сообщения, он блокирует только самое старое сообщение (то есть следующее сообщение в очереди для отправки пульпера MAPI). Если самое старое сообщение в очереди ждет временно недоступного поставщика транспорта, а следующее сообщение в очереди использует другой поставщик транспорта, то пуллер MAPI может приступить к обработке более позднего сообщения. Он начинает обработку путем блокировки этого сообщения с помощью **SetLockState**.
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

После вызова пулера **MAPI SetLockState** с параметром  _ulLockState,_ заданным для MSG_LOCKED, необходимо звонков в [метод IMsgStore::AbortSubmit,](imsgstore-abortsubmit.md) чтобы отменить передачу сообщения. 
  
Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) в реализации **SetLockState,** чтобы сохранить все изменения, внесенные в сообщение до получения вызова **SetLockState.** 
  
## <a name="see-also"></a>См. также



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

