---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f42ccbeb94e1fc6b6cf880f1b32ee1bfeb24997e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807386"
---
# <a name="xlrunningoncluster"></a><span data-ttu-id="6e521-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="6e521-104">xlRunningOnCluster</span></span>

<span data-ttu-id="6e521-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6e521-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6e521-106">Возвращает значение, которое указывает, выполняется ли пользовательской функции в кластере.</span><span class="sxs-lookup"><span data-stu-id="6e521-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="6e521-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e521-107">Parameters</span></span>

<span data-ttu-id="6e521-108">Эта функция не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="6e521-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6e521-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="6e521-110">Если функция выполняется в процессе Excel, возвращает 0 в **XLOPER12** из типа **xlTypeInt**.</span><span class="sxs-lookup"><span data-stu-id="6e521-110">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**.</span></span> <span data-ttu-id="6e521-111">Если функция выполняется в кластере, тип возвращаемого значения и значение определяется поставщиком соединитель кластера.</span><span class="sxs-lookup"><span data-stu-id="6e521-111">If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="6e521-112">Требования</span><span class="sxs-lookup"><span data-stu-id="6e521-112">Requirements</span></span>

<span data-ttu-id="6e521-113">Эта функция определяется в файле Xlcall.h заголовка.</span><span class="sxs-lookup"><span data-stu-id="6e521-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e521-114">См. также</span><span class="sxs-lookup"><span data-stu-id="6e521-114">See also</span></span>

- [<span data-ttu-id="6e521-115">Функции защиты кластеров</span><span class="sxs-lookup"><span data-stu-id="6e521-115">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
- [<span data-ttu-id="6e521-116">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="6e521-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

