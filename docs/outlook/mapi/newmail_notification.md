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
ms.openlocfilehash: aad4d3be8757ca4cd7719bfd7a53ae8bbf6711f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810033"
---
# <a name="newmailnotification"></a>NEWMAIL_NOTIFICATION

  
  
**Относится к**: Outlook 
  
Описание сведений, которые относятся к поступления нового сообщения. 
  
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

## <a name="members"></a>Members

 **cbEntryID**
  
> Число байт в идентификаторе запись, на который указывает член **lpEntryID** . 
    
 **lpEntryID**
  
> Указатель на идентификатор записи вновь поступивших сообщения.
    
 **cbParentID**
  
> Число байт в идентификаторе запись, на который указывает член **lpParentID** . 
    
 **lpParentID**
  
> Указатель на идентификатор записи папки получения для недавно полученных сообщений.
    
 **ulFlags**
  
> Битовая маска флаги, используемые для описания формата строковые свойства, включенные в состав сообщения. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 **lpszMessageClass**
  
> Указатель на класс сообщения вновь поступивших сообщения. 
    
 **ulMessageFlags**
  
> Битовая маска флаги, описывающее текущее состояние вновь поступивших сообщений. Член **ulMessageFlags** является копию свойство message **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
## <a name="remarks"></a>Замечания

Структура **NEWMAIL_NOTIFICATION** — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) . Когда участник **info** структуры **уведомление** содержит структуру **NEWMAIL_NOTIFICATION** , член **ulEventType** структуры **УВЕДОМЛЕНИЙ** задано значение _fnevNewMail._
  
MAPI использует структуру **NEWMAIL_NOTIFICATION** только в качестве члена структуры **УВЕДОМЛЕНИЙ** , который содержит сведения о событии уведомления для приемник уведомлений. 
  
Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событиях в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор уведомлений и события уведомления.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомлений о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщиков услуг можно использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[�����������](notification.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Структуры MAPI](mapi-structures.md)

