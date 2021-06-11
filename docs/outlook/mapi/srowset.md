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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив [структур SRow.](srow.md) Каждая **структура SRow** описывает строку из таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макрос:  <br/> |[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>"Участники"

 **cRows**
  
> Количество **структур SRow** в **члене aRow.** 
    
 **aRow**
  
> Массив **структур SRow.** Каждая строка в таблице имеет одну структуру. 
    
## <a name="remarks"></a>Примечания

Структура **SRowSet** используется для описания нескольких строк данных из таблицы. **Структуры SRowSet** используются в [методах интерфейса IAddrBook,](iaddrbookimapiprop.md) [ITableData](itabledataiunknown.md)и [IMAPITable,](imapitableiunknown.md) а также в следующих функциях: 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 **Структуры SRowSet** определяются так же, как структуры [ADRLIST,](adrlist.md) что позволяет рассматривать строки таблицы получателей и записи в списке адресов. Как **структуры SRowSet,** так и **структуры ADRLIST** можно передать таким методам, как [IMessage::ModifyRecipients](imessage-modifyrecipients.md) и [IAddrBook::Address.](iaddrbook-address.md) 
  
Кроме того, правила распределения памяти для **структур SRowSet** такие же, как и для **структур ADRLIST.** Чтобы резюмировать, каждая структура [SPropValue](spropvalue.md) в массиве, на который указывает член **lpProps** каждой строки в наборе строк, должна быть выделена отдельно с помощью [MAPIAllocateBuffer](mapiallocatebuffer.md). Каждая структура значения свойств также должна быть расположена с помощью [MAPIFreeBuffer](mapifreebuffer.md) перед сделкой структуры **SRowSet,** чтобы не потерять указатели на выделенные **структуры SPropValue.** Выделенная память строки может быть сохранена и повторно использоваться вне контекста **структуры SRowSet.** 
  
Дополнительные сведения о выделении памяти для структур **SRowSet** см. в статью Управление памятью [для структур ADRLIST и SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md) 
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Структуры MAPI](mapi-structures.md)

