---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8f17c3cf3d3d00930f87acd004b24f683a3fc8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808448"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**Относится к**: Outlook 
  
Содержит массив структур [FLATENTRY](flatentry.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a>Members

**cEntries**
  
> Число структур **FLATENTRY** в массиве описано участником **abEntries** . 
    
**cbEntries**
  
> Число байт в массиве, описываемых **abEntries**. 
    
**abEntries**
  
> Массив байтов, который содержит один или несколько **FLATENTRY** структуры, организованы конечных конец. 
    
## <a name="remarks"></a>Замечания

В массиве **abEntries** каждого **FLATENTRY** структура выравнивается по границе естественно выравнивания. Дополнительные байты включены как внутренние поля, чтобы сделать проверьте естественным выравниванием между любые две структуры **FLATENTRY** . Так как смещение член **abEntries** 8 первого **FLATENTRY** структуру в массиве всегда выравнивается правильно. Чтобы вычислить смещение Далее структуры, используйте размер первой записи округлено до следующего несколькими 4. Используйте макрос [CbFLATENTRY](cbflatentry.md) для вычисления размер структуры **FLATENTRY** . 
  
К примеру второй структура **FLATENTRY** начинается со смещением, состоящее из смещение первой записи, а также длина первой записи, округленное до следующие четыре байта. Длина первой записи — длина его элементом **Сертификация** плюс длина его **abEntry** элементом. 
  
В следующем примере кода указывает способ вычисления смещения в структуре **FLATENTRYLIST** . Предположим, что _lpFlatEntry_ — это указатель на структуру первой в списке. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>См. также

- [FLATENTRY](flatentry.md)
- [Каноническое свойство PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)
- [Структуры MAPI](mapi-structures.md)

