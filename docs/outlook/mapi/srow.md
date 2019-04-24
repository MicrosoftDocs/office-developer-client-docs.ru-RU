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
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336520"
---
# <a name="srow"></a>SRow

**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает строку из таблицы, которая содержит выбранные свойства для определенного объекта. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a>Members

**Уладрентрипад**
  
> Заполнение байтов для правильного выравнивания значений свойств, на которые указывает элемент **лппропс** . 
    
**Квалуес**
  
> Количество значений свойств, на которые указывает **лппропс**. 
    
**Лппропс**
  
> Указатель на массив структур [спропвалуе](spropvalue.md) , описывающих значения свойств для столбцов в строке. 
    
## <a name="remarks"></a>Комментарии

Структура **сров** описывает строку в таблице. Он включен в структуру [табле_нотификатион](table_notification.md) , сопровождающую табличное уведомление. 
  
Структуры **сров** используются в следующих методах: 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [Итабледата: IUnknown](itabledataiunknown.md) (многие методы) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Если необходимо описать более одной строки, используется структура [SRowSet](srowset.md) . Структура **SRowSet** содержит массив структур **сров** и число структур в массиве. 
  
На следующем рисунке показана связь между **сров** и структурой данных **SRowSet** . 
  
**Отношение между SRow и SRowSet**
  
![Отношение между сров и SRowSet] (media/amapi_17.gif "Отношение между сров и SRowSet")
  
Структуры **сров** определяются так же, как структуры [адрентри](adrentry.md) . Таким образом, строка таблицы получателей и запись в списке адресов могут рассматриваться как один и тот же. 
  
Сведения о том, как следует выделить память для структур **сров** , можно узнать в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>См. также

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [Структуры MAPI](mapi-structures.md)
- [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

