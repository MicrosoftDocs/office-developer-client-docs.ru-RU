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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406089"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="7eaff-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="7eaff-103">SPropertyRestriction</span></span>

<span data-ttu-id="7eaff-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7eaff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7eaff-105">Описывает ограничение свойств, которое используется для совпадения константы со значением свойства.</span><span class="sxs-lookup"><span data-stu-id="7eaff-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7eaff-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7eaff-106">Header file:</span></span>  <br/> |<span data-ttu-id="7eaff-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7eaff-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="7eaff-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="7eaff-108">Members</span></span>

<span data-ttu-id="7eaff-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="7eaff-109">**relop**</span></span>
  
> <span data-ttu-id="7eaff-110">Реляционный оператор, который будет использоваться в поиске.</span><span class="sxs-lookup"><span data-stu-id="7eaff-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="7eaff-111">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="7eaff-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="7eaff-112">RELOP_GE. Сравнение основано на большем или равном первом значении.</span><span class="sxs-lookup"><span data-stu-id="7eaff-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="7eaff-113">RELOP_GT. Сравнение выполнено на основе более первого значения.</span><span class="sxs-lookup"><span data-stu-id="7eaff-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="7eaff-114">RELOP_LE. Сравнение основано на меньшем или равном первом значении.</span><span class="sxs-lookup"><span data-stu-id="7eaff-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="7eaff-115">RELOP_LT. Сравнение выполнено на основе меньшего первого значения.</span><span class="sxs-lookup"><span data-stu-id="7eaff-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="7eaff-116">RELOP_NE. Сравнение основано на неравных значениях.</span><span class="sxs-lookup"><span data-stu-id="7eaff-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="7eaff-117">RELOP_RE. Сравнение основано на значениях LIKE (регулярное выражение).</span><span class="sxs-lookup"><span data-stu-id="7eaff-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="7eaff-118">RELOP_EQ. Сравнение основано на равных значениях.</span><span class="sxs-lookup"><span data-stu-id="7eaff-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="7eaff-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="7eaff-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="7eaff-120">Тег свойства, определяющий свойство, с чем следует сравнивать.</span><span class="sxs-lookup"><span data-stu-id="7eaff-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="7eaff-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="7eaff-121">**lpProp**</span></span>
  
> <span data-ttu-id="7eaff-122">Указатель на [структуру SPropValue,](spropvalue.md) которая содержит постоянное значение, которое будет использоваться в сравнении.</span><span class="sxs-lookup"><span data-stu-id="7eaff-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7eaff-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="7eaff-123">Remarks</span></span>

<span data-ttu-id="7eaff-124">В структуре **SPropertyRestriction** есть два тега свойств.</span><span class="sxs-lookup"><span data-stu-id="7eaff-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="7eaff-125">Один находится в **члене ulPropTag,** а другой — в **члене ulPropTag** структуры **SPropValue,** на который указывает **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="7eaff-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="7eaff-126">MAPI требует как поля идентификатора свойства, так и поля типа свойства.</span><span class="sxs-lookup"><span data-stu-id="7eaff-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="7eaff-127">**ulPropTag** в **SPropertyRestriction** — это свойство, необходимое для совпадения, а указатель **lpProp** **SPropertyRestriction** к типу **SPropTag SPropValue** указывает, как интерпретируются значения членов союза **lpProp.** </span><span class="sxs-lookup"><span data-stu-id="7eaff-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="7eaff-128">Два типа свойств должны совпадать, иначе значение ошибки MAPI_E_TOO_COMPLEX возвращается, когда ограничение используется в вызове [iMAPITable:::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="7eaff-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="7eaff-129">Порядок сравнения _(значение свойства) (реляционный оператор) (постоянное значение)._</span><span class="sxs-lookup"><span data-stu-id="7eaff-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="7eaff-130">Когда ограничение свойства передается **в IMAPITable:::Restrict** или **IMAPITable::FindRow** и целевое свойство не существует, результаты ограничения неопределяются.</span><span class="sxs-lookup"><span data-stu-id="7eaff-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="7eaff-131">Создав **ограничение AND,** которое присоединяется к ограничению свойств с ограничением **EXIST,** вызываемой может быть гарантирована точность результатов.</span><span class="sxs-lookup"><span data-stu-id="7eaff-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="7eaff-132">Чтобы определить ограничение EXIST и [структуру SAndRestriction,](sandrestriction.md) используйте структуру  [SExistRestriction.](sexistrestriction.md) </span><span class="sxs-lookup"><span data-stu-id="7eaff-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="7eaff-133">Теги свойств с несколькими значениями можно использовать в ограничениях свойств, если поставщик услуг, реализующий таблицу, поддерживает их.</span><span class="sxs-lookup"><span data-stu-id="7eaff-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="7eaff-134">При поддержке теги свойств с несколькими значениями можно использовать в любом месте, где можно использовать теги свойств с одним значением.</span><span class="sxs-lookup"><span data-stu-id="7eaff-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="7eaff-135">Теги свойств с несколькими значениями можно использовать в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="7eaff-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="7eaff-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="7eaff-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="7eaff-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="7eaff-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="7eaff-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="7eaff-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="7eaff-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="7eaff-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="7eaff-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="7eaff-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="7eaff-141">Примечателен случай, когда два тега свойств не совпадают, если они ограничиваются для свойства с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="7eaff-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="7eaff-142">В этом случае должно быть верно следующее.</span><span class="sxs-lookup"><span data-stu-id="7eaff-142">In this case the following must be true.</span></span> <span data-ttu-id="7eaff-143">> Если тип свойства **ulPropTag** **SPropertyRestriction** содержит многозначный флаг типа свойств MV_FLAG (0x1000), тип свойства **ulPropTag** **SPropValue** должен совпадать с прежним минусом флага MV_FLAG бита, то есть обратным.</span><span class="sxs-lookup"><span data-stu-id="7eaff-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="7eaff-144">> Например, чтобы ограничить использование нескольких значений настраиваемого свойства строки, например категории с тегом свойства для свойства 0x8012101f, то есть PROP_TAG (MV_FLAG|PT_UNICODE, 0x8012)), соответствующий **SPropertyRestriction** будет отображаться следующим образом.</span><span class="sxs-lookup"><span data-stu-id="7eaff-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="7eaff-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> обратите внимание, что если тип свойства **ulPropTag** **SPropValue** содержит флаг MV_FLAG бита, вероятно, возвращается MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="7eaff-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Note that if the property type of the **ulPropTag** of **SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="7eaff-146">Дополнительные сведения о структуре **SPropertyRestriction** см. в дополнительных [сведениях об ограничениях.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="7eaff-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7eaff-147">См. также</span><span class="sxs-lookup"><span data-stu-id="7eaff-147">See also</span></span>

- [<span data-ttu-id="7eaff-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="7eaff-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="7eaff-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="7eaff-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="7eaff-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7eaff-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="7eaff-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="7eaff-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="7eaff-152">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="7eaff-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="7eaff-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="7eaff-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="7eaff-154">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7eaff-154">MAPI Structures</span></span>](mapi-structures.md)

