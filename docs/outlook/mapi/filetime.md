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
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409505"
---
# <a name="filetime"></a>FILETIME

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит Неподписанное 64 – разрядное значение даты и времени для файла. Это значение представляет число единиц 100 НС с начала 1 января 1601. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>"Участники"

 **двловдатетиме**
  
> Младшие биты 32 значения времени файла. 
    
 **двхигхдатетиме**
  
> 32 бит высокого порядка бит значения времени файла.
    
## <a name="remarks"></a>Примечания

Свойство типа PT_SYSTIME имеет структуру **fileTime** для его значения. Такое свойство имеет тип данных **fileTime** для элемента **value** в его определении в структуре [спропвалуе](spropvalue.md) . 
  
Определение структуры **fileTime** находится в _справочнике программиста Win32_ и в файле заголовка MAPI MAPIDEFS. h. MAPI определяет структуру условно, чтобы убедиться, что она определена, когда определение Win32 недоступно. 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

