---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- кслфжетдеф
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310243"
---
# <a name="xlfgetdef"></a><span data-ttu-id="96ef1-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="96ef1-104">xlfGetDef</span></span>

<span data-ttu-id="96ef1-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="96ef1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="96ef1-106">Возвращает имя в виде текста, которое определено для определенной области, значения или формулы в книге.</span><span class="sxs-lookup"><span data-stu-id="96ef1-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="96ef1-107">В Excel это значение отображается в столбце **имя** диалогового окна **Диспетчер имен** , которое отображается при нажатии кнопки **Диспетчер имен** в разделе **определенные имена** на вкладке **формулы** . Используйте **кслфжетдеф** , чтобы получить имя, соответствующее определению.</span><span class="sxs-lookup"><span data-stu-id="96ef1-107">In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition.</span></span> <span data-ttu-id="96ef1-108">Чтобы получить определение имени, используйте [кслфжетнаме](xlfgetname.md).</span><span class="sxs-lookup"><span data-stu-id="96ef1-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="96ef1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="96ef1-109">Parameters</span></span>

<span data-ttu-id="96ef1-110">_пксдефтекст_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="96ef1-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="96ef1-111">Может быть любым, что можно определить имя для ссылки, включая ссылку, значение, объект или формулу.</span><span class="sxs-lookup"><span data-stu-id="96ef1-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="96ef1-112">Ссылки должны быть указаны в стиле R1C1, например `"R3C5"`.</span><span class="sxs-lookup"><span data-stu-id="96ef1-112">References must be given in R1C1 style, such as  `"R3C5"`.</span></span> <span data-ttu-id="96ef1-113">Если _пксдефтекст_ является значением или формулой, не нужно включать знак равенства, который отображается в столбце " **ссылки** " в диалоговом окне " **Диспетчер имен** ".</span><span class="sxs-lookup"><span data-stu-id="96ef1-113">If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box.</span></span> <span data-ttu-id="96ef1-114">Если для _пксдефтекст_существует несколько имен, **кслфжетдеф** возвращает первое имя.</span><span class="sxs-lookup"><span data-stu-id="96ef1-114">If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name.</span></span> <span data-ttu-id="96ef1-115">Если имя не соответствует _пксдефтекст_, **кслфжетдеф** возвращает значение `#NAME?` ошибки.</span><span class="sxs-lookup"><span data-stu-id="96ef1-115">If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="96ef1-116">_пксдокументтекст_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="96ef1-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="96ef1-117">Указывает лист, на котором находится _пксдефтекст_ .</span><span class="sxs-lookup"><span data-stu-id="96ef1-117">Specifies the sheet that  _pxDefText_ is on.</span></span> <span data-ttu-id="96ef1-118">Если _пксдокументтекст_ опущено, предполагается, что он является активным листом.</span><span class="sxs-lookup"><span data-stu-id="96ef1-118">If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="96ef1-119">_пкстипенум_ (**кслтипенум**)</span><span class="sxs-lookup"><span data-stu-id="96ef1-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="96ef1-120">Число от 1 до 3, указывающее, какие типы имен возвращаются.</span><span class="sxs-lookup"><span data-stu-id="96ef1-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="96ef1-121">**_Пкстипенум_**</span><span class="sxs-lookup"><span data-stu-id="96ef1-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="96ef1-122">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="96ef1-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="96ef1-123">1 или опущен</span><span class="sxs-lookup"><span data-stu-id="96ef1-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="96ef1-124">Только обычные имена.</span><span class="sxs-lookup"><span data-stu-id="96ef1-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="96ef1-125">2</span><span class="sxs-lookup"><span data-stu-id="96ef1-125">2</span></span>  <br/> |<span data-ttu-id="96ef1-126">Только скрытые имена.</span><span class="sxs-lookup"><span data-stu-id="96ef1-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="96ef1-127">4</span><span class="sxs-lookup"><span data-stu-id="96ef1-127">3</span></span>  <br/> |<span data-ttu-id="96ef1-128">Все имена.</span><span class="sxs-lookup"><span data-stu-id="96ef1-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="96ef1-129">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96ef1-129">Property value/Return value</span></span>

 <span data-ttu-id="96ef1-130">_пксрес_ (**кслтипестр** или **кслтипирр**)</span><span class="sxs-lookup"><span data-stu-id="96ef1-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="96ef1-131">Возвращает имя, связанное с указанным определением.</span><span class="sxs-lookup"><span data-stu-id="96ef1-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96ef1-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="96ef1-132">Remarks</span></span>

