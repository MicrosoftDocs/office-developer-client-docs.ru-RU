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
ms.openlocfilehash: 86fe4b0a1a7521c310788505b99f53bc8657de75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808397"
---
# <a name="errornotification"></a>ERROR_NOTIFICATION

  
  
**Относится к**: Outlook 
  
Описание сведений, которые относятся к критическая ошибка. В этом случае уведомление об ошибке был создан. 
  
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

## <a name="members"></a>Members

 **cbEntryID**
  
> Число байт в идентификаторе запись, на который указывает **lpEntryID**. 
    
 **lpEntryID**
  
> Указатель на идентификатор записи объекта, который вызывает ошибку.
    
 **SCODE**
  
> Значение ошибки для критическая ошибка. 
    
 **ulFlags**
  
> Битовая маска флагов используется для назначения формат текста, на который указывает член **lpszError** в структуре, на который указывает **lpMAPIError**. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 **lpMAPIError**
  
> Указатель на структуру [MAPIERROR](mapierror.md) , описывающее ошибку. 
    
## <a name="remarks"></a>Замечания

Структура **ERROR_NOTIFICATION** — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) . Когда участник **info** структуры **уведомление** содержит структуру **ERROR_NOTIFICATION** , член **ulEventType** структуры **УВЕДОМЛЕНИЙ** задано значение _fnevCriticalError_.
  
Значение **cbEntryID** , а **lpEntryID** может быть NULL. 
  
Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событиях в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор уведомлений и события уведомления.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомлений о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщиков услуг можно использовать метод **IMAPISupport** для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[�����������](notification.md)


[Структуры MAPI](mapi-structures.md)

