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
ms.openlocfilehash: ea841ef4bc551581fb2d9ca90201b4615e67f134
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808452"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**Относится к**: Outlook 
  
Содержит массив структур [MTSID](mtsid.md) , каждая из которых содержит идентификатор записи система X.400 сообщения транспорта. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a>Members

 **cMTSIDs**
  
> Число структур **MTSID** в массиве описано участником **abMTSIDs** . 
    
 **cbMTSIDs**
  
> Число байт в массиве, описываемых **abMTSIDs**.
    
 **abMTSIDs**
  
> Массив байтов, который содержит один или несколько **MTSID** структуры. 
    
## <a name="remarks"></a>Замечания

Использование **FLATMTSIDLIST** структуры в системе обмена сообщениями X.400 соответствует использования [FLATENTRYLIST](flatentrylist.md) структуры в системе обмена сообщениями MAPI. MAPI использует **FLATMTSIDLIST** структуры для сохранения свойств X.400 во время обработки сообщений. При обработке входящих и исходящих сообщений X.400 поставщиков услуг использовать структуры **FLATMTSIDLIST** . 
  
В массиве **abMTSIDs** каждого **MTSID** структура выравнивается по границе естественно выравнивания. Дополнительные байты включены как внутренние поля, чтобы сделать проверьте естественным выравниванием между любые две структуры **MTSID** . Так как смещение член **abMTSIDs** 8 первого **MTSID** структуру в массиве всегда выравнивается правильно. Чтобы вычислить смещение Далее структуры, используйте размер первой записи округлено до следующего несколькими 4. Используйте макрос [CbNewMTSID](cbnewmtsid.md) для вычисления размера структуры **MTSID** . 
  
## <a name="see-also"></a>См. также



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[Структуры MAPI](mapi-structures.md)

