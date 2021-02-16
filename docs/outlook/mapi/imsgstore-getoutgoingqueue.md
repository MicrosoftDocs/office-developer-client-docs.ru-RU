---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8ccb732dd587b2e5107290b2db7c48e85d0145d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434153"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице исходяющих очередей, которая содержит сведения обо всех сообщениях в исходя такой очереди. ���� ����� ���������� ������ ����������� ������� MAPI.
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу исходяющих очередей.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица исходяющих очередей успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::GetOutgoingQueue** предоставляет пуле MAPI доступ к таблице, в которую указывается очередь исходяющих сообщений в хранилище сообщений. Как правило, сообщения помещаются в исходячную таблицу очереди после того, как вызван метод [IMessage::SubmitMessage.](imessage-submitmessage.md) Однако, так как порядок отправки влияет на порядок предварительной подготовки и отправки поставщику транспорта, некоторые сообщения, помеченные для отправки, могут не отображаться в таблице исходячих очередей немедленно. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Список свойств, которые необходимо включить в качестве столбцов в таблицу исходяющих очередей, см. в таблицах [исходяющих очередей.](outgoing-queue-tables.md) 
  
Так как пулер MAPI предназначен для получения сообщений из магазина сообщений в порядке возрастания времени отправки, то можно разрешить пулу MAPI сортировать исходяжую таблицу очереди в соответствие этому порядку или установить ее в качестве порядка сортировки по умолчанию.
  
Необходимо поддерживать уведомления для таблицы очереди исходяющих сообщений, чтобы обеспечить уведомление пула MAPI при изменении содержимого очереди. 
  
## <a name="see-also"></a>См. также



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

