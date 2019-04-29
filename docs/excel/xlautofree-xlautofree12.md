---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- функция xlAutoFree [Excel 2007]
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
  
Вызывается Microsoft Excel сразу после того, как функция листа XLL ****/ **** возвращает для нее значение параметра, указывающее на наличие памяти, которую все еще требуется выпустить. Благодаря этому библиотека XLL может вернуть динамически выделяемые массивы, строки и внешние ссылки на лист без утечек памяти. Дополнительные сведения см. в статье [Управление памятью в Excel](memory-management-in-excel.md).
  
Начиная с Excel 2007, поддерживаются функция **xlAutoFree12** и тип данных **XLOPER12** . 
  
В Excel не требуется XLL для реализации и экспорта любой из этих функций. Тем не менее, это необходимо, если функции XLL возвращают XLOPER или XLOPER12, которые были динамически выделены или содержат указатели на динамически выделяемую память. Убедитесь, что выбор способа управления памятью для этих типов является единообразным для всех XLL и способов реализации **xlAutoFree** и **xlAutoFree12**.
  
В функции **xlAutoFree**/ **xlAutoFree12** обратные вызовы в Excel отключаются с одним исключением: **кслфри** можно вызвать для освобождения памяти, выделенной Excel. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Параметры

 _пксфри_ (**Лпкслопер в случае xlAutoFree**)
  
 _пксфри_ (**LPXLOPER12 в случае xlAutoFree12**)
  
Указатель на **XLOPER** или **XLOPER12** с памятью, которую необходимо освободить. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Эта функция не возвращает значение и должна объявляться, как возвращаемое значение void.
  
## <a name="remarks"></a>Примечания

Если в Excel настроено использование многопотокового пересчета, **xlAutoFree**/ **xlAutoFree12** вызывается в том же потоке, который использовался для вызова функции, которая возвращает ее. Вызов функции **xlAutoFree**/ **xlAutoFree12** всегда выполняется перед оценкой последующих ячеек листа для этого потока. Это упрощает потокобезопасную разработку библиотеки XLL. 
  
Если функция **xlAutoFree**/ **xlAutoFree12** выполняет поиск в поле **кслтипе** _пксфри_, помните, что бит **кслбитдллфри** будет по-прежнему установлен. 
  
## <a name="example"></a>Пример

 **Пример реализации 1**
  
В первом коде `\SAMPLES\EXAMPLE\EXAMPLE.C` показаны очень специфичная реализация **xlAutoFree**, предназначенная для работы только с одной функцией, **фаррай**. В общем случае XLL-модуль будет иметь больше, чем просто одна функция, возвращающая память, которую необходимо освободить, в этом случае требуется менее ограниченная реализация. 
  
 **Пример реализации 2**
  
Второй пример реализации согласуется с предположениями, используемыми в примерах создания **XLOPER12** в разделах 1.6.3, Xl12_Str_example, Xl12_Ref_example и xl12_Multi_example. Предполагается, что если установлен бит **кслбитдллфри** , вся строка, массив и внешняя Справочная память были динамически выделены с помощью **malloc**, и поэтому их необходимо освободить при вызове Free.
  
 **Пример реализации 3**
  
Третий пример реализации согласуется с XLL-МОДУЛЯми, в которых экспортированные **** функции, возвращающие строки распределения, внешние ссылки и массивы с помощью функции **malloc**и место, в котором также размещается объект **XLOPER12** . Возврат указателя на динамически выделенный объект **XLOPER12** является одним из способов обеспечения потокобезопасности функции. 
  
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

