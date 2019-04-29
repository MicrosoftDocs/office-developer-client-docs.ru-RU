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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив структур [флатентри](flatentry.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанные макросы:  <br/> |[Кбфлатентрилист](cbflatentrylist.md), [кбневфлатентрилист](cbnewflatentrylist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a>Members

**Центриес**
  
> Количество структур **флатентри** в массиве, описываемом членом **абентриес** . 
    
**Кбентриес**
  
> Количество байтов в массиве, описываемом **абентриес**. 
    
**Абентриес**
  
> Массив байтов, который содержит одну или несколько структур **флатентри** , упорядоченные в конец. 
    
## <a name="remarks"></a>Примечания

В массиве **абентриес** каждая структура **флатентри** выровнена по естественным выровненным границам. Дополнительные байты включаются в качестве внутренних полей, чтобы обеспечить естественное выравнивание между двумя структурами **флатентри** . Первая структура **флатентри** в массиве всегда выровнена правильно, так как смещение элемента **абентриес** равно 8. Чтобы вычислить смещение следующей структуры, используйте размер первой записи, округленной вплоть до числа до ближайшего кратного 4. Чтобы вычислить размер структуры **флатентри** , используйте макрос [кбфлатентри](cbflatentry.md) . 
  
Например, вторая структура **флатентри** начинается со смещения, состоящего из смещения первой записи плюс длина первого элемента, округленного до следующих четырех байтов. Длина первой записи — это длина члена **CB** , а также длина ее элемента **абентри** . 
  
В приведенном ниже примере кода показано, как вычислять смещения в структуре **флатентрилист** . Предположим, что _лпфлатентри_ является указателем на первую структуру в списке. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>См. также

- [FLATENTRY](flatentry.md)
- [Каноническое свойство PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)
- [Структуры MAPI](mapi-structures.md)

