---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407258"
---
# <a name="srowset"></a>SRowSet

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив структур [сров](srow.md) . Каждая структура **сров** описывает строку из таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанные макросы:  <br/> |[Кбневсровсет](cbnewsrowset.md), [кбсровсет](cbsrowset.md), [сизедсровсет](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>"Участники"

 **CRowset**
  
> Количество структур **сров** в элементе **аров** . 
    
 **аров**
  
> Массив структур **сров** . Для каждой строки в таблице существует одна структура. 
    
## <a name="remarks"></a>Примечания

Структура **SRowSet** используется для описания нескольких строк данных из таблицы. Структуры **SRowSet** используются в методах интерфейса [IAddrBook](iaddrbookimapiprop.md), [итабледата](itabledataiunknown.md)и [IMAPITable](imapitableiunknown.md) в дополнение к следующим функциям: 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 Структуры **SRowSet** определяются так же, как структуры [ADRLIST](adrlist.md) , чтобы можно было обрабатывать строки таблицы получателей и записи в списке адресов. Структуры **SRowSet** и структуры **ADRLIST** можно передавать в методы, такие как [iMessage:: МодифиреЦипиентс](imessage-modifyrecipients.md) и [IAddrBook:: Address](iaddrbook-address.md). 
  
Кроме того, правила выделения памяти для структур **SRowSet** одинаковы для структур **ADRLIST** . В качестве итогов каждая структура [спропвалуе](spropvalue.md) в массиве, на которую указывает элемент **лппропс** в наборе строк, должна выделяться отдельно с помощью [мапиаллокатебуффер](mapiallocatebuffer.md). Каждая структура значения свойства также должна быть освобождена с помощью [мапифрибуффер](mapifreebuffer.md) перед освобождением структуры **SRowSet** , чтобы указатели на выделенные структуры **спропвалуе** не терялись. Выделенная память строки может сохраняться и повторно использоваться вне контекста структуры **SRowSet** . 
  
Более подробную информацию о том, как следует выделить память для структур **SRowSet** , можно узнать в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Структуры MAPI](mapi-structures.md)

