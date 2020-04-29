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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает сведения, связанные с критической ошибкой. Это приводит к созданию уведомления об ошибке. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
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

 **кбентрид**
  
> Количество байтов в идентификаторе записи, на который указывает **лпентрид**. 
    
 **лпентрид**
  
> Указатель на идентификатор записи объекта, который вызывает ошибку.
    
 **SCODE**
  
> Значение ошибки для критической ошибки. 
    
 **ulFlags**
  
> Битовая маска флагов, используемая для обозначения формата текста, на который указывает элемент **лпсзеррор** в структуре, на которую указывает **лпмапиеррор**. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.
    
 **лпмапиеррор**
  
> Указатель на структуру [мапиеррор](mapierror.md) , описывающую ошибку. 
    
## <a name="remarks"></a>Примечания

Структура **ERROR_NOTIFICATION** — это один из членов объединения структур, включенных в элемент **info** структуры [уведомления](notification.md) . Когда элемент **info** элемента структуры **уведомлений** содержит структуру **ERROR_NOTIFICATION** , элемент **улевенттипе** структуры **уведомлений** имеет значение _фневкритикалеррор_.
  
Значение члена **кбентрид** и члена **лпентрид** могут иметь значение null. 
  
Дополнительные сведения об уведомлении можно найти в разделах, приведенных в следующей таблице.
  
|**Статья**|**Описание**|
|:-----|:-----|
|[Уведомление о событии в MAPI](event-notification-in-mapi.md) <br/> |Общие сведения о событиях уведомлений и уведомлений.  <br/> |
|[Обработка уведомлений](handling-notifications.md) <br/> |Обсуждение того, как клиенты должны обрабатывать уведомления.  <br/> |
|[Поддержка уведомлений о событиях](supporting-event-notification.md) <br/> |Обсуждение того, как поставщики услуг могут использовать метод **имаписуппорт** для создания уведомлений.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[�����������](notification.md)


[Структуры MAPI](mapi-structures.md)

