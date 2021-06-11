---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439221"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив структур [MTSID,](mtsid.md) каждая из которых содержит идентификатор входа ВТС X.400. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макрос:  <br/> |[CbFLATMTSIDLIST,](cbflatmtsidlist.md) [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a>"Участники"

 **cMTSIDs**
  
> Count of **MTSID** structures in the array described by the **abMTSIDs** member. 
    
 **cbMTSIDs**
  
> Количество bytes в массиве, описанного **abMTSIDs**.
    
 **abMTSIDs**
  
> Массив Byte, содержащий одну или несколько **структур MTSID.** 
    
## <a name="remarks"></a>Примечания

Использование **структуры FLATMTSIDLIST** в сообщении X.400 соответствует использованию структуры [FLATENTRYLIST](flatentrylist.md) в сообщении MAPI. MapI использует **структуры FLATMTSIDLIST** для поддержания свойств X.400 во время обработки сообщений. Поставщики служб используют **структуры FLATMTSIDLIST** при обработке входящих и исходяющих сообщений X.400. 
  
В **массиве abMTSIDs** каждая **структура MTSID** выравнивается на естественно выровненной границе. Дополнительные байты включены в качестве обивки, чтобы убедиться в естественном выравнивании между двумя **структурами MTSID.** Первая структура **MTSID** в массиве всегда выравнивается правильно, так как смещение члена **abMTSIDs** — 8. Чтобы вычислить смещение следующей структуры, используйте размер первой записи, округленной до следующей несколько из 4. Используйте [макрос CbNewMTSID](cbnewmtsid.md) для вычисления размера структуры **MTSID.** 
  
## <a name="see-also"></a>См. также



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[Структуры MAPI](mapi-structures.md)

