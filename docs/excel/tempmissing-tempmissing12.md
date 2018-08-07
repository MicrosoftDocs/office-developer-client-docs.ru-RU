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
- функция tempmissing [excel 2007], функция TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807330"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="d2a45-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="d2a45-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="d2a45-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d2a45-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d2a45-106">Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** тип **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="d2a45-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="d2a45-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2a45-107">Parameters</span></span>

<span data-ttu-id="d2a45-108">Эта функция не получает никаких параметров.</span><span class="sxs-lookup"><span data-stu-id="d2a45-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d2a45-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="d2a45-110">Возвращает указатель на **xltypeMissing** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="d2a45-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="d2a45-111">Пример</span><span class="sxs-lookup"><span data-stu-id="d2a45-111">Example</span></span>

<span data-ttu-id="d2a45-112">В этом примере использует **TempMissing12** для предоставления трех отсутствующие аргументы, которые нужно **xlcWorkspace** , а затем **логическое** **значение FALSE,** чтобы отображать полосы прокрутки листа.</span><span class="sxs-lookup"><span data-stu-id="d2a45-112">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars.</span></span> <span data-ttu-id="d2a45-113">Другие параметры рабочей области, которые не влияет на соответствуют первым трем аргументов.</span><span class="sxs-lookup"><span data-stu-id="d2a45-113">The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="d2a45-114">См. также</span><span class="sxs-lookup"><span data-stu-id="d2a45-114">See also</span></span>



[<span data-ttu-id="d2a45-115">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="d2a45-115">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

