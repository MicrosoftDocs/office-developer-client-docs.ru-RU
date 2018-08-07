---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- функция tempstr12 [excel 2007], функция TempStrConst [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807335"
---
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="77b8c-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="77b8c-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="77b8c-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="77b8c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="77b8c-106">Функции библиотеки Framework, который создает временные **XLOPER и XLOPER12** , который содержит строку **xltypeStr** , используя строку символом null источника в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="77b8c-106">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input.</span></span> <span data-ttu-id="77b8c-107">Функция выделяет новый буфер памяти и копирует переданной строки в нее.</span><span class="sxs-lookup"><span data-stu-id="77b8c-107">The function allocates a new memory buffer and copies the passed-in string into it.</span></span> <span data-ttu-id="77b8c-108">Входной строки не изменятся и поэтому объявлен как **const**.</span><span class="sxs-lookup"><span data-stu-id="77b8c-108">The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="77b8c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="77b8c-109">Parameters</span></span>

 <span data-ttu-id="77b8c-110">_str_</span><span class="sxs-lookup"><span data-stu-id="77b8c-110">_str_</span></span>
  
<span data-ttu-id="77b8c-111">Указатель на строке source символом null.</span><span class="sxs-lookup"><span data-stu-id="77b8c-111">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="77b8c-112">В случае **XLOPER**s TempStrConst ограничивает длину строки, представляющие больше 255 байт.</span><span class="sxs-lookup"><span data-stu-id="77b8c-112">In the case of **XLOPER**s, TempStrConst truncates strings that are longer than 255 bytes.</span></span> <span data-ttu-id="77b8c-113">В случае **XLOPER12**s TempStr12Const ограничивает длину строки, представляющие более 32 767 символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="77b8c-113">In the case of **XLOPER12**s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="77b8c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4">Return value</span></span>

<span data-ttu-id="77b8c-115">Возвращает строку **xltypeStr** , содержащий копию буфера переданной строки.</span><span class="sxs-lookup"><span data-stu-id="77b8c-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="77b8c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="77b8c-116">Remarks</span></span>

<span data-ttu-id="77b8c-117">Обратите внимание, что строка **XLOPER** функция Framework, **TempStr**, отличающиеся пытается заменить первым символом указанная строка длиной последующие строки.</span><span class="sxs-lookup"><span data-stu-id="77b8c-117">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="77b8c-118">Не всегда безопасных что следует сделать: Microsoft Excel может произойти сбой, если передается строка только для чтения.</span><span class="sxs-lookup"><span data-stu-id="77b8c-118">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> <span data-ttu-id="77b8c-119">Этот способ создания временной строки теперь устаревшим способом рабочих **TempStrConst** и **TempStr12** .</span><span class="sxs-lookup"><span data-stu-id="77b8c-119">This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work.</span></span> <span data-ttu-id="77b8c-120">Таким образом первым символом входной строки обрабатывается как начала строки, то есть, не как длина символов или ввода символов длины.</span><span class="sxs-lookup"><span data-stu-id="77b8c-120">Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character.</span></span> <span data-ttu-id="77b8c-121">Не следует передавать строк, которые имеют длину символ, закодированный в начале, как можно отнести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="77b8c-121">You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="77b8c-122">Пример</span><span class="sxs-lookup"><span data-stu-id="77b8c-122">Example</span></span>

<span data-ttu-id="77b8c-123">В этом примере функция **TempStr12** используется для создания строки для окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="77b8c-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="77b8c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="77b8c-124">See also</span></span>



[<span data-ttu-id="77b8c-125">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="77b8c-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

