---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- функция xlsheetid [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807366"
---
# <a name="xlsheetid"></a><span data-ttu-id="c618a-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="c618a-104">xlSheetId</span></span>

<span data-ttu-id="c618a-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c618a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c618a-106">Находит идентификатор листа именованные таблицы для создания внешних ссылок.</span><span class="sxs-lookup"><span data-stu-id="c618a-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="c618a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c618a-107">Parameters</span></span>

<span data-ttu-id="c618a-108">_pxSheetName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="c618a-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="c618a-109">(Необязательно).</span><span class="sxs-lookup"><span data-stu-id="c618a-109">(Optional).</span></span> <span data-ttu-id="c618a-110">Имя из книг и листов, которое можно найти сведения о.</span><span class="sxs-lookup"><span data-stu-id="c618a-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="c618a-111">Если этот параметр опущен, функция **xlSheetId** возвращает идентификатор листа листа активный (передний план).</span><span class="sxs-lookup"><span data-stu-id="c618a-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="c618a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

<span data-ttu-id="c618a-113">Возвращает идентификатор листа в _pxRes -\>val.mref.idSheet_.</span><span class="sxs-lookup"><span data-stu-id="c618a-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c618a-114">_PxRes -\>val.mref.lpmref_ указатель массив имеет значение NULL после этого вызова, чтобы не требуется для вызова **xlFree** для освобождения объем памяти, этот тип обычно содержит, хотя это и полностью безопасно.</span><span class="sxs-lookup"><span data-stu-id="c618a-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c618a-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="c618a-115">Remarks</span></span>

<span data-ttu-id="c618a-116">Книга, содержащая указанный лист должен быть открыт для использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="c618a-116">The workbook containing the specified sheet must be open to use this function.</span></span> <span data-ttu-id="c618a-117">Нет возможности для создания ссылку неоткрытый книги из библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="c618a-117">There is no way to construct a reference to an unopened workbook from a DLL.</span></span> <span data-ttu-id="c618a-118">Дополнительные сведения об использовании **xlSheetId** для создания ссылки на [Управление памятью в Excel](memory-management-in-excel.md) для примеров конструкции **xltypeRef** см.</span><span class="sxs-lookup"><span data-stu-id="c618a-118">For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c618a-119">Пример</span><span class="sxs-lookup"><span data-stu-id="c618a-119">Example</span></span>

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c618a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c618a-120">See also</span></span>

- [<span data-ttu-id="c618a-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="c618a-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="c618a-122">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="c618a-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

