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
- функция tempbool [excel 2007], функция TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807323"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="ad5cb-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="ad5cb-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="ad5cb-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ad5cb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ad5cb-106">Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** , содержащий **логическое** **значение TRUE** или **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="ad5cb-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="ad5cb-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="ad5cb-107">Parameters</span></span>

 <span data-ttu-id="ad5cb-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="ad5cb-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="ad5cb-109">Используйте 0, чтобы возвратить **значение FALSE**; Используйте другое значение возвращало **значение TRUE**.</span><span class="sxs-lookup"><span data-stu-id="ad5cb-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ad5cb-110">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad5cb-110">Property value/Return value</span></span>

<span data-ttu-id="ad5cb-111">Возвращает **xltypeBool** **логическое** содержащий логическое значение, переданное в.</span><span class="sxs-lookup"><span data-stu-id="ad5cb-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ad5cb-112">Пример</span><span class="sxs-lookup"><span data-stu-id="ad5cb-112">Example</span></span>

<span data-ttu-id="ad5cb-113">В следующем примере функция **TempBool12** снимите флажок в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="ad5cb-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="ad5cb-114">Временные память освобождается при вызове функции [Excel/Excel12f](excel-excel12f.md) .</span><span class="sxs-lookup"><span data-stu-id="ad5cb-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="ad5cb-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ad5cb-115">See also</span></span>



[<span data-ttu-id="ad5cb-116">Функции в библиотеке Framework</span><span class="sxs-lookup"><span data-stu-id="ad5cb-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

