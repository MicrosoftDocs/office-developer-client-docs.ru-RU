---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 876c8fc3667929e3c2e7403e71e6d392981d34f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573357"
---
# <a name="objectnotification"></a>OBJECT_NOTIFICATION

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит сведения об объекте, который внесено изменение, например, копирование или изменены.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a>Элементы

 **cbEntryID**
  
> Число байт в идентификаторе запись, на который указывает член **lpEntryID** . 
    
 **lpEntryID**
  
> Указатель на идентификатор записи затронутых объекта.
    
 **ulObjType**
  
> Тип объекта, связанного. Ниже приведены возможные типы:
    
MAPI_STORE 
  
> Хранение сообщений. 
    
MAPI_ADDRBOOK 
  
> Список адресов. 
    
MAPI_FOLDER 
  
> Папка.
    
MAPI_ABCONT 
  
> Контейнер адресной книги.
    
MAPI_MESSAGE 
  
> Сообщение.
    
MAPI_MAILUSER 
  
> Пользователь, обмена мгновенными сообщениями.
    
MAPI_ATTACH 
  
> Вложение.
    
MAPI_DISTLIST 
  
> Список рассылки.
    
MAPI_PROFSECT 
  
> Раздел профиля.
    
MAPI_STATUS 
  
> Состояние объекта.
    
MAPI_SESSION 
  
> Объект сеанса.
    
 **cbParentID**
  
> Число байт в идентификаторе запись, на который указывает член **lpParentID** . 
    
 **lpParentID**
  
> Указатель на идентификатор записи родительского объекта затронутых.
    
 **cbOldID**
  
> Число байт в идентификаторе запись, на который указывает член **lpOldID** . 
    
 **lpOldID**
  
> Указатель на идентификатор записи исходного объекта. В этом указатель может быть NULL, если событие не требуется исходный объект.
    
 **cbOldParentID**
  
> Число байт в идентификаторе запись, на который указывает член **lpOldParentID** . 
    
 **lpOldParentID**
  
> Указатель на идентификатор записи родительского исходного объекта. В этом указатель может быть NULL, если событие не требуется исходный объект.
    
 **lpPropTagArray**
  
> Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит свойство теги, идентифицирующий свойства, связанного с событием. 
    
## <a name="remarks"></a>Замечания

Структура **OBJECT_NOTIFICATION** — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) . Когда участник **info** структуры **уведомление** содержит структуру **OBJECT_NOTIFICATION** , член **ulEventType** структуры **УВЕДОМЛЕНИЙ** задано значение один из следующих типов событий: 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
Событие завершения поиска, в тип события fnevSearchComplete указывает, что начального поиска домена для папки поиска завершено.
  
Следующие члены, которые содержат сведения об исходном объекте используются только в перемещение и копирование событий. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Эти элементы не применяются к другим типам событий.
  
Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событии в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор уведомлений и события уведомления.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомления о событии](supporting-event-notification.md) <br/> |Обсуждение того, как поставщиков услуг можно использовать метод [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[�����������](notification.md)
  
[SPropTagArray](sproptagarray.md)


[Структуры MAPI](mapi-structures.md)

