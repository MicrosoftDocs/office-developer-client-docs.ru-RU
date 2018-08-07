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
ms.openlocfilehash: f378bdd473410b846328cbe1f911eba9401f88cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812380"
---
# <a name="spropvalue"></a><span data-ttu-id="af5d9-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="af5d9-103">SPropValue</span></span>

  
  
<span data-ttu-id="af5d9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af5d9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af5d9-105">Описывает свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="af5d9-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af5d9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="af5d9-106">Header file:</span></span>  <br/> |<span data-ttu-id="af5d9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af5d9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="af5d9-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="af5d9-108">Related macros:</span></span>  <br/> |<span data-ttu-id="af5d9-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="af5d9-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="af5d9-110">Members</span><span class="sxs-lookup"><span data-stu-id="af5d9-110">Members</span></span>

 <span data-ttu-id="af5d9-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="af5d9-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="af5d9-112">Свойство tag для свойства.</span><span class="sxs-lookup"><span data-stu-id="af5d9-112">Property tag for the property.</span></span> <span data-ttu-id="af5d9-113">Свойство теги являются целые числа без знака 32-разрядная версия, состоящий из свойство имеет уникальный идентификатор в 16 бит высокого приоритета и тип свойства в 16 бит низкого приоритета.</span><span class="sxs-lookup"><span data-stu-id="af5d9-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="af5d9-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="af5d9-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="af5d9-115">Зарезервировано для MAPI; не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="af5d9-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="af5d9-116">**Значение**</span><span class="sxs-lookup"><span data-stu-id="af5d9-116">**Value**</span></span>
  
