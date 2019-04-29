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
# <a name="newmailnotification"></a>NEWMAIL_NOTIFICATION

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сведения, связанные с поступлением нового сообщения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
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

 **Кбентрид**
  
> Количество байтов в идентификаторе записи, на который указывает элемент **лпентрид** . 
    
 **Лпентрид**
  
> Указатель на идентификатор вновь полученного сообщения.
    
 **Кбпарентид**
  
> Количество байтов в идентификаторе записи, на который указывает элемент **лппарентид** . 
    
 **Лппарентид**
  
> Указатель на идентификатор записи папки получения для вновь полученного сообщения.
    
 **ulFlags**
  
> Битовая маска флагов, используемых для описания формата строк свойств, включенных в сообщение. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки имеют формат Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.
    
 **Лпсзмессажекласс**
  
> Указатель на класс сообщения вновь полученного сообщения. 
    
 **Улмессажефлагс**
  
> Битовая маска флагов, описывающих текущее состояние вновь полученного сообщения. Элемент **улмессажефлагс** является копией свойства **пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения.
    
## <a name="remarks"></a>Примечания

Структура **невмаил_нотификатион** — это один из членов объединения структур, включенных в элемент **info** структуры [уведомления](notification.md) . Когда элемент **info** структуры **уведомлений** содержит структуру **Невмаил_нотификатион** , элемент **улевенттипе** структуры **уведомлений** имеет значение _фневневмаил._
  
MAPI использует структуру **невмаил_нотификатион** только в качестве члена структуры **уведомлений** , в которой хранятся сведения о событии уведомления для приемника уведомлений. 
  
Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о соБытии в MAPI](event-notification-in-mapi.md) <br/> |Общие сведения о событиях уведомлений и уведомлений.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение того, как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомлений о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщики услуг могут использовать метод [имаписуппорт](imapisupportiunknown.md) для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[�����������](notification.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Структуры MAPI](mapi-structures.md)

