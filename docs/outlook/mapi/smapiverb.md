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
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309487"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает команду MAPI.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
   
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

 **Лверб**
  
> Код, представляющий команду, которая передается в [имапиформ::D оверб](imapiform-doverb.md). Стандартные команды определяются в файле заголовка Ексчформ. h.
    
 **Сзвербнаме**
  
> Отображаемое имя команды в том виде, в котором оно отображается в меню формы.
    
 **Фуфлагс**
  
> Флаги для команды.
    
 **Грфаттрибс**
  
> Атрибуты команды. 
    
 **ulFlags**
  
> Флаг, указывающий формат отображаемого имени команды. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Отображаемое имя в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, отображаемое имя отображается в формате ANSI.
    
## <a name="remarks"></a>Замечания

Структура **смапиверб** передается в качестве параметра в следующих методах: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>См. также



[CbMessageClassArray](cbmessageclassarray.md)


[Структуры MAPI](mapi-structures.md)

