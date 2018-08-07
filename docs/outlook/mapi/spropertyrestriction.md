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
ms.openlocfilehash: f59b0041f271010e56dda2f73d2248f133bc1325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812355"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="2cda9-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="2cda9-103">SPropertyRestriction</span></span>

<span data-ttu-id="2cda9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2cda9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2cda9-105">Описывает свойства ограничение, которое используется для сопоставления константу со значением свойства.</span><span class="sxs-lookup"><span data-stu-id="2cda9-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2cda9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2cda9-106">Header file:</span></span>  <br/> |<span data-ttu-id="2cda9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2cda9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="2cda9-108">Members</span><span class="sxs-lookup"><span data-stu-id="2cda9-108">Members</span></span>

<span data-ttu-id="2cda9-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="2cda9-109">**relop**</span></span>
  
> <span data-ttu-id="2cda9-110">Оператор, который будет использоваться в поиск.</span><span class="sxs-lookup"><span data-stu-id="2cda9-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="2cda9-111">Ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="2cda9-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="2cda9-112">RELOP_GE: Сравнение выполняется на основе на больше или равно первого значения.</span><span class="sxs-lookup"><span data-stu-id="2cda9-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="2cda9-113">RELOP_GT: Сравнение выполняется на основе на более высокой версии первое значение.</span><span class="sxs-lookup"><span data-stu-id="2cda9-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="2cda9-114">RELOP_LE: Сравнение выполняется на основе на меньше или равно первого значения.</span><span class="sxs-lookup"><span data-stu-id="2cda9-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="2cda9-115">RELOP_LT: Сравнение выполняется на основе на меньшим первое значение.</span><span class="sxs-lookup"><span data-stu-id="2cda9-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="2cda9-116">RELOP_NE: Сравнение выполняется на основе на разные значения.</span><span class="sxs-lookup"><span data-stu-id="2cda9-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="2cda9-117">RELOP_RE: Сравнение выполняется на основе как значения (регулярное выражение).</span><span class="sxs-lookup"><span data-stu-id="2cda9-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="2cda9-118">RELOP_EQ: Сравнение выполняется на основе на равные значения.</span><span class="sxs-lookup"><span data-stu-id="2cda9-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="2cda9-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="2cda9-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="2cda9-120">Свойство tag идентификации свойства для сравнения.</span><span class="sxs-lookup"><span data-stu-id="2cda9-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="2cda9-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="2cda9-121">**lpProp**</span></span>
  
> <span data-ttu-id="2cda9-122">Указатель на структуру [SPropValue](spropvalue.md) , содержащий константа, которая будет использоваться для сравнения.</span><span class="sxs-lookup"><span data-stu-id="2cda9-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2cda9-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="2cda9-123">Remarks</span></span>

<span data-ttu-id="2cda9-124">Существует два свойства теги в структуре **SPropertyRestriction** .</span><span class="sxs-lookup"><span data-stu-id="2cda9-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="2cda9-125">В элемент **ulPropTag** , а другое — в член **ulPropTag** структуры **SPropValue** , на который указывает **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="2cda9-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="2cda9-126">MAPI требуется идентификатор поля и поле типа свойства.</span><span class="sxs-lookup"><span data-stu-id="2cda9-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="2cda9-127">**UlPropTag** в **SPropertyRestriction** является свойством для сопоставления и указывает указатель **lpProp** **SPropertyRestriction** **ulPropTag**по типу **SPropValue** как значение члены Объединение **lpProp** интерпретируются.</span><span class="sxs-lookup"><span data-stu-id="2cda9-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="2cda9-128">Типы два свойства должны совпадать, в противном случае MAPI_E_TOO_COMPLEX возвращается значение при ограничении удалось вызвать [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="2cda9-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="2cda9-129">Порядок сравнения _(значение свойства) (оператор сравнения) (константа)_.</span><span class="sxs-lookup"><span data-stu-id="2cda9-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="2cda9-130">Когда ограничение свойства передается **IMAPITable::Restrict** или **IMAPITable::FindRow** и свойства конечного объекта не существует, результаты ограничение не определено.</span><span class="sxs-lookup"><span data-stu-id="2cda9-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="2cda9-131">Путем создания **и** ограничения, объединяющий ограничение свойства ограничению **EXIST** Звонящий может гарантировать точных результатов.</span><span class="sxs-lookup"><span data-stu-id="2cda9-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="2cda9-132">Используйте структуру [SExistRestriction](sexistrestriction.md) , чтобы определить ограничение **EXIST** и структуру [SAndRestriction](sandrestriction.md) для определения **и** ограничение.</span><span class="sxs-lookup"><span data-stu-id="2cda9-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="2cda9-133">Многозначное свойство теги можно использовать в ограничений свойств, если их поддерживает поставщик услуг, реализация в таблице.</span><span class="sxs-lookup"><span data-stu-id="2cda9-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="2cda9-134">Если поддерживается, многозначное свойство теги можно использовать везде, где можно использовать теги одним значением свойства.</span><span class="sxs-lookup"><span data-stu-id="2cda9-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="2cda9-135">Многозначное свойство теги можно использовать в следующих методов:</span><span class="sxs-lookup"><span data-stu-id="2cda9-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="2cda9-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="2cda9-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="2cda9-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="2cda9-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="2cda9-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="2cda9-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="2cda9-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="2cda9-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="2cda9-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="2cda9-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="2cda9-141">Важные случай, когда теги два свойства могут не соответствовать — Если ограничение для многозначного свойства.</span><span class="sxs-lookup"><span data-stu-id="2cda9-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="2cda9-142">В данном случае следующие вопросы должны иметь значение true.</span><span class="sxs-lookup"><span data-stu-id="2cda9-142">In this case the following must be true.</span></span> <span data-ttu-id="2cda9-143">> Если тип свойства **ulPropTag** из **SPropertyRestriction** содержит многозначного свойства типа битовый флаг MV_FLAG (0x1000), тип свойства **ulPropTag** из **SPropValue** должна соответствовать бывшая минус MV_ ФЛАГ битовый флаг, то есть его обратное.</span><span class="sxs-lookup"><span data-stu-id="2cda9-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="2cda9-144">> Например, чтобы ограничить использование настраиваемой строки многозначного свойства, например категории с тега свойства для свойства 0x8012101f, то есть, PROP_TAG (MV_FLAG | PT_UNICODE 0x8012)), соответствующий **SPropertyRestriction** будет отображаться как следующим образом.</span><span class="sxs-lookup"><span data-stu-id="2cda9-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="2cda9-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Обратите внимание на то, что если тип свойства **ulPropTag** из **SPropValue** содержит битовый флаг MV_FLAG, скорее всего, возвращается MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="2cda9-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Note that if the property type of the **ulPropTag** of **SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="2cda9-146">Дополнительные сведения о структуре **SPropertyRestriction** [О ограничения](about-restrictions.md)см.</span><span class="sxs-lookup"><span data-stu-id="2cda9-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2cda9-147">См. также</span><span class="sxs-lookup"><span data-stu-id="2cda9-147">See also</span></span>

- [<span data-ttu-id="2cda9-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="2cda9-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="2cda9-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="2cda9-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="2cda9-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2cda9-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="2cda9-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="2cda9-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="2cda9-152">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="2cda9-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="2cda9-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="2cda9-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="2cda9-154">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="2cda9-154">MAPI Structures</span></span>](mapi-structures.md)