> <span data-ttu-id="af5d9-117">Объединение данных значения определенного значения, зависит от типа свойства.</span><span class="sxs-lookup"><span data-stu-id="af5d9-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="af5d9-118">В следующей таблице приведены для каждого типа свойств, члена объединения, который будет использоваться и его тип данных, связанного.</span><span class="sxs-lookup"><span data-stu-id="af5d9-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="af5d9-119">**Тип свойства**</span><span class="sxs-lookup"><span data-stu-id="af5d9-119">**Property type**</span></span>|<span data-ttu-id="af5d9-120">**Значение**</span><span class="sxs-lookup"><span data-stu-id="af5d9-120">**Value**</span></span>|<span data-ttu-id="af5d9-121">**Тип данных значения**</span><span class="sxs-lookup"><span data-stu-id="af5d9-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="af5d9-122">PT_I2 или PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="af5d9-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="af5d9-123">**я**</span><span class="sxs-lookup"><span data-stu-id="af5d9-123">**i**</span></span> <br/> |<span data-ttu-id="af5d9-124">короткое целое</span><span class="sxs-lookup"><span data-stu-id="af5d9-124">short int</span></span>  <br/> |
|<span data-ttu-id="af5d9-125">PT_I4 или PT_LONG (подпись)</span><span class="sxs-lookup"><span data-stu-id="af5d9-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="af5d9-126">**l**</span><span class="sxs-lookup"><span data-stu-id="af5d9-126">**l**</span></span> <br/> |<span data-ttu-id="af5d9-127">ДЛИННЫЙ</span><span class="sxs-lookup"><span data-stu-id="af5d9-127">LONG</span></span>  <br/> |
|<span data-ttu-id="af5d9-128">PT_I4 или PT_LONG (без знака)</span><span class="sxs-lookup"><span data-stu-id="af5d9-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="af5d9-129">**ul**</span><span class="sxs-lookup"><span data-stu-id="af5d9-129">**ul**</span></span> <br/> |<span data-ttu-id="af5d9-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="af5d9-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="af5d9-131">PT_R4 или PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="af5d9-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="af5d9-132">**Сбой**</span><span class="sxs-lookup"><span data-stu-id="af5d9-132">**flt**</span></span> <br/> |<span data-ttu-id="af5d9-133">с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="af5d9-133">float</span></span>  <br/> |
|<span data-ttu-id="af5d9-134">PT_R8 или PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="af5d9-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="af5d9-135">**двойной**</span><span class="sxs-lookup"><span data-stu-id="af5d9-135">**dbl**</span></span> <br/> |<span data-ttu-id="af5d9-136">double</span><span class="sxs-lookup"><span data-stu-id="af5d9-136">double</span></span>  <br/> |
|<span data-ttu-id="af5d9-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="af5d9-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="af5d9-138">**b**</span><span class="sxs-lookup"><span data-stu-id="af5d9-138">**b**</span></span> <br/> |<span data-ttu-id="af5d9-139">короткое целое число</span><span class="sxs-lookup"><span data-stu-id="af5d9-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="af5d9-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="af5d9-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="af5d9-141">**по**</span><span class="sxs-lookup"><span data-stu-id="af5d9-141">**cur**</span></span> <br/> |[<span data-ttu-id="af5d9-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="af5d9-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="af5d9-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="af5d9-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="af5d9-144">**в**</span><span class="sxs-lookup"><span data-stu-id="af5d9-144">**at**</span></span> <br/> |<span data-ttu-id="af5d9-145">double</span><span class="sxs-lookup"><span data-stu-id="af5d9-145">double</span></span>  <br/> |
|<span data-ttu-id="af5d9-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="af5d9-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="af5d9-147">**FT**</span><span class="sxs-lookup"><span data-stu-id="af5d9-147">**ft**</span></span> <br/> |[<span data-ttu-id="af5d9-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="af5d9-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="af5d9-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="af5d9-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="af5d9-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="af5d9-150">**lpszA**</span></span> <br/> |<span data-ttu-id="af5d9-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="af5d9-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="af5d9-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="af5d9-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="af5d9-153">**корзины**</span><span class="sxs-lookup"><span data-stu-id="af5d9-153">**bin**</span></span> <br/> |<span data-ttu-id="af5d9-154">BYTE [массива]</span><span class="sxs-lookup"><span data-stu-id="af5d9-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="af5d9-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af5d9-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="af5d9-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="af5d9-156">**lpszW**</span></span> <br/> |<span data-ttu-id="af5d9-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="af5d9-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="af5d9-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="af5d9-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="af5d9-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="af5d9-159">**lpguid**</span></span> <br/> |<span data-ttu-id="af5d9-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="af5d9-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="af5d9-161">PT_I8 или PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="af5d9-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="af5d9-162">**li**</span><span class="sxs-lookup"><span data-stu-id="af5d9-162">**li**</span></span> <br/> |<span data-ttu-id="af5d9-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="af5d9-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="af5d9-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="af5d9-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="af5d9-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="af5d9-165">**MVi**</span></span> <br/> |[<span data-ttu-id="af5d9-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="af5d9-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="af5d9-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="af5d9-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="af5d9-168">**MVI**</span></span> <br/> |[<span data-ttu-id="af5d9-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="af5d9-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="af5d9-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="af5d9-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="af5d9-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="af5d9-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="af5d9-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="af5d9-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="af5d9-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="af5d9-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="af5d9-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="af5d9-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="af5d9-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="af5d9-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="af5d9-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="af5d9-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="af5d9-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="af5d9-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="af5d9-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="af5d9-180">**MVat**</span></span> <br/> |[<span data-ttu-id="af5d9-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="af5d9-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="af5d9-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="af5d9-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="af5d9-183">**MVft**</span></span> <br/> |[<span data-ttu-id="af5d9-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="af5d9-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="af5d9-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="af5d9-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="af5d9-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="af5d9-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="af5d9-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="af5d9-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="af5d9-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="af5d9-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="af5d9-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="af5d9-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af5d9-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="af5d9-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="af5d9-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="af5d9-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="af5d9-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="af5d9-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="af5d9-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="af5d9-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="af5d9-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="af5d9-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="af5d9-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="af5d9-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="af5d9-198">**MVli**</span></span> <br/> |[<span data-ttu-id="af5d9-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="af5d9-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="af5d9-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="af5d9-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="af5d9-201">**err**</span><span class="sxs-lookup"><span data-stu-id="af5d9-201">**err**</span></span> <br/> |[<span data-ttu-id="af5d9-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="af5d9-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="af5d9-203">PT_NULL или PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="af5d9-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="af5d9-204">**x**</span><span class="sxs-lookup"><span data-stu-id="af5d9-204">**x**</span></span> <br/> |<span data-ttu-id="af5d9-205">ДЛИННЫЙ</span><span class="sxs-lookup"><span data-stu-id="af5d9-205">LONG</span></span>  <br/> |
|<span data-ttu-id="af5d9-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="af5d9-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="af5d9-207">**lpv**</span><span class="sxs-lookup"><span data-stu-id="af5d9-207">**lpv**</span></span> <br/> |<span data-ttu-id="af5d9-208">VOID\*</span><span class="sxs-lookup"><span data-stu-id="af5d9-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af5d9-209">Замечания</span><span class="sxs-lookup"><span data-stu-id="af5d9-209">Remarks</span></span>

<span data-ttu-id="af5d9-210">Член **ulPropTag** состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="af5d9-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="af5d9-211">Идентификатор в 16 бит высокого приоритета.</span><span class="sxs-lookup"><span data-stu-id="af5d9-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="af5d9-212">Тип в 16 бит низкого приоритета.</span><span class="sxs-lookup"><span data-stu-id="af5d9-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="af5d9-213">Идентификатор — числовое значение в рамках определенного диапазона.</span><span class="sxs-lookup"><span data-stu-id="af5d9-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="af5d9-214">Диапазоны идентификаторов для описания, для чего используется свойство и кто несет ответственность за обеспечение его определены MAPI.</span><span class="sxs-lookup"><span data-stu-id="af5d9-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="af5d9-215">MAPI определяет ограничения для каждого из тегов свойств, поддерживаемых в файле заголовка Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="af5d9-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="af5d9-216">Тип указывает формат, для которых значение свойства.</span><span class="sxs-lookup"><span data-stu-id="af5d9-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="af5d9-217">MAPI определяет константы для каждого типа свойства, поддерживаемые в файле заголовка Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="af5d9-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="af5d9-218">Полный список диапазонов допустимым свойством для идентификаторов и типы свойств содержатся в приложении [типов и идентификаторы свойств](property-identifiers-and-types.md) .</span><span class="sxs-lookup"><span data-stu-id="af5d9-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="af5d9-219">Член **dwAlignPad** используется как внутренние поля чтобы сделать что правильного выравнивания на компьютерах, которые требуют 8-байтовое выравнивание для 8-байтовых значений.</span><span class="sxs-lookup"><span data-stu-id="af5d9-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="af5d9-220">Разработчики, написание кода для таких компьютеров следует использовать процедур выделения памяти, выделить массивы **SPropValue** на 8-байтовое границы.</span><span class="sxs-lookup"><span data-stu-id="af5d9-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="af5d9-221">Для получения дополнительных сведений см. [Обзор типа свойств MAPI](mapi-property-type-overview.md) и [Обновление свойств MAPI](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="af5d9-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af5d9-222">См. также</span><span class="sxs-lookup"><span data-stu-id="af5d9-222">See also</span></span>



[<span data-ttu-id="af5d9-223">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="af5d9-223">MAPI Structures</span></span>](mapi-structures.md)

