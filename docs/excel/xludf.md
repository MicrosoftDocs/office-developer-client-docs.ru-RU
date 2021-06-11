---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- функция xludf [Excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 569334847c7612b86f6ddc967f159e2ef425cbbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430646"
---
# <a name="xludf"></a><span data-ttu-id="de87d-104">xlUDF</span><span class="sxs-lookup"><span data-stu-id="de87d-104">xlUDF</span></span>

<span data-ttu-id="de87d-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="de87d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="de87d-106">Вызывает функцию, определяемую пользователем (UDF).</span><span class="sxs-lookup"><span data-stu-id="de87d-106">Calls a user-defined function (UDF).</span></span> <span data-ttu-id="de87d-107">Эта функция позволяет DLL вызывать определенные пользователем функции Visual Basic для приложений(VBA), функции макроса XLM и зарегистрированные функции, содержащиеся в других надстройках.</span><span class="sxs-lookup"><span data-stu-id="de87d-107">This function allows a DLL to call Visual Basic for Applications (VBA) user-defined functions, XLM macro language functions, and registered functions contained in other add-ins.</span></span>
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a><span data-ttu-id="de87d-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="de87d-108">Parameters</span></span>

<span data-ttu-id="de87d-109">_pxFnRef_ **(xltypeRef,** **xltypeSRef,** **xltypeStr** или **xltypeNum)**</span><span class="sxs-lookup"><span data-stu-id="de87d-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="de87d-110">Ссылка на функцию, которая вам нужно вызвать.</span><span class="sxs-lookup"><span data-stu-id="de87d-110">The reference of the function you want to call.</span></span> <span data-ttu-id="de87d-111">Это может быть ссылка ячейки макроса, зарегистрированное имя функции в качестве строки или регистрация ID функции.</span><span class="sxs-lookup"><span data-stu-id="de87d-111">This can be a macro sheet cell reference, the registered name of the function as a string, or the register ID of the function.</span></span> <span data-ttu-id="de87d-112">Для функций надстройки XLL, зарегистрированных с помощью **xlfRegister** или **REGISTER** с предоставленным аргументом  _pxFunctionText,_ ID можно получить с помощью **xlfEvaluate,** чтобы найти имя.</span><span class="sxs-lookup"><span data-stu-id="de87d-112">For XLL add-in functions registered using **xlfRegister** or **REGISTER** with the argument  _pxFunctionText_ supplied, the ID can be obtained by using **xlfEvaluate** to look up the name.</span></span> 
  
<span data-ttu-id="de87d-113">_pxArg1, ..._</span><span class="sxs-lookup"><span data-stu-id="de87d-113">_pxArg1, ..._</span></span>
  
<span data-ttu-id="de87d-114">Ноль или более аргументов в пользу функции, определяемой пользователем.</span><span class="sxs-lookup"><span data-stu-id="de87d-114">Zero or more arguments to the user-defined function.</span></span> <span data-ttu-id="de87d-115">При вызове этой функции в версиях до Excel 2007 года максимальное количество дополнительных аргументов, которые можно передать, составляет 29, то есть 30, включая _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="de87d-115">When you are calling this function in versions earlier than Excel 2007, the maximum number of additional arguments that can be passed is 29, which is 30 including  _pxFnRef_.</span></span> <span data-ttu-id="de87d-116">Начиная с Excel 2007 г. это ограничение повышается до 254, что составляет 255, включая _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="de87d-116">Starting in Excel 2007, this limit is raised to 254, which is 255 including  _pxFnRef_.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="de87d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de87d-117">Return value</span></span>

<span data-ttu-id="de87d-118">Возвращает любое значение возвращенной функции, определенной пользователем.</span><span class="sxs-lookup"><span data-stu-id="de87d-118">Returns whatever value the user-defined function returned.</span></span>
  
## <a name="example"></a><span data-ttu-id="de87d-119">Пример</span><span class="sxs-lookup"><span data-stu-id="de87d-119">Example</span></span>

<span data-ttu-id="de87d-120">В следующем примере **выполняется TestMacro** на листе Macro1 в BOOK1.XLS.</span><span class="sxs-lookup"><span data-stu-id="de87d-120">The following example runs **TestMacro** on sheet Macro1 in BOOK1.XLS.</span></span> <span data-ttu-id="de87d-121">Убедитесь, что макрос находится на листе с именем Macro1.</span><span class="sxs-lookup"><span data-stu-id="de87d-121">Make sure that the macro is on a sheet named Macro1.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="de87d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="de87d-122">See also</span></span>

- [<span data-ttu-id="de87d-123">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="de87d-123">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

