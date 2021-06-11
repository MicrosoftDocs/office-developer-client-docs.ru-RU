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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к исходя из таблицы очереди, таблице, которая содержит сведения обо всех сообщениях в исходях очередях магазина сообщений. ���� ����� ���������� ������ ����������� ������� MAPI.
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lppTable_
  
> [вышел] Указатель на указатель на исходяю таблицу очереди.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Выходящий стол очереди был успешно возвращен.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::GetOutgoingQueue** предоставляет шпалеру MAPI доступ к таблице, которая отображает очередь исходяющих сообщений в хранилище сообщений. Обычно сообщения помещаются в исходяжую таблицу очереди после того, как называется их [метод IMessage::SubmitMessage.](imessage-submitmessage.md) Однако, поскольку порядок отправки влияет на порядок подготовки и отправки поставщику транспорта, некоторые сообщения, помеченные для отправки, могут появиться не сразу в исходячей таблице очереди. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Список свойств, которые необходимо включить в качестве столбцов в исходя из таблицы очереди, см. в статье [Исходяющие таблицы очередей.](outgoing-queue-tables.md) 
  
Поскольку spooler MAPI предназначен для приемки сообщений из магазина сообщений в порядке возрастания времени отправки, либо разрешить spooler MAPI сортировать исходяние таблицы очереди, чтобы соответствовать этому порядку или установить его в качестве порядка сортировки по умолчанию.
  
Необходимо поддерживать уведомления для таблицы очереди исходяющих сообщений, обеспечивая уведомление пулера MAPI при изменении содержимого очереди. 
  
## <a name="see-also"></a>См. также



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

