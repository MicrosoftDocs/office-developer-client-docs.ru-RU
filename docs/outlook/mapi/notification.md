---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432879"
---
# <a name="notification"></a>NOTIFICATION
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит сведения о событии, которое произошло, и данных, которые были затронуты этим событием.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a>"Участники"

**ulEventType**
  
> Тип события уведомления, которое произошло. Значение члена **ulEventType** соответствует структуре, включенной в **объединение данных.** Для **члена ulEventType** можно установить одно из следующих значений: 
    
 _fnevCriticalError_
  
> Произошла глобальная ошибка, например завершение сеанса. Член **info** содержит структуру [ERROR_NOTIFICATION](error_notification.md) данных. 
    
 _fnevExtended_
  
> Произошло внутреннее событие, определенное определенным поставщиком услуг. Член **info** содержит структуру [EXTENDED_NOTIFICATION](extended_notification.md) данных. 
    
 _fnevNewMail_
  
> Сообщение доставлено в соответствующую папку получения для класса сообщений и ожидает обработки. Член **info** содержит структуру [NEWMAIL_NOTIFICATION](newmail_notification.md) данных. 
    
 _fnevObjectCopied_
  
> Объект MAPI был скопирован. Член **info** содержит структуру [OBJECT_NOTIFICATION](object_notification.md) данных. 
    
 _fnevObjectCreated_
  
> Создан объект MAPI. Член **info** содержит структуру **OBJECT_NOTIFICATION** данных. 
    
 _fnevObjectDeleted_
  
> Объект MAPI удален. Член **info** содержит структуру **OBJECT_NOTIFICATION** данных. 
    
 _fnevObjectModified_
  
> Объект MAPI изменился. Член **info** содержит структуру **OBJECT_NOTIFICATION** данных. 
    
 _fnevObjectMoved_
  
> Хранилище сообщений или объект адресной книги перемещены. Член **info** содержит структуру **OBJECT_NOTIFICATION** данных. 
    
 _fnevSearchComplete_
  
> Операция поиска завершена, и результаты доступны. Член **info** содержит структуру **OBJECT_NOTIFICATION** данных. 
    
 _fnevTableModified_
  
> Сведения в таблице изменились. Член **info** содержит структуру [TABLE_NOTIFICATION](table_notification.md) данных. 
    
**info**
  
> Объединение структур уведомлений, описывающих затронутые данные для конкретного типа события. Структура, включенная в **член данных,** зависит от значения **члена ulEventType.** 
    
## <a name="remarks"></a>Примечания

Одна или несколько **структур NOTIFICATION** передаются в качестве входных параметров при каждом вызове метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) зарегистрированного приемника уведомлений. Структуры **УВЕДОМЛЕНий** содержат сведения о конкретных событиях, которые произошли, и описывают затронутые объекты. 
  
Прежде чем клиенты или поставщики услуг, получающие уведомление, смогут использовать структуру для обработки события, они должны проверить тип события, как указано в члене **ulEventType.** Например, показанный здесь пример кода проверяет наличие нового сообщения и при обнаружении события такого типа распечатает класс сообщения. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Дополнительные сведения об уведомлении см. в темах, описанных в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событии в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор событий уведомлений и уведомлений.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение того, как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомлений о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщики служб могут использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [Структуры MAPI](mapi-structures.md)

