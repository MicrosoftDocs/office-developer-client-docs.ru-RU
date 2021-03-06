---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439725"
---
# <a name="ssortorder"></a>SSortOrder
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет, как сортировать строки таблицы, какой столбец использовать в качестве ключа сортировки и направление сортировки. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a>"Участники"

**ulPropTag**
  
> Тег свойства, определяющий ключ сортировки или столбец категории.
    
**ulOrder**
  
> Порядок сортировки данных. Возможные значения:
    
  - TABLE_SORT_ASCEND. Таблица должна сортироваться в порядке восходящей.
      
  - TABLE_SORT_COMBINE. Операция сортировки должна создать категорию, которая объединяет свойство, указанное в качестве столбца ключа сортировки в члене **ulPropTag,** с столбцом ключа сортировки, указанным в предыдущей структуре **SSortOrder.** 
      
    TABLE_SORT_COMBINE можно использовать только в том случае, если структура **SSortOrder** используется в качестве записи в [структуре SSortOrderSet](ssortorderset.md) для указания нескольких заказов сортировки для классифицировать сорт. TABLE_SORT_COMBINE не может использоваться в первой **структуре SSortOrder** в **структуре SSortOrderSet.** 
      
  - TABLE_SORT_DESCEND. Таблица должна сортироваться в порядке убывания.
      
  - TABLE_SORT_CATEG_MAX. Таблица должна сортироваться по максимальному значению члена **ulPropTag** для строк данных в категориях, указанных в предыдущем порядке сортировки в структуре **SSortOrderSet.** 
      
  - TABLE_SORT_CATEG_MIN. Таблица должна сортироваться на минимальном значении члена **ulPropTag** для строк данных в категориях, указанных в предыдущем порядке сортировки в структуре **SSortOrderSet.** 
    
## <a name="remarks"></a>Примечания

Структура **SSortOrder используется** для описания выполнения стандартной операции сортировки или сортировки категории. **Структуры SSortOrder** обычно объединяются в **структуру SSortOrderSet** для описания нескольких ключей и направлений сортировки. **Структуры SSortOrderSet** используются в следующих функциях и методах интерфейса: 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Диапазон разрешенных столбцов в таблице, которые можно использовать в качестве ключа сортировки, зависит от поставщика. Столбцы, которые являются частью текущего набора столбцов, всегда можно использовать в качестве ключей сортировки. Однако каждый поставщик определяет, можно ли определить ключи сортировки с помощью доступных столбцов, которые не находятся в текущем наборе столбцов. Доступный столбец — это столбец, возвращаемый из [IMAPITable::QueryColumns](imapitable-querycolumns.md) при TBL_ALL_COLUMNS флага. 
  
Член **ulOrder** указывает как сведения о направлении порядка, так и о категоризации, например, по разговору [(PidTagConversationTopic),](pidtagconversationtopic-canonical-property.md)то есть разговорной теме, которая является серией сообщений и ответов. Строки можно сортировать в последовательности восходящих или убывающих строк со всеми записями NULL, позиционными последними. 
  
Значение TABLE_SORT_COMBINE указывает, что столбец, указанный в **ulPropTag,** должен сочетаться с предыдущим столбцом категории для формирования сводной категории. То есть вместо классификации уникальных значений отдельных столбцов TABLE_SORT_COMBINE позволяет классифицовать уникальные значения сочетания столбцов. Например, можно определить одну категорию для групповых сообщений, полученных от конкретного отправитель по определенному вопросу. Настройка значения TABLE_SORT_COMBINE уменьшает количество отображаемого числа строк категории. 
  
Сортировка на столбцах с несколькими значениями не поддерживается всеми реализации таблиц. Если поддерживается, MV_FLAG с помощью макроса MVI_PROP к тегу свойств в члене **ulPropTag,** чтобы определить ключ сортировки как столбец с несколькими значениями. Сортировка в столбце с несколькими значениями основана на использовании отдельных значений. 
  
> [!IMPORTANT]
> Значения **члена ulOrder** TABLE_SORT_CATEG_MAX и TABLE_SORT_CATEG_MIN могут быть не определены в загружаемом файле заголовки, который у вас сейчас есть, и в этом случае его можно добавить в код с помощью следующих значений: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Дополнительные сведения о стандартной и категоризации сортировки см. в [рубрике Сортировка и классификация.](sorting-and-categorization.md) 
  
## <a name="see-also"></a>См. также

- [SSortOrderSet](ssortorderset.md)
- [Структуры MAPI](mapi-structures.md)

