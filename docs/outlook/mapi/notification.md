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
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит сведения о произошедшем событии и данных, на которые повлияло событие.
  
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
  
> Тип события уведомления, которое произошло. Значение члена **ulEventType** соответствует структуре, включенной в **информационное** объединение. Член **ulEventType** может быть назначен одному из следующих значений: 
    
 _fnevCriticalError_
  
> Произошла глобальная ошибка, например завершение сеанса. Член **info** содержит [структуру ERROR_NOTIFICATION.](error_notification.md) 
    
 _fnevExtended_
  
> Произошло внутреннее событие, определенное конкретным поставщиком услуг. Член **info** содержит [структуру EXTENDED_NOTIFICATION.](extended_notification.md) 
    
 _fnevNewMail_
  
> Сообщение доставлено в соответствующую папку получения для класса сообщений и ожидает обработки. Член **info** содержит [структуру NEWMAIL_NOTIFICATION.](newmail_notification.md) 
    
 _fnevObjectCopied_
  
> Скопирован объект MAPI. Член **info** содержит [структуру OBJECT_NOTIFICATION.](object_notification.md) 
    
 _fnevObjectCreated_
  
> Создан объект MAPI. Член **info** содержит **структуру OBJECT_NOTIFICATION.** 
    
 _fnevObjectDeleted_
  
> Объект MAPI удален. Член **info** содержит **структуру OBJECT_NOTIFICATION.** 
    
 _fnevObjectModified_
  
> Объект MAPI изменился. Член **info** содержит **структуру OBJECT_NOTIFICATION.** 
    
 _fnevObjectMoved_
  
> Перенесено хранилище сообщений или объект адресной книги. Член **info** содержит **структуру OBJECT_NOTIFICATION.** 
    
 _fnevSearchComplete_
  
> Операция поиска завершена, и результаты доступны. Член **info** содержит **структуру OBJECT_NOTIFICATION.** 
    
 _fnevTableModified_
  
> Сведения в таблице изменились. Член **info** содержит [структуру TABLE_NOTIFICATION.](table_notification.md) 
    
**info**
  
> Объединение структур уведомлений, описывающих затронутые данные для определенного типа события. Структура, включенная в **член info,** зависит от значения члена **ulEventType.** 
    
## <a name="remarks"></a>Примечания

Одна или несколько **структур УВЕДОМЛЕНий** передаются в качестве параметров ввода с каждым вызовом в зарегистрированный метод [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md) Структуры **УВЕДОМЛЕНий** содержат сведения о конкретных событиях, которые произошли, и описывают затронутые объекты. 
  
Прежде чем клиенты или поставщики услуг, получающие уведомление, смогут использовать структуру для обработки события, они должны проверить тип события, указанный в члене **ulEventType.** Например, пример кода, показанный здесь, проверяет прибытие нового сообщения и при обнаружении события подобного рода распечатывает класс сообщения сообщения. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Дополнительные сведения об уведомлении см. в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событиях в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор событий уведомлений и уведомлений.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение того, как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомления о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщики услуг могут использовать [метод IMAPISupport](imapisupportiunknown.md) для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [Структуры MAPI](mapi-structures.md)

