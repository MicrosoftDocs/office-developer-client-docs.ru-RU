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
ms.openlocfilehash: 82fa1b0af504cc4774b1dc077a6ef48378740d26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580679"
---
# <a name="srowset"></a>SRowSet

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит массив структур [SRow](srow.md) . Структура каждого **SRow** описывает строку из таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md) [SizedSRowSet](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>Members

 **cRows**
  
> Число структур **SRow** в элемент **aRow** . 
    
 **aRow**
  
> Массив структур **SRow** . Существует один структуры для каждой строки в таблице. 
    
## <a name="remarks"></a>Замечания

Структура **SRowSet** используется для описания несколько строк данных из таблицы. **SRowSet** структуры используются в [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)и [IMAPITable](imapitableiunknown.md) методов интерфейса, кроме следующих функций: 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 Определения структур **SRowSet** так же, как [ADRLIST](adrlist.md) структуры строк получателей таблицы и операций в список адресов, чтобы быть обрабатывается так же. Методы, такие как [IMessage::ModifyRecipients](imessage-modifyrecipients.md) и [IAddrBook::Address](iaddrbook-address.md)могут передаваться **SRowSet** структуры и структуры **ADRLIST** . 
  
Кроме того правила для выделения памяти для структуры **SRowSet** совпадают с требованиями для структуры **ADRLIST** . В целом, каждый [SPropValue](spropvalue.md) структуру в массиве по член **lpProps** каждой строки в строке, на который указывает необходимо выделить отдельно с помощью [MAPIAllocateBuffer](mapiallocatebuffer.md). Структура значение каждого свойства должна быть отменено с помощью [MAPIFreeBuffer](mapifreebuffer.md) перед освобождение структуры **SRowSet** , чтобы указатели на выделенный **SPropValue** структуры не сохраняются. Строки выделенная объема памяти может затем сохранять и повторно использовать вне контекста **SRowSet** структуры. 
  
Дополнительные сведения о том, как следует выделить память для структуры **SRowSet** [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md)см. 
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Структуры MAPI](mapi-structures.md)

