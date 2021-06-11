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
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413859"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив [структур FLATENTRY.](flatentry.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макрос:  <br/> |[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a>"Участники"

**cEntries**
  
> Количество структур **FLATENTRY** в массиве, описанного участником **abEntries.** 
    
**cbEntries**
  
> Количество bytes в массиве, описанного **abEntries**. 
    
**abEntries**
  
> Массив Byte, содержащий одну или несколько структур **FLATENTRY,** расположены от конца до конца. 
    
## <a name="remarks"></a>Примечания

В **массиве abEntries** каждая структура **FLATENTRY** выравнивается на естественно выровненной границе. Дополнительные байты включены в качестве обивки, чтобы убедиться в естественном выравнивании между двумя **структурами FLATENTRY.** Первая структура **FLATENTRY** в массиве всегда выравнивается правильно, так как смещение члена **abEntries** — 8. Чтобы вычислить смещение следующей структуры, используйте размер первой записи, округленной до следующей несколько из 4. Чтобы вычислить размер структуры **FLATENTRY,** используйте макрос [CbFLATENTRY.](cbflatentry.md) 
  
Например, вторая структура **FLATENTRY** начинается с смещения, состоящего из смещения первой записи плюс длина первого входа, округленного до следующих четырех bytes. Длина первой записи — это длина члена **cb** плюс длина **абЕнтрийского** члена. 
  
В следующем примере кода указывается, как вычислять смещения в структуре **FLATENTRYLIST.** Предположим,  _что lpFlatEntry_ является указателем на первую структуру в списке. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>См. также

- [FLATENTRY](flatentry.md)
- [Каноническое свойство PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)
- [Структуры MAPI](mapi-structures.md)

