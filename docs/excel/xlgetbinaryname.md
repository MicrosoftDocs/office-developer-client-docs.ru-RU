---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- функция xlgetbinaryname [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807355"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="48d6c-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="48d6c-104">xlGetBinaryName</span></span>

<span data-ttu-id="48d6c-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="48d6c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="48d6c-106">Используется для возврата дескриптор для данных, сохраненных с помощью [функции xlDefineBinaryName](xldefinebinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="48d6c-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="48d6c-107">Данные с заданным именем двоичные сохраняется вместе с книгой и может быть доступен по имени в любое время.</span><span class="sxs-lookup"><span data-stu-id="48d6c-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="48d6c-108">Для получения дополнительных сведений см раздел «Имя ограничения области двоичный» [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="48d6c-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="48d6c-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="48d6c-109">Parameters</span></span>

<span data-ttu-id="48d6c-110">_pxRes_ (**xltypeBigData** или **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="48d6c-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="48d6c-111">Не удалось получить Bigdata структура извлеченные данные или ошибка является данных или имя не определено.</span><span class="sxs-lookup"><span data-stu-id="48d6c-111">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined.</span></span> <span data-ttu-id="48d6c-112">Если функция возвращает, **hdata** членом **XLOPER**/ **XLOPER12** содержит маркер для именованного данных.</span><span class="sxs-lookup"><span data-stu-id="48d6c-112">When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.</span></span>  <span data-ttu-id="48d6c-113">_pxRes_ нужно освободить в вызове **xlFree** больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="48d6c-113">_pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="48d6c-114">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="48d6c-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="48d6c-115">Строка, задающая имя данных.</span><span class="sxs-lookup"><span data-stu-id="48d6c-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48d6c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="48d6c-116">Remarks</span></span>

<span data-ttu-id="48d6c-117">Microsoft Excel несет ответственность за памяти дескриптор, возвращенный в **hdata**.</span><span class="sxs-lookup"><span data-stu-id="48d6c-117">Microsoft Excel owns the memory handle returned in **hdata**.</span></span> <span data-ttu-id="48d6c-118">В Windows дескриптор — это глобальный дескриптор памяти (выделены функцией **GlobalAlloc** ).</span><span class="sxs-lookup"><span data-stu-id="48d6c-118">In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48d6c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="48d6c-119">See also</span></span>

- [<span data-ttu-id="48d6c-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="48d6c-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="48d6c-121">Функции интерфейса API для C, которые могут вызываться только из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="48d6c-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

