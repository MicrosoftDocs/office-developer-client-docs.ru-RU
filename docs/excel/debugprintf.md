---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- функция debugprintf [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424800"
---
# <a name="debugprintf"></a><span data-ttu-id="14811-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="14811-104">debugPrintf</span></span>

<span data-ttu-id="14811-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="14811-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="14811-106">Функция библиотеки Framework, которая записывает строку byte-terminated null в активный отладчик с помощью функции Windows SDK **OutputDebugStringA.**</span><span class="sxs-lookup"><span data-stu-id="14811-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="14811-107">Если в приложении нет отладка, системный отладок отображает строку.</span><span class="sxs-lookup"><span data-stu-id="14811-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="14811-108">Если приложение не имеет отладка и системный отладок не активен, **debugPrintf** ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="14811-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="14811-109">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="14811-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="14811-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="14811-110">Parameters</span></span>

 <span data-ttu-id="14811-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="14811-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="14811-112">Строка формата, которая следует за синтаксис и правилами, используемыми с функцией **sprintf.**</span><span class="sxs-lookup"><span data-stu-id="14811-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="14811-113">_arguments_</span><span class="sxs-lookup"><span data-stu-id="14811-113">_arguments_</span></span>
  
<span data-ttu-id="14811-114">Ноль или больше аргументов для совпадения со строкой формата.</span><span class="sxs-lookup"><span data-stu-id="14811-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="14811-115">Пример</span><span class="sxs-lookup"><span data-stu-id="14811-115">Example</span></span>

<span data-ttu-id="14811-116">Эта функция печатает строку, чтобы показать, что управление передано в нее.</span><span class="sxs-lookup"><span data-stu-id="14811-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="14811-117">Флаг _DEBUG должен быть определен перед компиляторией, иначе эта функция ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="14811-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a><span data-ttu-id="14811-118">См. также</span><span class="sxs-lookup"><span data-stu-id="14811-118">See also</span></span>



[<span data-ttu-id="14811-119">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="14811-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

