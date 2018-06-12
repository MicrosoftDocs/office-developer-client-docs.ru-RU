---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- функция tempstr [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807332"
---
# <a name="tempstr"></a><span data-ttu-id="0edcb-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="0edcb-104">TempStr</span></span>

 <span data-ttu-id="0edcb-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0edcb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0edcb-106">Устаревшие функции библиотеки Framework, который создает временные **XLOPER** , содержащее строку **xltypeStr** байтов.</span><span class="sxs-lookup"><span data-stu-id="0edcb-106">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string.</span></span> <span data-ttu-id="0edcb-107">Строка исходного символом null принимает в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="0edcb-107">It takes a null-terminated source string as input.</span></span> <span data-ttu-id="0edcb-108">Она пытается заменить первым символом указанная строка длиной последующие строки.</span><span class="sxs-lookup"><span data-stu-id="0edcb-108">It tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="0edcb-109">Не всегда безопасных что следует сделать: Microsoft Excel может произойти сбой, если передается строка только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0edcb-109">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="0edcb-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="0edcb-110">Parameters</span></span>

 <span data-ttu-id="0edcb-111">_STR_</span><span class="sxs-lookup"><span data-stu-id="0edcb-111">_str_</span></span>
  
<span data-ttu-id="0edcb-112">Указатель на строке source символом null.</span><span class="sxs-lookup"><span data-stu-id="0edcb-112">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="0edcb-113">**TempStr** ограничивает длину строки, представляющие больше 255 байт.</span><span class="sxs-lookup"><span data-stu-id="0edcb-113">**TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="0edcb-114">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0edcb-114">Return value</span></span>

<span data-ttu-id="0edcb-115">Возвращает строку **xltypeStr** , содержащий указатель на буфер переданной строки.</span><span class="sxs-lookup"><span data-stu-id="0edcb-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0edcb-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="0edcb-116">Remarks</span></span>

<span data-ttu-id="0edcb-117">Этот способ создания временной строки теперь устаревшим способом обоих рабочих [TempStrConst и TempStr12](tempstrconst-tempstr12.md) .</span><span class="sxs-lookup"><span data-stu-id="0edcb-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span></span> <span data-ttu-id="0edcb-118">Эти функции выделить новый буфер памяти и скопируйте в него переданной строки.</span><span class="sxs-lookup"><span data-stu-id="0edcb-118">These functions allocate a new memory buffer and copy the passed-in string into it.</span></span> <span data-ttu-id="0edcb-119">Входные строки для **TempStrConst** и **TempStr12** не изменятся и поэтому объявлен как **const**.</span><span class="sxs-lookup"><span data-stu-id="0edcb-119">The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**.</span></span> <span data-ttu-id="0edcb-120">С другой стороны ввода строку, которую нужно **TempStr** изменения и поэтому не может быть объявлен как **const**.</span><span class="sxs-lookup"><span data-stu-id="0edcb-120">In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**.</span></span> <span data-ttu-id="0edcb-121">Первым символом входной строки рассматривается как пространство для знаков длины и перезаписанного этой функции.</span><span class="sxs-lookup"><span data-stu-id="0edcb-121">The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0edcb-122">См. также</span><span class="sxs-lookup"><span data-stu-id="0edcb-122">See also</span></span>



[<span data-ttu-id="0edcb-123">Функции в библиотеке Framework</span><span class="sxs-lookup"><span data-stu-id="0edcb-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

