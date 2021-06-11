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
- функция tempstr12 [Excel 2007], функция TempStrConst [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d93f9de021c7ba325d9c11af2cede0245ffbbf6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407153"
---
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="6dba4-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="6dba4-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="6dba4-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6dba4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6dba4-106">Функция библиотеки Framework, которая создает временную **строку XLOPER/XLOPER12,** содержаную строку **xltypeStr,** принимая в качестве входной строки исходные строки с нетленным разрешением.</span><span class="sxs-lookup"><span data-stu-id="6dba4-106">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input.</span></span> <span data-ttu-id="6dba4-107">Функция выделяет новый буфер памяти и копирует в нее переданную строку.</span><span class="sxs-lookup"><span data-stu-id="6dba4-107">The function allocates a new memory buffer and copies the passed-in string into it.</span></span> <span data-ttu-id="6dba4-108">Строка ввода не изменяется и поэтому объявляется **как const**.</span><span class="sxs-lookup"><span data-stu-id="6dba4-108">The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="6dba4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6dba4-109">Parameters</span></span>

 <span data-ttu-id="6dba4-110">_str_</span><span class="sxs-lookup"><span data-stu-id="6dba4-110">_str_</span></span>
  
<span data-ttu-id="6dba4-111">Указатель на строку источника с null-terminated.</span><span class="sxs-lookup"><span data-stu-id="6dba4-111">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="6dba4-112">В случае **XLOPER** s TempStrConst усечены строки длиной более 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="6dba4-112">In the case of **XLOPER** s, TempStrConst truncates strings that are longer than 255 bytes.</span></span> <span data-ttu-id="6dba4-113">В случае **XLOPER12** s TempStr12Const усечены строки, которые длиннее 32 767 символов Юникод.</span><span class="sxs-lookup"><span data-stu-id="6dba4-113">In the case of **XLOPER12** s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6dba4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6dba4-114">Return value</span></span>

<span data-ttu-id="6dba4-115">Возвращает **строку xltypeStr,** содержащую копию переданного буфера строки.</span><span class="sxs-lookup"><span data-stu-id="6dba4-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6dba4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="6dba4-116">Remarks</span></span>

<span data-ttu-id="6dba4-117">Обратите внимание, что функция **XLOPER** string Framework **TempStr** ведет себя по-разному и пытается переписать первый символ поставленной строки с последующей длиной строки.</span><span class="sxs-lookup"><span data-stu-id="6dba4-117">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="6dba4-118">Это не всегда безопасно: Microsoft Excel может произойти сбой при сдав строке только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6dba4-118">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> <span data-ttu-id="6dba4-119">Этот способ создания временных строк теперь отстает в пользу того, как работают **TempStrConst** и **TempStr12.**</span><span class="sxs-lookup"><span data-stu-id="6dba4-119">This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work.</span></span> <span data-ttu-id="6dba4-120">Поэтому первый символ строки ввода рассматривается как начало строки, то есть не как символ длины или как пространство для символа длины.</span><span class="sxs-lookup"><span data-stu-id="6dba4-120">Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character.</span></span> <span data-ttu-id="6dba4-121">Не следует передавать строки с закодированной в начале длиной, так как последствия могут быть непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="6dba4-121">You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6dba4-122">Пример</span><span class="sxs-lookup"><span data-stu-id="6dba4-122">Example</span></span>

<span data-ttu-id="6dba4-123">В этом примере используется **функция TempStr12** для создания строки для окна сообщений.</span><span class="sxs-lookup"><span data-stu-id="6dba4-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="6dba4-124">См. также</span><span class="sxs-lookup"><span data-stu-id="6dba4-124">See also</span></span>



[<span data-ttu-id="6dba4-125">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="6dba4-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

