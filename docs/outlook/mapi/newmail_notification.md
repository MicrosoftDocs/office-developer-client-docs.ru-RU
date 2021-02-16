---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439858"
---
# <a name="newmail_notification"></a>NEWMAIL_NOTIFICATION

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает сведения, которые относятся к поступлению нового сообщения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a>"Участники"

 **cbEntryID**
  
> Количество вхождений в идентификаторе записи, на который указывает **член lpEntryID.** 
    
 **lpEntryID**
  
> Указатель на идентификатор записи нового сообщения.
    
 **cbParentID**
  
> Количествобайтов в идентификаторе записи, на который указывает **член lpParentID.** 
    
 **lpParentID**
  
> Указатель на идентификатор записи папки получения для нового сообщения.
    
 **ulFlags**
  
> Битовая почта флагов, используемая для описания формата строки свойств, включенных в сообщение. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 **lpszMessageClass**
  
> Указатель на класс нового сообщения. 
    
 **ulMessageFlags**
  
> Битоваяmas флагов, описывающая текущее состояние нового сообщения. Член **ulMessageFlags** — это копия свойства PR_MESSAGE_FLAGS **сообщения** ([PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)
    
## <a name="remarks"></a>Примечания

Структура **NEWMAIL_NOTIFICATION** является одним из членов объединения структур, включенных в  состав данных структуры [NOTIFICATION.](notification.md) Если **информационный** член структуры **УВЕДОМЛЕНий** содержит NEWMAIL_NOTIFICATION, то для члена **ulEventType** структуры **NOTIFICATION** задается _fnevNewMail._ 
  
MAPI использует **NEWMAIL_NOTIFICATION** только в качестве члена структуры **NOTIFICATION,** в которой хранится информация о событии уведомления для висящего уведомления. 
  
Дополнительные сведения об уведомлении см. в темах, описанных в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событии в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор событий уведомлений и уведомлений.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение того, как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомлений о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщики служб могут использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[�����������](notification.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Структуры MAPI](mapi-structures.md)

