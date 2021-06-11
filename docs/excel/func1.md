---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- функция func1 [Excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408917"
---
# <a name="func1"></a><span data-ttu-id="baeb8-104">Func1</span><span class="sxs-lookup"><span data-stu-id="baeb8-104">Func1</span></span>

 <span data-ttu-id="baeb8-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="baeb8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="baeb8-106">Пример функции таблицы, определяемой пользователем, демонстрирует возвращение статического значения строки.</span><span class="sxs-lookup"><span data-stu-id="baeb8-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="baeb8-107">При загрузке GENERIC.xll она регистрирует эту функцию, чтобы она была вызвана из таблицы.</span><span class="sxs-lookup"><span data-stu-id="baeb8-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="baeb8-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="baeb8-108">Parameters</span></span>

 <span data-ttu-id="baeb8-109">_px_ **(LPXLOPER)**</span><span class="sxs-lookup"><span data-stu-id="baeb8-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="baeb8-110">Этот аргумент игнорируется и служит только для Microsoft Excel вызова функции.</span><span class="sxs-lookup"><span data-stu-id="baeb8-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="baeb8-111">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="baeb8-111">Property value/Return value</span></span>

 <span data-ttu-id="baeb8-112">**LPXLOPER12**: Всегда строка "Func1"</span><span class="sxs-lookup"><span data-stu-id="baeb8-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="baeb8-113">Пример</span><span class="sxs-lookup"><span data-stu-id="baeb8-113">Example</span></span>

<span data-ttu-id="baeb8-114">См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код этой функции.</span><span class="sxs-lookup"><span data-stu-id="baeb8-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="baeb8-115">См. также</span><span class="sxs-lookup"><span data-stu-id="baeb8-115">See also</span></span>



[<span data-ttu-id="baeb8-116">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="baeb8-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

