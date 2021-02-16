---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- Функция xlset [excel 2007]
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
# <a name="xlset"></a><span data-ttu-id="eded6-104">xlSet</span><span class="sxs-lookup"><span data-stu-id="eded6-104">xlSet</span></span>

<span data-ttu-id="eded6-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="eded6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="eded6-106">Очень быстро помещает постоянные значения в ячейки или диапазоны.</span><span class="sxs-lookup"><span data-stu-id="eded6-106">Puts constant values into cells or ranges very quickly.</span></span> <span data-ttu-id="eded6-107">Дополнительные сведения см. в подразении "XlSet and Workbooks with Array Formulas" в подраздах "Известные проблемы в разработке [XLL для Excel".](known-issues-in-excel-xll-development.md)</span><span class="sxs-lookup"><span data-stu-id="eded6-107">For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="eded6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eded6-108">Parameters</span></span>

<span data-ttu-id="eded6-109">_pxReference_ (**xltypeRef** или **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="eded6-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="eded6-110">Прямоугольная ссылка, описывающие целевую ячейку или ячейки.</span><span class="sxs-lookup"><span data-stu-id="eded6-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="eded6-111">Ссылка должна описывать смежные ячейки, чтобы в **xltypeRef** было установлено `val.mref.lpmref->count` 1.</span><span class="sxs-lookup"><span data-stu-id="eded6-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="eded6-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="eded6-112">_pxValue_</span></span>
  
<span data-ttu-id="eded6-113">Значение или значения, которые необходимо поместить в ячейку или ячейки.</span><span class="sxs-lookup"><span data-stu-id="eded6-113">The value or values to be placed into the cell or cells.</span></span> <span data-ttu-id="eded6-114">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="eded6-114">For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eded6-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="eded6-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="eded6-116">Аргумент pxValue</span><span class="sxs-lookup"><span data-stu-id="eded6-116">pxValue argument</span></span>

<span data-ttu-id="eded6-117">_pxValue_ может быть значением или массивом.</span><span class="sxs-lookup"><span data-stu-id="eded6-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="eded6-118">Если это значение, этим значением заполняется весь диапазон назначения.</span><span class="sxs-lookup"><span data-stu-id="eded6-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="eded6-119">Если это массив (**xltypeMulti),** элементы массива помещаются в соответствующие расположения в прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="eded6-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="eded6-120">При использовании горизонтального массива для второго аргумента он дублируется вниз, чтобы заполнить весь прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="eded6-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="eded6-121">При использовании вертикального массива он дублируется вправо для заполнения всего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="eded6-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="eded6-122">Если вы используете прямоугольный массив, который слишком мал для прямоугольного диапазона, в который вы хотите поместить его, этот диапазон заполнен **#N/A.**</span><span class="sxs-lookup"><span data-stu-id="eded6-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A** s.</span></span>
  
<span data-ttu-id="eded6-123">Если целевой диапазон меньше, чем исходный массив, значения копируется в пределах целевого диапазона, а дополнительные данные игнорируются.</span><span class="sxs-lookup"><span data-stu-id="eded6-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="eded6-124">Чтобы очистить элемент конечного прямоугольника, используйте элемент массива типов **xltypeNil** в массиве источника.</span><span class="sxs-lookup"><span data-stu-id="eded6-124">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array.</span></span> <span data-ttu-id="eded6-125">Чтобы очистить весь прямоугольник назначения, опустить второй аргумент.</span><span class="sxs-lookup"><span data-stu-id="eded6-125">To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="eded6-126">Ограничения</span><span class="sxs-lookup"><span data-stu-id="eded6-126">Restrictions</span></span>

<span data-ttu-id="eded6-127">**XLSet** нельзя отменить.</span><span class="sxs-lookup"><span data-stu-id="eded6-127">**xlSet** cannot be undone.</span></span> <span data-ttu-id="eded6-128">Кроме того, он уничтожает все сведения об отмене, которые могли быть доступны ранее.</span><span class="sxs-lookup"><span data-stu-id="eded6-128">In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="eded6-129">**xlSet** может поместить в ячейки только константы, а не формулы.</span><span class="sxs-lookup"><span data-stu-id="eded6-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="eded6-130">**xlSet** работает как функция, эквивалентная командам класса 3; то есть она доступна только в DLL, если DLL-объект вызван из объекта, макроса,  меню, панели  инструментов, сочетания клавиш  или кнопки "Выполнить" в диалоговом окне макроса (доступ к ней можно получить с помощью вкладки "Вид" на ленте, начиная с Excel 2007, и меню "Инструменты" в предыдущих версиях). </span><span class="sxs-lookup"><span data-stu-id="eded6-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="eded6-131">Пример</span><span class="sxs-lookup"><span data-stu-id="eded6-131">Example</span></span>

<span data-ttu-id="eded6-132">В следующем примере заполняется значение B205:B206, переданное из макроса.</span><span class="sxs-lookup"><span data-stu-id="eded6-132">The following example fills B205:B206 with the value that was passed in from a macro.</span></span> <span data-ttu-id="eded6-133">В этом примере функции команды требуется аргумент, поэтому он будет работать, только если он вызван из листа макроса XLM или из модуля VBA с помощью метода **Application.Run.**</span><span class="sxs-lookup"><span data-stu-id="eded6-133">This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="eded6-134">См. также</span><span class="sxs-lookup"><span data-stu-id="eded6-134">See also</span></span>

- [<span data-ttu-id="eded6-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="eded6-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="eded6-136">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="eded6-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

