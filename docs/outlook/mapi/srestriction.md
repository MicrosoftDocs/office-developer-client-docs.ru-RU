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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341743"
---
# <a name="srestriction"></a><span data-ttu-id="5c4be-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-103">SRestriction</span></span>

  
  
<span data-ttu-id="5c4be-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c4be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c4be-105">Описывает фильтр для ограничения представления таблицы определенными строками.</span><span class="sxs-lookup"><span data-stu-id="5c4be-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c4be-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5c4be-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c4be-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5c4be-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="5c4be-108">Members</span><span class="sxs-lookup"><span data-stu-id="5c4be-108">Members</span></span>

 <span data-ttu-id="5c4be-109">**RT**</span><span class="sxs-lookup"><span data-stu-id="5c4be-109">**rt**</span></span>
  
> <span data-ttu-id="5c4be-110">Тип ограничения.</span><span class="sxs-lookup"><span data-stu-id="5c4be-110">The restriction type.</span></span> <span data-ttu-id="5c4be-111">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5c4be-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="5c4be-112">РЕС_АНД</span><span class="sxs-lookup"><span data-stu-id="5c4be-112">RES_AND</span></span> 
  
> <span data-ttu-id="5c4be-113">Ограничение \*\*\*\* , которое применяет к ограничению операцию побитового **и** .</span><span class="sxs-lookup"><span data-stu-id="5c4be-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="5c4be-114">РЕС_БИТМАСК</span><span class="sxs-lookup"><span data-stu-id="5c4be-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="5c4be-115">Ограничение битовой маски, которое применяет битовую маску к значению свойства.</span><span class="sxs-lookup"><span data-stu-id="5c4be-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="5c4be-116">РЕС_КОММЕНТ</span><span class="sxs-lookup"><span data-stu-id="5c4be-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="5c4be-117">Ограничение комментария, которое связывает комментарий с ограничением.</span><span class="sxs-lookup"><span data-stu-id="5c4be-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="5c4be-118">РЕС_КОМПАРЕПРОПС</span><span class="sxs-lookup"><span data-stu-id="5c4be-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="5c4be-119">Ограничение на сравнение свойств, которое сравнивает два значения свойств.</span><span class="sxs-lookup"><span data-stu-id="5c4be-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="5c4be-120">РЕС_КОНТЕНТ</span><span class="sxs-lookup"><span data-stu-id="5c4be-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="5c4be-121">Ограничение содержимого, которое выполняет поиск определенного содержимого в значении свойства.</span><span class="sxs-lookup"><span data-stu-id="5c4be-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="5c4be-122">РЕС_ЕКСИСТ</span><span class="sxs-lookup"><span data-stu-id="5c4be-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="5c4be-123">Ограничение exist, определяющее, поддерживается ли свойство.</span><span class="sxs-lookup"><span data-stu-id="5c4be-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="5c4be-124">РЕС_НОТ</span><span class="sxs-lookup"><span data-stu-id="5c4be-124">RES_NOT</span></span> 
  
> <span data-ttu-id="5c4be-125">Ограничение **Not** , которое применяет логическую операцию **Not** к ограничению.</span><span class="sxs-lookup"><span data-stu-id="5c4be-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="5c4be-126">РЕС_ОР</span><span class="sxs-lookup"><span data-stu-id="5c4be-126">RES_OR</span></span> 
  
> <span data-ttu-id="5c4be-127">Ограничение \*\*\*\* , которое применяет логическую операцию **или** к ограничению.</span><span class="sxs-lookup"><span data-stu-id="5c4be-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="5c4be-128">РЕС_ПРОПЕРТИ</span><span class="sxs-lookup"><span data-stu-id="5c4be-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="5c4be-129">Ограничение свойства, которое определяет, совпадает ли значение свойства с определенным значением.</span><span class="sxs-lookup"><span data-stu-id="5c4be-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="5c4be-130">РЕС_СИЗЕ</span><span class="sxs-lookup"><span data-stu-id="5c4be-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="5c4be-131">Ограничение размера, определяющее, является ли значение свойства определенным размером.</span><span class="sxs-lookup"><span data-stu-id="5c4be-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="5c4be-132">РЕС_СУБРЕСТРИКТИОН</span><span class="sxs-lookup"><span data-stu-id="5c4be-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="5c4be-133">Ограничение вложенного объекта, которое применяет ограничение к вложениям или получателям сообщения.</span><span class="sxs-lookup"><span data-stu-id="5c4be-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="5c4be-134">**распределение**</span><span class="sxs-lookup"><span data-stu-id="5c4be-134">**res**</span></span>
  
