---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 32d5075af34cda9753c5d082bd4ab00afab1ecff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310250"
---
# <a name="xlasyncreturn"></a><span data-ttu-id="65220-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="65220-103">xlAsyncReturn</span></span>

<span data-ttu-id="65220-104">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="65220-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="65220-105">Используется для возврата результата асинхронной пользовательской функции (UDF).</span><span class="sxs-lookup"><span data-stu-id="65220-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="65220-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="65220-106">Parameters</span></span>

<span data-ttu-id="65220-107">_пксасинчандле_ (**кслтипебигдата**)</span><span class="sxs-lookup"><span data-stu-id="65220-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="65220-108">Асинхронный дескриптор объекта UDF, в который возвращается результат.</span><span class="sxs-lookup"><span data-stu-id="65220-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="65220-109">_Пксфунктионресулт_</span><span class="sxs-lookup"><span data-stu-id="65220-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="65220-110">Возвращаемое значение UDF.</span><span class="sxs-lookup"><span data-stu-id="65220-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="65220-111">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65220-111">Property value/Return value</span></span>

<span data-ttu-id="65220-112">В случае успеха возвращает **значение true** (**кслтипебул**).</span><span class="sxs-lookup"><span data-stu-id="65220-112">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="65220-113">В случае неудачной попытки возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="65220-113">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65220-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="65220-114">Remarks</span></span>

<span data-ttu-id="65220-115">**ксласинкретурн** — единственный обратный вызов, позволяющий использовать в процессе пересчета потоки, не связанные с вычислениями.</span><span class="sxs-lookup"><span data-stu-id="65220-115">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation.</span></span> <span data-ttu-id="65220-116">Асинхронная часть асинхронной UDF не должна выполнять обратные вызовы, кроме **ксласинкретурн**.</span><span class="sxs-lookup"><span data-stu-id="65220-116">The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**.</span></span> <span data-ttu-id="65220-117">XLL должен освободить память, выделенную для хранения возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="65220-117">The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="65220-118">Параметры _пксасинчандле_ и _пксфунктионресулт_ также могут иметь тип **xltypeMulti** при использовании для возвращения массива дескрипторов и соответствующих значений в едином обратном вызове.</span><span class="sxs-lookup"><span data-stu-id="65220-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="65220-119">При использовании одного обратного вызова передайте LPXLOPER12, который указывает на структуры XLOPER12, содержащие одномерные массивы, содержащие асинхронные дескрипторы и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="65220-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="65220-120">Эти массивы должны находиться в том же порядке, что и Excel, чтобы они правильно совпадали с асинхронным дескриптором и соответствующим значением.</span><span class="sxs-lookup"><span data-stu-id="65220-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="65220-121">В приведенном ниже примере показано, как выполнить пакетный вызов с помощью **ксласинкретурн**.</span><span class="sxs-lookup"><span data-stu-id="65220-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="65220-122">См. также</span><span class="sxs-lookup"><span data-stu-id="65220-122">See also</span></span>

- [<span data-ttu-id="65220-123">Асинхронные пользовательские функции</span><span class="sxs-lookup"><span data-stu-id="65220-123">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

