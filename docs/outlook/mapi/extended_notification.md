---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415721"
---
# <a name="extended_notification"></a>EXTENDED_NOTIFICATION

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает сведения, которые относятся к событию, определенному поставщику услуг. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a>"Участники"

 **ulEvent**
  
> Расширенный код события, определенный поставщиком.
    
 **cb**
  
> Количество bytes в параметрах, определенных событиями, на которые указывают **pbEventParameters.** 
    
 **pbEventParameters**
  
> Указатель на параметры, определенные событиям. Тип используемых параметров зависит от значения члена **ulEvent;** эти параметры документируются поставщиком, выдав событие. 
    
## <a name="remarks"></a>Примечания

Структура **EXTENDED_NOTIFICATION** является одним из членов союза структур, включенных в  состав информационного члена [структуры NOTIFICATION.](notification.md) Если член **структуры**  **УВЕДОМЛЕНий** содержит структуру EXTENDED_NOTIFICATION, то член **ulEventType** структуры **УВЕДОМЛЕНий** задает _fnevExtended_.
  
Расширенное событие определяется поставщиком услуг для представления типа изменений, которые не могут быть охвачены любыми другими предопределяемых событий. Только клиенты, которые знают перед регистрацией, что поставщик услуг поддерживает расширенное событие, могут зарегистрироваться для этого события. Клиенты не могут определить без дополнительных знаний, поддерживает ли поставщик услуг расширенное событие. Если поставщик служб поддерживает расширенное событие, он показывает, как обращаться с таким событием при его получении.
  
Расширенное уведомление отправляется сеансом при отключении клиента. Зарегистрируйтесь для этого уведомления, позвонив [в IMAPISession:::Advise](imapisession-advise.md) с параметром  _lpEntryID,_ заданным nULL, и  _параметром cbEntryID,_ заданным до нуля. 
  
Дополнительные сведения об уведомлении см. в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событиях в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор событий уведомлений и уведомлений.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение того, как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомления о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщики услуг могут использовать методы [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[�����������](notification.md)


[Структуры MAPI](mapi-structures.md)

