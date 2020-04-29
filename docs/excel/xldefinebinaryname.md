---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- Функция кслдефинебинаринаме [Excel 2007]
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
# <a name="xldefinebinaryname"></a><span data-ttu-id="66d84-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="66d84-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="66d84-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="66d84-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="66d84-106">Используется для выделения постоянного хранилища для **кслтипебигдата** **XLOPER**/ **.**</span><span class="sxs-lookup"><span data-stu-id="66d84-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="66d84-107">Данные с определенным двоичным именем сохраняются вместе с книгой и могут быть доступны по имени в любое время.</span><span class="sxs-lookup"><span data-stu-id="66d84-107">Data with a defined binary name is saved with the workbook, and can be accessed by name at any time.</span></span> <span data-ttu-id="66d84-108">Дополнительные сведения [см. в разделе "](known-issues-in-excel-xll-development.md)ограничения области двоичных имен".</span><span class="sxs-lookup"><span data-stu-id="66d84-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="66d84-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="66d84-109">Parameters</span></span>

 <span data-ttu-id="66d84-110">_пкснаме_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="66d84-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="66d84-111">Строка, указывающая имя данных.</span><span class="sxs-lookup"><span data-stu-id="66d84-111">A string specifying the name of the data.</span></span> <span data-ttu-id="66d84-112">В этой строке действуют те же ограничения именования, что и в определенных именах.</span><span class="sxs-lookup"><span data-stu-id="66d84-112">The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="66d84-113">_пксдата_ (**кслтипебигдата**)</span><span class="sxs-lookup"><span data-stu-id="66d84-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="66d84-114">Структура бигдата, указывающая сохраняемые данные.</span><span class="sxs-lookup"><span data-stu-id="66d84-114">Bigdata structure specifying the data to be stored.</span></span> <span data-ttu-id="66d84-115">При вызове этой функции элемент **лпбдата** структуры **бигдата** должен указать данные, для которых определяется имя, а элемент **КБДата** должен содержать длину данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="66d84-115">When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="66d84-116">Если аргумент _пксдата_ не указан (**кслтипемиссинг**), удаляется именованное выделение, указанное с помощью _пкснаме_ .</span><span class="sxs-lookup"><span data-stu-id="66d84-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66d84-117">См. также</span><span class="sxs-lookup"><span data-stu-id="66d84-117">See also</span></span>



[<span data-ttu-id="66d84-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="66d84-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="66d84-119">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="66d84-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="66d84-120">Известные проблемы разработки XLL в Excel</span><span class="sxs-lookup"><span data-stu-id="66d84-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

