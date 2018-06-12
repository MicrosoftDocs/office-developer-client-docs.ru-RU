---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e7ba37629ff2198339394448410ffd16477d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807340"
---
# <a name="xlasyncreturn"></a>xlAsyncReturn

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Используется для возвращения результата асинхронные пользовательские функции (UDF).
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Parameters

_pxAsyncHandle_ (**xltypeBigData**)
  
Асинхронный дескриптор UDF, для которого возвращается результат.
  
_pxFunctionResult_
  
Возвращаемое значение пользовательской функции.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

В случае успешного выполнения возвращает **значение TRUE** (**xltypeBool**). В случае неудачи возвращает **значение FALSE**.
  
## <a name="remarks"></a>Замечания

**xlAsyncReturn** является единственным обратного вызова позволяет Excel не вычислений потоков во время пересчета. Асинхронные часть асинхронных пользовательских Функций нельзя выполнять любые обратных вызовов, отличный от **xlAsyncReturn**. XLL необходимо освободить память для хранения возвращаемого значения.
  
Параметры _pxAsyncHandle_ и _pxFunctionResult_ также могут иметь тип **xltypeMulti** при использовании возвращает массив значками и соответствующие значения в одном обратного вызова. При использовании одного обратного вызова, передайте LPXLOPER12, указывающий на XLOPER12 структуры, содержащие одну двухмерные массивы, которые содержат асинхронных значками и возвращаемые значения. Эти массивы должны находиться в том же порядке для правильно match асинхронных дескриптора с его соответствующее значение в Excel. 
  
В следующем примере показано, как можно усовершенствовать вызовы с использованием **xlAsyncReturn**пакета.
  
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

