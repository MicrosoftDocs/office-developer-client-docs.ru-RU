---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- функция initframework [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2d7e3286d794d6f21da9ef83ca44d18ec242c063
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807256"
---
# <a name="initframework"></a><span data-ttu-id="a31b7-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="a31b7-104">InitFramework</span></span>

 <span data-ttu-id="a31b7-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a31b7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a31b7-106">Функция библиотеки Framework, инициализирует библиотеки Framework, который просто инициализирует временные **XLOPER**/ структуры данных**XLOPER12** памяти, что освобождает память, которая уже была распределена.</span><span class="sxs-lookup"><span data-stu-id="a31b7-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="a31b7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a31b7-107">Parameters</span></span>

<span data-ttu-id="a31b7-108">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="a31b7-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="a31b7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="a31b7-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a31b7-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="a31b7-111">Пример</span><span class="sxs-lookup"><span data-stu-id="a31b7-111">Example</span></span>

<span data-ttu-id="a31b7-112">В этом примере используется функция **InitFramework** для освобождения всех временной памяти.</span><span class="sxs-lookup"><span data-stu-id="a31b7-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a31b7-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a31b7-113">See also</span></span>



[<span data-ttu-id="a31b7-114">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="a31b7-114">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

