---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- Функция инитфрамеворк [Excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34fe8f4a606956b90a0d005b0bc523cea460153f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310684"
---
# <a name="initframework"></a><span data-ttu-id="71ec0-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="71ec0-104">InitFramework</span></span>

 <span data-ttu-id="71ec0-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="71ec0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="71ec0-106">Функция библиотеки Framework, которая инициализирует библиотеку Framework, которая просто инициализирует временные структуры данных о памяти **XLOPER**/ **XLOPER12** , освобождая память, которая уже была выделена.</span><span class="sxs-lookup"><span data-stu-id="71ec0-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="71ec0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="71ec0-107">Parameters</span></span>

<span data-ttu-id="71ec0-108">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="71ec0-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="71ec0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71ec0-109">Return value</span></span>

<span data-ttu-id="71ec0-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="71ec0-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="71ec0-111">Пример</span><span class="sxs-lookup"><span data-stu-id="71ec0-111">Example</span></span>

<span data-ttu-id="71ec0-112">В этом примере функция **инитфрамеворк** используется для освобождения всей временной памяти.</span><span class="sxs-lookup"><span data-stu-id="71ec0-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="71ec0-113">См. также</span><span class="sxs-lookup"><span data-stu-id="71ec0-113">See also</span></span>



[<span data-ttu-id="71ec0-114">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="71ec0-114">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

