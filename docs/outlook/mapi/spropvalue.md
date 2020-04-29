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
# <a name="spropvalue"></a><span data-ttu-id="3acee-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3acee-103">SPropValue</span></span>

  
  
<span data-ttu-id="3acee-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3acee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3acee-105">Описывает свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="3acee-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3acee-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3acee-106">Header file:</span></span>  <br/> |<span data-ttu-id="3acee-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3acee-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3acee-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="3acee-108">Related macros:</span></span>  <br/> |<span data-ttu-id="3acee-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="3acee-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="3acee-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="3acee-110">Members</span></span>

 <span data-ttu-id="3acee-111">**улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="3acee-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="3acee-112">Тег свойства для свойства.</span><span class="sxs-lookup"><span data-stu-id="3acee-112">Property tag for the property.</span></span> <span data-ttu-id="3acee-113">Теги свойств — это 32 — битовые целые числа без знака, состоящие из уникального идентификатора свойства в высоком порядке 16 бит и тип свойства в младших 16 битах.</span><span class="sxs-lookup"><span data-stu-id="3acee-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="3acee-114">**двалигнпад**</span><span class="sxs-lookup"><span data-stu-id="3acee-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="3acee-115">Зарезервировано для MAPI; не используйте.</span><span class="sxs-lookup"><span data-stu-id="3acee-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="3acee-116">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3acee-116">**Value**</span></span>
  
