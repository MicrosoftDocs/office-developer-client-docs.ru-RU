---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- функция xlUDF [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8f45f800ca50d2a46792e7cf5e00ac25bd099e8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807377"
---
# <a name="xludf"></a><span data-ttu-id="cf5b9-104">xlUDF</span><span class="sxs-lookup"><span data-stu-id="cf5b9-104">xlUDF</span></span>

<span data-ttu-id="cf5b9-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cf5b9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cf5b9-106">Вызов пользовательской функции (UDF).</span><span class="sxs-lookup"><span data-stu-id="cf5b9-106">Calls a user-defined function (UDF).</span></span> <span data-ttu-id="cf5b9-107">Эта функция позволяет DLL для вызова Visual Basic для приложений (VBA) пользовательские функции, функции языка макросов XLM и зарегистрированных функции, содержащиеся в другие надстройки.</span><span class="sxs-lookup"><span data-stu-id="cf5b9-107">This function allows a DLL to call Visual Basic for Applications (VBA) user-defined functions, XLM macro language functions, and registered functions contained in other add-ins.</span></span>
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a><span data-ttu-id="cf5b9-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="cf5b9-108">Parameters</span></span>

<span data-ttu-id="cf5b9-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** или **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="cf5b9-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="cf5b9-110">Справочник по функции, которому нужно позвонить.</span><span class="sxs-lookup"><span data-stu-id="cf5b9-110">The reference of the function you want to call.</span></span> <span data-ttu-id="cf5b9-111">Это может быть макрос листа ссылки на ячейки, зарегистрированное имя функции, что строка или идентификатор регистрации функции.</span><span class="sxs-lookup"><span data-stu-id="cf5b9-111">This can be a macro sheet cell reference, the registered name of the function as a string, or the register ID of the function.</span></span> <span data-ttu-id="cf5b9-112">Для добавления в функции XLL зарегистрировано с помощью **xlfRegister** или **ЗАРЕГИСТРИРУЙТЕ** с аргумента _pxFunctionText_ указано идентификатор можно получить с помощью **xlfEvaluate** для поиска имени.</span><span class="sxs-lookup"><span data-stu-id="cf5b9-112">For XLL add-in functions registered using **xlfRegister** or **REGISTER** with the argument  _pxFunctionText_ supplied, the ID can be obtained by using **xlfEvaluate** to look up the name.</span></span> 
  
<span data-ttu-id="cf5b9-113">_pxArg1..._</span><span class="sxs-lookup"><span data-stu-id="cf5b9-113">_pxArg1, ..._</span></span>
  
<span data-ttu-id="cf5b9-114">Ноль или больше аргументов пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="cf5b9-114">Zero or more arguments to the user-defined function.</span></span> <span data-ttu-id="cf5b9-115">При вызове этой функции в версиях более ранних версий, чем Excel 2007, максимальное число дополнительные аргументы, которые можно передавать — 29, которая является 30 включая _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="cf5b9-115">When you are calling this function in versions earlier than Excel 2007, the maximum number of additional arguments that can be passed is 29, which is 30 including  _pxFnRef_.</span></span> <span data-ttu-id="cf5b9-116">Начиная с версии Excel 2007, это ограничение возникает до 254, которая является 255 включая _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="cf5b9-116">Starting in Excel 2007, this limit is raised to 254, which is 255 including  _pxFnRef_.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="cf5b9-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="cf5b9-117">Return value</span></span>

<span data-ttu-id="cf5b9-118">Возвращает значение, возвращаемое пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="cf5b9-118">Returns whatever value the user-defined function returned.</span></span>
  
## <a name="example"></a><span data-ttu-id="cf5b9-119">Пример</span><span class="sxs-lookup"><span data-stu-id="cf5b9-119">Example</span></span>

<span data-ttu-id="cf5b9-120">Следующий пример запускает **TestMacro** на листе Macro1 Книга1. XLS.</span><span class="sxs-lookup"><span data-stu-id="cf5b9-120">The following example runs **TestMacro** on sheet Macro1 in BOOK1.XLS.</span></span> <span data-ttu-id="cf5b9-121">Убедитесь, что макрос на лист с именем Macro1.</span><span class="sxs-lookup"><span data-stu-id="cf5b9-121">Make sure that the macro is on a sheet named Macro1.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="cf5b9-122">См. также</span><span class="sxs-lookup"><span data-stu-id="cf5b9-122">See also</span></span>

- [<span data-ttu-id="cf5b9-123">Функции интерфейса API для C, которые могут вызываться только из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="cf5b9-123">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

