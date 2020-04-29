---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- кслфжетнаме
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436631"
---
# <a name="xlfgetname"></a><span data-ttu-id="b2ccf-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="b2ccf-104">xlfGetName</span></span>

<span data-ttu-id="b2ccf-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b2ccf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b2ccf-106">Возвращает определение имени, которое отображается в столбце " **ссылки** " в диалоговом окне " **Диспетчер имен** ", которое отображается при нажатии кнопки **Диспетчер имен** в разделе **определенные имена** на вкладке **формулы** . Если определение содержит ссылки, им присваиваются ссылки в стиле R1C1.</span><span class="sxs-lookup"><span data-stu-id="b2ccf-106">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references.</span></span> <span data-ttu-id="b2ccf-107">Используйте **кслфжетнаме** , чтобы проверить значение, заданное именем.</span><span class="sxs-lookup"><span data-stu-id="b2ccf-107">Use **xlfGetName** to check the value defined by a name.</span></span> <span data-ttu-id="b2ccf-108">Чтобы получить имя, соответствующее определению, используйте [кслфжетдеф](xlfgetdef.md).</span><span class="sxs-lookup"><span data-stu-id="b2ccf-108">To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="b2ccf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2ccf-109">Parameters</span></span>

<span data-ttu-id="b2ccf-110">_пкснаметекст_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="b2ccf-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="b2ccf-111">Может быть именем, определенным на листе; Внешняя ссылка на имя, заданное для активной книги, например, `"!Sales"`; или внешнюю ссылку на имя, определенное в конкретной открытой книге, например: `"[Book1]SHEET1!Sales"`.</span><span class="sxs-lookup"><span data-stu-id="b2ccf-111">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.</span></span>  <span data-ttu-id="b2ccf-112">_пкснаметекст_ также может быть скрытым именем.</span><span class="sxs-lookup"><span data-stu-id="b2ccf-112">_pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="b2ccf-113">_пксинфотипе_ (**кслтипебул**)</span><span class="sxs-lookup"><span data-stu-id="b2ccf-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="b2ccf-114">Указывает тип возвращаемых сведений об имени.</span><span class="sxs-lookup"><span data-stu-id="b2ccf-114">Specifies the type of information to return about the name.</span></span> <span data-ttu-id="b2ccf-115">Если этот параметр **имеет значение false** или опущен, определение будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="b2ccf-115">If **FALSE** or omitted, the definition is returned.</span></span> <span data-ttu-id="b2ccf-116">Если этот параметр **имеет значение true**, возвращает **значение true** , если имя определено только для листа, **значение false** , если имя определено для всей книги.</span><span class="sxs-lookup"><span data-stu-id="b2ccf-116">If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b2ccf-117">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2ccf-117">Property value/Return value</span></span>

<span data-ttu-id="b2ccf-118">_пксрес_ (**кслтипестр**, **кслтипебул**или **кслтипирр**)</span><span class="sxs-lookup"><span data-stu-id="b2ccf-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="b2ccf-119">В зависимости от значения, переданного для _пксинфотипе_, возвращает определение указанного имени (**Кслтипестр**) или **true** или **false** (**кслтипебул**).</span><span class="sxs-lookup"><span data-stu-id="b2ccf-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b2ccf-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="b2ccf-120">Remarks</span></span>

<span data-ttu-id="b2ccf-121">Если установлен флажок **защитить лист и содержимое заблокированных ячеек** в диалоговом окне **Защита листа** для защиты книги, содержащей имя, **кслфжетнаме** возвращает значение `#N/A` ошибки.</span><span class="sxs-lookup"><span data-stu-id="b2ccf-121">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value.</span></span> <span data-ttu-id="b2ccf-122">Чтобы увидеть диалоговое окно **Защита листа** , щелкните **защитить лист** в разделе **изменения** вкладки **Рецензирование** .</span><span class="sxs-lookup"><span data-stu-id="b2ccf-122">To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="b2ccf-123">В следующей таблице перечислены три примера значений, возвращаемых при вызове **кслфжетдеф** с указанным аргументом _пкснаметекст_ .</span><span class="sxs-lookup"><span data-stu-id="b2ccf-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="b2ccf-124">**Определение в Excel**</span><span class="sxs-lookup"><span data-stu-id="b2ccf-124">**Definition in Excel**</span></span>|<span data-ttu-id="b2ccf-125">**_пкснаметекст_**</span><span class="sxs-lookup"><span data-stu-id="b2ccf-125">**_pxNameText_**</span></span>|<span data-ttu-id="b2ccf-126">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="b2ccf-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2ccf-127">Имя Sales на листе определяется как число 523.</span><span class="sxs-lookup"><span data-stu-id="b2ccf-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="b2ccf-128">Продаже</span><span class="sxs-lookup"><span data-stu-id="b2ccf-128">"Sales"</span></span>  <br/> |<span data-ttu-id="b2ccf-129">"= 523"</span><span class="sxs-lookup"><span data-stu-id="b2ccf-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="b2ccf-130">Прибыль по названию на активном листе определяется как формула = Sales-затраты.</span><span class="sxs-lookup"><span data-stu-id="b2ccf-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="b2ccf-131">"! Отчете</span><span class="sxs-lookup"><span data-stu-id="b2ccf-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="b2ccf-132">"= Sales — затраты"</span><span class="sxs-lookup"><span data-stu-id="b2ccf-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="b2ccf-133">База данных имен на активном листе определяется как диапазон a1: F500.</span><span class="sxs-lookup"><span data-stu-id="b2ccf-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="b2ccf-134">"! Базу</span><span class="sxs-lookup"><span data-stu-id="b2ccf-134">"!Database"</span></span>  <br/> |<span data-ttu-id="b2ccf-135">"= R1C1: R500C6"</span><span class="sxs-lookup"><span data-stu-id="b2ccf-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2ccf-136">См. также</span><span class="sxs-lookup"><span data-stu-id="b2ccf-136">See also</span></span>

- [<span data-ttu-id="b2ccf-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="b2ccf-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="b2ccf-138">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="b2ccf-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

