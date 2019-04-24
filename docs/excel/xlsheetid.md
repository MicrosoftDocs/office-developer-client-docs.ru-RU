---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- Функция кслшитид [Excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310306"
---
# <a name="xlsheetid"></a><span data-ttu-id="81346-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="81346-104">xlSheetId</span></span>

<span data-ttu-id="81346-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="81346-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="81346-106">Находит идентификатор именованного листа, чтобы создать внешние ссылки.</span><span class="sxs-lookup"><span data-stu-id="81346-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="81346-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="81346-107">Parameters</span></span>

<span data-ttu-id="81346-108">_пксшитнаме_ (**кслтипестр**)</span><span class="sxs-lookup"><span data-stu-id="81346-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="81346-109">(НеОбязательно).</span><span class="sxs-lookup"><span data-stu-id="81346-109">(Optional).</span></span> <span data-ttu-id="81346-110">Название книги и листа, о которых вы хотите узнать.</span><span class="sxs-lookup"><span data-stu-id="81346-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="81346-111">Если этот параметр опущен, функция **кслшитид** возвращает идентификатор активного (переднего) листа.</span><span class="sxs-lookup"><span data-stu-id="81346-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="81346-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81346-112">Return value</span></span>

<span data-ttu-id="81346-113">Возвращает идентификатор листа в _пксрес —\>Val. мреф. идшит_.</span><span class="sxs-lookup"><span data-stu-id="81346-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="81346-114">После этого вызова в указателе массива _пксрес-\>Val. мреф. лпмреф_ ЗАдается значение null, поэтому нет необходимости вызывать **кслфри** , чтобы освободить память, которую обычно содержит этот тип, хотя это совершенно безопасно для этого.</span><span class="sxs-lookup"><span data-stu-id="81346-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="81346-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="81346-115">Remarks</span></span>

<span data-ttu-id="81346-116">Чтобы использовать эту функцию, необходимо открыть книгу, содержащую указанный лист.</span><span class="sxs-lookup"><span data-stu-id="81346-116">The workbook containing the specified sheet must be open to use this function.</span></span> <span data-ttu-id="81346-117">Невозможно создать ссылку на неоткрытую книгу из библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="81346-117">There is no way to construct a reference to an unopened workbook from a DLL.</span></span> <span data-ttu-id="81346-118">Дополнительные сведения об использовании **кслшитид** для создания ссылок приведены в статье [Управление памятью в Excel](memory-management-in-excel.md) для примера конструкции **кслтипереф** .</span><span class="sxs-lookup"><span data-stu-id="81346-118">For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="81346-119">Пример</span><span class="sxs-lookup"><span data-stu-id="81346-119">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="81346-120">См. также</span><span class="sxs-lookup"><span data-stu-id="81346-120">See also</span></span>

- [<span data-ttu-id="81346-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="81346-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="81346-122">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="81346-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

