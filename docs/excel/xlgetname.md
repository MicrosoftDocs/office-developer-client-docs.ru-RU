---
title: xlGetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetName
keywords:
- функция xlgetname [excel 2007]
localization_priority: Normal
ms.assetid: 72dbebc0-7436-4771-8fbf-2b445341da65
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 069676957d280a0bf3b398bb23b27f0e654bc655
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807356"
---
# <a name="xlgetname"></a><span data-ttu-id="189df-104">xlGetName</span><span class="sxs-lookup"><span data-stu-id="189df-104">xlGetName</span></span>

<span data-ttu-id="189df-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="189df-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="189df-106">Возвращает полный путь и имя библиотеки DLL в виде строки.</span><span class="sxs-lookup"><span data-stu-id="189df-106">Returns the full path and file name of the DLL in the form of a string.</span></span>
  
```cs
Excel12(xlGetName, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="189df-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="189df-107">Parameters</span></span>

<span data-ttu-id="189df-108">Эта функция не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="189df-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="189df-109">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="189df-109">Property value/Return value</span></span>

<span data-ttu-id="189df-110">Возвращает путь и имя файла (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="189df-110">Returns the path and file name (**xltypeStr**).</span></span> 
  
## <a name="example"></a><span data-ttu-id="189df-111">Пример</span><span class="sxs-lookup"><span data-stu-id="189df-111">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="189df-112">См. также</span><span class="sxs-lookup"><span data-stu-id="189df-112">See also</span></span>

- [<span data-ttu-id="189df-113">Функции интерфейса API для C, которые могут вызываться только из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="189df-113">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

