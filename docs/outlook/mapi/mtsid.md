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
ms.openlocfilehash: e42bbf23ea8cf4e6196017a962329366e168420d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810042"
---
# <a name="mtsid"></a>MTSID

  
  
**Относится к**: Outlook 
  
Содержит идентификатор записи система X.400 сообщения транспорта. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a>Members

 **cb**
  
> Число байт в массиве описано участником **abEntry** . 
    
 **abEntry**
  
> Массив байтов, который содержит данные идентификатор MTS запись.
    
## <a name="remarks"></a>Замечания

Структура **MTSID** используется только для сопоставления X.400 идентификаторов запись MAPI. Оно соответствует MAPI [FLATENTRY](flatentry.md) структуры. 
  
Идентификатор MTS имеет тот же формат как идентификатор записи MAPI или двоичного свойства значение. Идентификаторы MTS может быть полезно для отмены отложенные сообщения. 
  
## <a name="see-also"></a>См. также



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[Структуры MAPI](mapi-structures.md)

