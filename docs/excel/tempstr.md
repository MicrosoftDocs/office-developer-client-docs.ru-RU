---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- Функция темпстр [Excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310320"
---
# <a name="tempstr"></a><span data-ttu-id="78d2c-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="78d2c-104">TempStr</span></span>

 <span data-ttu-id="78d2c-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="78d2c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="78d2c-106">Устаревшая функция библиотеки Framework, которая создает временную структуру, содержащую строку байта **кслтипестр** . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="78d2c-106">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string.</span></span> <span data-ttu-id="78d2c-107">В качестве входных данных принимается строка источника, заканчивающаяся нулем.</span><span class="sxs-lookup"><span data-stu-id="78d2c-107">It takes a null-terminated source string as input.</span></span> <span data-ttu-id="78d2c-108">Он пытается перезаписать первый символ предоставленной строки с длиной следующей строки.</span><span class="sxs-lookup"><span data-stu-id="78d2c-108">It tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="78d2c-109">Это не всегда является безопасным действием: Microsoft Excel может выполнить сбой, если передать строку, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="78d2c-109">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="78d2c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="78d2c-110">Parameters</span></span>

 <span data-ttu-id="78d2c-111">_str_</span><span class="sxs-lookup"><span data-stu-id="78d2c-111">_str_</span></span>
  
<span data-ttu-id="78d2c-112">Указатель на строку источника, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="78d2c-112">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="78d2c-113">**Темпстр** усекает строки, размер которых превышает 255 байт.</span><span class="sxs-lookup"><span data-stu-id="78d2c-113">**TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="78d2c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78d2c-114">Return value</span></span>

<span data-ttu-id="78d2c-115">Возвращает строку **кслтипестр** , содержащую указатель на переданный буфер строк.</span><span class="sxs-lookup"><span data-stu-id="78d2c-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="78d2c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="78d2c-116">Remarks</span></span>

<span data-ttu-id="78d2c-117">Такой способ создания временных строк теперь является нерекомендуемым в пользу того, как работают как в [темпстрконст, так и в TempStr12](tempstrconst-tempstr12.md) .</span><span class="sxs-lookup"><span data-stu-id="78d2c-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span></span> <span data-ttu-id="78d2c-118">Эти функции выделяют новый буфер памяти и копируют в него переданную строку.</span><span class="sxs-lookup"><span data-stu-id="78d2c-118">These functions allocate a new memory buffer and copy the passed-in string into it.</span></span> <span data-ttu-id="78d2c-119">Входные строки для **темпстрконст** и **TempStr12** не изменяются, поэтому объявляются как **const**.</span><span class="sxs-lookup"><span data-stu-id="78d2c-119">The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**.</span></span> <span data-ttu-id="78d2c-120">В отличие от того, входная строка в **темпстр** изменяется и не может быть объявлена **константой**.</span><span class="sxs-lookup"><span data-stu-id="78d2c-120">In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**.</span></span> <span data-ttu-id="78d2c-121">Первый символ входной строки считается пространством для знака длины и перезаписывается этой функцией.</span><span class="sxs-lookup"><span data-stu-id="78d2c-121">The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="78d2c-122">См. также</span><span class="sxs-lookup"><span data-stu-id="78d2c-122">See also</span></span>



[<span data-ttu-id="78d2c-123">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="78d2c-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

