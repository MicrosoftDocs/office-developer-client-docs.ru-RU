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
# <a name="xlasyncreturn"></a><span data-ttu-id="d4b48-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="d4b48-103">xlAsyncReturn</span></span>

<span data-ttu-id="d4b48-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d4b48-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d4b48-105">Используется для возврата результата асинхронной функции, определенной пользователем (UDF).</span><span class="sxs-lookup"><span data-stu-id="d4b48-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="d4b48-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d4b48-106">Parameters</span></span>

<span data-ttu-id="d4b48-107">_pxAsyncHandle_ **(xltypeBigData)**</span><span class="sxs-lookup"><span data-stu-id="d4b48-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="d4b48-108">Асинхронная ручка UDF, в которую возвращается результат.</span><span class="sxs-lookup"><span data-stu-id="d4b48-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="d4b48-109">_pxFunctionResult_</span><span class="sxs-lookup"><span data-stu-id="d4b48-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="d4b48-110">Возвращаемая стоимость UDF.</span><span class="sxs-lookup"><span data-stu-id="d4b48-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d4b48-111">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4b48-111">Property value/Return value</span></span>

<span data-ttu-id="d4b48-112">В случае успешной работы **возвращает TRUE** **(xltypeBool).**</span><span class="sxs-lookup"><span data-stu-id="d4b48-112">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="d4b48-113">В случае неудачи возвращает **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="d4b48-113">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d4b48-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d4b48-114">Remarks</span></span>

<span data-ttu-id="d4b48-115">**xlAsyncReturn** — это единственная возможность Excel для потоков без вычисления во время пересчета.</span><span class="sxs-lookup"><span data-stu-id="d4b48-115">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation.</span></span> <span data-ttu-id="d4b48-116">Асинхронная часть асинхронного UDF не должна выполнять никаких откатов, кроме **xlAsyncReturn.**</span><span class="sxs-lookup"><span data-stu-id="d4b48-116">The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**.</span></span> <span data-ttu-id="d4b48-117">XLL должен освободить память, выделенную для удержания возвращаемой суммы.</span><span class="sxs-lookup"><span data-stu-id="d4b48-117">The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="d4b48-118">Параметры _pxAsyncHandle_ и  _pxFunctionResult_ также могут быть типа **xltypeMulti** при возвращении массива рули и соответствующих значений в одном обратном вызове.</span><span class="sxs-lookup"><span data-stu-id="d4b48-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="d4b48-119">При использовании единого обратного вызова передай LPXLOPER12, который указывает на структуры XLOPER12, содержащие одномерные массивы, содержащие асинхронные ручки и значения возврата.</span><span class="sxs-lookup"><span data-stu-id="d4b48-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="d4b48-120">Эти массивы должны быть в том же порядке, чтобы Excel правильно соответствовать асинхронной ручке с соответствующим значением.</span><span class="sxs-lookup"><span data-stu-id="d4b48-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="d4b48-121">В следующем примере показано, как можно сделать пакетный вызов с **помощью xlAsyncReturn.**</span><span class="sxs-lookup"><span data-stu-id="d4b48-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="d4b48-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d4b48-122">See also</span></span>

- [<span data-ttu-id="d4b48-123">Асинхронные пользовательские функции</span><span class="sxs-lookup"><span data-stu-id="d4b48-123">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

