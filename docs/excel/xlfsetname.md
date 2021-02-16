---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- Функция xlfsetname [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404262"
---
# <a name="xlfsetname"></a><span data-ttu-id="86dd4-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="86dd4-104">xlfSetName</span></span>

<span data-ttu-id="86dd4-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="86dd4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="86dd4-106">Используется для создания и удаления определенных имен, связанных с DLL.</span><span class="sxs-lookup"><span data-stu-id="86dd4-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="86dd4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="86dd4-107">Parameters</span></span>

<span data-ttu-id="86dd4-108">_pxNameText_ (**xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="86dd4-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="86dd4-109">Имя диапазона, которое должно соответствовать обычным ограничениям в Microsoft Excel для допустимого имени.</span><span class="sxs-lookup"><span data-stu-id="86dd4-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="86dd4-110">_pxNameDefinition_ (**xltypeStr,** **xltypeNum,** **xltypeBool,** **xltypeErr,** **xltypeMulti,** **xltypeSRef,** **xltypeRef** или **xltypeInt)**</span><span class="sxs-lookup"><span data-stu-id="86dd4-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="86dd4-111">(Необязательно).</span><span class="sxs-lookup"><span data-stu-id="86dd4-111">(Optional).</span></span> <span data-ttu-id="86dd4-112">Значение, набор значений, ячейка или диапазон ячеек, как определено _в pxNameText._</span><span class="sxs-lookup"><span data-stu-id="86dd4-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="86dd4-113">Если опущен, имя удаляется.</span><span class="sxs-lookup"><span data-stu-id="86dd4-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="86dd4-114">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86dd4-114">Property value/Return value</span></span>

<span data-ttu-id="86dd4-115">_pxRes_ (**xltypeBool** или **xltypeErr)**</span><span class="sxs-lookup"><span data-stu-id="86dd4-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="86dd4-116">ИМЕЕТ true, если операция была успешной, или FALSE, если имя не удалось создать или удалить.</span><span class="sxs-lookup"><span data-stu-id="86dd4-116">TRUE if the operation succeeded or FALSE if the name could not be created or deleted.</span></span> <span data-ttu-id="86dd4-117">Возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="86dd4-117">Returns #VALUE!</span></span> <span data-ttu-id="86dd4-118">если один или несколько аргументов недействительны.</span><span class="sxs-lookup"><span data-stu-id="86dd4-118">if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86dd4-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="86dd4-119">Remarks</span></span>

<span data-ttu-id="86dd4-120">При регистрации функции или команды с помощью **xlfRegister** с допустимым аргументом  _pxFunctionText_ Excel создает имя, связанное с ресурсом DLL.</span><span class="sxs-lookup"><span data-stu-id="86dd4-120">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource.</span></span> <span data-ttu-id="86dd4-121">При выгрузке DLL такие имена следует удалять с помощью функции [xlfSetName.](xlfsetname.md)</span><span class="sxs-lookup"><span data-stu-id="86dd4-121">When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="86dd4-122">Однако из-за известной проблемы в Excel операция удаления не удаться.</span><span class="sxs-lookup"><span data-stu-id="86dd4-122">However, due to a known issue in Excel, this deletion operation fails.</span></span> <span data-ttu-id="86dd4-123">Дополнительные сведения см. в статье [Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="86dd4-123">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="86dd4-124">Пример</span><span class="sxs-lookup"><span data-stu-id="86dd4-124">Example</span></span>

<span data-ttu-id="86dd4-125">См. код функции **xlAutoClose** в  `\SAMPLES\GENERIC\GENERIC.C` .</span><span class="sxs-lookup"><span data-stu-id="86dd4-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86dd4-126">См. также</span><span class="sxs-lookup"><span data-stu-id="86dd4-126">See also</span></span>

- [<span data-ttu-id="86dd4-127">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="86dd4-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

