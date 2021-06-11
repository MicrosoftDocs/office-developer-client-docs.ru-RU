---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425444"
---
# <a name="error_notification"></a>ERROR_NOTIFICATION

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает сведения, которые относятся к критической ошибке. Это приводит к сгенерированию уведомления об ошибке. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a>"Участники"

 **cbEntryID**
  
> Количество bytes в идентификаторе записи, на который указывает **lpEntryID.** 
    
 **lpEntryID**
  
> Указатель на идентификатор входа объекта, который вызывает ошибку.
    
 **scode**
  
> Значение ошибки для критической ошибки. 
    
 **ulFlags**
  
> Bitmask флагов, используемых для назначить формат текста, указанный членом **lpszError** в структуре, указанной **lpMAPIError**. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
 **lpMAPIError**
  
> Указатель на [структуру MAPIERROR](mapierror.md) с описанием ошибки. 
    
## <a name="remarks"></a>Примечания

Структура **ERROR_NOTIFICATION** является одним из членов союза структур, включенных  в состав информационного члена [структуры NOTIFICATION.](notification.md) Если член **структуры**  УВЕДОМЛЕНий  содержит структуру ERROR_NOTIFICATION, член **ulEventType** структуры **УВЕДОМЛЕНий** задает _fnevCriticalError_.
  
Значение участника **cbEntryID** и **члена lpEntryID** может быть NULL. 
  
Дополнительные сведения об уведомлении см. в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событиях в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор событий уведомлений и уведомлений.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение того, как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомления о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщики услуг могут использовать **метод IMAPISupport** для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[�����������](notification.md)


[Структуры MAPI](mapi-structures.md)

