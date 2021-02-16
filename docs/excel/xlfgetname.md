---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
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
# <a name="xlfgetname"></a><span data-ttu-id="279c8-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="279c8-104">xlfGetName</span></span>

<span data-ttu-id="279c8-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="279c8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="279c8-106">Возвращает определение имени, отображаемого в столбце **"Ссылается** на" диалогового окна "Диспетчер имен", которое отображается при нажатии кнопки "Диспетчер имен" в разделе "Определенные имена" на вкладке    **"Формулы".** Если определение содержит ссылки, они даются в качестве ссылок в стиле R1C1.</span><span class="sxs-lookup"><span data-stu-id="279c8-106">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references.</span></span> <span data-ttu-id="279c8-107">Используйте **xlfGetName** для проверки значения, определяемого именем.</span><span class="sxs-lookup"><span data-stu-id="279c8-107">Use **xlfGetName** to check the value defined by a name.</span></span> <span data-ttu-id="279c8-108">Чтобы получить имя, соответствующее определению, используйте [xlfGetDef.](xlfgetdef.md)</span><span class="sxs-lookup"><span data-stu-id="279c8-108">To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="279c8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="279c8-109">Parameters</span></span>

<span data-ttu-id="279c8-110">_pxNameText_ (**xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="279c8-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="279c8-111">Может быть именем, определенным на листе; внешняя ссылка на имя, определенное в активной книге, например; или внешняя ссылка на имя, определенное в конкретной открытой  `"!Sales"` книге, например  `"[Book1]SHEET1!Sales"` .</span><span class="sxs-lookup"><span data-stu-id="279c8-111">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.</span></span>  <span data-ttu-id="279c8-112">_pxNameText_ также может быть скрытым именем.</span><span class="sxs-lookup"><span data-stu-id="279c8-112">_pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="279c8-113">_pxInfoType_ (**xltypeBool)**</span><span class="sxs-lookup"><span data-stu-id="279c8-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="279c8-114">Указывает тип возвращаемой информации об имени.</span><span class="sxs-lookup"><span data-stu-id="279c8-114">Specifies the type of information to return about the name.</span></span> <span data-ttu-id="279c8-115">Если **false** или опущен, возвращается определение.</span><span class="sxs-lookup"><span data-stu-id="279c8-115">If **FALSE** or omitted, the definition is returned.</span></span> <span data-ttu-id="279c8-116">Если **установлено** true, **возвращается true,** если имя определено только для листа, **FALSE,** если имя определено для всей книги.</span><span class="sxs-lookup"><span data-stu-id="279c8-116">If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="279c8-117">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="279c8-117">Property value/Return value</span></span>

<span data-ttu-id="279c8-118">_pxRes_ (**xltypeStr,** **xltypeBool** или **xltypeErr)**</span><span class="sxs-lookup"><span data-stu-id="279c8-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="279c8-119">В зависимости от значения, переданного для _pxInfoType,_ возвращает определение указанного имени **(xltypeStr)** или **TRUE** или **FALSE** (**xltypeBool).**</span><span class="sxs-lookup"><span data-stu-id="279c8-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="279c8-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="279c8-120">Remarks</span></span>

<span data-ttu-id="279c8-121">Если  в диалоговом окне "Защищенный лист" установлено  значение "Защитить лист" и содержимое заблокированных ячеек для защиты книги, содержащей имя, **xlfGetName** возвращает значение `#N/A` ошибки.</span><span class="sxs-lookup"><span data-stu-id="279c8-121">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value.</span></span> <span data-ttu-id="279c8-122">Чтобы просмотреть **диалоговое** окно "Защищенный лист", щелкните **"Защитить** лист" в разделе **"Изменения"** на вкладке **"Проверка".**</span><span class="sxs-lookup"><span data-stu-id="279c8-122">To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="279c8-123">В следующей таблице перечислены три примера значений, возвращаемого вызовом **xlfGetDef** с указанным _аргументом pxNameText._</span><span class="sxs-lookup"><span data-stu-id="279c8-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="279c8-124">**Определение в Excel**</span><span class="sxs-lookup"><span data-stu-id="279c8-124">**Definition in Excel**</span></span>|<span data-ttu-id="279c8-125">**_pxNameText_**</span><span class="sxs-lookup"><span data-stu-id="279c8-125">**_pxNameText_**</span></span>|<span data-ttu-id="279c8-126">**Возвращаемая величина**</span><span class="sxs-lookup"><span data-stu-id="279c8-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="279c8-127">Имя "Продажи" на листе определяется как число 523.</span><span class="sxs-lookup"><span data-stu-id="279c8-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="279c8-128">"Sales" (Продажи)</span><span class="sxs-lookup"><span data-stu-id="279c8-128">"Sales"</span></span>  <br/> |<span data-ttu-id="279c8-129">"=523"</span><span class="sxs-lookup"><span data-stu-id="279c8-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="279c8-130">Имя "Прибыль" на активном листе определяется как формула =Sales-Costs.</span><span class="sxs-lookup"><span data-stu-id="279c8-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="279c8-131">"! Прибыль"</span><span class="sxs-lookup"><span data-stu-id="279c8-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="279c8-132">"=Sales-Costs"</span><span class="sxs-lookup"><span data-stu-id="279c8-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="279c8-133">Имя базы данных на активном листе определяется как диапазон A1:F500.</span><span class="sxs-lookup"><span data-stu-id="279c8-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="279c8-134">"! База данных"</span><span class="sxs-lookup"><span data-stu-id="279c8-134">"!Database"</span></span>  <br/> |<span data-ttu-id="279c8-135">"=R1C1:R500C6"</span><span class="sxs-lookup"><span data-stu-id="279c8-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="279c8-136">См. также</span><span class="sxs-lookup"><span data-stu-id="279c8-136">See also</span></span>

- [<span data-ttu-id="279c8-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="279c8-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="279c8-138">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="279c8-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

