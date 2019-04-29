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
- Функция темпбул [Excel 2007], функция TempBool12 [Excel 2007]
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
# <a name="tempbooltempbool12"></a><span data-ttu-id="9e32b-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="9e32b-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="9e32b-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9e32b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9e32b-106">Функция библиотеки Framework, которая создает временную структуру **XLOPER**/ \*\*\*\* , содержащую **логическое** **значение true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="9e32b-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="9e32b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e32b-107">Parameters</span></span>

 <span data-ttu-id="9e32b-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="9e32b-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="9e32b-109">Чтобы возвращать **значение false**, используйте значение 0; Используйте любое другое значение, чтобы возвратить **значение true**.</span><span class="sxs-lookup"><span data-stu-id="9e32b-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9e32b-110">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e32b-110">Property value/Return value</span></span>

<span data-ttu-id="9e32b-111">Возвращает объект \*\*\*\* **Boolean** кслтипебул, содержащий логическое значение, переданное в параметре.</span><span class="sxs-lookup"><span data-stu-id="9e32b-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9e32b-112">Пример</span><span class="sxs-lookup"><span data-stu-id="9e32b-112">Example</span></span>

<span data-ttu-id="9e32b-113">В примере ниже показано, как очистить строку состояния с помощью функции **TempBool12** .</span><span class="sxs-lookup"><span data-stu-id="9e32b-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="9e32b-114">Временная память освобождается при вызове функции [Excel/Excel12f](excel-excel12f.md) .</span><span class="sxs-lookup"><span data-stu-id="9e32b-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="9e32b-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9e32b-115">See also</span></span>



[<span data-ttu-id="9e32b-116">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="9e32b-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

