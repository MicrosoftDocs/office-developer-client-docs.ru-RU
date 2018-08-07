---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8b4e090b3dd6bf8ecd2517dee57093106147e22d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812381"
---
# <a name="srow"></a>SRow

**Относится к**: Outlook 
  
Описывает строку из таблицы, содержащей выбранных свойств для указанного объекта. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a>Members

**ulAdrEntryPad**
  
> Внутренние поля байт для правильного выравнивания значения свойств указывает член **lpProps** . 
    
**cValues**
  
> Количество значений свойств, на который указывает **lpProps**. 
    
**lpProps**
  
> Указатель на массив структур [SPropValue](spropvalue.md) , которые описывают значения свойств для столбцов в строке. 
    
## <a name="remarks"></a>Замечания

Структура с **SRow** Описание строки в таблице. Она включена в структуре [TABLE_NOTIFICATION](table_notification.md) , который описывается в таблице уведомлений. 
  
**SRow** структуры используются следующие методы: 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData: IUnknown](itabledataiunknown.md) (множество методов) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Если более одного ряда должен быть описано, используется структуру [SRowSet](srowset.md) . Структура **SRowSet** содержит массив структур **SRow** и число структур в массиве. 
  
На следующем рисунке показана связь между **SRow** и **SRowSet** структуру данных. 
  
**Отношение между SRow и SRowSet**
  
![Отношение между SRow и SRowSet] (media/amapi_17.gif "Отношение между SRow и SRowSet")
  
Определения структур **SRow** то же, что [ADRENTRY](adrentry.md) структуры. Таким образом, может быть строку таблице получателей и запись в список адресов обрабатывается так же. 
  
Сведения о том, как следует выделить память для структуры **SRow** [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md)см.
  
## <a name="see-also"></a>См. также

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [Структуры MAPI](mapi-structures.md)
- [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

