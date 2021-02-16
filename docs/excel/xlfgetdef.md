---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422000"
---
# <a name="xlfgetdef"></a><span data-ttu-id="94b9a-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="94b9a-104">xlfGetDef</span></span>

<span data-ttu-id="94b9a-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="94b9a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="94b9a-106">Возвращает имя в виде текста, определенное для конкретной области, значения или формулы в книге.</span><span class="sxs-lookup"><span data-stu-id="94b9a-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="94b9a-107">В Excel это значение отображается в столбце  "Имя" диалоговых окна диспетчера  имен, которое  отображается при нажатии кнопки "Диспетчер имен" в разделе "Определенные имена" на вкладке **"Формулы".**  Используйте **xlfGetDef,** чтобы получить имя, соответствующее определению.</span><span class="sxs-lookup"><span data-stu-id="94b9a-107">In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition.</span></span> <span data-ttu-id="94b9a-108">Чтобы получить определение имени, используйте [xlfGetName.](xlfgetname.md)</span><span class="sxs-lookup"><span data-stu-id="94b9a-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="94b9a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="94b9a-109">Parameters</span></span>

<span data-ttu-id="94b9a-110">_pxDefText_ (**xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="94b9a-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="94b9a-111">Это может быть все, на что можно определить имя, включая ссылку, значение, объект или формулу.</span><span class="sxs-lookup"><span data-stu-id="94b9a-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="94b9a-112">Ссылки должны быть предоставлены в стиле R1C1, например  `"R3C5"` .</span><span class="sxs-lookup"><span data-stu-id="94b9a-112">References must be given in R1C1 style, such as  `"R3C5"`.</span></span> <span data-ttu-id="94b9a-113">Если _pxDefText_ является значением или формулой, нет необходимости включать знак равного значения,  отображаемого в столбце **"Ссылок** на" в диалоговом окне диспетчера имен.</span><span class="sxs-lookup"><span data-stu-id="94b9a-113">If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box.</span></span> <span data-ttu-id="94b9a-114">Если у  _pxDefText_ несколько имен, **xlfGetDef** возвращает имя.</span><span class="sxs-lookup"><span data-stu-id="94b9a-114">If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name.</span></span> <span data-ttu-id="94b9a-115">Если имя не соответствует  _pxDefText,_ **xlfGetDef** возвращает значение  `#NAME?` ошибки.</span><span class="sxs-lookup"><span data-stu-id="94b9a-115">If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="94b9a-116">_pxDocumentText_ (**xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="94b9a-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="94b9a-117">Указывает лист, на который установлен _pxDefText._</span><span class="sxs-lookup"><span data-stu-id="94b9a-117">Specifies the sheet that  _pxDefText_ is on.</span></span> <span data-ttu-id="94b9a-118">Если  _pxDocumentText_ опущен, он считается активным листом.</span><span class="sxs-lookup"><span data-stu-id="94b9a-118">If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="94b9a-119">_pxTypeNum_ (**xltypeNum)**</span><span class="sxs-lookup"><span data-stu-id="94b9a-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="94b9a-120">Число от 1 до 3, указывав, какие типы имен возвращаются.</span><span class="sxs-lookup"><span data-stu-id="94b9a-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="94b9a-121">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="94b9a-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="94b9a-122">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="94b9a-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94b9a-123">1 или пропущено</span><span class="sxs-lookup"><span data-stu-id="94b9a-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="94b9a-124">Только обычные имена.</span><span class="sxs-lookup"><span data-stu-id="94b9a-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="94b9a-125">2 </span><span class="sxs-lookup"><span data-stu-id="94b9a-125">2</span></span>  <br/> |<span data-ttu-id="94b9a-126">Только скрытые имена.</span><span class="sxs-lookup"><span data-stu-id="94b9a-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="94b9a-127">3 </span><span class="sxs-lookup"><span data-stu-id="94b9a-127">3</span></span>  <br/> |<span data-ttu-id="94b9a-128">Все имена.</span><span class="sxs-lookup"><span data-stu-id="94b9a-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="94b9a-129">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94b9a-129">Property value/Return value</span></span>

 <span data-ttu-id="94b9a-130">_pxRes_ (**xltypeStr** или **xltypeErr)**</span><span class="sxs-lookup"><span data-stu-id="94b9a-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="94b9a-131">Возвращает имя, связанное с указанным определением.</span><span class="sxs-lookup"><span data-stu-id="94b9a-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94b9a-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="94b9a-132">Remarks</span></span>

<span data-ttu-id="94b9a-133">В следующей таблице перечислены четыре примера значений, возвращаемого вызовом **xlfGetDef** с указанными аргументами.</span><span class="sxs-lookup"><span data-stu-id="94b9a-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="94b9a-134">**Имя, определенное в Excel**</span><span class="sxs-lookup"><span data-stu-id="94b9a-134">**Name defined in Excel**</span></span>|<span data-ttu-id="94b9a-135">**_pxDefText_**</span><span class="sxs-lookup"><span data-stu-id="94b9a-135">**_pxDefText_**</span></span>|<span data-ttu-id="94b9a-136">**_pxDocumentText_**</span><span class="sxs-lookup"><span data-stu-id="94b9a-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="94b9a-137">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="94b9a-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="94b9a-138">**Возвращаемая величина**</span><span class="sxs-lookup"><span data-stu-id="94b9a-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="94b9a-139">Указанный диапазон в листе Sheet4 называется Sales.</span><span class="sxs-lookup"><span data-stu-id="94b9a-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="94b9a-140">"R2C2:R9C6"</span><span class="sxs-lookup"><span data-stu-id="94b9a-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="94b9a-141">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="94b9a-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="94b9a-142">\<опущен\></span><span class="sxs-lookup"><span data-stu-id="94b9a-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="94b9a-143">"Sales" (Продажи)</span><span class="sxs-lookup"><span data-stu-id="94b9a-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="94b9a-144">Значение 100 в листе Sheet4 определяется как Константа.</span><span class="sxs-lookup"><span data-stu-id="94b9a-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="94b9a-145">"100"</span><span class="sxs-lookup"><span data-stu-id="94b9a-145">"100"</span></span>  <br/> |<span data-ttu-id="94b9a-146">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="94b9a-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="94b9a-147">\<опущен\></span><span class="sxs-lookup"><span data-stu-id="94b9a-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="94b9a-148">"Constant"</span><span class="sxs-lookup"><span data-stu-id="94b9a-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="94b9a-149">Указанная формула в листе Sheet4 называется SumTotal.</span><span class="sxs-lookup"><span data-stu-id="94b9a-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="94b9a-150">"SUM(R1C1:R10C1)"</span><span class="sxs-lookup"><span data-stu-id="94b9a-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="94b9a-151">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="94b9a-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="94b9a-152">\<опущен\></span><span class="sxs-lookup"><span data-stu-id="94b9a-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="94b9a-153">"SumTotal"</span><span class="sxs-lookup"><span data-stu-id="94b9a-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="94b9a-154">3 определяется как скрытый счетчик имен на активном листе.</span><span class="sxs-lookup"><span data-stu-id="94b9a-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="94b9a-155">"3"</span><span class="sxs-lookup"><span data-stu-id="94b9a-155">"3"</span></span>  <br/> |<span data-ttu-id="94b9a-156">\<опущен\></span><span class="sxs-lookup"><span data-stu-id="94b9a-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="94b9a-157">2 </span><span class="sxs-lookup"><span data-stu-id="94b9a-157">2</span></span>  <br/> |<span data-ttu-id="94b9a-158">"Counter"</span><span class="sxs-lookup"><span data-stu-id="94b9a-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94b9a-159">См. также</span><span class="sxs-lookup"><span data-stu-id="94b9a-159">See also</span></span>

- [<span data-ttu-id="94b9a-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="94b9a-160">xlfGetName</span></span>](xlfgetname.md)
- [<span data-ttu-id="94b9a-161">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="94b9a-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

