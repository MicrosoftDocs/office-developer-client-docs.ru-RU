---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433530"
---
# <a name="spropvalue"></a><span data-ttu-id="82b56-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="82b56-103">SPropValue</span></span>

  
  
<span data-ttu-id="82b56-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82b56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82b56-105">Описывает свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="82b56-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82b56-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="82b56-106">Header file:</span></span>  <br/> |<span data-ttu-id="82b56-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82b56-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="82b56-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="82b56-108">Related macros:</span></span>  <br/> |<span data-ttu-id="82b56-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md) [, PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="82b56-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="82b56-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="82b56-110">Members</span></span>

 <span data-ttu-id="82b56-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="82b56-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="82b56-112">Тег свойства для свойства.</span><span class="sxs-lookup"><span data-stu-id="82b56-112">Property tag for the property.</span></span> <span data-ttu-id="82b56-113">Теги свойств — это 32-битные неподписаные группы, состоящие из уникального идентификатора свойства в 16 битах высокого порядка и типа свойства в 16 битах низкого порядка.</span><span class="sxs-lookup"><span data-stu-id="82b56-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="82b56-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="82b56-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="82b56-115">Зарезервировано для MAPI; не использовать.</span><span class="sxs-lookup"><span data-stu-id="82b56-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="82b56-116">**Значение**</span><span class="sxs-lookup"><span data-stu-id="82b56-116">**Value**</span></span>
  
> <span data-ttu-id="82b56-117">Союз значений данных, определенное значение, продиктованное типом свойства.</span><span class="sxs-lookup"><span data-stu-id="82b56-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="82b56-118">В следующей таблице перечислены для каждого типа свойств, члена союза, который должен использоваться, и связанного с ним типа данных.</span><span class="sxs-lookup"><span data-stu-id="82b56-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="82b56-119">**Тип свойства**</span><span class="sxs-lookup"><span data-stu-id="82b56-119">**Property type**</span></span>|<span data-ttu-id="82b56-120">**Значение**</span><span class="sxs-lookup"><span data-stu-id="82b56-120">**Value**</span></span>|<span data-ttu-id="82b56-121">**Тип значения данных**</span><span class="sxs-lookup"><span data-stu-id="82b56-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="82b56-122">PT_I2 или PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="82b56-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="82b56-123">**i**</span><span class="sxs-lookup"><span data-stu-id="82b56-123">**i**</span></span> <br/> |<span data-ttu-id="82b56-124">short int</span><span class="sxs-lookup"><span data-stu-id="82b56-124">short int</span></span>  <br/> |
|<span data-ttu-id="82b56-125">PT_I4 или PT_LONG (подписан)</span><span class="sxs-lookup"><span data-stu-id="82b56-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="82b56-126">**l**</span><span class="sxs-lookup"><span data-stu-id="82b56-126">**l**</span></span> <br/> |<span data-ttu-id="82b56-127">LONG</span><span class="sxs-lookup"><span data-stu-id="82b56-127">LONG</span></span>  <br/> |
|<span data-ttu-id="82b56-128">PT_I4 или PT_LONG (без подписи)</span><span class="sxs-lookup"><span data-stu-id="82b56-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="82b56-129">**ul**</span><span class="sxs-lookup"><span data-stu-id="82b56-129">**ul**</span></span> <br/> |<span data-ttu-id="82b56-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="82b56-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="82b56-131">PT_R4 или PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="82b56-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="82b56-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="82b56-132">**flt**</span></span> <br/> |<span data-ttu-id="82b56-133">float</span><span class="sxs-lookup"><span data-stu-id="82b56-133">float</span></span>  <br/> |
|<span data-ttu-id="82b56-134">PT_R8 или PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="82b56-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="82b56-135">**dbl**</span><span class="sxs-lookup"><span data-stu-id="82b56-135">**dbl**</span></span> <br/> |<span data-ttu-id="82b56-136">double</span><span class="sxs-lookup"><span data-stu-id="82b56-136">double</span></span>  <br/> |
|<span data-ttu-id="82b56-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="82b56-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="82b56-138">**b**</span><span class="sxs-lookup"><span data-stu-id="82b56-138">**b**</span></span> <br/> |<span data-ttu-id="82b56-139">unsigned short int</span><span class="sxs-lookup"><span data-stu-id="82b56-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="82b56-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="82b56-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="82b56-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="82b56-141">**cur**</span></span> <br/> |[<span data-ttu-id="82b56-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="82b56-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="82b56-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="82b56-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="82b56-144">**в**</span><span class="sxs-lookup"><span data-stu-id="82b56-144">**at**</span></span> <br/> |<span data-ttu-id="82b56-145">double</span><span class="sxs-lookup"><span data-stu-id="82b56-145">double</span></span>  <br/> |
|<span data-ttu-id="82b56-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="82b56-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="82b56-147">**FT**</span><span class="sxs-lookup"><span data-stu-id="82b56-147">**ft**</span></span> <br/> |[<span data-ttu-id="82b56-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="82b56-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="82b56-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="82b56-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="82b56-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="82b56-150">**lpszA**</span></span> <br/> |<span data-ttu-id="82b56-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="82b56-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="82b56-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="82b56-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="82b56-153">**bin**</span><span class="sxs-lookup"><span data-stu-id="82b56-153">**bin**</span></span> <br/> |<span data-ttu-id="82b56-154">BYTE [массив]</span><span class="sxs-lookup"><span data-stu-id="82b56-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="82b56-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="82b56-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="82b56-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="82b56-156">**lpszW**</span></span> <br/> |<span data-ttu-id="82b56-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="82b56-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="82b56-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="82b56-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="82b56-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="82b56-159">**lpguid**</span></span> <br/> |<span data-ttu-id="82b56-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="82b56-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="82b56-161">PT_I8 или PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="82b56-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="82b56-162">**li**</span><span class="sxs-lookup"><span data-stu-id="82b56-162">**li**</span></span> <br/> |<span data-ttu-id="82b56-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="82b56-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="82b56-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="82b56-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="82b56-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="82b56-165">**MVi**</span></span> <br/> |[<span data-ttu-id="82b56-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="82b56-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="82b56-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="82b56-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="82b56-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="82b56-168">**MVI**</span></span> <br/> |[<span data-ttu-id="82b56-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="82b56-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="82b56-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="82b56-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="82b56-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="82b56-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="82b56-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="82b56-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="82b56-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="82b56-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="82b56-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="82b56-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="82b56-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="82b56-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="82b56-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="82b56-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="82b56-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="82b56-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="82b56-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="82b56-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="82b56-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="82b56-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="82b56-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="82b56-180">**MVat**</span></span> <br/> |[<span data-ttu-id="82b56-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="82b56-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="82b56-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="82b56-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="82b56-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="82b56-183">**MVft**</span></span> <br/> |[<span data-ttu-id="82b56-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="82b56-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="82b56-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="82b56-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="82b56-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="82b56-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="82b56-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="82b56-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="82b56-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="82b56-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="82b56-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="82b56-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="82b56-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="82b56-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="82b56-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="82b56-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="82b56-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="82b56-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="82b56-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="82b56-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="82b56-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="82b56-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="82b56-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="82b56-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="82b56-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="82b56-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="82b56-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="82b56-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="82b56-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="82b56-198">**MVli**</span></span> <br/> |[<span data-ttu-id="82b56-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="82b56-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="82b56-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="82b56-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="82b56-201">**err**</span><span class="sxs-lookup"><span data-stu-id="82b56-201">**err**</span></span> <br/> |[<span data-ttu-id="82b56-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="82b56-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="82b56-203">PT_NULL или PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="82b56-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="82b56-204">**x**</span><span class="sxs-lookup"><span data-stu-id="82b56-204">**x**</span></span> <br/> |<span data-ttu-id="82b56-205">LONG</span><span class="sxs-lookup"><span data-stu-id="82b56-205">LONG</span></span>  <br/> |
|<span data-ttu-id="82b56-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="82b56-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="82b56-207">**lpv**</span><span class="sxs-lookup"><span data-stu-id="82b56-207">**lpv**</span></span> <br/> |<span data-ttu-id="82b56-208">VOID \*</span><span class="sxs-lookup"><span data-stu-id="82b56-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82b56-209">Примечания</span><span class="sxs-lookup"><span data-stu-id="82b56-209">Remarks</span></span>

<span data-ttu-id="82b56-210">Член **ulPropTag** состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="82b56-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="82b56-211">Идентификатор в 16 битах высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="82b56-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="82b56-212">Тип в 16 битах низкого порядка.</span><span class="sxs-lookup"><span data-stu-id="82b56-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="82b56-213">Идентификатор — это числовая величина в определенном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="82b56-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="82b56-214">MAPI определяет диапазоны для идентификаторов, чтобы описать, для чего используется свойство и кто отвечает за его обслуживание.</span><span class="sxs-lookup"><span data-stu-id="82b56-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="82b56-215">MAPI определяет ограничения для каждого из тегов свойств, поддерживаемых в файле загона Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="82b56-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="82b56-216">Тип указывает формат значения свойства.</span><span class="sxs-lookup"><span data-stu-id="82b56-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="82b56-217">MAPI определяет константы для каждого из типов свойств, поддерживаемых в файле загона Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="82b56-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="82b56-218">Полный список допустимого диапазона свойств для идентификаторов и типов свойств см. в приложении Идентификаторы свойств [и типы.](property-identifiers-and-types.md)</span><span class="sxs-lookup"><span data-stu-id="82b56-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="82b56-219">Член **dwAlignPad** используется в качестве обивки, чтобы убедиться в правильной выравнивании на компьютерах, которые требуют выравнивания 8 байт для значений 8 байт.</span><span class="sxs-lookup"><span data-stu-id="82b56-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="82b56-220">Разработчикам, которые пишут код на таких компьютерах, следует использовать процедуры распределения памяти, которые выделяют массивы **SPropValue** на границах 8-byte.</span><span class="sxs-lookup"><span data-stu-id="82b56-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="82b56-221">Дополнительные сведения см. в [обзоре](mapi-property-type-overview.md) типов свойств MAPI и [обновлении свойств MAPI.](updating-mapi-properties.md)</span><span class="sxs-lookup"><span data-stu-id="82b56-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82b56-222">См. также</span><span class="sxs-lookup"><span data-stu-id="82b56-222">See also</span></span>



[<span data-ttu-id="82b56-223">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="82b56-223">MAPI Structures</span></span>](mapi-structures.md)

