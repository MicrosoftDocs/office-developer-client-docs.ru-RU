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
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807369"
---
# <a name="xlfgetdef"></a><span data-ttu-id="029c8-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="029c8-104">xlfGetDef</span></span>

<span data-ttu-id="029c8-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="029c8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="029c8-106">Возвращает имя, в виде текста, определенное для конкретной области, значение или формулу в книге.</span><span class="sxs-lookup"><span data-stu-id="029c8-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="029c8-107">В Excel, это значение отображается в столбце **имя** диалогового окна **Диспетчер имен** , которая отображается при нажатии кнопки **Диспетчер имен** в разделе **Определенные имена** на вкладке **формул** использования **xlfGetDef** для получения имя, соответствующее определение.</span><span class="sxs-lookup"><span data-stu-id="029c8-107">In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition.</span></span> <span data-ttu-id="029c8-108">Чтобы получить определения имени, используйте [xlfGetName](xlfgetname.md).</span><span class="sxs-lookup"><span data-stu-id="029c8-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="029c8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="029c8-109">Parameters</span></span>

<span data-ttu-id="029c8-110">_pxDefText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="029c8-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="029c8-111">Может быть любым можно определить имя для ссылки, включая ссылки, значение, объект или формулы.</span><span class="sxs-lookup"><span data-stu-id="029c8-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="029c8-112">Справочные материалы должно быть задано в формате R1C1, таких как `"R3C5"`.</span><span class="sxs-lookup"><span data-stu-id="029c8-112">References must be given in R1C1 style, such as  `"R3C5"`.</span></span> <span data-ttu-id="029c8-113">Если _pxDefText_ значение или формула, не нужно добавить знак равенства, который отображается в столбце **Относится к** в диалоговом окне **Диспетчер имен** .</span><span class="sxs-lookup"><span data-stu-id="029c8-113">If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box.</span></span> <span data-ttu-id="029c8-114">При наличии более одного имени для _pxDefText_, **xlfGetDef** возвращает имя.</span><span class="sxs-lookup"><span data-stu-id="029c8-114">If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name.</span></span> <span data-ttu-id="029c8-115">Если имя не соответствует _pxDefText_, **xlfGetDef** возвращает `#NAME?` значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="029c8-115">If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="029c8-116">_pxDocumentText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="029c8-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="029c8-117">Указывает листа, _pxDefText_ включен.</span><span class="sxs-lookup"><span data-stu-id="029c8-117">Specifies the sheet that  _pxDefText_ is on.</span></span> <span data-ttu-id="029c8-118">Если _pxDocumentText_ указан, то предполагается, что оно является активный лист.</span><span class="sxs-lookup"><span data-stu-id="029c8-118">If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="029c8-119">_pxTypeNum_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="029c8-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="029c8-120">Число от 1 до 3, определяющее, какие типы имен возвращаются.</span><span class="sxs-lookup"><span data-stu-id="029c8-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="029c8-121">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="029c8-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="029c8-122">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="029c8-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="029c8-123">1 или опущен</span><span class="sxs-lookup"><span data-stu-id="029c8-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="029c8-124">Только обычный имена.</span><span class="sxs-lookup"><span data-stu-id="029c8-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="029c8-125">2</span><span class="sxs-lookup"><span data-stu-id="029c8-125">2</span></span>  <br/> |<span data-ttu-id="029c8-126">Только скрытые имена.</span><span class="sxs-lookup"><span data-stu-id="029c8-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="029c8-127">3</span><span class="sxs-lookup"><span data-stu-id="029c8-127">3</span></span>  <br/> |<span data-ttu-id="029c8-128">Все имена.</span><span class="sxs-lookup"><span data-stu-id="029c8-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="029c8-129">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="029c8-129">Property value/Return value</span></span>

 <span data-ttu-id="029c8-130">_pxRes_ (**xltypeStr** или **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="029c8-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="029c8-131">Возвращает имя, связанное с указанным определением.</span><span class="sxs-lookup"><span data-stu-id="029c8-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="029c8-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="029c8-132">Remarks</span></span>

<span data-ttu-id="029c8-133">Ниже перечислены четыре примеры значений, возвращаемых вызовом **xlfGetDef** с заданными параметрами.</span><span class="sxs-lookup"><span data-stu-id="029c8-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="029c8-134">**Имя, определенное в Excel**</span><span class="sxs-lookup"><span data-stu-id="029c8-134">**Name defined in Excel**</span></span>|<span data-ttu-id="029c8-135">**_pxDefText_**</span><span class="sxs-lookup"><span data-stu-id="029c8-135">**_pxDefText_**</span></span>|<span data-ttu-id="029c8-136">**_pxDocumentText_**</span><span class="sxs-lookup"><span data-stu-id="029c8-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="029c8-137">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="029c8-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="029c8-138">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="029c8-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="029c8-139">Указанный диапазон в Лист4 именем Sales.</span><span class="sxs-lookup"><span data-stu-id="029c8-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="029c8-140">«R2C2:R9C6»</span><span class="sxs-lookup"><span data-stu-id="029c8-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="029c8-141">«Лист4»</span><span class="sxs-lookup"><span data-stu-id="029c8-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="029c8-142">\<опускается, если\></span><span class="sxs-lookup"><span data-stu-id="029c8-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="029c8-143">«Продажи»</span><span class="sxs-lookup"><span data-stu-id="029c8-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="029c8-144">Значение 100 в Лист4 определяется как константа.</span><span class="sxs-lookup"><span data-stu-id="029c8-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="029c8-145">«100»</span><span class="sxs-lookup"><span data-stu-id="029c8-145">"100"</span></span>  <br/> |<span data-ttu-id="029c8-146">«Лист4»</span><span class="sxs-lookup"><span data-stu-id="029c8-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="029c8-147">\<опускается, если\></span><span class="sxs-lookup"><span data-stu-id="029c8-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="029c8-148">«Константу»</span><span class="sxs-lookup"><span data-stu-id="029c8-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="029c8-149">Указанную формулу в Лист4 называется SumTotal.</span><span class="sxs-lookup"><span data-stu-id="029c8-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="029c8-150">«SUM(R1C1:R10C1)»</span><span class="sxs-lookup"><span data-stu-id="029c8-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="029c8-151">«Лист4»</span><span class="sxs-lookup"><span data-stu-id="029c8-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="029c8-152">\<опускается, если\></span><span class="sxs-lookup"><span data-stu-id="029c8-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="029c8-153">«SumTotal»</span><span class="sxs-lookup"><span data-stu-id="029c8-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="029c8-154">3 — это скрытый имя счетчика на активном листе.</span><span class="sxs-lookup"><span data-stu-id="029c8-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="029c8-155">«3»</span><span class="sxs-lookup"><span data-stu-id="029c8-155">"3"</span></span>  <br/> |<span data-ttu-id="029c8-156">\<опускается, если\></span><span class="sxs-lookup"><span data-stu-id="029c8-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="029c8-157">2</span><span class="sxs-lookup"><span data-stu-id="029c8-157">2</span></span>  <br/> |<span data-ttu-id="029c8-158">«Счетчик»</span><span class="sxs-lookup"><span data-stu-id="029c8-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="029c8-159">См. также</span><span class="sxs-lookup"><span data-stu-id="029c8-159">See also</span></span>

- [<span data-ttu-id="029c8-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="029c8-160">xlfGetName</span></span>](xlfgetname.md)
- [<span data-ttu-id="029c8-161">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="029c8-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

