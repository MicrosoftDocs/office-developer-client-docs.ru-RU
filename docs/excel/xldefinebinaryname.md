---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- функция xldefinebinaryname [Excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3c7fc4f6b6fc7179c1ca84043895273b2781f8b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430254"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="1c3b1-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="1c3b1-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="1c3b1-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1c3b1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1c3b1-106">Используется для выделения постоянного хранилища **для xltypeBigData** **XLOPER** /  **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="1c3b1-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="1c3b1-107">Данные с определенным двоичным именем сохраняются в книге и могут быть доступны по имени в любое время.</span><span class="sxs-lookup"><span data-stu-id="1c3b1-107">Data with a defined binary name is saved with the workbook, and can be accessed by name at any time.</span></span> <span data-ttu-id="1c3b1-108">Дополнительные сведения см. в "Двоичное ограничение области имен" в известных проблемах [Excel XLL Development.](known-issues-in-excel-xll-development.md)</span><span class="sxs-lookup"><span data-stu-id="1c3b1-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="1c3b1-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="1c3b1-109">Parameters</span></span>

 <span data-ttu-id="1c3b1-110">_pxName_ **(xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="1c3b1-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="1c3b1-111">Строка с указанием имени данных.</span><span class="sxs-lookup"><span data-stu-id="1c3b1-111">A string specifying the name of the data.</span></span> <span data-ttu-id="1c3b1-112">Строка подвержена тем же ограничениям именования, что и определенные имена.</span><span class="sxs-lookup"><span data-stu-id="1c3b1-112">The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="1c3b1-113">_pxData_ **(xltypeBigData)**</span><span class="sxs-lookup"><span data-stu-id="1c3b1-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="1c3b1-114">Структура bigdata, указывая данные, которые будут храниться.</span><span class="sxs-lookup"><span data-stu-id="1c3b1-114">Bigdata structure specifying the data to be stored.</span></span> <span data-ttu-id="1c3b1-115">При вызове этой функции член **lpbData** структуры **bigdata** должен указать на данные, для которых определяется имя, а член **cbData** должен содержать длину данных в bytes.</span><span class="sxs-lookup"><span data-stu-id="1c3b1-115">When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="1c3b1-116">Если аргумент  _pxData_ не указан **(xltypeMissing),** то указанное  _pxName_ выделено.</span><span class="sxs-lookup"><span data-stu-id="1c3b1-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1c3b1-117">См. также</span><span class="sxs-lookup"><span data-stu-id="1c3b1-117">See also</span></span>



[<span data-ttu-id="1c3b1-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="1c3b1-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="1c3b1-119">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="1c3b1-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="1c3b1-120">Известные проблемы в Excel XLL</span><span class="sxs-lookup"><span data-stu-id="1c3b1-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

