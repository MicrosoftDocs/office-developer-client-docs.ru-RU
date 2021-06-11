---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- функция xlautofree [Excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3dfba5ae98b0635c95308eac01bf2f10867678e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413292"
---
# <a name="xlautofreexlautofree12"></a><span data-ttu-id="e0fbe-104">xlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="e0fbe-104">xlAutoFree/xlAutoFree12</span></span>

 <span data-ttu-id="e0fbe-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e0fbe-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e0fbe-106">Вызванная Microsoft Excel сразу после того, как функция таблицы XLL возвращает **XLOPER XLOPER12** в нее со набором флагов, который сообщает ему, что есть память, которую XLL по-прежнему необходимо /   выпустить.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-106">Called by Microsoft Excel just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** to it with a flag set that tells it there is memory that the XLL still needs to release.</span></span> <span data-ttu-id="e0fbe-107">Благодаря этому библиотека XLL может вернуть динамически выделяемые массивы, строки и внешние ссылки на лист без утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-107">This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks.</span></span> <span data-ttu-id="e0fbe-108">Дополнительные сведения см. в статье [Управление памятью в Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="e0fbe-108">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="e0fbe-109">Начиная с Excel 2007 г. поддерживаются функция **xlAutoFree12** и **тип данных XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="e0fbe-109">Starting in Excel 2007, the **xlAutoFree12** function and the **XLOPER12** data type are supported.</span></span> 
  
<span data-ttu-id="e0fbe-110">Excel XLL не требуется для реализации и экспорта этих функций.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-110">Excel does not require an XLL to implement and export either of these functions.</span></span> <span data-ttu-id="e0fbe-111">Однако это необходимо сделать, если функции XLL возвращают XLOPER или XLOPER12, которые были динамически выделены или содержат указатели для динамически выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-111">However, you must do so if your XLL functions return an XLOPER or XLOPER12 that has been dynamically allocated or that contains pointers to dynamically allocated memory.</span></span> <span data-ttu-id="e0fbe-112">Убедитесь, что выбор управления памятью для этих типов согласуется во всем XLL и с реализацией **xlAutoFree** и **xlAutoFree12.**</span><span class="sxs-lookup"><span data-stu-id="e0fbe-112">Ensure that your choice of how to manage memory for these types is consistent throughout your XLL and with how you implemented **xlAutoFree** and **xlAutoFree12**.</span></span>
  
<span data-ttu-id="e0fbe-113">Внутри **функции xlAutoFree** /  **xlAutoFree12** отключены вызовы в Excel, за одним исключением: **xlFree** можно вызвать для Excel выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-113">Inside the **xlAutoFree**/ **xlAutoFree12** function, callbacks into Excel are disabled, with one exception: **xlFree** can be called to free Excel-allocated memory.</span></span> 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a><span data-ttu-id="e0fbe-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="e0fbe-114">Parameters</span></span>

 <span data-ttu-id="e0fbe-115">_pxFree_ **(LPXLOPER в случае xlAutoFree)**</span><span class="sxs-lookup"><span data-stu-id="e0fbe-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span></span>
  
 <span data-ttu-id="e0fbe-116">_pxFree_ **(LPXLOPER12 в случае xlAutoFree12)**</span><span class="sxs-lookup"><span data-stu-id="e0fbe-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span></span>
  
<span data-ttu-id="e0fbe-117">Указатель на **XLOPER** или **XLOPER12** с памятью, которую необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-117">A pointer to the **XLOPER** or the **XLOPER12** that has memory that needs to be freed.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e0fbe-118">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0fbe-118">Property value/Return value</span></span>

<span data-ttu-id="e0fbe-119">Эта функция не возвращает значение и должна быть объявлена недействительной.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-119">This function does not return a value and should be declared as returning void.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0fbe-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="e0fbe-120">Remarks</span></span>

<span data-ttu-id="e0fbe-121">Когда Excel настраивается для пересчета многопотоковых книг, **xlAutoFree** /  **xlAutoFree12** используется для вызова функции, которая вернула ее.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-121">When Excel is configured to use multithreaded workbook recalculation, **xlAutoFree**/ **xlAutoFree12** is called on the same thread used to call the function that returned it.</span></span> <span data-ttu-id="e0fbe-122">Вызов функции **xlAutoFree**/ **xlAutoFree12** всегда выполняется перед оценкой последующих ячеек листа для этого потока.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-122">The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread.</span></span> <span data-ttu-id="e0fbe-123">Это упрощает потокобезопасную разработку библиотеки XLL.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-123">This simplifies thread-safe design in your XLL.</span></span> 
  
<span data-ttu-id="e0fbe-124">Если **предоставляемая функция xlAutoFree** /  **xlAutoFree12** выглядит в поле **xltype** _pxFree,_ помните, что бит **xlbitDLLFree** будет по-прежнему задат.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-124">If the **xlAutoFree**/ **xlAutoFree12** function you provide looks at the **xltype** field of  _pxFree_, remember that the **xlbitDLLFree** bit will still be set.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e0fbe-125">Пример</span><span class="sxs-lookup"><span data-stu-id="e0fbe-125">Example</span></span>

 <span data-ttu-id="e0fbe-126">**Пример реализации 1**</span><span class="sxs-lookup"><span data-stu-id="e0fbe-126">**Example Implementation 1**</span></span>
  
<span data-ttu-id="e0fbe-127">Первый код демонстрирует очень конкретную реализацию  `\SAMPLES\EXAMPLE\EXAMPLE.C` **xlAutoFree**, которая предназначена для работы только с одной функцией, **fArray**.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-127">The first code from  `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstrates a very specific implementation of **xlAutoFree**, which is designed to work with just one function, **fArray**.</span></span> <span data-ttu-id="e0fbe-128">Как правило, у XLL будет не одна функция, возвращаемая память, которая должна быть освобождена, и в этом случае требуется менее ограниченная реализация.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-128">In general, your XLL will have more than just one function returning memory that needs to be freed, in which case a less restricted implementation is required.</span></span> 
  
 <span data-ttu-id="e0fbe-129">**Пример реализации 2**</span><span class="sxs-lookup"><span data-stu-id="e0fbe-129">**Example implementation 2**</span></span>
  
<span data-ttu-id="e0fbe-130">Реализация второго примера соответствует предположениям, используемым в примерах создания **XLOPER12** в разделе 1.6.3, xl12_Str_example, xl12_Ref_example и xl12_Multi_example.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-130">The second example implementation is consistent with the assumptions used in the **XLOPER12** creation examples in section 1.6.3, xl12_Str_example, xl12_Ref_example, and xl12_Multi_example.</span></span> <span data-ttu-id="e0fbe-131">Предположения в том, что при наборе **бита xlbitDLLFree** все строки, массивы и внешняя справочная память динамически распределяются с помощью мэллок, поэтому необходимо освободить в вызове бесплатно.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-131">The assumptions are that, when the **xlbitDLLFree** bit has been set, all string, array, and external reference memory has been dynamically allocated using **malloc**, and so needs to be freed in a call to free.</span></span>
  
 <span data-ttu-id="e0fbe-132">**Пример реализации 3**</span><span class="sxs-lookup"><span data-stu-id="e0fbe-132">**Example implementation 3**</span></span>
  
<span data-ttu-id="e0fbe-133">Реализация третьего примера согласуется с XLL, в котором экспортируются функции, возвращая **выделенные строки XLOPER12,** внешние ссылки и массивы с использованием мэллок, а также динамически распределен сам **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="e0fbe-133">The third example implementation is consistent with an XLL where exported functions that return **XLOPER12** s allocate strings, external references and arrays using **malloc**, and where the **XLOPER12** itself is also dynamically allocated.</span></span> <span data-ttu-id="e0fbe-134">Возвращение указателя к динамически выделенной **XLOPER12** — это один из способов обеспечения безопасности функции потока.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-134">Returning a pointer to a dynamically allocated **XLOPER12** is one way to ensure that the function is thread safe.</span></span> 
  
```cs
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 1
//////////////////////////////////////////
LPXLOPER12 WINAPI fArray(void)
{
    LPXLOPER12 pxArray;
    static XLOPER12 xMulti;
    int i;
    int rwcol;
    xMulti.xltype = xltypeMulti | xlbitDLLFree;
    xMulti.val.array.columns = 1;
    xMulti.val.array.rows = 8;
    // For large values of rows and columns, this would overflow
    // use __int64 in that case and return an error if rwcol
    // contains a number that won't fit in sizeof(int) bytes
    rwcol = xMulti.val.array.columns * xMulti.val.array.rows; 
    pxArray = (LPXLOPER12)GlobalLock(hArray = GlobalAlloc(GMEM_ZEROINIT, rwcol * sizeof(XLOPER12)));
    xMulti.val.array.lparray = pxArray;
    for(i = 0; i < rwcol; i++) 
    {
        pxArray[i].xltype = xltypeInt;
        pxArray[i].val.w = i;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe, use alternate memory allocation mechanisms
    return (LPXLOPER12)&xMulti;
}
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    GlobalUnlock(hArray);
    GlobalFree(hArray);
    return;
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 2
//////////////////////////////////////////
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
/* Assume all string elements were allocated using malloc, and
** need to be freed using free.  Then free the array itself.
*/
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 3
//////////////////////////////////////////
LPXLOPER12 WINAPI example_xll_function(LPXLOPER12 pxArg)
{
// Thread-safe return value. Every invocation of this function
// gets its own piece of memory.
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
// Initialize to a safe default
    pxRtnValue->xltype = xltypeNil;
// Set the value of pxRtnValue making sure that strings, external
// references, arrays, and strings within arrays are all dynamically
// allocated using malloc.
//    (code omitted)
//    ...
// Set xlbitDLLFree regardless of the type of the return value to
// ensure xlAutoFree12 is called and pxRtnValue is freed.
    pxRtnValue->xltype |= xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
// Assume all string elements were allocated using malloc, and
// need to be freed using free. Then free the array itself.
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
// Assume pxFree was itself dynamically allocated using malloc.
    free(pxFree);
}
```

## <a name="see-also"></a><span data-ttu-id="e0fbe-135">См. также</span><span class="sxs-lookup"><span data-stu-id="e0fbe-135">See also</span></span>



[<span data-ttu-id="e0fbe-136">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="e0fbe-136">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

