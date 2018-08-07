---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- функция xlsheetnm [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 815565d886b1aea203f6b3b9774325d6b534abd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807376"
---
# <a name="xlsheetnm"></a><span data-ttu-id="cea86-104">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="cea86-104">xlSheetNm</span></span>

<span data-ttu-id="cea86-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cea86-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cea86-106">Возвращает имя листа электронной таблицы или макрос из его идентификатор внутреннего листа, содержатся в внешней ссылки или имя активного листа, если передается внутреннюю ссылку.</span><span class="sxs-lookup"><span data-stu-id="cea86-106">Returns the name of a worksheet or macro sheet from its internal sheet ID contained within an external reference, or the name of the current sheet if passed an internal reference.</span></span>
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a><span data-ttu-id="cea86-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cea86-107">Parameters</span></span>

<span data-ttu-id="cea86-108">_pxExtref_ (**xltypeRef** или **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="cea86-108">_pxExtref_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="cea86-109">Ссылка на лист, имя которого вы хотите.</span><span class="sxs-lookup"><span data-stu-id="cea86-109">A reference to the sheet whose name you want.</span></span>
  
<span data-ttu-id="cea86-110">При передаче внешняя ссылка (**xltypeRef**) должны содержать только идентификатор листа.</span><span class="sxs-lookup"><span data-stu-id="cea86-110">If you are passing an external reference (**xltypeRef**) it need only contain the ID of the sheet.</span></span> <span data-ttu-id="cea86-111">Структуры данных, которые описывают ячеек на листе игнорируется, а не должна быть предоставлена.</span><span class="sxs-lookup"><span data-stu-id="cea86-111">The data structures that describe the cells on the worksheet are ignored and do not need to be provided.</span></span> <span data-ttu-id="cea86-112">Если идентификатор нулевое значение, **xlSheetNm** возвращает имя активного листа.</span><span class="sxs-lookup"><span data-stu-id="cea86-112">If the ID is set to zero, **xlSheetNm** returns the name of the current sheet.</span></span> 
  
<span data-ttu-id="cea86-113">При передаче внутренних справочных (**xltypeSef**) **xlSheetNm** возвращает имя активного листа.</span><span class="sxs-lookup"><span data-stu-id="cea86-113">If you are passing an internal reference (**xltypeSef**), **xlSheetNm** returns the name of the current sheet.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="cea86-114">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cea86-114">Property value/Return value</span></span>

<span data-ttu-id="cea86-115">Возвращает имя листа (**xltypeStr**) в виде `[Book1]Sheet1`.</span><span class="sxs-lookup"><span data-stu-id="cea86-115">Returns the name of the sheet (**xltypeStr**) in the form  `[Book1]Sheet1`.</span></span>
  
## <a name="example"></a><span data-ttu-id="cea86-116">Пример</span><span class="sxs-lookup"><span data-stu-id="cea86-116">Example</span></span>

<span data-ttu-id="cea86-117">Следующий пример отображает имя листа, из которой был вызван функцию.</span><span class="sxs-lookup"><span data-stu-id="cea86-117">The following example displays the name of the sheet from which the function was called.</span></span> <span data-ttu-id="cea86-118">Функция работает правильно, только в том случае, если вызов выполняется из листа макросов во время выполнения команды макросов XLM.</span><span class="sxs-lookup"><span data-stu-id="cea86-118">The function works correctly only if called from a macro sheet while executing an XLM command macro.</span></span> <span data-ttu-id="cea86-119">Это, так как он вызывает **xlcAlert**, который можно выполнить только команды, и он должен быть вызван из листа, а не диалоговое окно, меню или панели команд в порядке для **xlfCaller** возвращает ссылку на.</span><span class="sxs-lookup"><span data-stu-id="cea86-119">This is because it calls **xlcAlert**, which only commands can do, and it needs to be called from a sheet rather than a dialog box, menu, or command bar in order for **xlfCaller** to return a reference.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="cea86-120">См. также</span><span class="sxs-lookup"><span data-stu-id="cea86-120">See also</span></span>

- [<span data-ttu-id="cea86-121">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="cea86-121">xlSheetId</span></span>](xlsheetid.md)
- [<span data-ttu-id="cea86-122">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="cea86-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

