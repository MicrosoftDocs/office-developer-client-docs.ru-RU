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
ms.openlocfilehash: de9b5e377840b1fbfa3b6dd73fd952c0c72efeb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580644"
---
# <a name="extendednotification"></a>EXTENDED_NOTIFICATION

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описывает сведения, относящиеся к событию, зависящие от поставщика службы. 
  
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

## <a name="members"></a>Members

 **ulEvent**
  
> Код расширенного событий, определяемый поставщиком.
    
 **cb**
  
> Число байт в параметрах конкретного события, на который указывает **pbEventParameters**. 
    
 **pbEventParameters**
  
> Указатель на параметры, относящиеся к события. Тип параметров, которые используются зависит от значение элемента **ulEvent** ; Эти параметры описаны поставщиком, выпустивший события. 
    
## <a name="remarks"></a>Замечания

Структура **EXTENDED_NOTIFICATION** — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) . Когда участник **info** структуры **уведомление** содержит структуру **EXTENDED_NOTIFICATION** , член **ulEventType** структуры **УВЕДОМЛЕНИЙ** задано значение _fnevExtended_.
  
Расширенные события определяется поставщиком услуг для представления тип изменения, не могут быть защищены торговыми любой из предварительно определенных событий. Для этого события можно регистрировать только клиентов, которые знать, прежде чем они зарегистрировать, что поставщик услуг поддерживает расширенные события. Не поддерживается для клиентов определить без высокий уровень знания, если поставщик услуг поддерживает расширенные события. Если поставщик услуг поддерживает расширенные события, его показано, как обрабатывать события при получении.
  
Уведомление о расширенных отправляется в сеансе, если это клиент выходит из системы. Регистрация для этого уведомления путем вызова [IMAPISession::Advise](imapisession-advise.md) с параметром _lpEntryID_ значение NULL, а параметр _cbEntryID_ , равным нулю. 
  
Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событиях в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор уведомлений и события уведомления.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомлений о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщиков услуг можно использовать методы [IMAPISupport](imapisupportiunknown.md) для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[�����������](notification.md)


[Структуры MAPI](mapi-structures.md)

