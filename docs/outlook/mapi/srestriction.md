---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439361"
---
# <a name="srestriction"></a><span data-ttu-id="6692d-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-103">SRestriction</span></span>

  
  
<span data-ttu-id="6692d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6692d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6692d-105">Описывает фильтр, ограничивающий представление таблицы определенными строками.</span><span class="sxs-lookup"><span data-stu-id="6692d-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6692d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6692d-106">Header file:</span></span>  <br/> |<span data-ttu-id="6692d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6692d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a><span data-ttu-id="6692d-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="6692d-108">Members</span></span>

 <span data-ttu-id="6692d-109">**rt**</span><span class="sxs-lookup"><span data-stu-id="6692d-109">**rt**</span></span>
  
> <span data-ttu-id="6692d-110">Тип ограничения.</span><span class="sxs-lookup"><span data-stu-id="6692d-110">The restriction type.</span></span> <span data-ttu-id="6692d-111">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="6692d-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="6692d-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="6692d-112">RES_AND</span></span> 
  
> <span data-ttu-id="6692d-113">Ограничение **AND,** которое применяется немного поохоть, **и** операция к ограничению.</span><span class="sxs-lookup"><span data-stu-id="6692d-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="6692d-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="6692d-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="6692d-115">Ограничение bitmask, которое применяет битмаску к значению свойства.</span><span class="sxs-lookup"><span data-stu-id="6692d-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="6692d-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="6692d-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="6692d-117">Ограничение комментариев, которое связывает комментарий с ограничением.</span><span class="sxs-lookup"><span data-stu-id="6692d-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="6692d-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="6692d-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="6692d-119">Ограничение сравнения свойств, которое сравнивает два значения свойств.</span><span class="sxs-lookup"><span data-stu-id="6692d-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="6692d-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="6692d-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="6692d-121">Ограничение контента, в котором выполняется поиск значения свойства для определенного контента.</span><span class="sxs-lookup"><span data-stu-id="6692d-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="6692d-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="6692d-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="6692d-123">Существует ограничение, которое определяет, поддерживается ли свойство.</span><span class="sxs-lookup"><span data-stu-id="6692d-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="6692d-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="6692d-124">RES_NOT</span></span> 
  
> <span data-ttu-id="6692d-125">Ограничение **NOT,** которое применяет логическую **операцию NOT** к ограничению.</span><span class="sxs-lookup"><span data-stu-id="6692d-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="6692d-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="6692d-126">RES_OR</span></span> 
  
> <span data-ttu-id="6692d-127">Ограничение **OR,** которое применяет к ограничению логическую **операцию OR.**</span><span class="sxs-lookup"><span data-stu-id="6692d-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="6692d-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="6692d-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="6692d-129">Ограничение свойства, которое определяет, соответствует ли значение свойства определенному значению.</span><span class="sxs-lookup"><span data-stu-id="6692d-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="6692d-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="6692d-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="6692d-131">Ограничение размера, которое определяет, является ли значение свойства определенным размером.</span><span class="sxs-lookup"><span data-stu-id="6692d-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="6692d-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="6692d-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="6692d-133">Ограничение под объекта, которое применяется к вложениям или получателям сообщения.</span><span class="sxs-lookup"><span data-stu-id="6692d-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="6692d-134">**res**</span><span class="sxs-lookup"><span data-stu-id="6692d-134">**res**</span></span>
  
> <span data-ttu-id="6692d-135">Объединение структур ограничений, описывающих применяемый фильтр.</span><span class="sxs-lookup"><span data-stu-id="6692d-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="6692d-136">Конкретная структура, включенная в **член res,** зависит от значения участника **rt.**</span><span class="sxs-lookup"><span data-stu-id="6692d-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="6692d-137">Сопоставление между типом ограничения и структурой перечислено в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6692d-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="6692d-138">**Тип ограничения**</span><span class="sxs-lookup"><span data-stu-id="6692d-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="6692d-139">**Структура ограничений**</span><span class="sxs-lookup"><span data-stu-id="6692d-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="6692d-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="6692d-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="6692d-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="6692d-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="6692d-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="6692d-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="6692d-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="6692d-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="6692d-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="6692d-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="6692d-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="6692d-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="6692d-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="6692d-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="6692d-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="6692d-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="6692d-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="6692d-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="6692d-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="6692d-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="6692d-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="6692d-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="6692d-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="6692d-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="6692d-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="6692d-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="6692d-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="6692d-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="6692d-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="6692d-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="6692d-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="6692d-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="6692d-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6692d-162">Примечания</span><span class="sxs-lookup"><span data-stu-id="6692d-162">Remarks</span></span>

<span data-ttu-id="6692d-163">Клиенты используют **структуру SRestriction** для ограничения количества и типа строк в представлении таблицы и поиска определенных сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="6692d-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="6692d-164">Чтобы наложить ограничение на таблицу, клиенты звонят [в IMAPITable:::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="6692d-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="6692d-165">Чтобы наложить ограничение на папку, клиенты звонят по методу [IMAPIContainer::SetSearchCriteria.](imapicontainer-setsearchcriteria.md)</span><span class="sxs-lookup"><span data-stu-id="6692d-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="6692d-166">Сведения об использовании ограничений со таблицами см. в таблице [О ограничениях.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="6692d-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6692d-167">См. также</span><span class="sxs-lookup"><span data-stu-id="6692d-167">See also</span></span>



[<span data-ttu-id="6692d-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="6692d-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="6692d-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="6692d-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="6692d-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="6692d-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="6692d-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="6692d-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="6692d-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="6692d-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="6692d-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="6692d-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="6692d-179">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="6692d-179">MAPI Structures</span></span>](mapi-structures.md)

