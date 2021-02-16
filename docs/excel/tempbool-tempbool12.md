---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- Функция tempbool [excel 2007],TempBool12 function [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433719"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="a70ac-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="a70ac-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="a70ac-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a70ac-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a70ac-106">Функция библиотеки Framework, которая создает временную  /  **XLOPER XLOPER12, содержащую** **boolean** **TRUE** или **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a70ac-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="a70ac-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a70ac-107">Parameters</span></span>

 <span data-ttu-id="a70ac-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="a70ac-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="a70ac-109">Используйте 0, чтобы вернуть **false;** используйте любое другое значение, чтобы вернуть **ЗНАЧЕНИЕ TRUE.**</span><span class="sxs-lookup"><span data-stu-id="a70ac-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a70ac-110">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a70ac-110">Property value/Return value</span></span>

<span data-ttu-id="a70ac-111">Возвращает логическое **значение xltypeBool,** **содержащее** переданные логические значения.</span><span class="sxs-lookup"><span data-stu-id="a70ac-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a70ac-112">Пример</span><span class="sxs-lookup"><span data-stu-id="a70ac-112">Example</span></span>

<span data-ttu-id="a70ac-113">В следующем примере функция **TempBool12** используется для очистки панели состояния.</span><span class="sxs-lookup"><span data-stu-id="a70ac-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="a70ac-114">Временная память освободиться при [вызвании функции Excel и Excel12f.](excel-excel12f.md)</span><span class="sxs-lookup"><span data-stu-id="a70ac-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a70ac-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a70ac-115">See also</span></span>



[<span data-ttu-id="a70ac-116">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="a70ac-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

