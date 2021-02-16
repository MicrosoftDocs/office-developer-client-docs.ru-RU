---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- функция tempmissing [excel 2007],TempMissing12 function [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435959"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="c4384-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="c4384-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="c4384-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c4384-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c4384-106">Функция библиотеки Framework, которая создает временную  /  **XLOPER XLOPER12** типа **xltypeMissing.**</span><span class="sxs-lookup"><span data-stu-id="c4384-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="c4384-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4384-107">Parameters</span></span>

<span data-ttu-id="c4384-108">Эта функция не получает никаких параметров.</span><span class="sxs-lookup"><span data-stu-id="c4384-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c4384-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4384-109">Return value</span></span>

<span data-ttu-id="c4384-110">Возвращает указатель на **XLtypeMissing** **XLOPER** /  **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="c4384-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="c4384-111">Пример</span><span class="sxs-lookup"><span data-stu-id="c4384-111">Example</span></span>

<span data-ttu-id="c4384-112">В этом примере **tempMissing12** используется для предоставления **xlcWorkspace** трех отсутствующих аргументов, за которыми следует **boolean** **FALSE** для подавления отображения полос прокрутки на рабочем экране.</span><span class="sxs-lookup"><span data-stu-id="c4384-112">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars.</span></span> <span data-ttu-id="c4384-113">Первые три аргумента соответствуют другим незатроченным настройкам рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c4384-113">The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c4384-114">См. также</span><span class="sxs-lookup"><span data-stu-id="c4384-114">See also</span></span>



[<span data-ttu-id="c4384-115">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="c4384-115">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

