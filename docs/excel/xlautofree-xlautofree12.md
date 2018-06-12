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
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Именем с Microsoft Excel, сразу после функция листа XLL возвращает **XLOPER**/ **XLOPER12** к нему с набором флаг, указывающий памяти, XLL, по которой нужно освободить. Это позволяет XLL-Модулей для возврата динамически назначаемых массивов строк и внешние ссылки на лист без утечки памяти. Дополнительные сведения содержатся в разделе [Управление памятью в Excel](memory-management-in-excel.md).
  
Начиная с версии Excel 2007, функция **xlAutoFree12** и тип данных **XLOPER12** поддерживаются. 
  
Excel не требуется XLL внедрение и экспортировать любой из этих функций. Тем не менее это необходимо сделать Если XLL функций возвращают XLOPER и XLOPER12, которая была распределена динамически или, который содержит указатели на динамически выделенной памяти. Убедитесь, что во всей вашей XLL и реализации **xlAutoFree** и **xlAutoFree12**Выбор использование памяти для этих типов.
  
Внутри **xlAutoFree**/ отключены функции**xlAutoFree12** , обратных вызовов в Excel, за исключением: **xlFree** могут вызываться для освобождения памяти, выделенной Excel. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Parameters

 _pxFree_ (**LPXLOPER в случае xlAutoFree**)
  
 _pxFree_ (**LPXLOPER12 в случае xlAutoFree12**)
  
Указатель на **XLOPER** или **XLOPER12** с объемом памяти, который необходимо освободить. 
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Эта функция не возвращает значение и должен быть объявлен как возвращающий void.
  
## <a name="remarks"></a>Замечания

Когда Excel настроен на использование пересчета многопоточные книги, **xlAutoFree**/ **xlAutoFree12** вызывается в том же потоке, используется для вызова функции, который возвращается его. Вызов **xlAutoFree**/ **xlAutoFree12** всегда выполняется до любого последующие ячейки оценки для данного потока. Это упрощает разработки потоками в вашей XLL. 
  
Если **xlAutoFree**/ **xlAutoFree12** предоставлении обращается поле **xltype** _pxFree_, помните, что будет установлен бит **xlbitDLLFree** . 
  
## <a name="example"></a>Пример

 **Пример реализации 1**
  
Первый код из `\SAMPLES\EXAMPLE\EXAMPLE.C` демонстрирует очень реализации **xlAutoFree**, которая предназначена для работы с одной функции **fArray**. В общем случае вашей XLL будут иметь несколько функция, возвращающая памяти, который необходим для освобождения, в противном случае менее ограниченных реализации является обязательным. 
  
 **Пример реализации 2**
  
Второй пример реализации согласуется с предположения, используемых в примерах **XLOPER12** создания в разделе 1.6.3, xl12_Str_example, xl12_Ref_example и xl12_Multi_example. Предположения, при **xlbitDLLFree** разрядная хранится набор, все string, array и памяти внешняя ссылка динамически выделен с помощью **malloc**и поэтому необходимо освободить в ходе звонка, чтобы освободить место на.
  
 **Пример реализации 3**
  
Третий пример реализации согласуется с XLL-модуль экспортированных функций, которые возвращают **XLOPER12**s выделение строки, внешние ссылки и массивов с помощью **malloc**, а также динамически выделяются **XLOPER12** самого. Указатель возвращается динамически выделяемый **XLOPER12** является одним из способов убедитесь, что функция потокобезопасными. 
  
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



[Диспетчер надстроек и функции XLL интерфейса](add-in-manager-and-xll-interface-functions.md)

