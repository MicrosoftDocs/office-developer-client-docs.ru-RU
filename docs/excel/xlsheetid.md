---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- xlsheetid function [Excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428433"
---
# <a name="xlsheetid"></a><span data-ttu-id="2272c-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="2272c-104">xlSheetId</span></span>

<span data-ttu-id="2272c-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2272c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2272c-106">Находит имя листа с именем листа для построения внешних ссылок.</span><span class="sxs-lookup"><span data-stu-id="2272c-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="2272c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="2272c-107">Parameters</span></span>

<span data-ttu-id="2272c-108">_pxSheetName_ **(xltypeStr)**</span><span class="sxs-lookup"><span data-stu-id="2272c-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="2272c-109">(Необязательный).</span><span class="sxs-lookup"><span data-stu-id="2272c-109">(Optional).</span></span> <span data-ttu-id="2272c-110">Имя книги и листа, о чем вы хотите узнать.</span><span class="sxs-lookup"><span data-stu-id="2272c-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="2272c-111">При опущении **функция xlSheetId** возвращает ID листа активного (переднего) листа.</span><span class="sxs-lookup"><span data-stu-id="2272c-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="2272c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2272c-112">Return value</span></span>

<span data-ttu-id="2272c-113">Возвращает ID листа в  _pxRes-val.mref.idSheet \>_.</span><span class="sxs-lookup"><span data-stu-id="2272c-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2272c-114">Указатель  _массива pxRes-val.mref.lpmref \>_ установлен в NULL после этого вызова, чтобы не было необходимости вызывать **xlFree,** чтобы освободить память, которая обычно содержится в этом типе, хотя это совершенно безопасно.</span><span class="sxs-lookup"><span data-stu-id="2272c-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2272c-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="2272c-115">Remarks</span></span>

<span data-ttu-id="2272c-116">Книга, содержащая указанный лист, должна быть открыта для использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="2272c-116">The workbook containing the specified sheet must be open to use this function.</span></span> <span data-ttu-id="2272c-117">Нет способа создать ссылку на незапертую книгу из DLL.</span><span class="sxs-lookup"><span data-stu-id="2272c-117">There is no way to construct a reference to an unopened workbook from a DLL.</span></span> <span data-ttu-id="2272c-118">Дополнительные сведения об использовании **xlSheetId** для создания ссылок [см.](memory-management-in-excel.md) в Excel примере **конструкции xltypeRef.**</span><span class="sxs-lookup"><span data-stu-id="2272c-118">For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2272c-119">Пример</span><span class="sxs-lookup"><span data-stu-id="2272c-119">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="2272c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="2272c-120">See also</span></span>

- [<span data-ttu-id="2272c-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="2272c-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="2272c-122">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="2272c-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

