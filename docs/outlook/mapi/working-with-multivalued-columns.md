---
title: Работа с многоценными столбцами
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420187"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="a14f3-103">Работа с многоценными столбцами</span><span class="sxs-lookup"><span data-stu-id="a14f3-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="a14f3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a14f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a14f3-105">Столбец с несколькими значениями содержит данные многоценного свойства, которое является свойством, которое содержит массив значений базового типа вместо одного значения.</span><span class="sxs-lookup"><span data-stu-id="a14f3-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="a14f3-106">Поскольку ни одна из таблиц не содержит многоценных свойств в наборах столбцов по умолчанию, многоценные свойства включаются в таблицу только в том случае, если пользователь таблицы запросит ее.</span><span class="sxs-lookup"><span data-stu-id="a14f3-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="a14f3-107">Многоценные столбцы могут отображаться в таблицах:</span><span class="sxs-lookup"><span data-stu-id="a14f3-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="a14f3-108">В одной строке все значения свойств отображаются в экземпляре одного столбца.</span><span class="sxs-lookup"><span data-stu-id="a14f3-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="a14f3-109">Этот параметр используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a14f3-109">This is the default.</span></span>
    
    - <span data-ttu-id="a14f3-110">Или -</span><span class="sxs-lookup"><span data-stu-id="a14f3-110">Or -</span></span>
    
- <span data-ttu-id="a14f3-111">В ряде строк с одной строкой для каждого значения свойства.</span><span class="sxs-lookup"><span data-stu-id="a14f3-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="a14f3-112">Каждое уникальное значение отображается в столбце в отдельной строке, где имеется столько строк, сколько имеется значений в многоценном свойстве.</span><span class="sxs-lookup"><span data-stu-id="a14f3-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="a14f3-113">Каждая строка имеет уникальное значение свойства **PR_INSTANCE_KEY** ([PidTagInstanceKey),](pidtaginstancekey-canonical-property.md)но те же значения для других столбцов.</span><span class="sxs-lookup"><span data-stu-id="a14f3-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="a14f3-114">Если строка содержит несколько столбцов с несколькими значениями, например два столбца со значениями  _M_ и  _N_ соответственно, то в таблице появятся экземпляры  _M \* N_ этой строки.</span><span class="sxs-lookup"><span data-stu-id="a14f3-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="a14f3-115">Пользователь таблицы запрашивает нестандартный тип отображения, вызывая метод [IMAPITable::SetColumns](imapitable-setcolumns.md) с флагом MVI_FLAG, установленным в типе свойства многоценного столбца.</span><span class="sxs-lookup"><span data-stu-id="a14f3-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="a14f3-116">Флаг MVI_FLAG является константой, определенной в результате объединения флагов MV_FLAG и MV_INSTANCE с логической операцией **OR.**</span><span class="sxs-lookup"><span data-stu-id="a14f3-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="a14f3-117">Помимо использования в **SetColumns,** MVI_FLAG также можно передать в [IMAPITable::SortTable](imapitable-sorttable.md) в _параметре lpSortCriteria_ и [IMAPITable::Restrict](imapitable-restrict.md) в члене **ulPropTag** _параметра lpRestriction._</span><span class="sxs-lookup"><span data-stu-id="a14f3-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="a14f3-118">При MVI_FLAG **сортировка выполняется** аналогично **SetColumns,** добавляя по одной строке для каждого значения в столбце с несколькими значениями и сортировать по одному значению в экземплярах.</span><span class="sxs-lookup"><span data-stu-id="a14f3-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="a14f3-119">Для каждого значения добавляется одна строка.</span><span class="sxs-lookup"><span data-stu-id="a14f3-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="a14f3-120">**Однако** ограничение не расширяет столбец с несколькими столбцами на дополнительные вычисляемую строку.</span><span class="sxs-lookup"><span data-stu-id="a14f3-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="a14f3-121">Многооценный столбец с набором MVI_FLAG предписывает поставщику услуг использовать этот столбец при ограничении таблицы.</span><span class="sxs-lookup"><span data-stu-id="a14f3-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="a14f3-122">Если в ограничении есть значение свойства, он должен быть одним тегом свойства значения, идентичным тому, который будет возвращен [IMAPITable::QueryRows](imapitable-queryrows.md) для столбца.</span><span class="sxs-lookup"><span data-stu-id="a14f3-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="a14f3-123">Для поддержки типа отображения по умолчанию требуются только MAPI_E_TOO_COMPLEX таблицы.</span><span class="sxs-lookup"><span data-stu-id="a14f3-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="a14f3-124">Поддержка обоих типов отображения наиболее важна для поставщиков содержимого сообщений, реализующих таблицы содержимого папок.</span><span class="sxs-lookup"><span data-stu-id="a14f3-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a14f3-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a14f3-125">See also</span></span>



[<span data-ttu-id="a14f3-126">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="a14f3-126">MAPI Tables</span></span>](mapi-tables.md)

