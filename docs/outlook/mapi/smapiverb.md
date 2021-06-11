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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410961"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает глагол MAPI.
  
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

## <a name="members"></a>"Участники"

 **lVerb**
  
> Код, представляющий глагол, который передается [IMAPIForm::D oVerb](imapiform-doverb.md). Стандартные глаголы определяются в файле загона Exchform.h.
    
 **szVerbname**
  
> Отображение имени глагола по мере его отображения в меню формы.
    
 **fuFlags**
  
> Флаги для глагола.
    
 **grfAttribs**
  
> Атрибуты глагола. 
    
 **ulFlags**
  
> Флаг с указанием формата отображаемого имени глагола. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Имя дисплея находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, имя отображения находится в формате ANSI.
    
## <a name="remarks"></a>Примечания

Структура **SMAPIVerb** передается в качестве параметра в следующих методах: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>См. также



[CbMessageClassArray](cbmessageclassarray.md)


[Структуры MAPI](mapi-structures.md)

