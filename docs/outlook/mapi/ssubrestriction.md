---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406327"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение под объекта, которое используется для фильтрации строк вложения или таблицы получателей сообщения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a>"Участники"

 **ulSubObject**
  
> Тип суб-объекта, который будет служить в качестве целевого объекта для ограничения. Возможные значения: 
    
PR_MESSAGE_RECIPIENTS 
  
> Применить ограничение к таблице получателей сообщения. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Применить ограничение к таблице вложений сообщения. 
    
 **lpRes**
  
> Указатель на [структуру SRestriction.](srestriction.md) 
    
## <a name="remarks"></a>Примечания

Ограничения под объекта поддерживаются не всеми таблицами. Обычно их поддерживают только таблицы содержимого папок и папки результатов поиска. Например, для поиска сообщения с определенным типом вложения или получателя используются ограничения под объекта. 
  
Если реализация не поддерживает суб-объектные ограничения, она возвращает MAPI_E_TOO_COMPLEX из методов [IMAPITable:::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow.](imapitable-findrow.md) 
  
Общие вопросы о том, как работают ограничения, см. в общих [обсуждениях об ограничениях.](about-restrictions.md) 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

