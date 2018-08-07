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
ms.openlocfilehash: 1b59071758aad9c71939eb9efc029005806b2a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809386"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**Относится к**: Outlook 
  
Предоставляет доступ к таблице исходящей очереди, таблицы, которая содержит сведения обо всех сообщений в очереди исходящих хранилища сообщений. ���� ����� ���������� ������ ����������� ������� MAPI.
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lppTable_
  
> [out] Указатель на указатель на таблице исходящей очереди.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В таблице исходящей очереди успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IMsgStore::GetOutgoingQueue** предоставляет диспетчер очереди MAPI с доступом к таблица, показывающая хранилища сообщений очереди исходящих сообщений. Как правило сообщения помещаются в таблицу исходящей очереди после вызова метода их [IMessage::SubmitMessage](imessage-submitmessage.md) . Тем не менее так как порядок отправки влияет на порядок обработки и отправки для поставщика транспорта, некоторые сообщения, помеченные для отправки могут не отображаться в таблице исходящей очереди немедленно. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Чтобы получить список свойств, которые должны быть включены в качестве столбцов в таблице исходящей очереди см [исходящей очереди](outgoing-queue-tables.md). 
  
Поскольку диспетчер очереди MAPI разработан для приема сообщений из хранилища сообщений по возрастанию время отправки, либо разрешить диспетчер очереди MAPI для сортировки исходящей очереди в соответствии с этой порядке или установить как порядок сортировки по умолчанию.
  
Должен поддерживать уведомления для в таблице очереди исходящих сообщений проверка того, что диспетчер очереди MAPI получает уведомление при изменении содержимого очереди. 
  
## <a name="see-also"></a>См. также



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

