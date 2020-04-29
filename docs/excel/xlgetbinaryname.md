---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- Функция кслжетбинаринаме [Excel 2007]
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
# <a name="xlgetbinaryname"></a><span data-ttu-id="28432-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="28432-104">xlGetBinaryName</span></span>

<span data-ttu-id="28432-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="28432-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="28432-106">Используется для возврата дескриптора для данных, сохраненных [функцией кслдефинебинаринаме](xldefinebinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="28432-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="28432-107">Данные с определенным двоичным именем сохраняются вместе с книгой и могут быть доступны по имени в любое время.</span><span class="sxs-lookup"><span data-stu-id="28432-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="28432-108">Дополнительные сведения [см. в разделе "](known-issues-in-excel-xll-development.md)ограничения области двоичных имен".</span><span class="sxs-lookup"><span data-stu-id="28432-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="28432-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="28432-109">Parameters</span></span>

<span data-ttu-id="28432-110">_пксрес_ (**кслтипебигдата** или **кслтипирр**)</span><span class="sxs-lookup"><span data-stu-id="28432-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="28432-111">Структура бигдата, указывающая извлеченные данные или ошибка — не удается получить данные или имя не определено.</span><span class="sxs-lookup"><span data-stu-id="28432-111">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined.</span></span> <span data-ttu-id="28432-112">Когда функция возвращает значение, элемент **хдата** в элементе **XLOPER**/ **XLOPER12** содержит дескриптор для именованных данных.</span><span class="sxs-lookup"><span data-stu-id="28432-112">When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.</span></span>  <span data-ttu-id="28432-113">_пксрес_ следует освобождать в вызове **кслфри** , когда он больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="28432-113">_pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="28432-114">_пкснаме_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="28432-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="28432-115">Строка, указывающая имя данных.</span><span class="sxs-lookup"><span data-stu-id="28432-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28432-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="28432-116">Remarks</span></span>

<span data-ttu-id="28432-117">Microsoft Excel владеет дескриптором памяти, возвращаемым в **хдата**.</span><span class="sxs-lookup"><span data-stu-id="28432-117">Microsoft Excel owns the memory handle returned in **hdata**.</span></span> <span data-ttu-id="28432-118">В Windows дескриптор является глобальным дескриптором памяти (выделенный функцией **глобалаллок** ).</span><span class="sxs-lookup"><span data-stu-id="28432-118">In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="28432-119">См. также</span><span class="sxs-lookup"><span data-stu-id="28432-119">See also</span></span>

- [<span data-ttu-id="28432-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="28432-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="28432-121">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="28432-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

