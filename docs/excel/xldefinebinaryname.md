---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- функция xlDefineBinaryName [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807339"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="1d5ff-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="1d5ff-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="1d5ff-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1d5ff-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1d5ff-106">Используется для выделения постоянное хранилище для **xltypeBigData** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="1d5ff-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="1d5ff-107">Данные с заданным именем двоичные сохраняется вместе с книгой и может осуществляться по имени в любое время.</span><span class="sxs-lookup"><span data-stu-id="1d5ff-107">Data with a defined binary name is saved with the workbook, and can be accessed by name at any time.</span></span> <span data-ttu-id="1d5ff-108">Для получения дополнительных сведений см «двоичный имя области» в разделе [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="1d5ff-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="1d5ff-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="1d5ff-109">Parameters</span></span>

 <span data-ttu-id="1d5ff-110">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="1d5ff-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="1d5ff-111">Строка, задающая имя данных.</span><span class="sxs-lookup"><span data-stu-id="1d5ff-111">A string specifying the name of the data.</span></span> <span data-ttu-id="1d5ff-112">Строка — это может быть таким же ограничения именования следующим определенных имен.</span><span class="sxs-lookup"><span data-stu-id="1d5ff-112">The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="1d5ff-113">_pxData_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="1d5ff-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="1d5ff-114">Bigdata структура данных для хранения.</span><span class="sxs-lookup"><span data-stu-id="1d5ff-114">Bigdata structure specifying the data to be stored.</span></span> <span data-ttu-id="1d5ff-115">При вызове этой функции должны указывать член **lpbData** **bigdata** структуры данных, для которого определяется имя и член **cbData** должен содержать длина данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="1d5ff-115">When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="1d5ff-116">Если аргумент _pxData_ не указанного (**xltypeMissing**), именованные распределения, указанного идентификатором _pxName_ будет удален.</span><span class="sxs-lookup"><span data-stu-id="1d5ff-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d5ff-117">См. также</span><span class="sxs-lookup"><span data-stu-id="1d5ff-117">See also</span></span>



[<span data-ttu-id="1d5ff-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="1d5ff-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="1d5ff-119">Функции интерфейса API для C, которые могут вызываться только из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="1d5ff-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="1d5ff-120">Известные проблемы, возникающие при разработке XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="1d5ff-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

