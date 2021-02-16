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
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
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
  
> Тег свойства, определяющий ключ сортировки или столбец категории для сортировки по категориям.
    
**ulOrder**
  
> Порядок сортировки данных. Возможные значения:
    
  - TABLE_SORT_ASCEND: таблица должна сортироваться по возрастанию.
      
  - TABLE_SORT_COMBINE: операция сортировки должна создать категорию, которая объединяет свойство, определенное как столбец ключа сортировки в элементе **ulPropTag,** с столбцом ключа сортировки, указанным в предыдущей структуре **SSortOrder.** 
      
    TABLE_SORT_COMBINE можно использовать, только если структура **SSortOrder** используется в качестве записи в [структуре SSortOrderSet](ssortorderset.md) для указания нескольких заказов сортировки для сортировки по категориям. TABLE_SORT_COMBINE не может использоваться в первой **структуре SSortOrder** в **структуре SSortOrderSet.** 
      
  - TABLE_SORT_DESCEND: таблица должна сортироваться по убываю.
      
  - TABLE_SORT_CATEG_MAX: таблица должна сортироваться по максимальному значению члена **ulPropTag** для строк данных в категориях, указанных предыдущим порядком сортировки в структуре **SSortOrderSet.** 
      
  - TABLE_SORT_CATEG_MIN: таблица должна сортироваться по минимальному значению члена **ulPropTag** для строк данных в категориях, указанных предыдущим порядком сортировки в структуре **SSortOrderSet.** 
    
## <a name="remarks"></a>Примечания

Структура **SSortOrder** используется для описания выполнения стандартной или классизированной операции сортировки. **Структуры SSortOrder** обычно объединяются в структуру **SSortOrderSet** для описания нескольких ключей и направлений сортировки. **Структуры SSortOrderSet** используются в следующих функциях и методах интерфейса: 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Диапазон разрешенных столбцов в таблице, который можно использовать в качестве ключа сортировки, зависит от поставщика. Столбцы, которые являются частью текущего набора столбцов, всегда можно использовать в качестве ключей сортировки. Однако каждый поставщик определяет, можно ли определить ключи сортировки с помощью доступных столбцов, которых нет в текущем наборе столбцов. Доступный столбец — это столбец, который возвращается из [IMAPITable::QueryColumns](imapitable-querycolumns.md) при TBL_ALL_COLUMNS флага. 
  
Член **ulOrder** указывает как порядок направления, так и сведения о категоризации, например по беседе ([PidTagConversationTopic),](pidtagconversationtopic-canonical-property.md)то есть по цепочке беседы, которая является серию сообщений и ответов. Строки можно отсортировать по возрастанию или убыванию, при этом все записи NULL будут иметь последнее положение. 
  
Значение TABLE_SORT_COMBINE указывает, что столбец, указанный в **ulPropTag,** следует объединить с предыдущим столбцом категории для формирования составной категории. То есть вместо категоризации уникальных значений отдельных столбцов TABLE_SORT_COMBINE классифицируются по уникальным значениям сочетания столбцов. Например, можно определить одну категорию для группировки сообщений, полученных от определенного отправитель по определенной теме. Установка значения TABLE_SORT_COMBINE уменьшает количество отображаемого числа строк категорий. 
  
Сортировка по столбцам с несколькими значениями не всегда поддерживается всеми реализациями таблиц. При поддержке применив MV_FLAG макрос MVI_PROP к тегу свойства в элементе **ulPropTag,** чтобы определить ключ сортировки как столбец с несколькими значениями. Сортировка по столбцам с несколькими значениями основана на использовании отдельных значений. 
  
> [!IMPORTANT]
> Значения **членов ulOrder** TABLE_SORT_CATEG_MAX и TABLE_SORT_CATEG_MIN могут быть не определены в загружаемом файле заголовок, который у вас есть в настоящее время. В этом случае вы можете добавить его в код, используя следующие значения: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Дополнительные сведения о стандартной и категоризации сортировки см. в этой [теме.](sorting-and-categorization.md) 
  
## <a name="see-also"></a>См. также

- [SSortOrderSet](ssortorderset.md)
- [Структуры MAPI](mapi-structures.md)

