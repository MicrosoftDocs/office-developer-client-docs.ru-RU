---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- функция xlfCaller [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807346"
---
# <a name="xlfcaller"></a><span data-ttu-id="7aa03-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="7aa03-104">xlfCaller</span></span>

 <span data-ttu-id="7aa03-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7aa03-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7aa03-106">Возвращает сведения о ячейку, диапазон ячеек, команда меню, средство на панели инструментов или объекта, который вызвал команду DLL или функции, которые в настоящее время работает.</span><span class="sxs-lookup"><span data-stu-id="7aa03-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="7aa03-107">**Вызывается из кода**</span><span class="sxs-lookup"><span data-stu-id="7aa03-107">**Code called from**</span></span>|<span data-ttu-id="7aa03-108">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="7aa03-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7aa03-109">БИБЛИОТЕКИ DLL</span><span class="sxs-lookup"><span data-stu-id="7aa03-109">DLL</span></span>  <br/> |<span data-ttu-id="7aa03-110">Идентификатор регистрации.</span><span class="sxs-lookup"><span data-stu-id="7aa03-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="7aa03-111">Одна ячейка</span><span class="sxs-lookup"><span data-stu-id="7aa03-111">A single cell</span></span>  <br/> |<span data-ttu-id="7aa03-112">Ссылка из одной ячейки.</span><span class="sxs-lookup"><span data-stu-id="7aa03-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="7aa03-113">Формулы массивов с несколькими ячейками</span><span class="sxs-lookup"><span data-stu-id="7aa03-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="7aa03-114">Ссылка на ячейку несколькими.</span><span class="sxs-lookup"><span data-stu-id="7aa03-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="7aa03-115">Выражение условного форматирования</span><span class="sxs-lookup"><span data-stu-id="7aa03-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="7aa03-116">Ссылка на ячейку, к которому применяется условие форматирования.</span><span class="sxs-lookup"><span data-stu-id="7aa03-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="7aa03-117">Меню</span><span class="sxs-lookup"><span data-stu-id="7aa03-117">A menu</span></span>  <br/> | <span data-ttu-id="7aa03-118">Массив одной строки четырех элементов:</span><span class="sxs-lookup"><span data-stu-id="7aa03-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="7aa03-119">Идентификатор панели.</span><span class="sxs-lookup"><span data-stu-id="7aa03-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="7aa03-120">Положение меню.</span><span class="sxs-lookup"><span data-stu-id="7aa03-120">The menu position.</span></span>  <br/>  <span data-ttu-id="7aa03-121">Положение подменю.</span><span class="sxs-lookup"><span data-stu-id="7aa03-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="7aa03-122">Положение команды.</span><span class="sxs-lookup"><span data-stu-id="7aa03-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="7aa03-123">Панель инструментов</span><span class="sxs-lookup"><span data-stu-id="7aa03-123">A toolbar</span></span>  <br/> | <span data-ttu-id="7aa03-124">Массив одной строки из двух элементов:</span><span class="sxs-lookup"><span data-stu-id="7aa03-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="7aa03-125">Номер панели инструментов встроенные панели инструментов или имя панели инструментов для пользовательских панелей инструментов.</span><span class="sxs-lookup"><span data-stu-id="7aa03-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="7aa03-126">Положение на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="7aa03-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="7aa03-127">Графический объект</span><span class="sxs-lookup"><span data-stu-id="7aa03-127">A graphic object</span></span>  <br/> |<span data-ttu-id="7aa03-128">Идентификатор объекта (имя объекта).</span><span class="sxs-lookup"><span data-stu-id="7aa03-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="7aa03-129">Команда, связанная с xlcOnEnter на. ВВЕСТИ, выполнилось событий</span><span class="sxs-lookup"><span data-stu-id="7aa03-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="7aa03-130">Ссылка на одну или несколько ячеек, вводимые.</span><span class="sxs-lookup"><span data-stu-id="7aa03-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="7aa03-131">Команда, связанная с xlcOnDoubleclick на. DOUBLECLICK выполнилось события.</span><span class="sxs-lookup"><span data-stu-id="7aa03-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="7aa03-132">Ячейки, которая была двойном щелчке (не обязательно содержит активную ячейку).</span><span class="sxs-lookup"><span data-stu-id="7aa03-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="7aa03-133">Макрос Авто_открыть, AutoClose, Auto_Activate или Auto_Deactivate</span><span class="sxs-lookup"><span data-stu-id="7aa03-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="7aa03-134">Имя вызывающего листа.</span><span class="sxs-lookup"><span data-stu-id="7aa03-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="7aa03-135">Другие методы, отсутствует в списке</span><span class="sxs-lookup"><span data-stu-id="7aa03-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="7aa03-136">#REF!</span><span class="sxs-lookup"><span data-stu-id="7aa03-136">#REF!</span></span> <span data-ttu-id="7aa03-137">Ошибка</span><span class="sxs-lookup"><span data-stu-id="7aa03-137">Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="7aa03-138">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7aa03-138">Property value/Return value</span></span>

<span data-ttu-id="7aa03-139">Возвращаемое значение — это один из следующих **XLOPER**/ **XLOPER12** типы данных: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**или **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="7aa03-139">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**.</span></span> <span data-ttu-id="7aa03-140">Так как три из следующих типов пункты выделенной памяти, возвращаемое значение **xlfCaller** нужно всегда освободить в вызове [функции xlFree](xlfree.md) при больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="7aa03-140">Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="7aa03-141">Дополнительные сведения о **XLOPERs**/ **XLOPER12s** увидеть [Управление памятью в Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="7aa03-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7aa03-142">Замечания</span><span class="sxs-lookup"><span data-stu-id="7aa03-142">Remarks</span></span>

<span data-ttu-id="7aa03-143">Эта функция — это функция только листа, который можно вызывать из DLL или XLL функции рабочего листа.</span><span class="sxs-lookup"><span data-stu-id="7aa03-143">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function.</span></span> <span data-ttu-id="7aa03-144">Другие сведения о функции XLM могут вызываться только из команды или иметь эквивалентные права лист макросов функции.</span><span class="sxs-lookup"><span data-stu-id="7aa03-144">Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="7aa03-145">Пример</span><span class="sxs-lookup"><span data-stu-id="7aa03-145">Example</span></span>

 <span data-ttu-id="7aa03-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="7aa03-146"></span></span> <span data-ttu-id="7aa03-147">Эта функция вызывает команду макросов (xlcSelect) и будет работать только в том случае, когда вызов выполняется из листа макросов.</span><span class="sxs-lookup"><span data-stu-id="7aa03-147">This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="7aa03-148">См. также</span><span class="sxs-lookup"><span data-stu-id="7aa03-148">See also</span></span>



[<span data-ttu-id="7aa03-149">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="7aa03-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

