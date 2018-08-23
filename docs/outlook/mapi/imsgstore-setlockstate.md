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
ms.openlocfilehash: 2efee531e277b6295b7d4bc299eefc789a805d34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571089"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Блокирует или разблокирует сообщение. ���� ����� ���������� ������ ����������� ������� MAPI.
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>���������

 _lpMessage_
  
> [in] Указатель на сообщение необходимо заблокировать или разблокировать.
    
 _ulLockState_
  
> [in] Значение, указывающее, заблокирован или блокируется сообщения. Допустим один из следующих значений:
    
MSG_LOCKED 
  
> Следует заблокировать сообщения. 
    
MSG_UNLOCKED 
  
> Сообщение необходимо разблокировать.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Состояние блокировки сообщение успешно установлены.
    
## <a name="remarks"></a>Замечания

Метод **IMsgStore::SetLockState** блокирует или разблокирует сообщение. **SetLockState** может быть вызван только диспетчер очереди MAPI во время отправляет сообщение. 
  
Как правило, когда диспетчер очереди MAPI вызывает **SetLockState** заблокировать сообщения, блокирует только наиболее старых сообщений (то есть, следующее сообщение в очереди для очереди MAPI для отправки). Если наиболее старых сообщений в очередь ожидает поставщика транспорта временно недоступен и следующее сообщение в очереди используется другой поставщик, диспетчер очереди MAPI могут начать обработку сообщений более поздней версии. Обработка начинается с блокировкой этого сообщения с помощью **SetLockState**.
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

После диспетчер очереди MAPI вызова с параметром _ulLockState_ , задайте значение MSG_LOCKED **SetLockState** должен выполнить аварийное переключение вызовы метода [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) Отмена передачи сообщений. 
  
Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения в реализации **SetLockState** , чтобы сохранить все изменения, внесенные в сообщение перед **SetLockState** звонок был получен. 
  
## <a name="see-also"></a>См. также



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

