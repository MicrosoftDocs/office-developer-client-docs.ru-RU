---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- кслруннингонклустер
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f5c630c73899b07e2727a7d42b18eb1891797bab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418290"
---
# <a name="xlrunningoncluster"></a><span data-ttu-id="44912-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="44912-104">xlRunningOnCluster</span></span>

<span data-ttu-id="44912-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="44912-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="44912-106">Возвращает значение, которое указывает, выполняется ли пользовательская функция в кластере.</span><span class="sxs-lookup"><span data-stu-id="44912-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="44912-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="44912-107">Parameters</span></span>

<span data-ttu-id="44912-108">У этой функции нет аргументов.</span><span class="sxs-lookup"><span data-stu-id="44912-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="44912-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44912-109">Return value</span></span>

<span data-ttu-id="44912-110">Если функция выполняется в процессе Excel, возвращает значение 0 в **XLOPER12** типа **кслтипеинт**.</span><span class="sxs-lookup"><span data-stu-id="44912-110">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**.</span></span> <span data-ttu-id="44912-111">Если функция выполняется на кластере, тип возвращаемого значения и его значение определяются поставщиком соединителей кластера.</span><span class="sxs-lookup"><span data-stu-id="44912-111">If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="44912-112">Требования</span><span class="sxs-lookup"><span data-stu-id="44912-112">Requirements</span></span>

<span data-ttu-id="44912-113">Эта функция определена в файле заголовка Xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="44912-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44912-114">См. также</span><span class="sxs-lookup"><span data-stu-id="44912-114">See also</span></span>

- [<span data-ttu-id="44912-115">Функции защиты кластеров</span><span class="sxs-lookup"><span data-stu-id="44912-115">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
- [<span data-ttu-id="44912-116">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="44912-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

