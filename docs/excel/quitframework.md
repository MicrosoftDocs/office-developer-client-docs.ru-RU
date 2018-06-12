---
title: QuitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- QuitFramework
keywords:
- функция quitframework
localization_priority: Normal
ms.assetid: d17a3efe-c278-4ef1-b8f9-b958ae012361
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5c4b122b200d9de0cf098d2bc9e2fbd887ad9ff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807313"
---
# <a name="quitframework"></a><span data-ttu-id="97947-104">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="97947-104">QuitFramework</span></span>

 <span data-ttu-id="97947-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="97947-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="97947-106">Функция библиотеки Framework, которая отменяет инициализацию библиотеки Framework, который просто повторно инициализирует временные **XLOPER**/ структуры данных**XLOPER12** памяти, что освобождает память, которая уже была распределена.</span><span class="sxs-lookup"><span data-stu-id="97947-106">Framework library function that uninitializes the Framework library, which simply re-initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI QuitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="97947-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="97947-107">Parameters</span></span>

<span data-ttu-id="97947-108">Эта функция не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="97947-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="97947-109">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97947-109">Property value/Return value</span></span>

<span data-ttu-id="97947-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="97947-110">This function does not return a value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="97947-111">См. также</span><span class="sxs-lookup"><span data-stu-id="97947-111">See also</span></span>



[<span data-ttu-id="97947-112">Функции в библиотеке Framework</span><span class="sxs-lookup"><span data-stu-id="97947-112">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

