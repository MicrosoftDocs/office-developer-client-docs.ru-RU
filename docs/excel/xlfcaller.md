---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- функция xlfCaller [Excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405732"
---
# <a name="xlfcaller"></a><span data-ttu-id="6dbe2-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="6dbe2-104">xlfCaller</span></span>

 <span data-ttu-id="6dbe2-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6dbe2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6dbe2-106">Возвращает сведения о ячейке, диапазоне ячеек, команде меню, инструменте на панели инструментов или объекте, вызвавшем команду или функцию DLL, которая выполняется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="6dbe2-107">**Код, вызываемый из**</span><span class="sxs-lookup"><span data-stu-id="6dbe2-107">**Code called from**</span></span>|<span data-ttu-id="6dbe2-108">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="6dbe2-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6dbe2-109">ФАЙЛ</span><span class="sxs-lookup"><span data-stu-id="6dbe2-109">DLL</span></span>  <br/> |<span data-ttu-id="6dbe2-110">Идентификатор регистра.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="6dbe2-111">Одна ячейка</span><span class="sxs-lookup"><span data-stu-id="6dbe2-111">A single cell</span></span>  <br/> |<span data-ttu-id="6dbe2-112">Ссылка на одну ячейку.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="6dbe2-113">Формула массива с несколькими ячейками</span><span class="sxs-lookup"><span data-stu-id="6dbe2-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="6dbe2-114">Ссылка на несколько ячеек.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="6dbe2-115">Выражение условного форматирования</span><span class="sxs-lookup"><span data-stu-id="6dbe2-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="6dbe2-116">Ссылка на ячейку, к которой применяется условие форматирования.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="6dbe2-117">Меню</span><span class="sxs-lookup"><span data-stu-id="6dbe2-117">A menu</span></span>  <br/> | <span data-ttu-id="6dbe2-118">Однострочный массив из четырех элементов:</span><span class="sxs-lookup"><span data-stu-id="6dbe2-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="6dbe2-119">Идентификатор столбца.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="6dbe2-120">Положение меню.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-120">The menu position.</span></span>  <br/>  <span data-ttu-id="6dbe2-121">Положение вложенного меню.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="6dbe2-122">Положение команды.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="6dbe2-123">Панель инструментов</span><span class="sxs-lookup"><span data-stu-id="6dbe2-123">A toolbar</span></span>  <br/> | <span data-ttu-id="6dbe2-124">Однострочный массив из двух элементов:</span><span class="sxs-lookup"><span data-stu-id="6dbe2-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="6dbe2-125">Номер панели инструментов для встроенных панелей инструментов или имя панели инструментов для настраиваемых панелей инструментов.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="6dbe2-126">Положение на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="6dbe2-127">Графический объект</span><span class="sxs-lookup"><span data-stu-id="6dbe2-127">A graphic object</span></span>  <br/> |<span data-ttu-id="6dbe2-128">Идентификатор объекта (имя объекта).</span><span class="sxs-lookup"><span data-stu-id="6dbe2-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="6dbe2-129">Команда, связанная с параметром Кслконентер, ON. Ввод, ловушка события</span><span class="sxs-lookup"><span data-stu-id="6dbe2-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="6dbe2-130">Ссылка на вводимую ячейку или ячейки.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="6dbe2-131">Команда, связанная с параметром Кслкондаублекликк, ON. DOUBLECLICK, ловушка события.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="6dbe2-132">Ячейка, которая была двойным щелчком (не обязательно является активной ячейкой).</span><span class="sxs-lookup"><span data-stu-id="6dbe2-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="6dbe2-133">Auto_Open, Автозакрытие, Auto_Activate или Auto_Deactivate макрос</span><span class="sxs-lookup"><span data-stu-id="6dbe2-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="6dbe2-134">Имя телефонной ведомости.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="6dbe2-135">Другие методы, не указанные в списке</span><span class="sxs-lookup"><span data-stu-id="6dbe2-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="6dbe2-136">#ССЫЛКА!</span><span class="sxs-lookup"><span data-stu-id="6dbe2-136">#REF!</span></span> <span data-ttu-id="6dbe2-137">Ошибка</span><span class="sxs-lookup"><span data-stu-id="6dbe2-137">Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="6dbe2-138">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6dbe2-138">Property value/Return value</span></span>

<span data-ttu-id="6dbe2-139">Возвращаемое значение — один из следующих типов данных **XLOPER**/ **XLOPER12** : **кслтипереф**, **кслтипесреф**, **кслтипенум**, **кслтипестр**, **кслтипирр**или **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-139">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**.</span></span> <span data-ttu-id="6dbe2-140">Так как три этих типа наделяются на выделенную память, возвращаемое значение **xlfCaller** всегда должно освобождаться в вызове [функции кслфри](xlfree.md) , когда он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-140">Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="6dbe2-141">Для получения дополнительных сведений о параметрах **XLOPER**/ **XLOPER12s** см [в Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="6dbe2-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6dbe2-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="6dbe2-142">Remarks</span></span>

<span data-ttu-id="6dbe2-143">Эта функция является единственной функцией, не являющейся функцией, которая может вызываться из функции листа DLL/XLL.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-143">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function.</span></span> <span data-ttu-id="6dbe2-144">Другие функции данных XLM могут вызываться только из команд или эквивалентных функций листа макросов.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-144">Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="6dbe2-145">Пример</span><span class="sxs-lookup"><span data-stu-id="6dbe2-145">Example</span></span>

 <span data-ttu-id="6dbe2-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="6dbe2-147">Эта функция вызывает макрос Command (Кслкселект) и будет работать правильно только при вызове из листа макросов.</span><span class="sxs-lookup"><span data-stu-id="6dbe2-147">This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="6dbe2-148">См. также</span><span class="sxs-lookup"><span data-stu-id="6dbe2-148">See also</span></span>



[<span data-ttu-id="6dbe2-149">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="6dbe2-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

