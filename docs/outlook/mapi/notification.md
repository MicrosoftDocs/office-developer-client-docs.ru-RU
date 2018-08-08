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
ms.openlocfilehash: 7a8d25dc7cac4226f38baab593b254108210549e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810060"
---
# <a name="notification"></a>NOTIFICATION
 
**Относится к**: Outlook 
  
Содержит сведения о возникновении события и данные, которые были затронуты события.
  
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

## <a name="members"></a>Members

**ulEventType**
  
> Тип события уведомления, которое происходит. Значение элемента **ulEventType** соответствует структуре, включенную в **сведения** объединения. Элемент **ulEventType** может быть присвоено одно из следующих значений: 
    
 _fnevCriticalError_
  
> Глобальные ошибка, такие как сеанс, завершите работу в стадии разработки. Член **info** содержит структуру [ERROR_NOTIFICATION](error_notification.md) . 
    
 _fnevExtended_
  
> Внутренний определенные поставщиком услуг конкретного события. Член **info** содержит структуру [EXTENDED_NOTIFICATION](extended_notification.md) . 
    
 _fnevNewMail_
  
> Сообщение было доставлено в соответствующей получать папку для класса сообщений и ожидает обработки. Член **info** содержит структуру [NEWMAIL_NOTIFICATION](newmail_notification.md) . 
    
 _fnevObjectCopied_
  
> Объект MAPI был скопирован. Член **info** содержит структуру [OBJECT_NOTIFICATION](object_notification.md) . 
    
 _fnevObjectCreated_
  
> Объект MAPI был создан. Член **info** содержит структуру **OBJECT_NOTIFICATION** . 
    
 _fnevObjectDeleted_
  
> Объект MAPI был удален. Член **info** содержит структуру **OBJECT_NOTIFICATION** . 
    
 _fnevObjectModified_
  
> Объект MAPI был изменен. Член **info** содержит структуру **OBJECT_NOTIFICATION** . 
    
 _fnevObjectMoved_
  
> Хранение сообщений или адрес был перемещен объект книги. Член **info** содержит структуру **OBJECT_NOTIFICATION** . 
    
 _fnevSearchComplete_
  
> Результаты доступны и завершения операции поиска. Член **info** содержит структуру **OBJECT_NOTIFICATION** . 
    
 _fnevTableModified_
  
> Сведения в таблице, была изменена. Член **info** содержит структуру [TABLE_NOTIFICATION](table_notification.md) . 
    
**сведения о**
  
> Объединение структур уведомлений, описывающих затронутых данных для конкретного типа событий. Структура, включенных в член **info** зависит от значение элемента **ulEventType** . 
    
## <a name="remarks"></a>Замечания

Один или несколько **УВЕДОМЛЕНИЙ** , структуры, передаются в качестве входных параметров с каждым вызовом метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник зарегистрированных уведомлений. Структур **УВЕДОМЛЕНИЙ** содержат сведения о конкретных событий, которые происходили и описания затронутые объекты. 
  
Перед клиентов или поставщиков услуг, получении уведомления можно использовать структуры для обработки событий, их необходимо проверить тип события, указанного в элемент **ulEventType** . Например в образце кода, приведенные здесь проверяет наличие поступления нового сообщения и при обнаружении события этого типа выводит данные об класса сообщений для сообщения. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событиях в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор уведомлений и события уведомления.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомлений о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщиков услуг можно использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [Структуры MAPI](mapi-structures.md)

