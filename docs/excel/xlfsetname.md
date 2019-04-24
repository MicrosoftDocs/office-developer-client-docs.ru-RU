---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- Функция xlfSetName [Excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310278"
---
# <a name="xlfsetname"></a><span data-ttu-id="d0906-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="d0906-104">xlfSetName</span></span>

<span data-ttu-id="d0906-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d0906-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d0906-106">Используется для создания и удаления определенных имен, связанных с БИБЛИОТЕКой DLL.</span><span class="sxs-lookup"><span data-stu-id="d0906-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="d0906-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0906-107">Parameters</span></span>

<span data-ttu-id="d0906-108">_пкснаметекст_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="d0906-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="d0906-109">Имя диапазона, которое должно соответствовать обычным ограничениям в Microsoft Excel по действительным именам.</span><span class="sxs-lookup"><span data-stu-id="d0906-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="d0906-110">_пкснамедефинитион_ (**кслтипестр**, **кслтипенум**, **кслтипебул**, **кслтипирр**, **xltypeMulti**, **кслтипесреф**, **кслтипереф**или **кслтипеинт**)</span><span class="sxs-lookup"><span data-stu-id="d0906-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="d0906-111">(НеОбязательно).</span><span class="sxs-lookup"><span data-stu-id="d0906-111">(Optional).</span></span> <span data-ttu-id="d0906-112">Значение, набор значений, ячейка или диапазон ячеек, которые _пкснаметекст_ задают как.</span><span class="sxs-lookup"><span data-stu-id="d0906-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="d0906-113">Если этот параметр не задан, имя удаляется.</span><span class="sxs-lookup"><span data-stu-id="d0906-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d0906-114">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0906-114">Property value/Return value</span></span>

<span data-ttu-id="d0906-115">_пксрес_ (**кслтипебул** или **кслтипирр**)</span><span class="sxs-lookup"><span data-stu-id="d0906-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="d0906-116">ЗНАЧЕНИЕ TRUE, если операция завершилась успешно, или значение FALSE, если имя не удалось создать или удалить.</span><span class="sxs-lookup"><span data-stu-id="d0906-116">TRUE if the operation succeeded or FALSE if the name could not be created or deleted.</span></span> <span data-ttu-id="d0906-117">Возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="d0906-117">Returns #VALUE!</span></span> <span data-ttu-id="d0906-118">Если один или несколько аргументов являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="d0906-118">if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0906-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="d0906-119">Remarks</span></span>

<span data-ttu-id="d0906-120">Если функция или команда зарегистрирована с помощью **xlfRegister** с допустимым аргументом _пксфунктионтекст_ , Excel создает имя, связанНОЕ с ресурсом DLL.</span><span class="sxs-lookup"><span data-stu-id="d0906-120">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource.</span></span> <span data-ttu-id="d0906-121">При выгрузке библиотеки DLL такие имена необходимо удалить с помощью [функции xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="d0906-121">When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="d0906-122">Однако из-за известной проблемы в Excel эта операция удаления завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d0906-122">However, due to a known issue in Excel, this deletion operation fails.</span></span> <span data-ttu-id="d0906-123">Дополнительные сведения см. в статье [Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="d0906-123">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="d0906-124">Пример</span><span class="sxs-lookup"><span data-stu-id="d0906-124">Example</span></span>

<span data-ttu-id="d0906-125">Обратитесь к коду функции **xlAutoClose** в `\SAMPLES\GENERIC\GENERIC.C`файле.</span><span class="sxs-lookup"><span data-stu-id="d0906-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0906-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d0906-126">See also</span></span>

- [<span data-ttu-id="d0906-127">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="d0906-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

