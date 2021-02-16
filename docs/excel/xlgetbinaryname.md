---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- Функция xlgetbinaryname [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6d063213e3f83451e8a072e71f0878174214f73e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412466"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="55342-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="55342-104">xlGetBinaryName</span></span>

<span data-ttu-id="55342-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="55342-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="55342-106">Используется для возврата работки данных, сохраненных функцией [xlDefineBinaryName.](xldefinebinaryname.md)</span><span class="sxs-lookup"><span data-stu-id="55342-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="55342-107">Данные с определенным двоичным именем сохраняются в книге и доступны по имени в любое время.</span><span class="sxs-lookup"><span data-stu-id="55342-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="55342-108">Дополнительные сведения см. в подразданном "Binary name Scope Limitation" (Ограничение области двоичных имен) в подраздах ["Известные проблемы" в разработке XLL для Excel.](known-issues-in-excel-xll-development.md)</span><span class="sxs-lookup"><span data-stu-id="55342-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="55342-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="55342-109">Parameters</span></span>

<span data-ttu-id="55342-110">_pxRes_ (**xltypeBigData** или **xltypeErr)**</span><span class="sxs-lookup"><span data-stu-id="55342-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="55342-111">Структура Bigdata, указывая извлеченные данные или ошибка, — это то, что данные не удалось извлечь или имя не определено.</span><span class="sxs-lookup"><span data-stu-id="55342-111">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined.</span></span> <span data-ttu-id="55342-112">Когда функция возвращается, член **hdata** **XLOPER** /  **XLOPER12** содержит лад для именуемых данных.</span><span class="sxs-lookup"><span data-stu-id="55342-112">When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.</span></span>  <span data-ttu-id="55342-113">_pxRes_ следует освободить в вызове **xlFree,** когда это больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="55342-113">_pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="55342-114">_pxName_ (**xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="55342-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="55342-115">Строка, указывая имя данных.</span><span class="sxs-lookup"><span data-stu-id="55342-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="55342-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="55342-116">Remarks</span></span>

<span data-ttu-id="55342-117">Microsoft Excel является владельцем окна памяти, возвращаемой **в формате hdata.**</span><span class="sxs-lookup"><span data-stu-id="55342-117">Microsoft Excel owns the memory handle returned in **hdata**.</span></span> <span data-ttu-id="55342-118">В Windows handle — это глобальный работник памяти (выделенный функцией **GlobalAlloc).**</span><span class="sxs-lookup"><span data-stu-id="55342-118">In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55342-119">См. также</span><span class="sxs-lookup"><span data-stu-id="55342-119">See also</span></span>

- [<span data-ttu-id="55342-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="55342-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="55342-121">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="55342-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

