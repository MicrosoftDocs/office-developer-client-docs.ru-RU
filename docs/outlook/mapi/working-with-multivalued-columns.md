---
title: Работа с многозначными столбцами
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ee3307836e8b167efbc2cdc870e698257526ef97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812620"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="566ed-103">Работа с многозначными столбцами</span><span class="sxs-lookup"><span data-stu-id="566ed-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="566ed-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="566ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="566ed-105">Многозначных столбцов с данными многозначные свойства, которое является свойством, которое содержит массив значений базового типа, а не одним значением.</span><span class="sxs-lookup"><span data-stu-id="566ed-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="566ed-106">Так как ни одна из таблиц многозначных свойств в их наборы столбцов по умолчанию, в таблицу включены многозначные свойства только в том случае, если пользователь таблицы запрашивает его.</span><span class="sxs-lookup"><span data-stu-id="566ed-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="566ed-107">Многозначные столбцы может отображаться в таблицах:</span><span class="sxs-lookup"><span data-stu-id="566ed-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="566ed-108">В одной строке, со всеми значения свойств, изображения которых появляются в экземпляр одного столбца.</span><span class="sxs-lookup"><span data-stu-id="566ed-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="566ed-109">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="566ed-109">This is the default.</span></span>
    
    - <span data-ttu-id="566ed-110">Или -</span><span class="sxs-lookup"><span data-stu-id="566ed-110">Or -</span></span>
    
- <span data-ttu-id="566ed-111">В набор строк, по одной строке для каждого из значений свойств.</span><span class="sxs-lookup"><span data-stu-id="566ed-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="566ed-112">Каждое уникальное значение отображается в столбце в отдельной строке с него, как много строк имеется значений в многозначного свойства.</span><span class="sxs-lookup"><span data-stu-id="566ed-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="566ed-113">Каждая строка имеет уникальное значение для свойства **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), но те же значения для других столбцов.</span><span class="sxs-lookup"><span data-stu-id="566ed-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="566ed-114">Если строка содержит более одного столбца с несколькими значениями, например, два столбца с _M_ и _N_ значения соответственно, затем _M\*N_ экземпляров строки отображаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="566ed-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="566ed-115">В таблице пользователь запрашивает отличные тип отображения путем вызова метода [IMAPITable::SetColumns](imapitable-setcolumns.md) с флагом MVI_FLAG в типе свойство многозначных столбцов.</span><span class="sxs-lookup"><span data-stu-id="566ed-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="566ed-116">Флаг MVI_FLAG — константа, определенного как результат объединения флаги MV_FLAG и MV_INSTANCE с операцией логического **или** .</span><span class="sxs-lookup"><span data-stu-id="566ed-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="566ed-117">В дополнение к используется в **метода SetColumns**, MVI_FLAG можно также передавать [IMAPITable::SortTable](imapitable-sorttable.md) в параметре _lpSortCriteria_ и [IMAPITable::Restrict](imapitable-restrict.md) в **ulPropTag** членом _lpRestriction_ параметр.</span><span class="sxs-lookup"><span data-stu-id="566ed-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="566ed-118">При передаче MVI_FLAG **SortTable** выполняет аналогично **метода SetColumns**, добавление одной строке для каждого значения в многозначных столбцов и сортировка на отдельные значения в экземплярах.</span><span class="sxs-lookup"><span data-stu-id="566ed-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="566ed-119">Для каждого значения добавляется одна строка.</span><span class="sxs-lookup"><span data-stu-id="566ed-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="566ed-120">**Ограничить**тем не менее, не развертывая многозначных столбцов в дополнительные вычисляемые строки.</span><span class="sxs-lookup"><span data-stu-id="566ed-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="566ed-121">Многозначных столбцов с набором MVI_FLAG указывает, что поставщик услуг использует этот столбец в ограничение в таблице.</span><span class="sxs-lookup"><span data-stu-id="566ed-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="566ed-122">Если значение свойства в ограничении, он должен быть тег одним значением свойства идентичен то, которое будет возвращено с [IMAPITable::QueryRows](imapitable-queryrows.md) для столбца.</span><span class="sxs-lookup"><span data-stu-id="566ed-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="566ed-123">В таблице специалистов по внедрению только необходимых для поддержки типа по умолчанию для отображения и может возвращать значение MAPI_E_TOO_COMPLEX, когда вызывающий объект запрашивает альтернативные варианты.</span><span class="sxs-lookup"><span data-stu-id="566ed-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="566ed-124">Возможность поддержки обоих типов отображения наиболее важные для реализации таблиц содержимое папки поставщиков хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="566ed-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="566ed-125">См. также</span><span class="sxs-lookup"><span data-stu-id="566ed-125">See also</span></span>



[<span data-ttu-id="566ed-126">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="566ed-126">MAPI Tables</span></span>](mapi-tables.md)