> <span data-ttu-id="5c4be-135">Объединение структур ограничений, описывающих применяемый фильтр.</span><span class="sxs-lookup"><span data-stu-id="5c4be-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="5c4be-136">Конкретная структура, включенная в состав элемента **RES** , зависит от значения элемента **RT** .</span><span class="sxs-lookup"><span data-stu-id="5c4be-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="5c4be-137">Сопоставление типа и структуры ограничения представлено в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5c4be-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="5c4be-138">**Тип ограничения**</span><span class="sxs-lookup"><span data-stu-id="5c4be-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="5c4be-139">**Структура ограничения**</span><span class="sxs-lookup"><span data-stu-id="5c4be-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="5c4be-140">РЕС_АНД</span><span class="sxs-lookup"><span data-stu-id="5c4be-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="5c4be-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="5c4be-142">РЕС_БИТМАСК</span><span class="sxs-lookup"><span data-stu-id="5c4be-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="5c4be-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="5c4be-144">РЕС_КОММЕНТ</span><span class="sxs-lookup"><span data-stu-id="5c4be-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="5c4be-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="5c4be-146">РЕС_КОМПАРЕПРОПС</span><span class="sxs-lookup"><span data-stu-id="5c4be-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="5c4be-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="5c4be-148">РЕС_КОНТЕНТ</span><span class="sxs-lookup"><span data-stu-id="5c4be-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="5c4be-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="5c4be-150">РЕС_ЕКСИСТ</span><span class="sxs-lookup"><span data-stu-id="5c4be-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="5c4be-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="5c4be-152">РЕС_НОТ</span><span class="sxs-lookup"><span data-stu-id="5c4be-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="5c4be-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="5c4be-154">РЕС_ОР</span><span class="sxs-lookup"><span data-stu-id="5c4be-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="5c4be-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="5c4be-156">РЕС_ПРОПЕРТИ</span><span class="sxs-lookup"><span data-stu-id="5c4be-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="5c4be-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="5c4be-158">РЕС_СИЗЕ</span><span class="sxs-lookup"><span data-stu-id="5c4be-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="5c4be-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="5c4be-160">РЕС_СУБРЕСТРИКТИОН</span><span class="sxs-lookup"><span data-stu-id="5c4be-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="5c4be-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c4be-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c4be-162">Remarks</span></span>

<span data-ttu-id="5c4be-163">Клиенты используют структуру **срестриктион** для ограничения числа и типа строк в представлении таблицы, а также для поиска определенных сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="5c4be-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="5c4be-164">Чтобы наложить ограничение на таблицу, клиенты вызывают вызов [IMAPITable:: restrict](imapitable-restrict.md) или [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="5c4be-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="5c4be-165">Чтобы наложить ограничение на папку, клиенты вызывают метод [IMAPIContainer:: сетсеарчкритериа](imapicontainer-setsearchcriteria.md) папки.</span><span class="sxs-lookup"><span data-stu-id="5c4be-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="5c4be-166">Дополнительные сведения об ограничениях на использование таблиц приведены в статье [об ограничениях](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="5c4be-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5c4be-167">См. также</span><span class="sxs-lookup"><span data-stu-id="5c4be-167">See also</span></span>



[<span data-ttu-id="5c4be-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="5c4be-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="5c4be-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="5c4be-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="5c4be-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="5c4be-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="5c4be-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="5c4be-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="5c4be-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="5c4be-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="5c4be-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="5c4be-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="5c4be-179">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5c4be-179">MAPI Structures</span></span>](mapi-structures.md)

