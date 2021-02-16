---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426270"
---
# <a name="status_object_notification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает объект состояния, на который повлияло изменение. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a>"Участники"

 **cbEntryID**
  
> Количество вхождений в идентификаторе записи, на который указывает **член lpEntryID.** 
    
 **lpEntryID**
  
> Указатель на идентификатор записи измененного объекта состояния.
    
 **cValues**
  
> Количество структур [SPropValue](spropvalue.md) в массиве, на который указывает **член lpPropVals.** 
    
 **lpPropVals**
  
> Указатель на массив структур **SPropValue,** описывая свойства измененного объекта состояния. 
    
## <a name="remarks"></a>Примечания

Структура **STATUS_OBJECT_NOTIFICATION** является одним из членов объединения структур, включенных в  состав данных структуры [NOTIFICATION.](notification.md) Структура **STATUS_OBJECT_NOTIFICATION** включается в уведомление объекта состояния для события типа  _fnevStatusObjectModified_. Уведомление объекта состояния — это внутреннее уведомление MAPI; клиенты и поставщики услуг не могут зарегистрироваться для него, а поставщики услуг не могут создать его.
  
Дополнительные сведения об уведомлении см. в темах, описанных в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событии в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор событий уведомлений и уведомлений.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение того, как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомлений о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщики служб могут использовать метод **IMAPISupport** для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[�����������](notification.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

