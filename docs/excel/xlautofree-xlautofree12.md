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
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Вызванная Microsoft Excel сразу после того, как функция таблицы XLL возвращает **XLOPER XLOPER12** в нее со набором флагов, который сообщает ему, что есть память, которую XLL по-прежнему необходимо /   выпустить. Благодаря этому библиотека XLL может вернуть динамически выделяемые массивы, строки и внешние ссылки на лист без утечек памяти. Дополнительные сведения см. в статье [Управление памятью в Excel](memory-management-in-excel.md).
  
Начиная с Excel 2007 г. поддерживаются функция **xlAutoFree12** и **тип данных XLOPER12.** 
  
Excel XLL не требуется для реализации и экспорта этих функций. Однако это необходимо сделать, если функции XLL возвращают XLOPER или XLOPER12, которые были динамически выделены или содержат указатели для динамически выделенной памяти. Убедитесь, что выбор управления памятью для этих типов согласуется во всем XLL и с реализацией **xlAutoFree** и **xlAutoFree12.**
  
Внутри **функции xlAutoFree** /  **xlAutoFree12** отключены вызовы в Excel, за одним исключением: **xlFree** можно вызвать для Excel выделенной памяти. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Parameters

 _pxFree_ **(LPXLOPER в случае xlAutoFree)**
  
 _pxFree_ **(LPXLOPER12 в случае xlAutoFree12)**
  
Указатель на **XLOPER** или **XLOPER12** с памятью, которую необходимо освободить. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Эта функция не возвращает значение и должна быть объявлена недействительной.
  
## <a name="remarks"></a>Примечания

Когда Excel настраивается для пересчета многопотоковых книг, **xlAutoFree** /  **xlAutoFree12** используется для вызова функции, которая вернула ее. Вызов функции **xlAutoFree**/ **xlAutoFree12** всегда выполняется перед оценкой последующих ячеек листа для этого потока. Это упрощает потокобезопасную разработку библиотеки XLL. 
  
Если **предоставляемая функция xlAutoFree** /  **xlAutoFree12** выглядит в поле **xltype** _pxFree,_ помните, что бит **xlbitDLLFree** будет по-прежнему задат. 
  
## <a name="example"></a>Пример

 **Пример реализации 1**
  
Первый код демонстрирует очень конкретную реализацию  `\SAMPLES\EXAMPLE\EXAMPLE.C` **xlAutoFree**, которая предназначена для работы только с одной функцией, **fArray**. Как правило, у XLL будет не одна функция, возвращаемая память, которая должна быть освобождена, и в этом случае требуется менее ограниченная реализация. 
  
 **Пример реализации 2**
  
Реализация второго примера соответствует предположениям, используемым в примерах создания **XLOPER12** в разделе 1.6.3, xl12_Str_example, xl12_Ref_example и xl12_Multi_example. Предположения в том, что при наборе **бита xlbitDLLFree** все строки, массивы и внешняя справочная память динамически распределяются с помощью мэллок, поэтому необходимо освободить в вызове бесплатно.
  
 **Пример реализации 3**
  
Реализация третьего примера согласуется с XLL, в котором экспортируются функции, возвращая **выделенные строки XLOPER12,** внешние ссылки и массивы с использованием мэллок, а также динамически распределен сам **XLOPER12.** Возвращение указателя к динамически выделенной **XLOPER12** — это один из способов обеспечения безопасности функции потока. 
  
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

## <a name="see-also"></a>См. также



[Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)

