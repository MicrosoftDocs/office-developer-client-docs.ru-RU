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
# <a name="spropvalue"></a><span data-ttu-id="a2085-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a2085-103">SPropValue</span></span>

  
  
<span data-ttu-id="a2085-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2085-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2085-105">Описывает свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="a2085-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a2085-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a2085-106">Header file:</span></span>  <br/> |<span data-ttu-id="a2085-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2085-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a2085-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="a2085-108">Related macros:</span></span>  <br/> |<span data-ttu-id="a2085-109">[CHANGE_PROP_TYPE,](change_prop_type.md) [MVI_PROP,](mvi_prop.md) [PROP_ID,](prop_id.md) [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="a2085-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="a2085-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="a2085-110">Members</span></span>

 <span data-ttu-id="a2085-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="a2085-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="a2085-112">Тег свойства для свойства.</span><span class="sxs-lookup"><span data-stu-id="a2085-112">Property tag for the property.</span></span> <span data-ttu-id="a2085-113">Теги свойств — это 32-битные неподписаные integers, состоящие из уникального идентификатора свойства в 16 битах высокого порядка и типа свойства в 16 битах низкого порядка.</span><span class="sxs-lookup"><span data-stu-id="a2085-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="a2085-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="a2085-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="a2085-115">Зарезервировано для MAPI; не используйте.</span><span class="sxs-lookup"><span data-stu-id="a2085-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="a2085-116">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a2085-116">**Value**</span></span>
  
