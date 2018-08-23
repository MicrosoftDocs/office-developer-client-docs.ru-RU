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
ms.openlocfilehash: 5f8a76cb317ac9bf1b6a4dc4a92b6d6f0098e1d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577403"
---
# <a name="srestriction"></a><span data-ttu-id="7494a-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-103">SRestriction</span></span>

  
  
<span data-ttu-id="7494a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7494a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7494a-105">Описание фильтр ограничения представления таблицы в конкретной строки.</span><span class="sxs-lookup"><span data-stu-id="7494a-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7494a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7494a-106">Header file:</span></span>  <br/> |<span data-ttu-id="7494a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7494a-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="7494a-108">Members</span><span class="sxs-lookup"><span data-stu-id="7494a-108">Members</span></span>

 <span data-ttu-id="7494a-109">**время выполнения**</span><span class="sxs-lookup"><span data-stu-id="7494a-109">**rt**</span></span>
  
> <span data-ttu-id="7494a-110">Тип ограничения.</span><span class="sxs-lookup"><span data-stu-id="7494a-110">The restriction type.</span></span> <span data-ttu-id="7494a-111">Ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="7494a-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="7494a-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="7494a-112">RES_AND</span></span> 
  
> <span data-ttu-id="7494a-113">Ограничения **и** применяет побитовую операцию **и** ограничение.</span><span class="sxs-lookup"><span data-stu-id="7494a-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="7494a-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="7494a-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="7494a-115">Ограничение Битовая маска применяется Битовая маска значение свойства.</span><span class="sxs-lookup"><span data-stu-id="7494a-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="7494a-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="7494a-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="7494a-117">Ограничение комментарий связывает комментария с ограничением.</span><span class="sxs-lookup"><span data-stu-id="7494a-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="7494a-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="7494a-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="7494a-119">Ограничение свойства сравнения, который сравнивает два значения свойств.</span><span class="sxs-lookup"><span data-stu-id="7494a-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="7494a-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="7494a-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="7494a-121">Контента ограничение, которая осуществляет поиск значения для определенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="7494a-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="7494a-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="7494a-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="7494a-123">Ограничение exist определяет, поддерживается ли свойство.</span><span class="sxs-lookup"><span data-stu-id="7494a-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="7494a-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="7494a-124">RES_NOT</span></span> 
  
> <span data-ttu-id="7494a-125">**Не** ограничение, который применим логическая операция **не** ограничение.</span><span class="sxs-lookup"><span data-stu-id="7494a-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="7494a-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="7494a-126">RES_OR</span></span> 
  
> <span data-ttu-id="7494a-127">**Или** ограничение, который применим к ограничению логической операции **или** .</span><span class="sxs-lookup"><span data-stu-id="7494a-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="7494a-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="7494a-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="7494a-129">Ограничение свойства определяет, соответствует ли значение свойства определенного значения.</span><span class="sxs-lookup"><span data-stu-id="7494a-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="7494a-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="7494a-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="7494a-131">Ограничения размера, который определяет, является ли значение свойства определенного размера.</span><span class="sxs-lookup"><span data-stu-id="7494a-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="7494a-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="7494a-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="7494a-133">Ограничение дочерний объект применяет ограничение для вложения или получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="7494a-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="7494a-134">**RES**</span><span class="sxs-lookup"><span data-stu-id="7494a-134">**res**</span></span>
  
> <span data-ttu-id="7494a-135">Объединение структур ограничений, описывающих фильтр нужно применить.</span><span class="sxs-lookup"><span data-stu-id="7494a-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="7494a-136">Определенную структуру, включенные в элемент **res** зависит от значение элемента **rt** .</span><span class="sxs-lookup"><span data-stu-id="7494a-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="7494a-137">В следующей таблице указано сопоставление между тип ограничения и структуры.</span><span class="sxs-lookup"><span data-stu-id="7494a-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="7494a-138">**Тип ограничения**</span><span class="sxs-lookup"><span data-stu-id="7494a-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="7494a-139">**Ограничение структуры**</span><span class="sxs-lookup"><span data-stu-id="7494a-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="7494a-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="7494a-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="7494a-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="7494a-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="7494a-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="7494a-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="7494a-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="7494a-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="7494a-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="7494a-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="7494a-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="7494a-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="7494a-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="7494a-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="7494a-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="7494a-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="7494a-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="7494a-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="7494a-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="7494a-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="7494a-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="7494a-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="7494a-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="7494a-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="7494a-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="7494a-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="7494a-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="7494a-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="7494a-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="7494a-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="7494a-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="7494a-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="7494a-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7494a-162">Замечания</span><span class="sxs-lookup"><span data-stu-id="7494a-162">Remarks</span></span>

<span data-ttu-id="7494a-163">Клиенты используют структуру **SRestriction** для ограничения числа и типа строк в режиме таблицы и для поиска конкретных сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="7494a-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="7494a-164">Чтобы наложить ограничение на таблицу клиентов вызовите [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="7494a-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="7494a-165">Чтобы наложить ограничение на папку, клиенты вызовите метод [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) папки.</span><span class="sxs-lookup"><span data-stu-id="7494a-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="7494a-166">Для получения сведений об использовании ограничения с таблицами, обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="7494a-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7494a-167">См. также</span><span class="sxs-lookup"><span data-stu-id="7494a-167">See also</span></span>



[<span data-ttu-id="7494a-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="7494a-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="7494a-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="7494a-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="7494a-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="7494a-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="7494a-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="7494a-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="7494a-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="7494a-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="7494a-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="7494a-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="7494a-179">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7494a-179">MAPI Structures</span></span>](mapi-structures.md)

