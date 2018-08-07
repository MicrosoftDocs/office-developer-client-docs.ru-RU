---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a5f950907e2b14cb4101a094715c24b25beb2016
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808440"
---
# <a name="filetime"></a>FILETIME

  
  
**Относится к**: Outlook 
  
Содержит неподписанные 64-разрядная версия значения даты и времени для файла. Это значение представляет число единиц 100 наносекунд с момента запуска 1 января 1601. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Members

 **dwLowDateTime**
  
> Младшие 32 разряда значение времени, в файл. 
    
 **dwHighDateTime**
  
> Старшие 32 разряда значение времени, в файл.
    
## <a name="remarks"></a>Замечания

Свойство типа PT_SYSTIME имеет структуру **FILETIME** его значение. Такое свойство имеет тип данных **FILETIME** для элемента **значение** в его определение в структуре [SPropValue](spropvalue.md) . 
  
Определение структуры **FILETIME** происходит в _Справочник программиста Win32_ в файл заголовка MAPI Mapidefs.h. MAPI определяет структуру условию, убедитесь в том, что оно указано при определении Win32 недоступен. 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

