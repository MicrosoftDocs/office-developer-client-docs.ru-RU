---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e7ba37629ff2198339394448410ffd16477d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807340"
---
# <a name="xlasyncreturn"></a><span data-ttu-id="82be9-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="82be9-103">xlAsyncReturn</span></span>

<span data-ttu-id="82be9-104">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="82be9-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="82be9-105">Используется для возвращения результата асинхронные пользовательские функции (UDF).</span><span class="sxs-lookup"><span data-stu-id="82be9-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="82be9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82be9-106">Parameters</span></span>

<span data-ttu-id="82be9-107">_pxAsyncHandle_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="82be9-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="82be9-108">Асинхронный дескриптор UDF, для которого возвращается результат.</span><span class="sxs-lookup"><span data-stu-id="82be9-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="82be9-109">_pxFunctionResult_</span><span class="sxs-lookup"><span data-stu-id="82be9-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="82be9-110">Возвращаемое значение пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="82be9-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="82be9-111">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82be9-111">Property value/Return value</span></span>

<span data-ttu-id="82be9-112">В случае успешного выполнения возвращает **значение TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="82be9-112">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="82be9-113">В случае неудачи возвращает **значение FALSE**.</span><span class="sxs-lookup"><span data-stu-id="82be9-113">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82be9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="82be9-114">Remarks</span></span>

<span data-ttu-id="82be9-115">**xlAsyncReturn** является единственным обратного вызова позволяет Excel не вычислений потоков во время пересчета.</span><span class="sxs-lookup"><span data-stu-id="82be9-115">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation.</span></span> <span data-ttu-id="82be9-116">Асинхронные часть асинхронных пользовательских Функций нельзя выполнять любые обратных вызовов, отличный от **xlAsyncReturn**.</span><span class="sxs-lookup"><span data-stu-id="82be9-116">The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**.</span></span> <span data-ttu-id="82be9-117">XLL необходимо освободить память для хранения возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="82be9-117">The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="82be9-118">Параметры _pxAsyncHandle_ и _pxFunctionResult_ также могут иметь тип **xltypeMulti** при использовании возвращает массив значками и соответствующие значения в одном обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="82be9-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="82be9-119">При использовании одного обратного вызова, передайте LPXLOPER12, указывающий на XLOPER12 структуры, содержащие одну двухмерные массивы, которые содержат асинхронных значками и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="82be9-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="82be9-120">Эти массивы должны находиться в том же порядке для правильно match асинхронных дескриптора с его соответствующее значение в Excel.</span><span class="sxs-lookup"><span data-stu-id="82be9-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="82be9-121">В следующем примере показано, как можно усовершенствовать вызовы с использованием **xlAsyncReturn**пакета.</span><span class="sxs-lookup"><span data-stu-id="82be9-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="82be9-122">См. также</span><span class="sxs-lookup"><span data-stu-id="82be9-122">See also</span></span>

- [<span data-ttu-id="82be9-123">Асинхронные пользовательские функции</span><span class="sxs-lookup"><span data-stu-id="82be9-123">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

