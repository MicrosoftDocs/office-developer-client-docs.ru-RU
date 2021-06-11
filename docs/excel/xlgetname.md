---
title: xlGetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetName
keywords:
- функция xlgetname [Excel 2007]
localization_priority: Normal
ms.assetid: 72dbebc0-7436-4771-8fbf-2b445341da65
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 350ae99baf088a36fa3e1159caa1805cdd623276
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430590"
---
# <a name="xlgetname"></a><span data-ttu-id="f8161-104">xlGetName</span><span class="sxs-lookup"><span data-stu-id="f8161-104">xlGetName</span></span>

<span data-ttu-id="f8161-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f8161-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f8161-106">Возвращает полный путь и имя файла DLL в виде строки.</span><span class="sxs-lookup"><span data-stu-id="f8161-106">Returns the full path and file name of the DLL in the form of a string.</span></span>
  
```cs
Excel12(xlGetName, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="f8161-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="f8161-107">Parameters</span></span>

<span data-ttu-id="f8161-108">Эта функция не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="f8161-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f8161-109">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8161-109">Property value/Return value</span></span>

<span data-ttu-id="f8161-110">Возвращает путь и имя файла **(xltypeStr).**</span><span class="sxs-lookup"><span data-stu-id="f8161-110">Returns the path and file name (**xltypeStr**).</span></span> 
  
## <a name="example"></a><span data-ttu-id="f8161-111">Пример</span><span class="sxs-lookup"><span data-stu-id="f8161-111">Example</span></span>

`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetNameExample(void)
{
    XLOPER12 xRes;
    Excel12(xlGetName, (LPXLOPER12)&xRes, 0);
    Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="f8161-112">См. также</span><span class="sxs-lookup"><span data-stu-id="f8161-112">See also</span></span>

- [<span data-ttu-id="f8161-113">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="f8161-113">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

