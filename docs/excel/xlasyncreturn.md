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
  
Используется для возврата результата асинхронной функции, определенной пользователем (UDF).
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Parameters

_pxAsyncHandle_ **(xltypeBigData)**
  
Асинхронная ручка UDF, в которую возвращается результат.
  
_pxFunctionResult_
  
Возвращаемая стоимость UDF.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

В случае успешной работы **возвращает TRUE** **(xltypeBool).** В случае неудачи возвращает **FALSE.**
  
## <a name="remarks"></a>Примечания

**xlAsyncReturn** — это единственная возможность Excel для потоков без вычисления во время пересчета. Асинхронная часть асинхронного UDF не должна выполнять никаких откатов, кроме **xlAsyncReturn.** XLL должен освободить память, выделенную для удержания возвращаемой суммы.
  
Параметры _pxAsyncHandle_ и  _pxFunctionResult_ также могут быть типа **xltypeMulti** при возвращении массива рули и соответствующих значений в одном обратном вызове. При использовании единого обратного вызова передай LPXLOPER12, который указывает на структуры XLOPER12, содержащие одномерные массивы, содержащие асинхронные ручки и значения возврата. Эти массивы должны быть в том же порядке, чтобы Excel правильно соответствовать асинхронной ручке с соответствующим значением. 
  
В следующем примере показано, как можно сделать пакетный вызов с **помощью xlAsyncReturn.**
  
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

