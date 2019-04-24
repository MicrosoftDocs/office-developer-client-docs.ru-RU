---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- Функция кслсет [Excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303859"
---
# <a name="xlset"></a><span data-ttu-id="f2cd1-104">xlSet</span><span class="sxs-lookup"><span data-stu-id="f2cd1-104">xlSet</span></span>

<span data-ttu-id="f2cd1-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f2cd1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f2cd1-106">Очень быстро поМещает постоянные значения в ячейки или диапазоны.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-106">Puts constant values into cells or ranges very quickly.</span></span> <span data-ttu-id="f2cd1-107">Для получения дополнительных сведений обратитесь к разделу "Кслсет and книги с формулами массива" в статье " [Известные проблемы разработки XLL для Excel](known-issues-in-excel-xll-development.md)".</span><span class="sxs-lookup"><span data-stu-id="f2cd1-107">For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="f2cd1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2cd1-108">Parameters</span></span>

<span data-ttu-id="f2cd1-109">_пксреференце_ (**кслтипереф** или **кслтипесреф**)</span><span class="sxs-lookup"><span data-stu-id="f2cd1-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="f2cd1-110">Прямоугольная ссылка, описывающая целевую ячейку или ячейки.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="f2cd1-111">Ссылка должна описывать смежные ячейки, поэтому в **кслтипереф** `val.mref.lpmref->count` должно быть задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="f2cd1-112">_Пксвалуе_</span><span class="sxs-lookup"><span data-stu-id="f2cd1-112">_pxValue_</span></span>
  
<span data-ttu-id="f2cd1-113">Значение или значения, помещаемые в ячейки или ячейки.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-113">The value or values to be placed into the cell or cells.</span></span> <span data-ttu-id="f2cd1-114">Для получения дополнительных сведений см раздел "Примечания".</span><span class="sxs-lookup"><span data-stu-id="f2cd1-114">For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f2cd1-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="f2cd1-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="f2cd1-116">аргумент Пксвалуе</span><span class="sxs-lookup"><span data-stu-id="f2cd1-116">pxValue argument</span></span>

<span data-ttu-id="f2cd1-117">_пксвалуе_ может быть либо значением, либо массивом.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="f2cd1-118">Если это значение, весь конечный диапазон заполняется этим значением.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="f2cd1-119">Если это массив (**xltypeMulti**), элементы массива помещаются в соответствующие расположения в прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="f2cd1-120">Если для второго аргумента используется горизонтальный массив, он повторяется, чтобы заполнить весь прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="f2cd1-121">Если вы используете вертикальный массив, он дублируется справа, чтобы заполнить весь прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="f2cd1-122">Если используется прямоугольный массив, и он слишком мал для прямоугольного диапазона, в который его следует поместить, этот диапазон дополняются **#N/a**s.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A**s.</span></span>
  
<span data-ttu-id="f2cd1-123">Если целевой диапазон меньше исходного массива, значения копируются вплоть до пределов целевого диапазона, а дополнительные данные игнорируются.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="f2cd1-124">Чтобы очистить элемент конечного прямоугольника, используйте элемент массива типа **кслтипенил** в исходном массиве.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-124">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array.</span></span> <span data-ttu-id="f2cd1-125">Чтобы очистить весь прямоугольник назначения, опустите второй аргумент.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-125">To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="f2cd1-126">Наложен</span><span class="sxs-lookup"><span data-stu-id="f2cd1-126">Restrictions</span></span>

<span data-ttu-id="f2cd1-127">**кслсет** не может быть отменен.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-127">**xlSet** cannot be undone.</span></span> <span data-ttu-id="f2cd1-128">Кроме того, он уничтожает все сведения об отмене, которые могли быть доступны до.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-128">In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="f2cd1-129">**кслсет** может помещать в ячейки только константы, а не формулы.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="f2cd1-130">**кслсет** функционирует как функция, эквивалентная команде класса 3; то есть он доступен только в библиотеке DLL, когда DLL вызывается из объекта, макроса, меню, панели инструментов, сочетания клавиш или кнопки **выполнить** в диалоговом окне **макрос** (доступного из вкладки **вид** на ленте, начиная с Excel 2007, а \*\*средства \*\*меню более ранних версий).</span><span class="sxs-lookup"><span data-stu-id="f2cd1-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="f2cd1-131">Пример</span><span class="sxs-lookup"><span data-stu-id="f2cd1-131">Example</span></span>

<span data-ttu-id="f2cd1-132">В следующем примере заполняются B205: B206 со значением, переданным из макроса.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-132">The following example fills B205:B206 with the value that was passed in from a macro.</span></span> <span data-ttu-id="f2cd1-133">В этом примере функции команды требуется аргумент, поэтому он будет работать только при вызове из листа макросов XLM или из модуля VBA с помощью метода **Application. Run** .</span><span class="sxs-lookup"><span data-stu-id="f2cd1-133">This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="f2cd1-134">См. также</span><span class="sxs-lookup"><span data-stu-id="f2cd1-134">See also</span></span>

- [<span data-ttu-id="f2cd1-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="f2cd1-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="f2cd1-136">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="f2cd1-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

