---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- функция func1 [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807257"
---
# <a name="func1"></a><span data-ttu-id="a3a2d-104">Func1</span><span class="sxs-lookup"><span data-stu-id="a3a2d-104">Func1</span></span>

 <span data-ttu-id="a3a2d-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a3a2d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a3a2d-106">Пример пользовательской функции показано возвращение статического строковое значение.</span><span class="sxs-lookup"><span data-stu-id="a3a2d-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="a3a2d-107">При загрузке GENERIC.xll регистрирует эту функцию, чтобы его можно вызывать из рабочего листа.</span><span class="sxs-lookup"><span data-stu-id="a3a2d-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="a3a2d-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="a3a2d-108">Parameters</span></span>

 <span data-ttu-id="a3a2d-109">_точек_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="a3a2d-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="a3a2d-110">Этот аргумент игнорируется и используется только для запуска Microsoft Excel для вызова функции.</span><span class="sxs-lookup"><span data-stu-id="a3a2d-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a3a2d-111">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3a2d-111">Property value/Return value</span></span>

 <span data-ttu-id="a3a2d-112">**LPXLOPER12**: всегда строка «Func1»</span><span class="sxs-lookup"><span data-stu-id="a3a2d-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="a3a2d-113">Пример</span><span class="sxs-lookup"><span data-stu-id="a3a2d-113">Example</span></span>

<span data-ttu-id="a3a2d-114">Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="a3a2d-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3a2d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a3a2d-115">See also</span></span>



[<span data-ttu-id="a3a2d-116">В универсальные библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="a3a2d-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

