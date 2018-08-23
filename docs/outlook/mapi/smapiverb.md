---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 11f11ae2d90a951a119895f3e0e3e3ca0dbc0fc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573700"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описываются команды MAPI.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a>Members

 **lVerb**
  
> Код, который представляет команду, которая передается [IMAPIForm::DoVerb](imapiform-doverb.md). Стандартные команды определены в файле заголовка Exchform.h.
    
 **szVerbname**
  
> Отображаемое имя команды, как оно отображается в виде меню.
    
 **fuFlags**
  
> Флаги для команды.
    
 **grfAttribs**
  
> Атрибуты команды. 
    
 **ulFlags**
  
> Флаг, указывающий формат команды отображаемое имя. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Отображаемое имя — в формате Юникод. Если флаг MAPI_UNICODE не установлен, отображаемое имя — в формате ANSI.
    
## <a name="remarks"></a>Замечания

Структура **SMAPIVerb** передается как параметр в следующих методов: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>См. также



[CbMessageClassArray](cbmessageclassarray.md)


[Структуры MAPI](mapi-structures.md)

