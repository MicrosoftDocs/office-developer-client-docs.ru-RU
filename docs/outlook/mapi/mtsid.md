---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342772"
---
# <a name="mtsid"></a>MTSID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи системы передачи сообщений X. 400 (MTS). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанные макросы:  <br/> |[Кбмтсид](cbmtsid.md), [кбневмтсид](cbnewmtsid.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a>Members

 **cb**
  
> Количество байтов в массиве, описываемом элементом **абентри** . 
    
 **Абентри**
  
> Массив байтов, который содержит данные идентификатора записи MTS.
    
## <a name="remarks"></a>Комментарии

Структура **мтсид** используется только для сопоставлений X. 400 идентификаторов записей MAPI. Он соответствует структуре MAPI [флатентри](flatentry.md) . 
  
Идентификатор MTS имеет тот же формат, что и идентификатор записи MAPI, или двоичное значение свойства. Идентификаторы MTS могут быть особенно полезными для отмены отложенных сообщений. 
  
## <a name="see-also"></a>См. также



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[Структуры MAPI](mapi-structures.md)

