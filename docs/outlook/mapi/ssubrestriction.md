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
ms.openlocfilehash: de92a1328eb9a089a7914978ab20ab0bf5c430ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581960"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описываются ограничения дочерний объект, который используется для фильтрации строк вложения сообщения или получателей в таблице.
  
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

## <a name="members"></a>Members

 **ulSubObject**
  
> Тип дочерний объект в качестве целевого для ограничения. Ниже приведены возможные значения: 
    
PR_MESSAGE_RECIPIENTS 
  
> Ограничения применяются к таблице получателей сообщения. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Ограничения применяются к таблице вложений сообщений. 
    
 **lpRes**
  
> Указатель на структуру [SRestriction](srestriction.md) . 
    
## <a name="remarks"></a>Замечания

Ограничения дочерних объектов не поддерживаются все таблицы. Как правило содержимого только папки таблиц и их поддержка папок результатов поиска. Например ограничения дочерний объект используются для найдите сообщение, которое имеет определенный тип вложения или получателя. 
  
Если реализация не поддерживает ограничения дочерний объект, она возвращает MAPI_E_TOO_COMPLEX методов [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md) . 
  
Общие сведения о работе ограничения обратитесь к разделу [О ограничения](about-restrictions.md). 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

