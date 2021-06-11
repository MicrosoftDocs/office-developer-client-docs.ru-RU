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
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430170"
---
# <a name="object_notification"></a>OBJECT_NOTIFICATION

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит сведения об объекте, который подвергся изменениям, например о копировании или изменении.
  
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

## <a name="members"></a>"Участники"

 **cbEntryID**
  
> Количество bytes в идентификаторе записи, на который указывает член **lpEntryID.** 
    
 **lpEntryID**
  
> Указатель на идентификатор входа затронутого объекта.
    
 **ulObjType**
  
> Тип затронутого объекта. Возможные типы:
    
MAPI_STORE 
  
> Хранилище сообщений. 
    
MAPI_ADDRBOOK 
  
> Адресная книга. 
    
MAPI_FOLDER 
  
> Папка.
    
MAPI_ABCONT 
  
> Контейнер адресной книги.
    
MAPI_MESSAGE 
  
> Сообщение.
    
MAPI_MAILUSER 
  
> Пользователь обмена сообщениями.
    
MAPI_ATTACH 
  
> Вложение.
    
MAPI_DISTLIST 
  
> Список рассылки.
    
MAPI_PROFSECT 
  
> Раздел Профиль.
    
MAPI_STATUS 
  
> Объект Status.
    
MAPI_SESSION 
  
> Объект Session.
    
 **cbParentID**
  
> Количество bytes в идентификаторе записи, на который указывает член **lpParentID.** 
    
 **lpParentID**
  
> Указатель на идентификатор записи родителя пострадавшего объекта.
    
 **cbOldID**
  
> Количество bytes в идентификаторе записи, на который указывает член **lpOldID.** 
    
 **lpOldID**
  
> Указатель на идентификатор входа исходного объекта. Этот указатель может быть NULL, если для события не требуется исходный объект.
    
 **cbOldParentID**
  
> Количество bytes в идентификаторе записи, на который указывает член **lpOldParentID.** 
    
 **lpOldParentID**
  
> Указатель на идентификатор записи родительского исходного объекта. Этот указатель может быть NULL, если для события не требуется исходный объект.
    
 **lpPropTagArray**
  
> Указатель на [структуру SPropTagArray,](sproptagarray.md) которая содержит теги свойств, определяющие свойства, затронутые событием. 
    
## <a name="remarks"></a>Примечания

Структура **OBJECT_NOTIFICATION** является одним из членов союза структур, включенных в  состав информационного члена [структуры NOTIFICATION.](notification.md) Если член **структуры**  уведомлений  содержит структуру OBJECT_NOTIFICATION, то член **ulEventType** структуры **УВЕДОМЛЕНий** устанавливается к одному из следующих типов событий: 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
Полное событие поиска, представленное типом события fnevSearchComplete, указывает, что начальный поиск домена для одной папки поиска завершен.
  
Следующие участники, содержащие сведения о исходном объекте, используются только в событиях перемещения и копирования. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Эти участники не применяются к другим типам событий.
  
Дополнительные сведения об уведомлении см. в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событиях в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор событий уведомлений и уведомлений.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение того, как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомления о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщики услуг могут использовать [метод IMAPISupport](imapisupportiunknown.md) для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[�����������](notification.md)
  
[SPropTagArray](sproptagarray.md)


[Структуры MAPI](mapi-structures.md)

