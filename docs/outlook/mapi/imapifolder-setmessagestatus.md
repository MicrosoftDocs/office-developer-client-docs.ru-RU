---
title: имапифолдерсетмессажестатус
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

 _кбентрид_
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ . 
    
 _лпентрид_
  
> возврата Указатель на идентификатор записи для сообщения, состояние которого задано.
    
 _улневстатус_
  
> возврата Новое состояние, которое будет назначено. 
    
 _улневстатусмаск_
  
> возврата Битовая маска флагов, которая применяется к новому статусу и указывает флаги, которые необходимо задать. Можно задать следующие флаги:
    
MSGSTATUS_DELMARKED 
  
> Сообщение помечено для удаления.
    
MSGSTATUS_HIDDEN 
  
> Сообщение не будет отображаться.
    
MSGSTATUS_HIGHLIGHTED 
  
> Сообщение будет отображаться выделенным.
    
MSGSTATUS_REMOTE_DELETE 
  
> Сообщение помечено для удаления в удаленном хранилище сообщений без загрузки на локальный клиент.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Сообщение помечено для скачивания из удаленного хранилища сообщений в локальный клиент.
    
MSGSTATUS_TAGGED 
  
> Сообщение было отмечено для определенного клиентом назначения.
    
 _лпулолдстатус_
  
> вышли Указатель на предыдущее состояние сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние сообщения успешно задано.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder:: сетмессажестатус** задает для состояния сообщения значение, хранящееся в его свойстве **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Как задаются, очищаются и используются биты состояния сообщения, полностью зависят от реализации, за исключением того, что биты от 0 до 15 зарезервированы и должны равняться нулю. 
  
Реализация этого метода у поставщика удаленного транспорта должна соответствовать семантике, описанной здесь. Нет специальных рекомендаций. Клиенты используют этот метод для установки MSGSTATUS_REMOTE_DOWNLOAD и MSGSTATUS_REMOTE_DELETE бит, указывающих на то, что конкретное сообщение должно быть загружено или удалено из удаленного хранилища сообщений. Удаленный поставщик транспорта не должен реализовывать связанный метод [IMAPIFolder:: жетмессажестатус](imapifolder-getmessagestatus.md) . Клиенты должны выполнить поиск в таблице содержимого папки, чтобы определить состояние сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать свойство **PR_MSG_STATUS** сообщения для согласования операции блокировки сообщений с другими клиентами. Назначьте бит блокировки. Чтобы определить, установлен ли бит блокировки, изучите предыдущее значение состояния сообщения в параметре _лпулолдстатус_ . Используйте другие биты в параметре _улневстатус_ для отслеживания состояния сообщений, не мешая битам блокировки. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

