---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357857"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="b3674-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="b3674-103">SPropertyRestriction</span></span>

<span data-ttu-id="b3674-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3674-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3674-105">Описывает ограничение свойства, которое используется для сравнения константы со значением свойства.</span><span class="sxs-lookup"><span data-stu-id="b3674-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3674-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b3674-106">Header file:</span></span>  <br/> |<span data-ttu-id="b3674-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b3674-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="b3674-108">Members</span><span class="sxs-lookup"><span data-stu-id="b3674-108">Members</span></span>

<span data-ttu-id="b3674-109">**релоп**</span><span class="sxs-lookup"><span data-stu-id="b3674-109">**relop**</span></span>
  
> <span data-ttu-id="b3674-110">Оператор отношения, который будет использоваться при поиске.</span><span class="sxs-lookup"><span data-stu-id="b3674-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="b3674-111">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b3674-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="b3674-112">РЕЛОП_ЖЕ: сравнение выполняется на основе более высокого или равного первого значения.</span><span class="sxs-lookup"><span data-stu-id="b3674-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="b3674-113">РЕЛОП_ГТ: сравнение выполняется на основе большего первого значения.</span><span class="sxs-lookup"><span data-stu-id="b3674-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="b3674-114">РЕЛОП_ЛЕ: сравнение выполняется на основе меньшего или равного первого значения.</span><span class="sxs-lookup"><span data-stu-id="b3674-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="b3674-115">РЕЛОП_ЛТ: сравнение выполняется на основе меньшего первого значения.</span><span class="sxs-lookup"><span data-stu-id="b3674-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="b3674-116">РЕЛОП_НЕ: сравнение выполняется на основе неодинаковых значений.</span><span class="sxs-lookup"><span data-stu-id="b3674-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="b3674-117">РЕЛОП_РЕ: сравнение выполняется на основе значений LIKE (регулярное выражение).</span><span class="sxs-lookup"><span data-stu-id="b3674-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="b3674-118">РЕЛОП_ЕК: сравнение выполняется на основе равных значений.</span><span class="sxs-lookup"><span data-stu-id="b3674-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="b3674-119">**Улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="b3674-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="b3674-120">Тег свойства, определяющий свойство, которое требуется сравнить.</span><span class="sxs-lookup"><span data-stu-id="b3674-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="b3674-121">**Лппроп**</span><span class="sxs-lookup"><span data-stu-id="b3674-121">**lpProp**</span></span>
  
> <span data-ttu-id="b3674-122">Указатель на структуру [спропвалуе](spropvalue.md) , которая содержит значение константы, которое будет использоваться при сравнении.</span><span class="sxs-lookup"><span data-stu-id="b3674-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b3674-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3674-123">Remarks</span></span>

<span data-ttu-id="b3674-124">Структура **Спропертирестриктион** содержит два тега свойств.</span><span class="sxs-lookup"><span data-stu-id="b3674-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="b3674-125">Один находится в элементе **улпроптаг** , а другой — в элементе **улпроптаг** структуры **Спропвалуе** , на которую указывает **лппроп**.</span><span class="sxs-lookup"><span data-stu-id="b3674-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="b3674-126">Для MAPI требуются поля "идентификатор свойства" и "тип свойства".</span><span class="sxs-lookup"><span data-stu-id="b3674-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="b3674-127">**Улпроптаг** в **спропертирестриктион** — это свойство, для которого выполняется сравнение, а указатель **Лппроп** **спропертирестриктион** к типу **улпроптаг** **спропвалуе** указывает, как значение Members элемента **лппроп** Union интерпретируется.</span><span class="sxs-lookup"><span data-stu-id="b3674-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="b3674-128">Два типа свойств должны соблюдаться, иначе значение ошибки МАПИ_Е_ТУ_КОМПЛЕКС возвращается, если ограничение используется при вызове [IMAPITable:: restrict](imapitable-restrict.md) или [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="b3674-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="b3674-129">Порядок сравнения: _(значение свойства) (оператор отношения) (постоянное значение)_.</span><span class="sxs-lookup"><span data-stu-id="b3674-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="b3674-130">Если ограничение свойства передается в **IMAPITable::** restricts или **IMAPITable:: FindRow** , а свойство Target не существует, результаты ограничения не определены.</span><span class="sxs-lookup"><span data-stu-id="b3674-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="b3674-131">Создавая ограничение, \*\*\*\* которое присоединяется к ограничению свойств с ограничением **Exists** , вызывающий абонент может гарантировать точный результат.</span><span class="sxs-lookup"><span data-stu-id="b3674-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="b3674-132">Используйте структуру [сексистрестриктион](sexistrestriction.md) , чтобы определить ограничение **exist** и структуру [сандрестриктион](sandrestriction.md) для определения ограничения. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b3674-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="b3674-133">Теги свойств с несколькими значениями можно использовать в ограничениях свойств, если поставщик услуг, реализующий эту таблицу, поддерживает их.</span><span class="sxs-lookup"><span data-stu-id="b3674-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="b3674-134">Если поддерживается, можно использовать теги свойств с несколькими значениями везде.</span><span class="sxs-lookup"><span data-stu-id="b3674-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="b3674-135">Теги свойств с несколькими значениями можно использовать в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="b3674-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="b3674-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="b3674-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="b3674-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="b3674-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="b3674-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="b3674-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="b3674-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="b3674-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="b3674-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="b3674-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="b3674-141">В важном случае, если два тега свойства не совпадают, то в случае ограничения для свойства с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="b3674-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="b3674-142">В этом случае должны быть соблюдены следующие условия.</span><span class="sxs-lookup"><span data-stu-id="b3674-142">In this case the following must be true.</span></span> <span data-ttu-id="b3674-143">_Гт_ если тип свойства **улпроптаг** объекта **спропертирестриктион** содержит многозначный флаг типа многозначного свойства мв_флаг (0x1000), то тип свойства **улпроптаг** **СПРОПВАЛУЕ** должен отличаться от предыдущего минуса мв_ Битовый флаг ФЛАГа, то есть обратное.</span><span class="sxs-lookup"><span data-stu-id="b3674-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="b3674-144">_Гт_ например, чтобы ограничить использование многозначного настраиваемого строкового свойства, например категории с тегом свойства для свойства 0x8012101f, то есть ПРОП_ТАГ (МВ_ФЛАГ | ПТ_УНИКОДЕ, 0x8012)), соответствующие **спропертирестриктион** будут выглядеть как состоит.</span><span class="sxs-lookup"><span data-stu-id="b3674-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="b3674-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property\`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid\`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`_Гт_ Обратите внимание, что если тип свойства *\*улпроптаг** объекта *\*СПРОПВАЛУЕ** содержит флаг мв_флаг bit, скорее всего возвращается мапи_е_ту_комплекс.</span><span class="sxs-lookup"><span data-stu-id="b3674-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property\`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid\`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";\`> Note that if the property type of the *\*ulPropTag** of *\*SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="b3674-146">Более подробную информацию о структуре **спропертирестриктион** можно узнать в статье [ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="b3674-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3674-147">См. также</span><span class="sxs-lookup"><span data-stu-id="b3674-147">See also</span></span>

- [<span data-ttu-id="b3674-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="b3674-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="b3674-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="b3674-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="b3674-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b3674-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="b3674-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="b3674-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="b3674-152">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="b3674-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="b3674-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="b3674-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="b3674-154">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="b3674-154">MAPI Structures</span></span>](mapi-structures.md)

