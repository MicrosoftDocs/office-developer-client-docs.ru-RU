---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- функция xlset [Excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404605"
---
# <a name="xlset"></a><span data-ttu-id="03861-104">xlSet</span><span class="sxs-lookup"><span data-stu-id="03861-104">xlSet</span></span>

<span data-ttu-id="03861-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="03861-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="03861-106">Очень быстро помещает постоянные значения в ячейки или диапазоны.</span><span class="sxs-lookup"><span data-stu-id="03861-106">Puts constant values into cells or ranges very quickly.</span></span> <span data-ttu-id="03861-107">Дополнительные сведения см. в книге "xlSet и книги с формулами массива" в [журнале Known Issues in Excel XLL Development.](known-issues-in-excel-xll-development.md)</span><span class="sxs-lookup"><span data-stu-id="03861-107">For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="03861-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="03861-108">Parameters</span></span>

<span data-ttu-id="03861-109">_pxReference_ **(xltypeRef** или **xltypeSRef)**</span><span class="sxs-lookup"><span data-stu-id="03861-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="03861-110">Прямоугольная ссылка с описанием целевой ячейки или ячейки.</span><span class="sxs-lookup"><span data-stu-id="03861-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="03861-111">Ссылка должна описывать соседние ячейки, чтобы в **xltypeRef** было `val.mref.lpmref->count` установлено 1.</span><span class="sxs-lookup"><span data-stu-id="03861-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="03861-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="03861-112">_pxValue_</span></span>
  
<span data-ttu-id="03861-113">Значение или значения, которые необходимо поместить в ячейку или ячейки.</span><span class="sxs-lookup"><span data-stu-id="03861-113">The value or values to be placed into the cell or cells.</span></span> <span data-ttu-id="03861-114">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="03861-114">For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="03861-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="03861-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="03861-116">аргумент pxValue</span><span class="sxs-lookup"><span data-stu-id="03861-116">pxValue argument</span></span>

<span data-ttu-id="03861-117">_pxValue может_ быть значением или массивом.</span><span class="sxs-lookup"><span data-stu-id="03861-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="03861-118">Если это значение, весь диапазон назначения заполняется этим значением.</span><span class="sxs-lookup"><span data-stu-id="03861-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="03861-119">Если это массив **(xltypeMulti),** элементы массива помещаются в соответствующие расположения прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="03861-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="03861-120">Если для второго аргумента используется горизонтальный массив, он дублируется вниз, чтобы заполнить весь прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="03861-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="03861-121">Если вы используете вертикальный массив, он дублируется правой для заполнения всего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="03861-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="03861-122">Если вы используете прямоугольный массив и он слишком мал для прямоугольного диапазона, в который вы хотите поместить его, этот диапазон **#N/A.**</span><span class="sxs-lookup"><span data-stu-id="03861-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A** s.</span></span>
  
<span data-ttu-id="03861-123">Если целевой диапазон меньше массива исходных данных, значения копируется до пределов целевого диапазона, а дополнительные данные игнорируются.</span><span class="sxs-lookup"><span data-stu-id="03861-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="03861-124">Чтобы очистить элемент прямоугольника назначения, используйте элемент **массива типа xltypeNil** в массиве источника.</span><span class="sxs-lookup"><span data-stu-id="03861-124">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array.</span></span> <span data-ttu-id="03861-125">Чтобы очистить весь прямоугольник назначения, ограничь второй аргумент.</span><span class="sxs-lookup"><span data-stu-id="03861-125">To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="03861-126">Ограничения</span><span class="sxs-lookup"><span data-stu-id="03861-126">Restrictions</span></span>

<span data-ttu-id="03861-127">**xlSet** нельзя отменить.</span><span class="sxs-lookup"><span data-stu-id="03861-127">**xlSet** cannot be undone.</span></span> <span data-ttu-id="03861-128">Кроме того, он уничтожает любые сведения об отменить, которые могли быть доступны ранее.</span><span class="sxs-lookup"><span data-stu-id="03861-128">In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="03861-129">**xlSet** может поместить в ячейки только константы, а не формулы.</span><span class="sxs-lookup"><span data-stu-id="03861-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="03861-130">**xlSet** ведет себя как функция, эквивалентная классу 3; то есть она доступна только в DLL, когда DLL вызвана из объекта, макроса, меню, панели  инструментов, клавиши ярлыка  или кнопки **Выполнить** в диалоговом окне Макрос (доступ к нему можно получить из вкладки Просмотр на ленте, начиная с Excel 2007 г., и меню **Tools** в более ранних версиях).</span><span class="sxs-lookup"><span data-stu-id="03861-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="03861-131">Пример</span><span class="sxs-lookup"><span data-stu-id="03861-131">Example</span></span>

<span data-ttu-id="03861-132">В следующем примере B205:B206 заполняется значение, переданное с макроса.</span><span class="sxs-lookup"><span data-stu-id="03861-132">The following example fills B205:B206 with the value that was passed in from a macro.</span></span> <span data-ttu-id="03861-133">Этот пример функции команды требует аргумента, поэтому он будет работать только в том случае, если он вызван с макрос XLM или из модуля VBA с помощью **метода Application.Run.**</span><span class="sxs-lookup"><span data-stu-id="03861-133">This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="03861-134">См. также</span><span class="sxs-lookup"><span data-stu-id="03861-134">See also</span></span>

- [<span data-ttu-id="03861-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="03861-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="03861-136">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="03861-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