> <span data-ttu-id="a2085-117">Объединение значений данных, определенное значение, определенное типом свойства.</span><span class="sxs-lookup"><span data-stu-id="a2085-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="a2085-118">В следующей таблице перечислены для каждого типа свойства, члена объединения, который должен использоваться, и связанного с ним типа данных.</span><span class="sxs-lookup"><span data-stu-id="a2085-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="a2085-119">**Тип свойства**</span><span class="sxs-lookup"><span data-stu-id="a2085-119">**Property type**</span></span>|<span data-ttu-id="a2085-120">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a2085-120">**Value**</span></span>|<span data-ttu-id="a2085-121">**Тип данных значения**</span><span class="sxs-lookup"><span data-stu-id="a2085-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a2085-122">PT_I2 или PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="a2085-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="a2085-123">**i**</span><span class="sxs-lookup"><span data-stu-id="a2085-123">**i**</span></span> <br/> |<span data-ttu-id="a2085-124">short int</span><span class="sxs-lookup"><span data-stu-id="a2085-124">short int</span></span>  <br/> |
|<span data-ttu-id="a2085-125">PT_I4 или PT_LONG (подписан)</span><span class="sxs-lookup"><span data-stu-id="a2085-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="a2085-126">**l**</span><span class="sxs-lookup"><span data-stu-id="a2085-126">**l**</span></span> <br/> |<span data-ttu-id="a2085-127">LONG</span><span class="sxs-lookup"><span data-stu-id="a2085-127">LONG</span></span>  <br/> |
|<span data-ttu-id="a2085-128">PT_I4 или PT_LONG (без подписи)</span><span class="sxs-lookup"><span data-stu-id="a2085-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="a2085-129">**ul**</span><span class="sxs-lookup"><span data-stu-id="a2085-129">**ul**</span></span> <br/> |<span data-ttu-id="a2085-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="a2085-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="a2085-131">PT_R4 или PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="a2085-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="a2085-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="a2085-132">**flt**</span></span> <br/> |<span data-ttu-id="a2085-133">float</span><span class="sxs-lookup"><span data-stu-id="a2085-133">float</span></span>  <br/> |
|<span data-ttu-id="a2085-134">PT_R8 или PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="a2085-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="a2085-135">**dbl**</span><span class="sxs-lookup"><span data-stu-id="a2085-135">**dbl**</span></span> <br/> |<span data-ttu-id="a2085-136">double</span><span class="sxs-lookup"><span data-stu-id="a2085-136">double</span></span>  <br/> |
|<span data-ttu-id="a2085-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a2085-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="a2085-138">**b**</span><span class="sxs-lookup"><span data-stu-id="a2085-138">**b**</span></span> <br/> |<span data-ttu-id="a2085-139">unsigned short int</span><span class="sxs-lookup"><span data-stu-id="a2085-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="a2085-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="a2085-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="a2085-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="a2085-141">**cur**</span></span> <br/> |[<span data-ttu-id="a2085-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="a2085-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="a2085-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="a2085-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="a2085-144">**at**</span><span class="sxs-lookup"><span data-stu-id="a2085-144">**at**</span></span> <br/> |<span data-ttu-id="a2085-145">double</span><span class="sxs-lookup"><span data-stu-id="a2085-145">double</span></span>  <br/> |
|<span data-ttu-id="a2085-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a2085-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="a2085-147">**ft**</span><span class="sxs-lookup"><span data-stu-id="a2085-147">**ft**</span></span> <br/> |[<span data-ttu-id="a2085-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="a2085-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="a2085-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a2085-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="a2085-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="a2085-150">**lpszA**</span></span> <br/> |<span data-ttu-id="a2085-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="a2085-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="a2085-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a2085-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="a2085-153">**bin**</span><span class="sxs-lookup"><span data-stu-id="a2085-153">**bin**</span></span> <br/> |<span data-ttu-id="a2085-154">BYTE [array]</span><span class="sxs-lookup"><span data-stu-id="a2085-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="a2085-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a2085-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="a2085-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="a2085-156">**lpszW**</span></span> <br/> |<span data-ttu-id="a2085-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a2085-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="a2085-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="a2085-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="a2085-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="a2085-159">**lpguid**</span></span> <br/> |<span data-ttu-id="a2085-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="a2085-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="a2085-161">PT_I8 или PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="a2085-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="a2085-162">**li**</span><span class="sxs-lookup"><span data-stu-id="a2085-162">**li**</span></span> <br/> |<span data-ttu-id="a2085-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="a2085-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="a2085-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="a2085-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="a2085-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="a2085-165">**MVi**</span></span> <br/> |[<span data-ttu-id="a2085-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="a2085-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="a2085-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="a2085-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="a2085-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="a2085-168">**MVI**</span></span> <br/> |[<span data-ttu-id="a2085-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="a2085-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="a2085-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="a2085-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="a2085-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="a2085-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="a2085-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="a2085-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="a2085-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="a2085-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="a2085-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="a2085-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="a2085-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="a2085-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="a2085-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="a2085-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="a2085-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="a2085-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="a2085-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="a2085-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="a2085-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="a2085-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="a2085-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="a2085-180">**MVat**</span></span> <br/> |[<span data-ttu-id="a2085-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="a2085-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="a2085-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a2085-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="a2085-183">**MVFT**</span><span class="sxs-lookup"><span data-stu-id="a2085-183">**MVft**</span></span> <br/> |[<span data-ttu-id="a2085-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="a2085-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="a2085-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="a2085-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="a2085-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="a2085-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="a2085-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="a2085-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="a2085-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="a2085-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="a2085-189">**MVSzA**</span><span class="sxs-lookup"><span data-stu-id="a2085-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="a2085-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="a2085-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="a2085-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a2085-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="a2085-192">**MVSzW**</span><span class="sxs-lookup"><span data-stu-id="a2085-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="a2085-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="a2085-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="a2085-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="a2085-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="a2085-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="a2085-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="a2085-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="a2085-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="a2085-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="a2085-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="a2085-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="a2085-198">**MVli**</span></span> <br/> |[<span data-ttu-id="a2085-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="a2085-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="a2085-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="a2085-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="a2085-201">**err**</span><span class="sxs-lookup"><span data-stu-id="a2085-201">**err**</span></span> <br/> |[<span data-ttu-id="a2085-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="a2085-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="a2085-203">PT_NULL или PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="a2085-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="a2085-204">**x**</span><span class="sxs-lookup"><span data-stu-id="a2085-204">**x**</span></span> <br/> |<span data-ttu-id="a2085-205">LONG</span><span class="sxs-lookup"><span data-stu-id="a2085-205">LONG</span></span>  <br/> |
|<span data-ttu-id="a2085-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="a2085-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="a2085-207">**lpv**</span><span class="sxs-lookup"><span data-stu-id="a2085-207">**lpv**</span></span> <br/> |<span data-ttu-id="a2085-208">VOID \*</span><span class="sxs-lookup"><span data-stu-id="a2085-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2085-209">Примечания</span><span class="sxs-lookup"><span data-stu-id="a2085-209">Remarks</span></span>

<span data-ttu-id="a2085-210">Член **ulPropTag** состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="a2085-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="a2085-211">Идентификатор в 16 битах высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="a2085-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="a2085-212">Тип в 16 битах низкого порядка.</span><span class="sxs-lookup"><span data-stu-id="a2085-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="a2085-213">Идентификатор — это числовая величина в определенном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="a2085-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="a2085-214">MAPI определяет диапазоны для идентификаторов, чтобы описать, для чего используется свойство и кто несет ответственность за его обслуживание.</span><span class="sxs-lookup"><span data-stu-id="a2085-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="a2085-215">MAPI определяет ограничения для каждого тега свойства, поддерживаемого в файле загона Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="a2085-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="a2085-216">Тип указывает формат значения свойства.</span><span class="sxs-lookup"><span data-stu-id="a2085-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="a2085-217">MAPI определяет константы для каждого из типов свойств, поддерживаемые в файле загона Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="a2085-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="a2085-218">Полный список допустимого диапазона свойств для идентификаторов и типов свойств см. в приложении ["Идентификаторы](property-identifiers-and-types.md) и типы свойств".</span><span class="sxs-lookup"><span data-stu-id="a2085-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="a2085-219">Член **dwAlignPad** используется в качестве заполнения для правильного выравнивания на компьютерах, которые требуют выравнивания 8 байт для 8-байтовых значений.</span><span class="sxs-lookup"><span data-stu-id="a2085-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="a2085-220">Разработчикам, которые пишут код на таких компьютерах, следует использовать процедуры выделения памяти, которые выделяют массивы **SPropValue** на границах 8-byte.</span><span class="sxs-lookup"><span data-stu-id="a2085-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="a2085-221">Дополнительные сведения см. в обзоре [типов свойств MAPI](mapi-property-type-overview.md) и обновлении [свойств MAPI.](updating-mapi-properties.md)</span><span class="sxs-lookup"><span data-stu-id="a2085-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2085-222">См. также</span><span class="sxs-lookup"><span data-stu-id="a2085-222">See also</span></span>



[<span data-ttu-id="a2085-223">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a2085-223">MAPI Structures</span></span>](mapi-structures.md)

