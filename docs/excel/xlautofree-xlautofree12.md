---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- функция xlAutoFree [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a2d2b8e60b484ba8156acc80d543493e3ec9c564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807344"
---
# <a name="xlautofreexlautofree12"></a><span data-ttu-id="26635-104">xlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="26635-104">xlAutoFree/xlAutoFree12</span></span>

 <span data-ttu-id="26635-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="26635-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="26635-106">Именем с Microsoft Excel, сразу после функция листа XLL возвращает **XLOPER**/ **XLOPER12** к нему с набором флаг, указывающий памяти, XLL, по которой нужно освободить.</span><span class="sxs-lookup"><span data-stu-id="26635-106">Called by Microsoft Excel just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** to it with a flag set that tells it there is memory that the XLL still needs to release.</span></span> <span data-ttu-id="26635-107">Это позволяет XLL-Модулей для возврата динамически назначаемых массивов строк и внешние ссылки на лист без утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="26635-107">This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks.</span></span> <span data-ttu-id="26635-108">Дополнительные сведения содержатся в разделе [Управление памятью в Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="26635-108">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="26635-109">Начиная с версии Excel 2007, функция **xlAutoFree12** и тип данных **XLOPER12** поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26635-109">Starting in Excel 2007, the **xlAutoFree12** function and the **XLOPER12** data type are supported.</span></span> 
  
<span data-ttu-id="26635-110">Excel не требуется XLL внедрение и экспортировать любой из этих функций.</span><span class="sxs-lookup"><span data-stu-id="26635-110">Excel does not require an XLL to implement and export either of these functions.</span></span> <span data-ttu-id="26635-111">Тем не менее это необходимо сделать Если XLL функций возвращают XLOPER и XLOPER12, которая была распределена динамически или, который содержит указатели на динамически выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="26635-111">However, you must do so if your XLL functions return an XLOPER or XLOPER12 that has been dynamically allocated or that contains pointers to dynamically allocated memory.</span></span> <span data-ttu-id="26635-112">Убедитесь, что во всей вашей XLL и реализации **xlAutoFree** и **xlAutoFree12**Выбор использование памяти для этих типов.</span><span class="sxs-lookup"><span data-stu-id="26635-112">Ensure that your choice of how to manage memory for these types is consistent throughout your XLL and with how you implemented **xlAutoFree** and **xlAutoFree12**.</span></span>
  
<span data-ttu-id="26635-113">Внутри **xlAutoFree**/ отключены функции**xlAutoFree12** , обратных вызовов в Excel, за исключением: **xlFree** могут вызываться для освобождения памяти, выделенной Excel.</span><span class="sxs-lookup"><span data-stu-id="26635-113">Inside the **xlAutoFree**/ **xlAutoFree12** function, callbacks into Excel are disabled, with one exception: **xlFree** can be called to free Excel-allocated memory.</span></span> 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a><span data-ttu-id="26635-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="26635-114">Parameters</span></span>

 <span data-ttu-id="26635-115">_pxFree_ (**LPXLOPER в случае xlAutoFree**)</span><span class="sxs-lookup"><span data-stu-id="26635-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span></span>
  
 <span data-ttu-id="26635-116">_pxFree_ (**LPXLOPER12 в случае xlAutoFree12**)</span><span class="sxs-lookup"><span data-stu-id="26635-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span></span>
  
<span data-ttu-id="26635-117">Указатель на **XLOPER** или **XLOPER12** с объемом памяти, который необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="26635-117">A pointer to the **XLOPER** or the **XLOPER12** that has memory that needs to be freed.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="26635-118">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26635-118">Property value/Return value</span></span>

<span data-ttu-id="26635-119">Эта функция не возвращает значение и должен быть объявлен как возвращающий void.</span><span class="sxs-lookup"><span data-stu-id="26635-119">This function does not return a value and should be declared as returning void.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26635-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="26635-120">Remarks</span></span>

<span data-ttu-id="26635-121">Когда Excel настроен на использование пересчета многопоточные книги, **xlAutoFree**/ **xlAutoFree12** вызывается в том же потоке, используется для вызова функции, который возвращается его.</span><span class="sxs-lookup"><span data-stu-id="26635-121">When Excel is configured to use multithreaded workbook recalculation, **xlAutoFree**/ **xlAutoFree12** is called on the same thread used to call the function that returned it.</span></span> <span data-ttu-id="26635-122">Вызов **xlAutoFree**/ **xlAutoFree12** всегда выполняется до любого последующие ячейки оценки для данного потока.</span><span class="sxs-lookup"><span data-stu-id="26635-122">The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread.</span></span> <span data-ttu-id="26635-123">Это упрощает разработки потоками в вашей XLL.</span><span class="sxs-lookup"><span data-stu-id="26635-123">This simplifies thread-safe design in your XLL.</span></span> 
  
<span data-ttu-id="26635-124">Если **xlAutoFree**/ **xlAutoFree12** предоставлении обращается поле **xltype** _pxFree_, помните, что будет установлен бит **xlbitDLLFree** .</span><span class="sxs-lookup"><span data-stu-id="26635-124">If the **xlAutoFree**/ **xlAutoFree12** function you provide looks at the **xltype** field of  _pxFree_, remember that the **xlbitDLLFree** bit will still be set.</span></span> 
  
## <a name="example"></a><span data-ttu-id="26635-125">Пример</span><span class="sxs-lookup"><span data-stu-id="26635-125">Example</span></span>

 <span data-ttu-id="26635-126">**Пример реализации 1**</span><span class="sxs-lookup"><span data-stu-id="26635-126">**Example Implementation 1**</span></span>
  
<span data-ttu-id="26635-127">Первый код из `\SAMPLES\EXAMPLE\EXAMPLE.C` демонстрирует очень реализации **xlAutoFree**, которая предназначена для работы с одной функции **fArray**.</span><span class="sxs-lookup"><span data-stu-id="26635-127">The first code from  `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstrates a very specific implementation of **xlAutoFree**, which is designed to work with just one function, **fArray**.</span></span> <span data-ttu-id="26635-128">В общем случае вашей XLL будут иметь несколько функция, возвращающая памяти, который необходим для освобождения, в противном случае менее ограниченных реализации является обязательным.</span><span class="sxs-lookup"><span data-stu-id="26635-128">In general, your XLL will have more than just one function returning memory that needs to be freed, in which case a less restricted implementation is required.</span></span> 
  
 <span data-ttu-id="26635-129">**Пример реализации 2**</span><span class="sxs-lookup"><span data-stu-id="26635-129">**Example implementation 2**</span></span>
  
<span data-ttu-id="26635-130">Второй пример реализации согласуется с предположения, используемых в примерах **XLOPER12** создания в разделе 1.6.3, xl12_Str_example, xl12_Ref_example и xl12_Multi_example.</span><span class="sxs-lookup"><span data-stu-id="26635-130">The second example implementation is consistent with the assumptions used in the **XLOPER12** creation examples in section 1.6.3, xl12_Str_example, xl12_Ref_example, and xl12_Multi_example.</span></span> <span data-ttu-id="26635-131">Предположения, при **xlbitDLLFree** разрядная хранится набор, все string, array и памяти внешняя ссылка динамически выделен с помощью **malloc**и поэтому необходимо освободить в ходе звонка, чтобы освободить место на.</span><span class="sxs-lookup"><span data-stu-id="26635-131">The assumptions are that, when the **xlbitDLLFree** bit has been set, all string, array, and external reference memory has been dynamically allocated using **malloc**, and so needs to be freed in a call to free.</span></span>
  
 <span data-ttu-id="26635-132">**Пример реализации 3**</span><span class="sxs-lookup"><span data-stu-id="26635-132">**Example implementation 3**</span></span>
  
<span data-ttu-id="26635-133">Третий пример реализации согласуется с XLL-модуль экспортированных функций, которые возвращают **XLOPER12**s выделение строки, внешние ссылки и массивов с помощью **malloc**, а также динамически выделяются **XLOPER12** самого.</span><span class="sxs-lookup"><span data-stu-id="26635-133">The third example implementation is consistent with an XLL where exported functions that return **XLOPER12**s allocate strings, external references and arrays using **malloc**, and where the **XLOPER12** itself is also dynamically allocated.</span></span> <span data-ttu-id="26635-134">Указатель возвращается динамически выделяемый **XLOPER12** является одним из способов убедитесь, что функция потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="26635-134">Returning a pointer to a dynamically allocated **XLOPER12** is one way to ensure that the function is thread safe.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="26635-135">См. также</span><span class="sxs-lookup"><span data-stu-id="26635-135">See also</span></span>



[<span data-ttu-id="26635-136">Диспетчер надстроек и функции XLL интерфейса</span><span class="sxs-lookup"><span data-stu-id="26635-136">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