> <span data-ttu-id="3acee-117">Объединение значений данных, определенное значение, которое определяется типом свойства.</span><span class="sxs-lookup"><span data-stu-id="3acee-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="3acee-118">В приведенной ниже таблице перечислены типы свойств, элементы объединения, которые следует использовать, и связанные с ними типы данных.</span><span class="sxs-lookup"><span data-stu-id="3acee-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="3acee-119">**Тип свойства**</span><span class="sxs-lookup"><span data-stu-id="3acee-119">**Property type**</span></span>|<span data-ttu-id="3acee-120">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3acee-120">**Value**</span></span>|<span data-ttu-id="3acee-121">**Тип данных value**</span><span class="sxs-lookup"><span data-stu-id="3acee-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3acee-122">PT_I2 или PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="3acee-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="3acee-123">**i**</span><span class="sxs-lookup"><span data-stu-id="3acee-123">**i**</span></span> <br/> |<span data-ttu-id="3acee-124">short int</span><span class="sxs-lookup"><span data-stu-id="3acee-124">short int</span></span>  <br/> |
|<span data-ttu-id="3acee-125">PT_I4 или PT_LONG (со знаком)</span><span class="sxs-lookup"><span data-stu-id="3acee-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="3acee-126">**l**</span><span class="sxs-lookup"><span data-stu-id="3acee-126">**l**</span></span> <br/> |<span data-ttu-id="3acee-127">БОЛЬШОМ</span><span class="sxs-lookup"><span data-stu-id="3acee-127">LONG</span></span>  <br/> |
|<span data-ttu-id="3acee-128">PT_I4 или PT_LONG (без знака)</span><span class="sxs-lookup"><span data-stu-id="3acee-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="3acee-129">**сертифицирован**</span><span class="sxs-lookup"><span data-stu-id="3acee-129">**ul**</span></span> <br/> |<span data-ttu-id="3acee-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="3acee-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="3acee-131">PT_R4 или PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="3acee-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="3acee-132">**флт**</span><span class="sxs-lookup"><span data-stu-id="3acee-132">**flt**</span></span> <br/> |<span data-ttu-id="3acee-133">с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="3acee-133">float</span></span>  <br/> |
|<span data-ttu-id="3acee-134">PT_R8 или PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="3acee-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="3acee-135">**нажат**</span><span class="sxs-lookup"><span data-stu-id="3acee-135">**dbl**</span></span> <br/> |<span data-ttu-id="3acee-136">double</span><span class="sxs-lookup"><span data-stu-id="3acee-136">double</span></span>  <br/> |
|<span data-ttu-id="3acee-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3acee-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="3acee-138">**з**</span><span class="sxs-lookup"><span data-stu-id="3acee-138">**b**</span></span> <br/> |<span data-ttu-id="3acee-139">короткое целое без знака</span><span class="sxs-lookup"><span data-stu-id="3acee-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="3acee-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="3acee-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="3acee-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="3acee-141">**cur**</span></span> <br/> |[<span data-ttu-id="3acee-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="3acee-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="3acee-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="3acee-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="3acee-144">**в**</span><span class="sxs-lookup"><span data-stu-id="3acee-144">**at**</span></span> <br/> |<span data-ttu-id="3acee-145">double</span><span class="sxs-lookup"><span data-stu-id="3acee-145">double</span></span>  <br/> |
|<span data-ttu-id="3acee-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3acee-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="3acee-147">**метр**</span><span class="sxs-lookup"><span data-stu-id="3acee-147">**ft**</span></span> <br/> |[<span data-ttu-id="3acee-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="3acee-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="3acee-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3acee-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="3acee-150">**лпсза**</span><span class="sxs-lookup"><span data-stu-id="3acee-150">**lpszA**</span></span> <br/> |<span data-ttu-id="3acee-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="3acee-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="3acee-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3acee-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="3acee-153">**bin**</span><span class="sxs-lookup"><span data-stu-id="3acee-153">**bin**</span></span> <br/> |<span data-ttu-id="3acee-154">BYTE [Массив]</span><span class="sxs-lookup"><span data-stu-id="3acee-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="3acee-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3acee-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="3acee-156">**лпсзв**</span><span class="sxs-lookup"><span data-stu-id="3acee-156">**lpszW**</span></span> <br/> |<span data-ttu-id="3acee-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="3acee-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="3acee-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="3acee-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="3acee-159">**лпгуид**</span><span class="sxs-lookup"><span data-stu-id="3acee-159">**lpguid**</span></span> <br/> |<span data-ttu-id="3acee-160">лпгуид</span><span class="sxs-lookup"><span data-stu-id="3acee-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="3acee-161">PT_I8 или PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="3acee-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="3acee-162">**Li**</span><span class="sxs-lookup"><span data-stu-id="3acee-162">**li**</span></span> <br/> |<span data-ttu-id="3acee-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="3acee-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="3acee-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="3acee-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="3acee-165">**мви**</span><span class="sxs-lookup"><span data-stu-id="3acee-165">**MVi**</span></span> <br/> |[<span data-ttu-id="3acee-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="3acee-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="3acee-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="3acee-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="3acee-168">**мви**</span><span class="sxs-lookup"><span data-stu-id="3acee-168">**MVI**</span></span> <br/> |[<span data-ttu-id="3acee-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="3acee-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="3acee-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="3acee-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="3acee-171">**мвфлт**</span><span class="sxs-lookup"><span data-stu-id="3acee-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="3acee-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="3acee-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="3acee-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="3acee-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="3acee-174">**мвдбл**</span><span class="sxs-lookup"><span data-stu-id="3acee-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="3acee-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="3acee-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="3acee-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="3acee-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="3acee-177">**мвкур**</span><span class="sxs-lookup"><span data-stu-id="3acee-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="3acee-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="3acee-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="3acee-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="3acee-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="3acee-180">**мват**</span><span class="sxs-lookup"><span data-stu-id="3acee-180">**MVat**</span></span> <br/> |[<span data-ttu-id="3acee-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="3acee-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="3acee-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3acee-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="3acee-183">**мвфт**</span><span class="sxs-lookup"><span data-stu-id="3acee-183">**MVft**</span></span> <br/> |[<span data-ttu-id="3acee-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="3acee-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="3acee-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="3acee-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="3acee-186">**мвбин**</span><span class="sxs-lookup"><span data-stu-id="3acee-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="3acee-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="3acee-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="3acee-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="3acee-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="3acee-189">**мвсза**</span><span class="sxs-lookup"><span data-stu-id="3acee-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="3acee-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="3acee-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="3acee-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3acee-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="3acee-192">**мвсзв**</span><span class="sxs-lookup"><span data-stu-id="3acee-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="3acee-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="3acee-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="3acee-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="3acee-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="3acee-195">**мвгуид**</span><span class="sxs-lookup"><span data-stu-id="3acee-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="3acee-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="3acee-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="3acee-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="3acee-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="3acee-198">**мвли**</span><span class="sxs-lookup"><span data-stu-id="3acee-198">**MVli**</span></span> <br/> |[<span data-ttu-id="3acee-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="3acee-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="3acee-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="3acee-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="3acee-201">**err**</span><span class="sxs-lookup"><span data-stu-id="3acee-201">**err**</span></span> <br/> |[<span data-ttu-id="3acee-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="3acee-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="3acee-203">PT_NULL или PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="3acee-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="3acee-204">**x**</span><span class="sxs-lookup"><span data-stu-id="3acee-204">**x**</span></span> <br/> |<span data-ttu-id="3acee-205">БОЛЬШОМ</span><span class="sxs-lookup"><span data-stu-id="3acee-205">LONG</span></span>  <br/> |
|<span data-ttu-id="3acee-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="3acee-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="3acee-207">**лпв**</span><span class="sxs-lookup"><span data-stu-id="3acee-207">**lpv**</span></span> <br/> |<span data-ttu-id="3acee-208">ОТМЕНИТЬ\*</span><span class="sxs-lookup"><span data-stu-id="3acee-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3acee-209">Примечания</span><span class="sxs-lookup"><span data-stu-id="3acee-209">Remarks</span></span>

<span data-ttu-id="3acee-210">Элемент **улпроптаг** состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="3acee-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="3acee-211">Идентификатор в высоком порядке 16 бит.</span><span class="sxs-lookup"><span data-stu-id="3acee-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="3acee-212">Тип в 16 младших битах.</span><span class="sxs-lookup"><span data-stu-id="3acee-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="3acee-213">Идентификатор — это числовое значение в определенном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="3acee-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="3acee-214">MAPI определяет диапазоны для идентификаторов, описывающих, для чего используется свойство и кто отвечает за его обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3acee-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="3acee-215">MAPI определяет ограничения для каждого из тегов свойств, которые он поддерживает, в файле заголовка Мапитагс. h.</span><span class="sxs-lookup"><span data-stu-id="3acee-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="3acee-216">Тип указывает формат значения свойства.</span><span class="sxs-lookup"><span data-stu-id="3acee-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="3acee-217">MAPI определяет константы для каждого из типов свойств, поддерживаемых в файле заголовка MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="3acee-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="3acee-218">Полный список допустимых диапазонов свойств для идентификаторов и типов свойств представлен в приложении [идентификаторы и типы](property-identifiers-and-types.md) свойств.</span><span class="sxs-lookup"><span data-stu-id="3acee-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="3acee-219">Элемент **двалигнпад** используется в качестве заполнения для обеспечения правильного выравнивания на компьютерах, для которых требуется 8-байтное выравнивание для 8-байтовых значений.</span><span class="sxs-lookup"><span data-stu-id="3acee-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="3acee-220">Разработчики, которые пишут код на такие компьютеры, должны использовать процедуры выделения памяти, которые распределяют массивы **спропвалуе** по 8 байтам.</span><span class="sxs-lookup"><span data-stu-id="3acee-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="3acee-221">Для получения дополнительных сведений см. [Обзор типов свойств MAPI](mapi-property-type-overview.md) и [Обновление свойств MAPI](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3acee-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3acee-222">См. также</span><span class="sxs-lookup"><span data-stu-id="3acee-222">See also</span></span>



[<span data-ttu-id="3acee-223">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3acee-223">MAPI Structures</span></span>](mapi-structures.md)