<span data-ttu-id="96ef1-133">В следующей таблице перечислены четыре примера значений, возвращаемых при вызове **кслфжетдеф** с указанными аргументами.</span><span class="sxs-lookup"><span data-stu-id="96ef1-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="96ef1-134">**Имя, определенное в Excel**</span><span class="sxs-lookup"><span data-stu-id="96ef1-134">**Name defined in Excel**</span></span>|<span data-ttu-id="96ef1-135">**_Пксдефтекст_**</span><span class="sxs-lookup"><span data-stu-id="96ef1-135">**_pxDefText_**</span></span>|<span data-ttu-id="96ef1-136">**_Пксдокументтекст_**</span><span class="sxs-lookup"><span data-stu-id="96ef1-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="96ef1-137">**_Пкстипенум_**</span><span class="sxs-lookup"><span data-stu-id="96ef1-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="96ef1-138">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="96ef1-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="96ef1-139">Указанный диапазон в Sheet4 называется Sales.</span><span class="sxs-lookup"><span data-stu-id="96ef1-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="96ef1-140">"R2C2: R9C6"</span><span class="sxs-lookup"><span data-stu-id="96ef1-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="96ef1-141">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="96ef1-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="96ef1-142">\<опущен\></span><span class="sxs-lookup"><span data-stu-id="96ef1-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="96ef1-143">Продаже</span><span class="sxs-lookup"><span data-stu-id="96ef1-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="96ef1-144">Значение 100 в Sheet4 определено как константа.</span><span class="sxs-lookup"><span data-stu-id="96ef1-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="96ef1-145">"100"</span><span class="sxs-lookup"><span data-stu-id="96ef1-145">"100"</span></span>  <br/> |<span data-ttu-id="96ef1-146">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="96ef1-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="96ef1-147">\<опущен\></span><span class="sxs-lookup"><span data-stu-id="96ef1-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="96ef1-148">Измен</span><span class="sxs-lookup"><span data-stu-id="96ef1-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="96ef1-149">Указанная формула в Sheet4 называется Сумтотал.</span><span class="sxs-lookup"><span data-stu-id="96ef1-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="96ef1-150">"SUM (R1C1: R10C1)"</span><span class="sxs-lookup"><span data-stu-id="96ef1-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="96ef1-151">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="96ef1-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="96ef1-152">\<опущен\></span><span class="sxs-lookup"><span data-stu-id="96ef1-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="96ef1-153">"Сумтотал"</span><span class="sxs-lookup"><span data-stu-id="96ef1-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="96ef1-154">3 определен в качестве счетчика скрытого имени на активном листе.</span><span class="sxs-lookup"><span data-stu-id="96ef1-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="96ef1-155">4</span><span class="sxs-lookup"><span data-stu-id="96ef1-155">"3"</span></span>  <br/> |<span data-ttu-id="96ef1-156">\<опущен\></span><span class="sxs-lookup"><span data-stu-id="96ef1-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="96ef1-157">2</span><span class="sxs-lookup"><span data-stu-id="96ef1-157">2</span></span>  <br/> |<span data-ttu-id="96ef1-158">Счетчик</span><span class="sxs-lookup"><span data-stu-id="96ef1-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96ef1-159">См. также</span><span class="sxs-lookup"><span data-stu-id="96ef1-159">See also</span></span>

- [<span data-ttu-id="96ef1-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="96ef1-160">xlfGetName</span></span>](xlfgetname.md)
- [<span data-ttu-id="96ef1-161">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="96ef1-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

