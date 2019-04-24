---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- Функция func1 [Excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304083"
---
# <a name="func1"></a><span data-ttu-id="616fc-104">Func1</span><span class="sxs-lookup"><span data-stu-id="616fc-104">Func1</span></span>

 <span data-ttu-id="616fc-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="616fc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="616fc-106">В примере пользовательской функции листа показано возвращение статического строкового значения.</span><span class="sxs-lookup"><span data-stu-id="616fc-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="616fc-107">Когда GENERIC. XLL загружается, она регистрирует эту функцию, чтобы ее можно было вызывать из листа.</span><span class="sxs-lookup"><span data-stu-id="616fc-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="616fc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="616fc-108">Parameters</span></span>

 <span data-ttu-id="616fc-109">_px_ (**Лпкслопер**)</span><span class="sxs-lookup"><span data-stu-id="616fc-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="616fc-110">Этот аргумент игнорируется и служит только для вызова функции в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="616fc-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="616fc-111">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="616fc-111">Property value/Return value</span></span>

 <span data-ttu-id="616fc-112">**LPXLOPER12**: всегда строка "func1"</span><span class="sxs-lookup"><span data-stu-id="616fc-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="616fc-113">Пример</span><span class="sxs-lookup"><span data-stu-id="616fc-113">Example</span></span>

<span data-ttu-id="616fc-114">Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе.</span><span class="sxs-lookup"><span data-stu-id="616fc-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="616fc-115">См. также</span><span class="sxs-lookup"><span data-stu-id="616fc-115">See also</span></span>



[<span data-ttu-id="616fc-116">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="616fc-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

