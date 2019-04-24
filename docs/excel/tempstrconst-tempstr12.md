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
- функция TempStr12 [Excel 2007], функция Темпстрконст [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d93f9de021c7ba325d9c11af2cede0245ffbbf6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310327"
---
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="1d77d-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="1d77d-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="1d77d-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1d77d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1d77d-106">Функция библиотеки Framework, которая создает временную структуру **XLOPER/XLOPER12** , содержащую строку **кслтипестр** , в качестве входных данных принимается строка источника, заканчивающаяся нулем.</span><span class="sxs-lookup"><span data-stu-id="1d77d-106">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input.</span></span> <span data-ttu-id="1d77d-107">Функция выделяет новый буфер памяти и копирует переданную строку в нее.</span><span class="sxs-lookup"><span data-stu-id="1d77d-107">The function allocates a new memory buffer and copies the passed-in string into it.</span></span> <span data-ttu-id="1d77d-108">Входная строка не изменена, поэтому она объявлена \*\*\*\* как константа.</span><span class="sxs-lookup"><span data-stu-id="1d77d-108">The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="1d77d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d77d-109">Parameters</span></span>

 <span data-ttu-id="1d77d-110">_str_</span><span class="sxs-lookup"><span data-stu-id="1d77d-110">_str_</span></span>
  
<span data-ttu-id="1d77d-111">Указатель на строку источника, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="1d77d-111">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="1d77d-112">В случае **XLOPER**s темпстрконст усекает строки, размер которых превышает 255 байт.</span><span class="sxs-lookup"><span data-stu-id="1d77d-112">In the case of **XLOPER**s, TempStrConst truncates strings that are longer than 255 bytes.</span></span> <span data-ttu-id="1d77d-113">В случае **XLOPER12**s TempStr12Const усекает строки, длина которых превышает 32 767 символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="1d77d-113">In the case of **XLOPER12**s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="1d77d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d77d-114">Return value</span></span>

<span data-ttu-id="1d77d-115">Возвращает строку **кслтипестр** , содержащую копию переданного строкового буфера.</span><span class="sxs-lookup"><span data-stu-id="1d77d-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1d77d-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="1d77d-116">Remarks</span></span>

<span data-ttu-id="1d77d-117">Обратите внимание, что функция Framework структуры **XLOPER** , **темпстр**, работает по-разному и пытается перезаписать первый символ предоставленной строки с длиной следующей строки.</span><span class="sxs-lookup"><span data-stu-id="1d77d-117">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="1d77d-118">Это не всегда является безопасным действием: Microsoft Excel может выполнить сбой, если передать строку, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1d77d-118">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> <span data-ttu-id="1d77d-119">Такой способ создания временных строк теперь является нерекомендуемым в пользу того, как работают как в **темпстрконст** , так и в **TempStr12** .</span><span class="sxs-lookup"><span data-stu-id="1d77d-119">This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work.</span></span> <span data-ttu-id="1d77d-120">Таким образом, первый символ входной строки обрабатывается как начало строки, то есть не как символ длины или как пробел для знака длины.</span><span class="sxs-lookup"><span data-stu-id="1d77d-120">Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character.</span></span> <span data-ttu-id="1d77d-121">Не следует передавать строки, закодированные с помощью знака длины, в начале, так как последствия могут быть непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="1d77d-121">You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1d77d-122">Пример</span><span class="sxs-lookup"><span data-stu-id="1d77d-122">Example</span></span>

<span data-ttu-id="1d77d-123">В этом примере функция **TempStr12** используется для создания строки для окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="1d77d-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="1d77d-124">См. также</span><span class="sxs-lookup"><span data-stu-id="1d77d-124">See also</span></span>



[<span data-ttu-id="1d77d-125">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="1d77d-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

