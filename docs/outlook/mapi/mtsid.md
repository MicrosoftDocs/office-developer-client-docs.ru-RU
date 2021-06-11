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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435175"
---
# <a name="mtsid"></a>MTSID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор входа транспортной системы сообщений X.400 (MTS). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макрос:  <br/> |[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a>"Участники"

 **cb**
  
> Количество bytes в массиве, описанного **участником abEntry.** 
    
 **abEntry**
  
> Массив Byte, содержащий данные идентификатора входа в МТС.
    
## <a name="remarks"></a>Примечания

Структура **MTSID** используется только для сопоставлений X.400 идентификаторов записей MAPI. Он соответствует структуре [FLATENTRY](flatentry.md) MAPI. 
  
Идентификатор МТС имеет тот же формат, что и идентификатор входа MAPI или двоичное значение свойства. Идентификаторы МТС могут быть особенно полезны для отмены отложенных сообщений. 
  
## <a name="see-also"></a>См. также



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[Структуры MAPI](mapi-structures.md)

