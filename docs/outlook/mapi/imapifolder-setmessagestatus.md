---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d06523625a20760faec7a6c73a6beaef757818b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575079"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Задание состояния, связанный с сообщением (например, будет ли это сообщение помечено для удаления).
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи для сообщения, состояние которого имеет значение.
    
 _ulNewStatus_
  
> [in] Новое состояние для назначения. 
    
 _ulNewStatusMask_
  
> [in] Битовая маска флаги, которая применяется к новое состояние и указывает флаги должно быть задано. Можно задать следующие флажки:
    
MSGSTATUS_DELMARKED 
  
> Сообщение было помечено для удаления.
    
MSGSTATUS_HIDDEN 
  
> Сообщение является не будет отображаться.
    
MSGSTATUS_HIGHLIGHTED 
  
> Это сообщение будет отображаться выделенный.
    
MSGSTATUS_REMOTE_DELETE 
  
> Сообщение было помечено для удаления в магазине удаленных сообщений без загрузки локального клиента.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Сообщение было помечено для загрузки с хранения удаленных сообщений для локального клиента.
    
MSGSTATUS_TAGGED 
  
> Сообщение уже помечен для определенного клиента цели.
    
 _lpulOldStatus_
  
> [out] Указатель на предыдущем состояние сообщения.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Сообщение было успешно установлено.
    
## <a name="remarks"></a>Замечания

Метод **IMAPIFolder::SetMessageStatus** задает состояние сообщения значения, которые хранятся в своем свойстве **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Как задать, снят и используется биты состояния сообщение полностью зависит от реализации, за исключением того, что бит 0 до 15 зарезервированы и должно быть равно нулю. 
  
Реализация поставщика транспорта удаленного этого метода должны соответствовать описанной здесь семантики. Существует не особенности. Клиенты используют этот метод для установки битов MSGSTATUS_REMOTE_DOWNLOAD и MSGSTATUS_REMOTE_DELETE означает, что конкретное сообщение для загрузки или удалены из хранилища удаленных сообщений. Поставщик удаленного транспорта не требуется реализовать метод [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) связанных с ними. Клиенты должны выглядеть в таблице содержимое папки для определения статуса сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Свойство **PR_MSG_STATUS** сообщения можно использовать для согласования режим блокировки сообщений с помощью других клиентов. Назначить немного как флаг блокировки. Чтобы определить, было ли задано разрядная блокировки, проверьте предыдущее состояние сообщения с помощью параметра _lpulOldStatus_ . Используйте другие двоичных файлов с помощью параметра _ulNewStatus_ для отслеживания состояния сообщения не мешая разрядная блокировки. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

