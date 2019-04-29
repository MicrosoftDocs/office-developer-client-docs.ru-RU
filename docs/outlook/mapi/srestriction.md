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
# <a name="srestriction"></a><span data-ttu-id="bd5c3-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-103">SRestriction</span></span>

  
  
<span data-ttu-id="bd5c3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd5c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd5c3-105">Описывает фильтр для ограничения представления таблицы определенными строками.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd5c3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bd5c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="bd5c3-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="bd5c3-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="bd5c3-108">Members</span><span class="sxs-lookup"><span data-stu-id="bd5c3-108">Members</span></span>

 <span data-ttu-id="bd5c3-109">**RT**</span><span class="sxs-lookup"><span data-stu-id="bd5c3-109">**rt**</span></span>
  
> <span data-ttu-id="bd5c3-110">Тип ограничения.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-110">The restriction type.</span></span> <span data-ttu-id="bd5c3-111">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bd5c3-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="bd5c3-112">РЕС_АНД</span><span class="sxs-lookup"><span data-stu-id="bd5c3-112">RES_AND</span></span> 
  
> <span data-ttu-id="bd5c3-113">Ограничение \*\*\*\* , которое применяет к ограничению операцию побитового **и** .</span><span class="sxs-lookup"><span data-stu-id="bd5c3-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="bd5c3-114">РЕС_БИТМАСК</span><span class="sxs-lookup"><span data-stu-id="bd5c3-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="bd5c3-115">Ограничение битовой маски, которое применяет битовую маску к значению свойства.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="bd5c3-116">РЕС_КОММЕНТ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="bd5c3-117">Ограничение комментария, которое связывает комментарий с ограничением.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="bd5c3-118">РЕС_КОМПАРЕПРОПС</span><span class="sxs-lookup"><span data-stu-id="bd5c3-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="bd5c3-119">Ограничение на сравнение свойств, которое сравнивает два значения свойств.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="bd5c3-120">РЕС_КОНТЕНТ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="bd5c3-121">Ограничение содержимого, которое выполняет поиск определенного содержимого в значении свойства.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="bd5c3-122">РЕС_ЕКСИСТ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="bd5c3-123">Ограничение exist, определяющее, поддерживается ли свойство.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="bd5c3-124">РЕС_НОТ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-124">RES_NOT</span></span> 
  
> <span data-ttu-id="bd5c3-125">Ограничение **Not** , которое применяет логическую операцию **Not** к ограничению.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="bd5c3-126">РЕС_ОР</span><span class="sxs-lookup"><span data-stu-id="bd5c3-126">RES_OR</span></span> 
  
> <span data-ttu-id="bd5c3-127">Ограничение \*\*\*\* , которое применяет логическую операцию **или** к ограничению.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="bd5c3-128">РЕС_ПРОПЕРТИ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="bd5c3-129">Ограничение свойства, которое определяет, совпадает ли значение свойства с определенным значением.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="bd5c3-130">РЕС_СИЗЕ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="bd5c3-131">Ограничение размера, определяющее, является ли значение свойства определенным размером.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="bd5c3-132">РЕС_СУБРЕСТРИКТИОН</span><span class="sxs-lookup"><span data-stu-id="bd5c3-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="bd5c3-133">Ограничение вложенного объекта, которое применяет ограничение к вложениям или получателям сообщения.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="bd5c3-134">**распределение**</span><span class="sxs-lookup"><span data-stu-id="bd5c3-134">**res**</span></span>
  
> <span data-ttu-id="bd5c3-135">Объединение структур ограничений, описывающих применяемый фильтр.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="bd5c3-136">Конкретная структура, включенная в состав элемента **RES** , зависит от значения элемента **RT** .</span><span class="sxs-lookup"><span data-stu-id="bd5c3-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="bd5c3-137">Сопоставление типа и структуры ограничения представлено в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="bd5c3-138">**Тип ограничения**</span><span class="sxs-lookup"><span data-stu-id="bd5c3-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="bd5c3-139">**Структура ограничения**</span><span class="sxs-lookup"><span data-stu-id="bd5c3-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="bd5c3-140">РЕС_АНД</span><span class="sxs-lookup"><span data-stu-id="bd5c3-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="bd5c3-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="bd5c3-142">РЕС_БИТМАСК</span><span class="sxs-lookup"><span data-stu-id="bd5c3-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="bd5c3-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="bd5c3-144">РЕС_КОММЕНТ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="bd5c3-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="bd5c3-146">РЕС_КОМПАРЕПРОПС</span><span class="sxs-lookup"><span data-stu-id="bd5c3-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="bd5c3-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="bd5c3-148">РЕС_КОНТЕНТ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="bd5c3-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="bd5c3-150">РЕС_ЕКСИСТ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="bd5c3-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="bd5c3-152">РЕС_НОТ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="bd5c3-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="bd5c3-154">РЕС_ОР</span><span class="sxs-lookup"><span data-stu-id="bd5c3-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="bd5c3-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="bd5c3-156">РЕС_ПРОПЕРТИ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="bd5c3-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="bd5c3-158">РЕС_СИЗЕ</span><span class="sxs-lookup"><span data-stu-id="bd5c3-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="bd5c3-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="bd5c3-160">РЕС_СУБРЕСТРИКТИОН</span><span class="sxs-lookup"><span data-stu-id="bd5c3-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="bd5c3-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd5c3-162">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd5c3-162">Remarks</span></span>

<span data-ttu-id="bd5c3-163">Клиенты используют структуру **срестриктион** для ограничения числа и типа строк в представлении таблицы, а также для поиска определенных сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="bd5c3-164">Чтобы наложить ограничение на таблицу, клиенты вызывают вызов [IMAPITable:: restrict](imapitable-restrict.md) или [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="bd5c3-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="bd5c3-165">Чтобы наложить ограничение на папку, клиенты вызывают метод [IMAPIContainer:: сетсеарчкритериа](imapicontainer-setsearchcriteria.md) папки.</span><span class="sxs-lookup"><span data-stu-id="bd5c3-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="bd5c3-166">Дополнительные сведения об ограничениях на использование таблиц приведены в статье [об ограничениях](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="bd5c3-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd5c3-167">См. также</span><span class="sxs-lookup"><span data-stu-id="bd5c3-167">See also</span></span>



[<span data-ttu-id="bd5c3-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="bd5c3-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="bd5c3-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="bd5c3-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="bd5c3-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="bd5c3-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="bd5c3-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="bd5c3-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="bd5c3-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="bd5c3-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="bd5c3-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="bd5c3-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="bd5c3-179">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="bd5c3-179">MAPI Structures</span></span>](mapi-structures.md)

