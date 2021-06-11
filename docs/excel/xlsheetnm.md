---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- xlsheetnm function [Excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5d62be7ebef71547de3a903db4c1a030984b8640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437415"
---
# <a name="xlsheetnm"></a><span data-ttu-id="bdb1c-104">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="bdb1c-104">xlSheetNm</span></span>

<span data-ttu-id="bdb1c-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bdb1c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bdb1c-106">Возвращает имя листа или макроса из его внутреннего ID листа, содержатого во внешней ссылке, или имя текущего листа, если прошло внутреннее упоминание.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-106">Returns the name of a worksheet or macro sheet from its internal sheet ID contained within an external reference, or the name of the current sheet if passed an internal reference.</span></span>
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a><span data-ttu-id="bdb1c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="bdb1c-107">Parameters</span></span>

<span data-ttu-id="bdb1c-108">_pxExtref_ **(xltypeRef** или **xltypeSRef)**</span><span class="sxs-lookup"><span data-stu-id="bdb1c-108">_pxExtref_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="bdb1c-109">Ссылка на лист, имя которого необходимо.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-109">A reference to the sheet whose name you want.</span></span>
  
<span data-ttu-id="bdb1c-110">Если вы проходите внешнюю ссылку **(xltypeRef),** она должна содержать только ID листа.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-110">If you are passing an external reference (**xltypeRef**) it need only contain the ID of the sheet.</span></span> <span data-ttu-id="bdb1c-111">Структуры данных, описывая ячейки на таблице, игнорируются и не требуются.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-111">The data structures that describe the cells on the worksheet are ignored and do not need to be provided.</span></span> <span data-ttu-id="bdb1c-112">Если для ID установлено значение нуля, **xlSheetNm** возвращает имя текущего листа.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-112">If the ID is set to zero, **xlSheetNm** returns the name of the current sheet.</span></span> 
  
<span data-ttu-id="bdb1c-113">Если вы передаете внутреннюю ссылку **(xltypeSef),** **xlSheetNm** возвращает имя текущего листа.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-113">If you are passing an internal reference (**xltypeSef**), **xlSheetNm** returns the name of the current sheet.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="bdb1c-114">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bdb1c-114">Property value/Return value</span></span>

<span data-ttu-id="bdb1c-115">Возвращает имя листа **(xltypeStr)** в форме  `[Book1]Sheet1` .</span><span class="sxs-lookup"><span data-stu-id="bdb1c-115">Returns the name of the sheet (**xltypeStr**) in the form  `[Book1]Sheet1`.</span></span>
  
## <a name="example"></a><span data-ttu-id="bdb1c-116">Пример</span><span class="sxs-lookup"><span data-stu-id="bdb1c-116">Example</span></span>

<span data-ttu-id="bdb1c-117">В следующем примере отображается имя листа, из которого была вызвана функция.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-117">The following example displays the name of the sheet from which the function was called.</span></span> <span data-ttu-id="bdb1c-118">Функция работает правильно, только если она вызвана с макроса при выполнении макроса команды XLM.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-118">The function works correctly only if called from a macro sheet while executing an XLM command macro.</span></span> <span data-ttu-id="bdb1c-119">Это вызвано тем, что он вызывает **xlcAlert,** который может делать только команды, и его нужно звонить из листа, а не из диалогового окна, меню или панели команд, чтобы **xlfCaller** вернул ссылку.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-119">This is because it calls **xlcAlert**, which only commands can do, and it needs to be called from a sheet rather than a dialog box, menu, or command bar in order for **xlfCaller** to return a reference.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="bdb1c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="bdb1c-120">See also</span></span>

- [<span data-ttu-id="bdb1c-121">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="bdb1c-121">xlSheetId</span></span>](xlsheetid.md)
- [<span data-ttu-id="bdb1c-122">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="bdb1c-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

