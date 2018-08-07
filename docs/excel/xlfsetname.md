---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- функция xlfSetName [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807349"
---
# <a name="xlfsetname"></a><span data-ttu-id="38a82-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="38a82-104">xlfSetName</span></span>

<span data-ttu-id="38a82-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="38a82-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="38a82-106">Используется для создания и удаления определенных имен, связанные с DLL.</span><span class="sxs-lookup"><span data-stu-id="38a82-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="38a82-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="38a82-107">Parameters</span></span>

<span data-ttu-id="38a82-108">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="38a82-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="38a82-109">Имя диапазона, который должен соответствовать типу обычным ограничения в Microsoft Excel в допустимых имен.</span><span class="sxs-lookup"><span data-stu-id="38a82-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="38a82-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**или **xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="38a82-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="38a82-111">(Необязательно).</span><span class="sxs-lookup"><span data-stu-id="38a82-111">(Optional).</span></span> <span data-ttu-id="38a82-112">Значение, набор значений, ячейки или диапазона ячеек этой _pxNameText_ определяется как.</span><span class="sxs-lookup"><span data-stu-id="38a82-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="38a82-113">Если этот параметр опущен, имя будет удален.</span><span class="sxs-lookup"><span data-stu-id="38a82-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="38a82-114">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38a82-114">Property value/Return value</span></span>

<span data-ttu-id="38a82-115">_pxRes_ (**xltypeBool** или **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="38a82-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="38a82-116">Значение TRUE, если операция выполнена успешно, или значение FALSE, если имя не может быть создан или удален.</span><span class="sxs-lookup"><span data-stu-id="38a82-116">TRUE if the operation succeeded or FALSE if the name could not be created or deleted.</span></span> <span data-ttu-id="38a82-117">Возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="38a82-117">Returns #VALUE!</span></span> <span data-ttu-id="38a82-118">Если один или несколько аргументов недопустима.</span><span class="sxs-lookup"><span data-stu-id="38a82-118">if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38a82-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="38a82-119">Remarks</span></span>

<span data-ttu-id="38a82-120">При команду или функция регистрируется с помощью **xlfRegister** с аргументом допустимый _pxFunctionText_ , Excel создает имя, связанное с DLL-Библиотеку ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38a82-120">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource.</span></span> <span data-ttu-id="38a82-121">После выгрузки библиотеки DLL, такие имена следует удалить с помощью [функции xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="38a82-121">When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="38a82-122">Тем не менее из-за известная проблема в Excel, эта операция удаления не удается выполнить.</span><span class="sxs-lookup"><span data-stu-id="38a82-122">However, due to a known issue in Excel, this deletion operation fails.</span></span> <span data-ttu-id="38a82-123">Для получения дополнительных сведений см [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="38a82-123">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="38a82-124">Пример</span><span class="sxs-lookup"><span data-stu-id="38a82-124">Example</span></span>

<span data-ttu-id="38a82-125">Просмотр кода для функции **xlAutoClose** в `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="38a82-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="38a82-126">См. также</span><span class="sxs-lookup"><span data-stu-id="38a82-126">See also</span></span>

- [<span data-ttu-id="38a82-127">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="38a82-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

