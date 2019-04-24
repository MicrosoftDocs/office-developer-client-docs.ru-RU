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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327309"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив структур [мтсид](mtsid.md) , каждый из которых содержит идентификатор записи MTS (X. 400 Message transporting System). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанные макросы:  <br/> |[Кбфлатмтсидлист](cbflatmtsidlist.md), [кбневфлатмтсидлист](cbnewflatmtsidlist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a>Members

 **Кмтсидс**
  
> Количество структур **мтсид** в массиве, описываемом членом **абмтсидс** . 
    
 **Кбмтсидс**
  
> Количество байтов в массиве, описываемом **абмтсидс**.
    
 **Абмтсидс**
  
> Массив байтов, который содержит одну или несколько структур **мтсид** . 
    
## <a name="remarks"></a>Замечания

Использование структуры **флатмтсидлист** в сообщениях X. 400 соответствует использованию структуры [флатентрилист](flatentrylist.md) в сообщениях MAPI. В MAPI используются структуры **флатмтсидлист** для хранения свойств X. 400 во время обработки сообщений. Поставщики услуг используют структуры **флатмтсидлист** при обработке входящих и исходящих сообщений X. 400. 
  
В массиве **абмтсидс** каждая структура **мтсид** выровнена по естественным выровненным границам. Дополнительные байты включаются в качестве внутренних полей, чтобы обеспечить естественное выравнивание между двумя структурами **мтсид** . Первая структура **мтсид** в массиве всегда выровнена правильно, так как смещение элемента **абмтсидс** равно 8. Чтобы вычислить смещение следующей структуры, используйте размер первой записи, округленной вплоть до числа до ближайшего кратного 4. Чтобы вычислить размер структуры **мтсид** , используйте макрос [кбневмтсид](cbnewmtsid.md) . 
  
## <a name="see-also"></a>См. также



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[Структуры MAPI](mapi-structures.md)

