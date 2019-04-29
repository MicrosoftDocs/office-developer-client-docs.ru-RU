---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 32d5075af34cda9753c5d082bd4ab00afab1ecff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414111"
---
# <a name="xlasyncreturn"></a>xlAsyncReturn

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Используется для возврата результата асинхронной пользовательской функции (UDF).
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Параметры

_пксасинчандле_ (**кслтипебигдата**)
  
Асинхронный дескриптор объекта UDF, в который возвращается результат.
  
_Пксфунктионресулт_
  
Возвращаемое значение UDF.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

В случае успеха возвращает **значение true** (**кслтипебул**). В случае неудачной попытки возвращает **значение false**.
  
## <a name="remarks"></a>Примечания

**ксласинкретурн** — единственный обратный вызов, позволяющий использовать в процессе пересчета потоки, не связанные с вычислениями. Асинхронная часть асинхронной UDF не должна выполнять обратные вызовы, кроме **ксласинкретурн**. XLL должен освободить память, выделенную для хранения возвращаемого значения.
  
Параметры _пксасинчандле_ и _пксфунктионресулт_ также могут иметь тип **xltypeMulti** при использовании для возвращения массива дескрипторов и соответствующих значений в едином обратном вызове. При использовании одного обратного вызова передайте LPXLOPER12, который указывает на структуры XLOPER12, содержащие одномерные массивы, содержащие асинхронные дескрипторы и возвращаемые значения. Эти массивы должны находиться в том же порядке, что и Excel, чтобы они правильно совпадали с асинхронным дескриптором и соответствующим значением. 
  
В приведенном ниже примере показано, как выполнить пакетный вызов с помощью **ксласинкретурн**.
  
```cpp
int batchSize = 10;
    LPXLOPER12 pHandles = new XLOPER12[batchSize];
    LPXLOPER12 pValues = new XLOPER12[batchSize];
    /*Add code to fill in LPXLOPER12 arrays (pHandles and pValues)
    with the XOPER12 structures that contain the asynchronous handles
    and values, in respective order*/
    //Create an XLOPER12 of type xltypeMulti, and fill the Handle array
    XLOPER12 handleArray;
    handleArray.xltype = xltypeMulti;
    handleArray.val.array.rows = 1;
    handleArray.val.array.columns = (COL)batchSize;
    handleArray.val.array.lparray = pHandles;
    
    //Create an XLOPER12 if type xltypeMulti, and fill the Values array
    XLOPER12 valueArray;
    valueArray.xltype = xltypeMulti;
    valueArray.val.array.rows = 1;
    valueArray.val.array.columns = (COL)batchSize;
    valueArray.val.array.lparray = pValues;
    //Make the callback with the return value
    int ret = Excel12(xlAsyncReturn, 0, 2, &amp;handleArray, &amp;valueArray);
    //Add code to free the allocated memory here (pHandles, pValues, valueArray, handleArray)
    return ret;

```

## <a name="see-also"></a>См. также

- [Асинхронные пользовательские функции](asynchronous-user-defined-functions.md)

