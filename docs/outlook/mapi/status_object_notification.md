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
ms.openlocfilehash: 71e0a08436c925f0d68d63111722cc01bd73cc5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812402"
---
# <a name="statusobjectnotification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Относится к**: Outlook 
  
Описывает объект состояния, которые были затронуты изменения. 
  
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

## <a name="members"></a>Members

 **cbEntryID**
  
> Число байт в идентификаторе запись, на который указывает член **lpEntryID** . 
    
 **lpEntryID**
  
> Указатель на идентификатор записи измененное состояние объекта.
    
 **cValues**
  
> Число структур [SPropValue](spropvalue.md) в массиве, на который указывает член **lpPropVals** . 
    
 **lpPropVals**
  
> Указатель на массив структур **SPropValue** , которые описывают свойства объекта измененное состояние. 
    
## <a name="remarks"></a>Замечания

Структура **STATUS_OBJECT_NOTIFICATION** — это один из участников объединение структуры, включенные в элемент **info** структуры [УВЕДОМЛЕНИЙ](notification.md) . Структура **STATUS_OBJECT_NOTIFICATION** входит в состав объекта уведомление о состоянии для события из типа _fnevStatusObjectModified_. Уведомление о доставке объект является внутренних уведомлений MAPI; для него нельзя зарегистрировать клиентов и поставщиков услуг и поставщиков услуг не удается создать его.
  
Дополнительные сведения о уведомлений видеть темы, описанные в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событиях в MAPI](event-notification-in-mapi.md) <br/> |Общий обзор уведомлений и события уведомления.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомлений о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщиков услуг можно использовать метод **IMAPISupport** для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[�����������](notification.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

