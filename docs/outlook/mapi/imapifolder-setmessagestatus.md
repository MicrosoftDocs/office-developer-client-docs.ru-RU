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
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417275"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает состояние, связанное с сообщением (например, помечено ли это сообщение для удаления).
  
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
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи для сообщения, состояние которого установлено.
    
 _ulNewStatus_
  
> [in] Новое состояние для присвоения. 
    
 _ulNewStatusMask_
  
> [in] Битоваяmas флагов, которая применяется к новому статусу и указывает флаги, которые необходимо установить. Можно установить следующие флаги:
    
MSGSTATUS_DELMARKED 
  
> Сообщение помечено для удаления.
    
MSGSTATUS_HIDDEN 
  
> Сообщение не должно отображаться.
    
MSGSTATUS_HIGHLIGHTED 
  
> Сообщение должно быть выделено.
    
MSGSTATUS_REMOTE_DELETE 
  
> Сообщение помечено для удаления в удаленном хранилище сообщений без загрузки в локальный клиент.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Сообщение помечено для скачивания из удаленного хранения сообщений в локальный клиент.
    
MSGSTATUS_TAGGED 
  
> Сообщение помечено для определенной клиентом цели.
    
 _lpulOldStatus_
  
> [out] Указатель на предыдущее состояние сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние сообщения успешно установлено.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::SetMessageStatus** задает для состояния сообщения значение, которое хранится в его свойстве **PR_MSG_STATUS** ([PidTagMessageStatus).](pidtagmessagestatus-canonical-property.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Настройка, очистка и применение битов состояния сообщения полностью зависит от реализации, за исключением того, что биты от 0 до 15 зарезервированы и должны быть нулем. 
  
Реализация этого метода удаленным поставщиком транспорта должна следовать семантике, описанной здесь. Нет особых соображений. Клиенты используют этот метод для MSGSTATUS_REMOTE_DOWNLOAD и MSGSTATUS_REMOTE_DELETE, чтобы указать, что определенное сообщение необходимо скачать или удалить из удаленного хранения сообщений. Поставщику удаленного транспорта не нужно реализовывать связанный метод [IMAPIFolder::GetMessageStatus.](imapifolder-getmessagestatus.md) Клиенты должны найти в таблице содержимого папки состояние сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать **PR_MSG_STATUS** сообщения для согласование операции блокировки сообщения с другими клиентами. Назначь бит в качестве бита блокировки. Чтобы определить, задан ли бит блокировки, проверьте предыдущее значение состояния сообщения в параметре _lpulOldStatus._ Используйте другие биты в параметре  _ulNewStatus_ для отслеживания состояния сообщения, не мешив биту блокировки. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

