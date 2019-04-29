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
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420187"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="b6543-103">Работа с многозначными столбцами</span><span class="sxs-lookup"><span data-stu-id="b6543-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="b6543-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6543-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6543-105">Многозначный столбец содержит данные многозначного свойства, который является свойством, имеющим массив значений базового типа, а не одно значение.</span><span class="sxs-lookup"><span data-stu-id="b6543-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="b6543-106">Так как ни одна таблица не содержит многозначные свойства в наборах столбцов по умолчанию, многозначные свойства включаются в таблицу только в том случае, если пользователь таблицы запрашивает ее.</span><span class="sxs-lookup"><span data-stu-id="b6543-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="b6543-107">Многозначные столбцы могут отображаться в таблицах:</span><span class="sxs-lookup"><span data-stu-id="b6543-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="b6543-108">В одной строке со всеми значениями свойств, отображаемыми в экземпляре с одним столбцом.</span><span class="sxs-lookup"><span data-stu-id="b6543-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="b6543-109">Это значение используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b6543-109">This is the default.</span></span>
    
    - <span data-ttu-id="b6543-110">Также</span><span class="sxs-lookup"><span data-stu-id="b6543-110">Or -</span></span>
    
- <span data-ttu-id="b6543-111">В серии строк с одной строкой для каждого значения свойства.</span><span class="sxs-lookup"><span data-stu-id="b6543-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="b6543-112">Каждое уникальное значение отображается в столбце в отдельной строке с количеством строк, которое содержит значения в многозначном свойстве.</span><span class="sxs-lookup"><span data-stu-id="b6543-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="b6543-113">Каждая строка имеет уникальное значение для свойства **пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), но одни и те же значения для других столбцов.</span><span class="sxs-lookup"><span data-stu-id="b6543-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="b6543-114">Если строка содержит несколько столбцов с несколькими значениями, например два столбца со значениями _M_ и _N_ соответственно, то в таблице отобразятся _\*N N_ экземпляров строки.</span><span class="sxs-lookup"><span data-stu-id="b6543-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="b6543-115">Пользователь таблицы запрашивает тип отображения, не используемый по умолчанию, вызывая метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) с ФЛАГом мви_флаг, установленным в типе свойства многозначный столбец.</span><span class="sxs-lookup"><span data-stu-id="b6543-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="b6543-116">Флаг МВИ_ФЛАГ — это константа, определенная в результате объединения флагов МВ_ФЛАГ и МВ_ИНСТАНЦЕ с логической операцией **or** .</span><span class="sxs-lookup"><span data-stu-id="b6543-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="b6543-117">В дополнение к использованию в **метода SetColumns**, мви_флаг также можно передать в [IMAPITable:: сорттабле](imapitable-sorttable.md) в параметрах _лпсорткритериа_ и [IMAPITable:: restrict](imapitable-restrict.md) в **улпроптаг** в _лпрестриктион_ параметр.</span><span class="sxs-lookup"><span data-stu-id="b6543-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="b6543-118">При передаче МВИ_ФЛАГ **сорттабле** выполняет аналогичный **метода SetColumns**, добавляя по одной строке для каждого значения в многозначном столбце и сортируя их по одиночным значениям в экземплярах.</span><span class="sxs-lookup"><span data-stu-id="b6543-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="b6543-119">Для каждого значения добавляется одна строка.</span><span class="sxs-lookup"><span data-stu-id="b6543-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="b6543-120">Однако **ограничения**не разворачивают многозначный столбец в дополнительные вычисляемые строки.</span><span class="sxs-lookup"><span data-stu-id="b6543-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="b6543-121">Многозначный столбец с набором МВИ_ФЛАГ предписывает поставщику услуг использовать этот столбец в ограничениях таблицы.</span><span class="sxs-lookup"><span data-stu-id="b6543-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="b6543-122">Если в ограничении есть значение свойства, оно должно быть тегом одиночного свойства Value, идентичным значению, которое будет возвращено методом [IMAPITable:: QueryRows](imapitable-queryrows.md) для столбца.</span><span class="sxs-lookup"><span data-stu-id="b6543-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="b6543-123">Средства реализации таблиц требуются только для поддержки типа отображения по умолчанию и могут возвращать значение МАПИ_Е_ТУ_КОМПЛЕКС, когда вызывающая сторона запрашивает другую альтернативу.</span><span class="sxs-lookup"><span data-stu-id="b6543-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="b6543-124">Возможность поддержки обоих типов отображения важна для поставщиков хранилищ сообщений, реализующих таблицы содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="b6543-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6543-125">См. также</span><span class="sxs-lookup"><span data-stu-id="b6543-125">See also</span></span>



[<span data-ttu-id="b6543-126">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="b6543-126">MAPI Tables</span></span>](mapi-tables.md)

