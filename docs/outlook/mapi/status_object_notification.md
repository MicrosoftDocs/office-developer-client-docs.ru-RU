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
  
Описывает объект status, на который влияет изменение. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
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

 **кбентрид**
  
> Количество байтов в идентификаторе записи, на который указывает элемент **лпентрид** . 
    
 **лпентрид**
  
> Указатель на идентификатор записи измененного объекта Status.
    
 **квалуес**
  
> Количество структур [спропвалуе](spropvalue.md) в массиве, на которое указывает элемент **лппропвалс** . 
    
 **лппропвалс**
  
> Указатель на массив структур **спропвалуе** , описывающих свойства измененного объекта Status. 
    
## <a name="remarks"></a>Примечания

Структура **STATUS_OBJECT_NOTIFICATION** — это один из членов объединения структур, включенных в элемент **info** структуры [уведомления](notification.md) . Структура **STATUS_OBJECT_NOTIFICATION** включена в уведомление объекта Status для события типа _фневстатусобжектмодифиед_. Уведомление объекта Status является внутренним уведомлением MAPI; Клиенты и поставщики услуг не могут регистрироваться для ИТ, и поставщики услуг не могут создать ее.
  
Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событии в MAPI](event-notification-in-mapi.md) <br/> |Общие сведения о событиях уведомлений и уведомлений.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение того, как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомлений о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщики услуг могут использовать метод **имаписуппорт** для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[�����������](notification.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

