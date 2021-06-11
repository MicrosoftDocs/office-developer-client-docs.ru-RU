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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410436"
---
# <a name="srow"></a>SRow

**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает строку из таблицы, которая содержит выбранные свойства для определенного объекта. 
  
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

## <a name="members"></a>"Участники"

**ulAdrEntryPad**
  
> Заполнение байтов для правильного выравнивания значений свойств, на которые указывает член **lpProps.** 
    
**cValues**
  
> Количество значений свойств, на которые указывает **lpProps.** 
    
**lpProps**
  
> Указатель на массив [структур SPropValue,](spropvalue.md) описывая значения свойств столбцов в строке. 
    
## <a name="remarks"></a>Примечания

Структура **SRow** описывает строку в таблице. Он включен в [структуру](table_notification.md) TABLE_NOTIFICATION, сопровождаемую уведомлением таблицы. 
  
**Структуры SRow** используются в следующих методах: 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData : IUnknown](itabledataiunknown.md) (многие методы) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
При описании более одной строки используется структура [SRowSet.](srowset.md) Структура **SRowSet** содержит массив **структур SRow** и количество структур в массиве. 
  
На следующем рисунке показана связь **между SRow** и **структурой данных SRowSet.** 
  
**Отношение между SRow и SRowSet**
  
![Связь между SRow и SRowSet связь](media/amapi_17.gif "между SRow и SRowSet")
  
**Структуры SRow** определяются так же, как [структуры ADRENTRY.](adrentry.md) Поэтому строка таблицы получателей и запись в списке адресов можно рассматривать одинаково. 
  
Сведения о выделении памяти для структур **SRow** см. в рубрике Управление памятью [для ADRLIST и SRowSet Structures.](managing-memory-for-adrlist-and-srowset-structures.md)
  
## <a name="see-also"></a>См. также

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [Структуры MAPI](mapi-structures.md)
- [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

