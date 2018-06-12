---
title: функция xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- функция xlSet функции [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 63f50e441f5d851677f36754a17bcd6403705239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807378"
---
# <a name="xlset"></a><span data-ttu-id="34142-104">функция xlSet</span><span class="sxs-lookup"><span data-stu-id="34142-104">xlSet</span></span>

<span data-ttu-id="34142-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="34142-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="34142-106">Очень быстро переводит постоянных значений в ячейки или диапазоны.</span><span class="sxs-lookup"><span data-stu-id="34142-106">Puts constant values into cells or ranges very quickly.</span></span> <span data-ttu-id="34142-107">Для получения дополнительных сведений см «функция xlSet и книги с формул массива» в разделе [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="34142-107">For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="34142-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="34142-108">Parameters</span></span>

<span data-ttu-id="34142-109">_pxReference_ (**xltypeRef** или **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="34142-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="34142-110">Прямоугольный ссылки на описания конечного одну или несколько ячеек.</span><span class="sxs-lookup"><span data-stu-id="34142-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="34142-111">Справочные материалы по необходимо описать смежных ячеек таким образом, в **xltypeRef** `val.mref.lpmref->count` должен иметь значение 1.</span><span class="sxs-lookup"><span data-stu-id="34142-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="34142-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="34142-112">_pxValue_</span></span>
  
<span data-ttu-id="34142-113">Значение или значения должен быть помещен в одну или несколько ячеек.</span><span class="sxs-lookup"><span data-stu-id="34142-113">The value or values to be placed into the cell or cells.</span></span> <span data-ttu-id="34142-114">Дополнительные сведения см в разделе «Примечания».</span><span class="sxs-lookup"><span data-stu-id="34142-114">For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="34142-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="34142-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="34142-116">Аргумент pxValue</span><span class="sxs-lookup"><span data-stu-id="34142-116">pxValue argument</span></span>

<span data-ttu-id="34142-117">_pxValue_ может быть значение или массив.</span><span class="sxs-lookup"><span data-stu-id="34142-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="34142-118">Если это значение, это значение заполняется весь диапазон назначения.</span><span class="sxs-lookup"><span data-stu-id="34142-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="34142-119">Если это массив (**xltypeMulti**) элементы массива помещаются в соответствующих расположений в прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="34142-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="34142-120">Если вы используете горизонтального массива для второй аргумент, дублируется вниз для заполнения всей прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="34142-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="34142-121">Если вы используете вертикального массива, уже используется для заполнения всей прямоугольника справа.</span><span class="sxs-lookup"><span data-stu-id="34142-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="34142-122">Если использовать прямоугольный массив слишком мал для прямоугольный диапазон, чтобы поместить его в, этот диапазон дополняется s **# Н/д**.</span><span class="sxs-lookup"><span data-stu-id="34142-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A**s.</span></span>
  
<span data-ttu-id="34142-123">Если указанный диапазон меньше исходного массива, значения копируются в до ограничения в указанный диапазон и дополнительных данных игнорируются.</span><span class="sxs-lookup"><span data-stu-id="34142-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="34142-124">Чтобы удалить элемент конечного прямоугольника, используйте элемент **xltypeNil** тип массива исходного массива.</span><span class="sxs-lookup"><span data-stu-id="34142-124">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array.</span></span> <span data-ttu-id="34142-125">Чтобы очистить всю конечного прямоугольника, не заданы второй.</span><span class="sxs-lookup"><span data-stu-id="34142-125">To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="34142-126">Ограничения</span><span class="sxs-lookup"><span data-stu-id="34142-126">Restrictions</span></span>

<span data-ttu-id="34142-127">**функция xlSet** невозможно отменить.</span><span class="sxs-lookup"><span data-stu-id="34142-127">**xlSet** cannot be undone.</span></span> <span data-ttu-id="34142-128">Кроме того какие-либо сведения отмены, которая была перед уничтожает.</span><span class="sxs-lookup"><span data-stu-id="34142-128">In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="34142-129">**функция xlSet** можно поместить только константы, не формулы в ячейках.</span><span class="sxs-lookup"><span data-stu-id="34142-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="34142-130">**функция xlSet** ведет себя как функция эквивалент команды класса 3; то есть оно доступно только в библиотеке DLL при вызове из объекта, макрос, меню, панели инструментов, сочетания клавиш или кнопки **запустить** в диалоговое окно **макроса** (доступного из **представления** вкладки на ленте, начиная с версии Excel 2007, а также средства **библиотеки DLL **меню в более ранних версий).</span><span class="sxs-lookup"><span data-stu-id="34142-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="34142-131">Пример</span><span class="sxs-lookup"><span data-stu-id="34142-131">Example</span></span>

<span data-ttu-id="34142-132">В следующем примере заполняется B205:B206 со значением, который был получен из макроса.</span><span class="sxs-lookup"><span data-stu-id="34142-132">The following example fills B205:B206 with the value that was passed in from a macro.</span></span> <span data-ttu-id="34142-133">В этом примере функция команда требуется аргумент и поэтому будет работать только при вызове из таблицы макросов XLM или из модуля VBA с помощью метода **Application.Run** .</span><span class="sxs-lookup"><span data-stu-id="34142-133">This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="34142-134">См. также</span><span class="sxs-lookup"><span data-stu-id="34142-134">See also</span></span>

- [<span data-ttu-id="34142-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="34142-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="34142-136">Функции интерфейса API для C, которые могут вызываться только из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="34142-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

